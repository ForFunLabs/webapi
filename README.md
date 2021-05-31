## Endpoints

### User Matches
`https://elevenvr.club/api/v1/accounts/<account_id>/matches`

parameter | type | default | description
------------ | ------------- | ------- | -------
page | object | `{page: {number: 1, size: 25} }` | matches per page, max 100
unranked | object | false | include unranked matches in results


### Latest User Match
`https://elevenvr.club/api/v1/accounts/<account_id>/matches/latest`



## Examples 

### (User Matches)

`https://elevenvr.club/api/v1/accounts/385684/matches?page%5Bnumber%5D=1&page%5Bsize%5D=1`

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
                "away-score": 2,
                "created-at": "2021-05-28T18:32:47.679Z",
                "elo-change": 6,
                "home-elo-avg": 3130,
                "away-elo-avg": 3240,
                "rounds": [
                    {
                        "id": "19612600",
                        "away-score": 11,
                        "home-score": 6,
                        "winner": 1,
                        "created-at": "2021-05-28T18:35:17.863Z"
                    },
                    {
                        "id": "19612412",
                        "away-score": 11,
                        "home-score": 8,
                        "winner": 1,
                        "created-at": "2021-05-28T18:32:47.679Z"
                    }
                ],
                "players": [
                    {
                        "id": "385684",
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
                        "id": "11111",
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
#### Match State

value | description
---- | -------------
< 0 | Pending State 
0 | In Progress
1 | Completed
2 | Cancelled
3 | Expired
4 | PendingCompletion
5 | Reverted
6 | Reversed

#### Team
value | description
--- | -------------
0 | Home
1 | Away

