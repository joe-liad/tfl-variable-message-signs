# tfl-variable-message-signs
_history of changes on tfl variable message signs_

<a href ="https://techforum.tfl.gov.uk/t/roadside-variable-message-signs-missing/1527"><img width="320" alt="tfl variable message signs" src="https://user-images.githubusercontent.com/92937667/151007266-65f861e8-f3f4-481d-bf0f-6b06835a941b.jpg"></a>
[source](https://techforum.tfl.gov.uk/t/roadside-variable-message-signs-missing/1527/2)

...with a [github action](./.github/workflows/main.yml) running every twenty minutes:

1. use cURL to fetch variable message [sign feed](https://api.tfl.gov.uk/Place/Type/VariableMessageSign) and save to [signs.json](./signs.json)
2. commit the json if the data has changed since the last run
3. create a [git-history](https://github.com/simonw/git-history) database/api with [datasette](https://datasette.io) 
4. publish to [vercel](https://lewisham-tfl-roadside-signs-history.vercel.app/tfl-roadside-signs-history)
