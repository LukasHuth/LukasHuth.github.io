# MALAnalyser

## Analyser

### userinput to add anime with mal id

## API

#### request:

```
GET /token/<secret>
```

#### response:

```
{
    token: String
}
```

### get anime by id

#### request:

```
GET /anime/<id>
```

#### response:

```
{
    name: String,
    malid: int,
    id: int,
    episodes: int,
    score: float,
    populatity: int,
    ranked: int,
    members: int
    favorites: int,
    type: String,
    status: String,
    aired: String,
    premiered: String,
    broadcast: String,
    producers: String Array,
    licensors: String Array,
    studios: String Array,
    source: String,
    genres: String Array,
    durationperepisode: int,
    rating: String,
    maincharacters: String Array,
    adaption: String Array,
    alternativeversion: String Array,
    sidestory: String Array,
    others: String Array,
    prequel: String Array,
    summary: String Array,
    sequel: String Array
}
```

### add anime

#### request:

```
POST /add

body:
{
    name: String,
    malid: int,
    id: int,
    episodes: int,
    score: float,
    populatity: int,
    ranked: int,
    members: int
    favorites: int,
    type: String,
    status: String,
    aired: String,
    premiered: String,
    broadcast: String,
    producers: String Array,
    licensors: String Array,
    studios: String Array,
    source: String,
    genres: String Array,
    durationperepisode: int,
    rating: String,
    maincharacters: String Array,
    adaption: String Array,
    alternativeversion: String Array,
    sidestory: String Array,
    others: String Array,
    prequel: String Array,
    summary: String Array,
    sequel: String Array
}
```

#### response:

```
{
    response: String
}
```

### get anime list size

#### request:

```
GET /size
```

#### response:

```
{
    id: int
}
```

### get animes

#### request:

```
GET /animes
```

#### response:

```
List of
[String, int, int]

[name, episodes, id]
```

### search anime

#### request:

```
GET /search

body:
{
    search: int,
    data: String
}

search: <search type>
    0: name
    1: full name
    2: eps
    3: score int
    4: type
    5: status
    6: producers
    7: licensors
    8: studios
    9: genre
    10: duration per episode as integer
    11: main character
    12: rating
data: <search Parameter>
```

#### response:

```
List of
[String, id, id]

[name, episodes, id]
```

## Discord bot

### Commands:

#### search:

```
search <type> <search Parameter>

or

search <type> <search Parameter> <type> <search Parameter>

or

seach <type> <search Parameter> ... infite stackable
```