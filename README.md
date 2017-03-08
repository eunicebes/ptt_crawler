# ptt_crawler

A web ptt crawler for catching plenty of articles through pages


## Environment
    python 3.6.0

## How to execute?

    $python3 ptt_crawler.py [board_name] [start_page] [end_page]

`If end_page = -1, it will directly choose the latest page of the board.`
    
## Example
    $python3 ptt_crawler.py Gossiping 20014 20018
    $python3 ptt_crawler.py Gossiping 20014 -1
    
## Ouput format
JSON file

    [
        {
            "Board": name of board,
            "Title": title of article,
            "Author": author of article,
            "Post_time": when article was posted,
            "Content": full content of article,
            "Push_num": amount of push,
            "Boo_num": amount of boo,
            "Arrow_num": amount of arrow,
            "Pushes":[
                {
                    "push_tag": symbol of push tag,
                    "push_user": who wrote the push,
                    "push_content": content of push,
                    "push_time": when push was posted
                },
                {
                    ...
                },
                ...
            ]
        },
        {
            ...
        },
        ...
    ]

## License
    MIT License

