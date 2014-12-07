---
title:  "Meet @SpillReport, the tiny robot tirelessly tweeting about oil spills"
date:   2014-12-01 21:00:00
categories: projects data environment
layout: big_header
header_img: /img/pi-big.jpg
header_img_alt: "Raspberry Pi - a new golden age of computing"
---

**tl;dr - I created a Twitter bot that scrapes reported oil and gas spills in Colorado and tweets in near-real time.  [Check it out on Twitter](https://twitter.com/SpillReport) and [read more about it in the Rocky Mountain Collegian](http://www.collegian.com/2014/12/colorado-state-student-updates-oil-spill-information-on-twitter/104016/)**

#### Some Backstory

It's no secret that [I'm a proponent of robot journalism](https://medium.com/@scogle/why-automated-journalism-will-save-lives-213397cc6358). There are a whole class of issues in the world--those that stick around for longer than a few days and are largely driven by data--that machines are simply *better* at covering than humans in many regards.

Living in Colorado, the environmental consequences of energey exploration are a perennially relevant issue; we are one of the top oil producing states in the country with nearly [*85,000* active wells](http://www.fractracker.org/2014/03/1-million-wells/). A consequence is that oil, gas, frack fluid and other drilling chemicals are spilled [every](https://twitter.com/search?q=%40spillreport%2011%2F26&src=typd) [single](https://twitter.com/search?q=%40spillreport%2011%2F25&src=typd) [day](https://twitter.com/search?q=%40spillreport%2011%2F24&src=typd).

Every few months I see an article [pointing out that there thousands of spills a year](http://www.denverpost.com/environment/ci_26233762/oil-and-gas-spills-surge-two-day-residents). These articles are better written, more informative and more thought provoking than what a robot can do. Where they fail is in keeping the issue in the spotlight for the long run, in constantly reminding us that *this is still happening*.

But why should they? Thought and reflection are for humans; quantity and duration for machines.

#### Building the Bot

There is a wealth of wonderful free (as in beer *and* speech!) open source tools available today that make this kind of thing easier than ever, and there is cheaper hardware than ever to run it on. The [Raspberry Pi](http://www.raspberrypi.org) is absolutely ideal for projects like this--cheap, tiny and efficient. It draws lest than 2 watts and cost less than $50 all after some cabling and an enclosure (pictured below). That works out to just over $4/month for a year, comparable to a low-end web hosting plan. The newest model, the A+, is [even cheaper](http://www.raspberrypi.org/raspberry-pi-model-a-plus-on-sale/).

To write it I used Python and [Beautiful Soup](http://www.crummy.com/software/BeautifulSoup/) to do the scraping. I store the data in a single table in an SQLite3 database and use the python-twitter library to Tweet. [Check out the app scaffold on GitHub](https://github.com/scogle/SpillReport/tree/master), clone it and build something cool.

I estimate that I spent about ten hours in total on this, and approximately four of that was spent building the actual plastic enclosure for the Raspberry Pi.

![My homebrew Raspberry Pi enclosure](/img/pi.jpg "My homebrew Raspberry Pi enclosure")

#### Raspberry Pi as a Tool for Journalism

The Raspberry Pi is an amazing tool for journalism. Either as a quick way to prototype ideas or as, in my case, a permanent solution for running things like this, the price and power efficiency is second to none. An average server might use in the hundreds of watts of power or more--a Raspberry Pi B+ only uses about 2w, often less.  This puts it on par with a dim nightlight, energy wise.

What's more, the accessibility of the hardware makes it ideal for a huge variety uses--sensors monitoring weather or other environmental factors, traffic, etc. They're cheap enough to practically be treated as disposable and have a vibrant community to help you get up and running.

But the best part is that *because* they're so cheap and tiny, a journalist can quickly create a prototype at their desk, make it live, and leave it running as long as it needs to. No need for costly servers or AWS time and no need for a lot of support from management or IT departments.

