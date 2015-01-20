---
title:  "A (stupid little) life-betterment script"
date:   2015-01-19 12:00:00
categories: bash tip
layout: post
---

Do you find yourself SSHing into different accounts on the same machine all the time? Add this to your `.bashrc`:

{% highlight bash %}
function hal() {
	ssh $1@xxx.xxx.xxx.xxx▫
}
export -f hal
{% endhighlight %}

The first line creates a function named after the machine (obviously, our server is named after [HAL-9000](http://en.wikipedia.org/wiki/HAL_9000))--name it whatever you'd like, although make sure not to step on any existing unix commands.

On the second line, change `xxx.xxx.xxx.xxx` to whatever the ip (or domain) of the machine you want to access is.  I assume no password or ssh keys but you could hardcode login credentials or add them as additional parameters.

The final line basically just turns the function into a command. The end result is that `ssh scott@xxx.xxx.xxx.xxx` can now be accessed with `hal scott`. No need to remember the ip, no need to type extra characters.  I suggest having an extra beer with that thirty seconds a day I just saved you.