# Wikipedia-Scraper

Tool for extracting plain text from Wikipedia

Adapted from https://github.com/goldsmith/Wikipedia and https://github.com/martin-majlis/Wikipedia-API

```ruby
>>> from wikipedia import Wikipedia
>>> wiki = Wikipedia()

# Search Wikipedia
>>> wiki.search("Wikipedia", limit=3)
# ['Wikipedia', 'English Wikipedia', 'List of Wikipedias']

# Get location coordinates if exists 
>>> wiki.coordinates("Wikipedia")
# (None, None)

# Extract plain text for given page
>>> page = wiki.page("Wikipedia")

# Get summary
>>> page.summary(exsentences=1)
# 'Wikipedia is a multilingual free online encyclopedia written and maintained by a community of volunteers, known as Wikipedians, through open collaboration and using a wiki-based editing system called MediaWiki.'

# Get section titles 
>>> page.section_titles[:5]
# ['History', 'Openness', 'Policies and laws', 'Governance', 'Community']
 
# Get content of given section
>>> page.section_by_title("History", exsentences=1)
# {'title': 'History',
#  'text': '',
#  'subsections': {
#     0: {'title': 'Nupedia',
#         'text': 'Various collaborative online encyclopedias were attempted before the start of Wikipedia, but with limited success.'},
#     1: {'title': 'Launch and growth',
#         'text': 'The domains wikipedia.com (later redirecting to wikipedia.org) and wikipedia.org were registered on January 12, 2001, and January 13, 2001, respectively, and Wikipedia was launched on January 15, 2001 as a single English-language edition at www.wikipedia.com, and announced by Sanger on the Nupedia mailing list.'},
#     2: {'title': 'Milestones',
#         'text': 'In January 2007, Wikipedia first became one of the ten most popular websites in the United States, according to Comscore Networks.'}}}
   
# Get full text
>>> page.text
```
