# webapi
webapi

### User Matches
`https://elevenvr.club/api/v1/accounts/385684/matches`

parameter | type | example 
------------ | ------------- | -------
page | object | `{page: {number: 1, size: 25} }` 

`https://elevenvr.club/api/v1/accounts/385684/matches?page%5Bnumber%5D=1&page%5Bsize%5D=1`

###### Example Output
```json
{
    "data": [
        {
            "id": "8746914",
            "type": "matches",
            "attributes": {
                "ranked": true,
                "number-of-rounds": 2,
                "state": 1,
                "winning-team": 1,
                "losing-team": 0,
                "home-score": 0,
                "away-score": 0,
                "created-at": "2021-05-28T18:32:47.679Z",
                "elo-change": 6,
                "home-elo-avg": 3130,
                "away-elo-avg": 3240,
                "rounds": [
                    {
                        "id": 19612600,
                        "away-score": 11,
                        "home-score": 6,
                        "round-number": 0,
                        "state": 0,
                        "winning-team": -1,
                        "created-at": "2021-05-28T18:35:17.863Z"
                    },
                    {
                        "id": 19612412,
                        "away-score": 11,
                        "home-score": 8,
                        "round-number": 0,
                        "state": 0,
                        "winning-team": -1,
                        "created-at": "2021-05-28T18:32:47.679Z"
                    }
                ],
                "players": [
                    {
                        "id": 385684,
                        "username": "BLANK",
                        "elo": 3240,
                        "rank": 195,
                        "wins": 915,
                        "losses": 251,
                        "last-online": "2021-05-28T18:52:48.276Z",
                        "team": 1,
                        "current-elo": 3254.2
                    },
                    {
                        "id": 11111,
                        "username": "PERSON",
                        "elo": 3130,
                        "rank": 89,
                        "wins": 652,
                        "losses": 107,
                        "last-online": "2021-05-30T03:51:57.036Z",
                        "team": 0,
                        "current-elo": 3103
                    }
                ]
            }
        }
    ],
    {
        "self": "https://elevenvr.club/api/v1/accounts/385684/matches?page%5Bnumber%5D=1&page%5Bsize%5D=1",
        "first": "https://elevenvr.club/api/v1/accounts/385684/matches?page%5Bnumber%5D=1&page%5Bsize%5D=1",
        "prev": null,
        "next": "https://elevenvr.club/api/v1/accounts/385684/matches?page%5Bnumber%5D=2&page%5Bsize%5D=1",
        "last": "https://elevenvr.club/api/v1/accounts/385684/matches?page%5Bnumber%5D=1183&page%5Bsize%5D=1"
    }
}
```
