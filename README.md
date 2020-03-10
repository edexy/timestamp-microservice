<h1>API Project: Timestamp Microservice </h1>
<h3>User stories :</h3>
<p>The API endpoint is GET [project_url]/api/timestamp/:date_string?</p>
<p>A date string is valid if can be successfully parsed by new Date(date_string) (JS) . Note that the unix timestamp needs to be an integer (not a string) specifying milliseconds. In our test we will use date strings compliant with ISO-8601 (e.g. "2016-11-20") because this will ensure an UTC timestamp.</p>
<p>If the date string is empty it should be equivalent to trigger new Date(), i.e. the service uses the current timestamp.</p>
<p>If the date string is valid the api returns a JSON having the structure {"unix": <date.getTime()>, "utc" : <date.toUTCString()> } e.g. {"unix": 1479663089000 ,"utc": "Sun, 20 Nov 2016 17:31:29 GMT"}.</p>
<p>If the date string is invalid the api returns a JSON having the structure {"unix": null, "utc" : "Invalid Date" }. It is what you get from the date manipulation functions used above.</p>

<h3>Example usage:</h3>
<p>https://curse-arrow.hyperdev.space/api/timestamp/2015-12-15</p>
<p>https://curse-arrow.hyperdev.space/api/timestamp/1450137600000</p>

<h3>Example output:</h3>
<p>{ "unix": 1450137600, "utc": "December 15, 2015" }</p>
