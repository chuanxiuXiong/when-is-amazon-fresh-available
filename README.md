# When is Amazon Fresh available?

<div>
    <img src='https://miro.medium.com/max/2560/0*8aY8pX5CoNGImZU4.png' height = 150px style='padding-right: 50px'>
    <img src='https://www.crummy.com/software/BeautifulSoup/bs4/doc/_images/6.1.jpg' height= 150px>
</div>

This tool helps to constantly monitor AmazonFresh delivery time-windows and alerts the user when there is a new timeslot.  It uses <a src='https://www.python.org/about/'>Python</a>, and mainly <a src='https://www.crummy.com/software/BeautifulSoup/'> BeautifulSoup</a>.

### Why it is developed?
The tool is developed during <a src='https://www.google.com/search?q=covid-19'>COVID-19 pandemic</a>, when the entire globe faces the unprecedented threat of the new coronavirus. People are social distancing themselves to help contain the virus. While most should stay at home and avoid contacts with others, the need for grocery shopping services surges and causes a shortage of delivery timewindows in many cities. Hopefully, this tool could make life easier for those who rely on AmazonFresh.

### How to use?
1. Install <a src='https://www.python.org/downloads/'>python</a> and <a src='https://pip.pypa.io/en/stable/installing/'>pip</a>.
2. Install all libraries in `requirements.txt`.
3. Under `when-is-amazon-fresh-available`, create a file named `.env`. All the environmental variables including your amazon email and password will be stored here. Copy paste the following into `.env`. Replace some of the fileds as described. For `COOKIE` and `SESSION_ID`, you could find it by opening up DevTools in your browser and see the request headers of the first network activity when you click on any link under <a src='https://www.amazon.com'>amazon</a>. (See <a src='https://developers.google.com/web/tools/chrome-devtools/network'>this article</a> if you don't know how to inspect network activities in the browser).
```
EMAIL={Replace with your amazon email}
PASSWORD={Replace with your amazon password}
LOG_FILENAME=log/when-is-amazon-fresh-available.log
COOKIE={Replace with your Cookie}
SESSION_ID={Replace with your SessionID}
```
4. Add all your Amazon fresh or Wholefoods items to your cart.
5. Run the program:
```
 # if you want amazon fresh
    python when.py 1
 # if you want wholefoods
    python when.py 0
```
6. You will receive alarms when there is a new slot available.

## Potential new features:
1. Finds a better way to make alarm sound on Mac.
2. Automatically checkout if there is an available timewindow.
3. Send emails to notify instead of alarming.

This tool is intended only for personal use and developed under a short time, which prioritizes practicality above others. I hope it could make your life easier during this special time.
