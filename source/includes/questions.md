# سوالات

## دریافت تمام سوالات


```shell
curl "https://javabkoo.com/api/v1/questions"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const javabkoo = require('javabkoo');

let api = javabkoo.authorize('{access_token}');
let questions = api.questions.get();
```

> کد بالا یک نتیجه JSON به صورت زیر بر می‌گرداند:

```json
[
  {
    "_id": "5a816275f8030b3bdd655b0d",
    "updatedAt": "2018-02-12T19:07:21.136Z",
    "createdAt": "2018-02-12T09:46:29.646Z",
    "title": "یک زندگی ایده‌آل چیست؟",
    "origin": {
      "_id": "5a73b1fcc48071e4c3da0e6c",
      "name": "جواب‌کو",
      "baseUrl": "https://javabkoo.com"
    },
    "lastAskedAt": "2018-02-12T09:46:29.642Z",
    "__v": 0,
    "lastAnsweredAt": "2018-02-12T19:07:21.135Z",
    "portals": [
      "5a73b1fcc48071e4c3da0e6c"
    ],
    "downvotes": [],
    "upvotes": [],
    "followers": [],
    "askers": [],
    "comments": [],
    "topics": [],
    "score": 0,
    "counts": {
      "asks": 1,
      "downvotes": 0,
      "upvotes": 0,
      "edits": 2,
      "comments": 0,
      "hiddenAnswers": 0,
      "answers": 2,
      "views": 8,
      "followers": 0
    },
    "type": "general",
    "anonymous": true,
    "verified": false,
    "locked": false,
    "followed": false
  }
]
```

این مسیر لیستی از تمام سوالات قابل دسرتس را نمایش می‌دهد.


### درخواست HTTP

<code class="request">GET /api/v1/questions</code>

### پارامترهای Query

<table>
  <thead>
    <th>پارامتر</th><th>پیش‌فرض</th><th class="rtl">توضیحات</th>
  </thead>
  <tbody>
    <tr>
      <td><code>page</code></td>
      <td>1</td>
      <td class="rtl">صفحه مورد نظر</td>
    </tr>
    <tr>
      <td><code>limit</code></td>
      <td>20</td>
      <td class="rtl">تعداد مواردی که فرستاده می‌شود</td>
    </tr>
    <tr>
      <td><code>sort</code></td>
      <td>createdAt.desc</td>
      <td class="rtl">فیلدی که بر اساس آن نتیجه مرتب‌سازی می‌شود</td>
    </tr>
  </tbody>
</table>


## دریافت یک سوال خاص


```shell
curl "https://javabkoo.com/api/v1/questions/5a816275f8030b3bdd655b0d"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const javabkoo = require('javabkoo');

let api = javabkoo.authorize('{access_token}');
let questions = api.questions.get('5a816275f8030b3bdd655b0d');
```

> کد بالا یک نتیجه JSON به صورت زیر بر می‌گرداند:

```json
{
  "_id": "5a816275f8030b3bdd655b0d",
  "updatedAt": "2018-02-12T19:07:21.136Z",
  "createdAt": "2018-02-12T09:46:29.646Z",
  "title": "یک زندگی ایده‌آل چیست؟",
  "origin": {
    "_id": "5a73b1fcc48071e4c3da0e6c",
    "name": "جواب‌کو",
    "baseUrl": "https://javabkoo.com"
  },
  "lastAskedAt": "2018-02-12T09:46:29.642Z",
  "__v": 0,
  "lastAnsweredAt": "2018-02-12T19:07:21.135Z",
  "portals": [
    "5a73b1fcc48071e4c3da0e6c"
  ],
  "downvotes": [],
  "upvotes": [],
  "followers": [],
  "askers": [],
  "comments": [],
  "topics": [],
  "score": 0,
  "counts": {
    "asks": 1,
    "downvotes": 0,
    "upvotes": 0,
    "edits": 2,
    "comments": 0,
    "hiddenAnswers": 0,
    "answers": 2,
    "views": 8,
    "followers": 0
  },
  "type": "general",
  "anonymous": true,
  "verified": false,
  "locked": false,
  "followed": false
}
```

این مسیر یک سوال با ID مشخص را بر می‌گرداند.

### درخواست HTTP

<code class="request">GET /api/v1/questions/{id}</code>


### پارامتر‌های URL

پارامتر | توضیحات
---------   | -----------
`id`        | شناسه سوال مورد نظر

## حذف یک سوال خاص


```shell
curl "https://javabkoo.com/api/v1/questions/5a816275f8030b3bdd655b0d"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const javabkoo = require('javabkoo');

let api = javabkoo.authorize('{access_token}');
let result = api.questions.delete('5a816275f8030b3bdd655b0d');
```

> کد بالا یک نتیجه JSON به صورت زیر بر می‌گرداند:

```json
{
  "success": true
}
```

این مسیر یک سوال با ID مشخص را پاک می‌کند.

### درخواست HTTP

<code class="request">DELETE /api/v1/questions/{id}</code>


### پارامتر‌های URL

پارامتر | توضیحات
---------   | -----------
`id`        | شناسه سوال مورد نظر
