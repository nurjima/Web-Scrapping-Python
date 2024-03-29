# Web Scrapping using Python.

## Installation

```bash
git clone 
cd webScrappingAssignment
pip install requirements.txt
```

## Usage

### MacOS 
```
python3 main.py
```


#### Search for coin in google search
```python
from src.scrapper import WebScrapper

if __name__ == '__main__':
    newWebScrapper = WebScrapper()
    search = "bitcoin"
    number_of_results = 10
    newWebScrapper.search_for_google(search, number_of_results)
```



#### Get exact coin
```python
from src.scrapper import WebScrapper

if __name__ == '__main__':
    newScapper = WebScrapper()
    data = newScapper.get_currency("ETH") #get exact coin with its symbol

    print("Rank: ", data[0])
    print("Name: ", data[1])
    print("Symbol: ", data[2])
    print("Market Cap: ", data[3])
    print("Price: ", data[4])
    print("Circulating Supply: ", data[5]) 
```

#### Get all loaded coins
```python
from src.scrapper import WebScrapper

if __name__ == '__main__':
    newScapper = WebScrapper()
    data = newScapper.get_currencies() #print out loaded currencies

    for i in range(len(data)):
        print("Rank: ", data[i][0])
        print("Name: ", data[i][1])
        print("Symbol: ", data[i][2])
        print("Market Cap: ", data[i][3])
        print("Price: ", data[i][4])
        print("Circulating Supply: ", data[i][5])
        print("---------------------------------")
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
