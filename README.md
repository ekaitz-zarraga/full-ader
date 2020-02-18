# Full Ader Database

Full Ader[^1] is a project that contains the `ads.txt` file of the 1M most
visited websites of the Alexa ranking[^2].

## About ads.txt files

<https://en.wikipedia.org/wiki/Ads.txt>

`ads.txt` files are an initiative from the IAB Technology Laboratory (you can
read [the description in their website][desc]) for websites that aims to
provide ad-selling companies a list of companies that are selling ads in the
website where the file is served.


## About this database

The goal of `ads.txt` files is to fight fraud but they can be used for many
other things. This database aims to encourage *you* to find new uses for the
collection of `ads.txt` files.

- What if we use the domains in the files as a list of blocked domains for
  AdBlockers?

- What if we make a network graph and check the hierarchies in the ad business?

- What if we compare the contents of the websites listed here with the ad
  companies they have?

- What if...?

## Structure of the database

The database is stored in a really inefficient way.

Each file is named after it's domain + `.txt` extension. Example:
`domain.com.txt`

Empty files mean there's no valid `ads.txt` file in the website or it's empty.
They are kept because if we don't keep them there's no way to know if the page
was in the top 1M websites or not.

## Update frequency

Code for updating is not made yet. First approach was a bulk downloader that
made a heavy use of multithreading and will be discarded for a better
downloader that is able to commit to this repository by its own.

[desc]: https://iabtechlab.com/ads-txt/

[^1]: Yeah... The name is a horrible joke
[^2]: The ranking is obtained from this weird link I found on the Internet:
  <https://s3.amazonaws.com/alexa-static/top-1m.csv.zip>
