# career-vault-api-documentation
Career Vault's Jobs API documentation
## Authentication
All requests to the API are authenticated by providing your API key. The API key should be provided as an HTTP header named Api-Token.
> :warning: **Remember to keep your API key secret. Do not share it and take care not to expose it publicly in client-side code.

## URL Parameters
Parameter | Description
------------ | -------------
page | A cursor for use in pagination. Returns the n-th chunk of perPage objects.
perPage | Return up to this number of jobs per response. Must be an integer between 1 and 500 (otherwise, it will default to 100). Defaults to 100.


## GET: List Jobs
### HTTP Request

```GET https://careervault.io/api/{id}```

### JSON Response
```
{
  "meta": {
    "page": 1,
    "perPage": 100,
    "pageCount": 112,
    "uniqueCompaniesCount": 1725,
    "totalNumberOfJobs": 8392,
    "newJobsCount": 0
  },
  "jobs": [
    {
      "JobID": 951238,
      "JobTitle": "Tech Talent Acquisition Specialist",
      "Location": "Remote - EMEA ",
      "Url": "https://jobs.lever.co/aircall/2f53b33c-b382-4cf8-b3d7-94be2ec6c184",
      "DatePosted": "2021-04-14T15:06:43.000Z",
      "Description": "<div class=\"section page-centered\"><div>Aircall is on a mission to revolutionize the business phone industry!</div><div><br></div><div>We exist to empower every professional to have richer conversations. We provide an entirely cloud-based voice solution, that integrates seamlessly with popular productivity and helpdesk tools that workplaces are already using. We have raised more than $100 Million since 2015, and we care about our growing base of 6000+ customers.</div><div><br></div><div>Behind our product are the amazing teams driving it, split between Paris, New York, Sydney, Madrid, and remote locations.</div><div><br></div><div>Aircall is looking for a Tech Talent Acquisition Specialist to join our passionate and high performing Talent Team. </div><div><br></div><div>Sitting within the Global People Team and reporting to our Tech Talent Acquisition Manager, </div><div>you will be responsible for various hiring needs in a hyper-growth context (we are recruiting 260 new Aircallees this year!!!)</div><div><br></div><div>You will be in charge of many projects within the Talent team or with our different partners.</div><div><br></div><div>Working along with very committed hiring managers at Aircall and a team of outstanding TAs, you will bring your creativity to experiment with new approaches to unleash your full potential and thrive with us. You will have the opportunity to work on a team that has a continuous improvement philosophy and in an international environment. </div><div><br></div><div><b>***This position is open to candidates willing to relocate to Paris, Madrid and depending on experience can also be fully remote from France, Spain, Portugal, Netherland or the UK***</b></div></div><div class=\"section page-centered\"><div><h3>Your mission @ Aircall</h3><ul class=\"posting-requirements plain-list\"><ul><li>Lead the full cycle recruitment process for your Tech business partners with the support of your manager and team members</li><li>Help build and improve communication around candidate experience &amp; hiring processes</li><li>Plan and participate in events to improve employer branding, communication, and strategy around hiring and retention</li><li>Bring your experience and share it with Talent team members</li><li>Each Talent Acquisition Team member can lead or participate in various projects: events, jobsite, editorial committee, compensation &amp; benefits strategy, ATS processes, hiring process, newcomers onboarding, interviewers training, external partner relationships, ... &amp; many more to come! </li></ul></ul></div></div><div class=\"section page-centered\"><div><h3>A little more about you:</h3><ul class=\"posting-requirements plain-list\"><ul><li>At least 2 years experience hiring in Tech with a passion for building high-performing teams </li><li>Experience in finding solutions to tough problems, and the ability to invest energy in the success of your work</li><li>Ability to meet deadlines and contribute to the structuring of our hiring processes </li><li>Ability to give and receive constructive feedback while remaining positive </li><li>Eager to learn and ready to collaborate with various teams, hiring managers, and coworkers</li></ul></ul></div></div><div class=\"section page-centered\"><div><h3>Our hiring process:</h3><ul class=\"posting-requirements plain-list\"><ul><li>Call with a Talent Acquisition Specialist </li><li>Zoom interview with our Talent Acquisition Manager </li><li>Use case with a Business Partner and another team member</li><li>Zoom Interview with our Chief People Officer </li></ul></ul></div></div><div class=\"section page-centered\"><div>We know that success comes from smart work and deserves to be recognized and rewarded</div><div><br></div><div>We value people who are bold, ambitious, collaborative and customer-centric. Even better, the ones who know how to work hard &amp; have fun at the same time. We’re a tribe of highly driven people, with a great sense of human connection and a clear focus. </div><div><br></div><div>If you love a good challenge, enjoy solving meaningful problems, and want to be a part of one of the fastest-growing B2B startups, then Aircall is the company you are looking for!</div><div>Aircall offers a unique work environment and the chance to collaborate with diverse teammates across continents. We'll provide freedom and tools to allow you to thrive at your best, and foster an environment you can do it in.</div><div><br></div><div><b>Why join us?</b></div><div><br></div><div>???? Key moment to join Aircall in term of growth and opportunities</div><div>????‍♀️ Our people matter, work-life balance is important at Aircall</div><div>???? Fast-learning environment, entrepreneurial and strong team spirit</div><div>???? 35+ Nationalities: cosmopolite &amp; multi-cultural mindset</div><div>???? Competitive salary package &amp; benefits (health coverage, lunch, commute, sports)</div><div><br></div><div><u><i>DE&amp;I Statement: </i></u></div><div><i>At Aircall, we believe diversity, equity and inclusion, irrespective of origins, identity, background and orientations, are </i><b><i>core to our Aircall journey.</i></b><i> </i></div><div><i>We promote active inclusion to foster a</i><b><i> strong sense of belonging</i></b><i> which is one of our main strengths as a business. We strive to assemble diverse people that can </i><b><i>enrich and learn from each other</i></b><i>. We pledge to make sure everyone not only has a seat at the table but is valued at the table -- providing </i><b><i>equal opportunities </i></b><i>to develop and thrive.  </i></div><div><i>We will constantly challenge ourselves to make sure that we live up to our ambitions around diversity, equity and inclusion, and </i><b><i>keep this conversation </i></b><i>open because we realize that we have work to do and much to learn.</i></div></div>",
      "CompanyName": "Aircall",
      "Logo": "https://lever-client-logos.s3.amazonaws.com/76909e1c-c61e-4134-a0d5-c22ff4bfb2dd-1555509307718.png",
      "Website": "http://aircall.io"
    }
  ]
}
```

### Attributes Descriptions
#### meta
Attribute | Description
------------- | -------------
page | A cursor for use in pagination. Returns the n-th chunk of perPage objects.
perPage | Number of jobs per response. Must be an integer between 1 and 500 (otherwise, it will default to 100). Defaults to 100.
pageCount | Number of pages 
uniqueCompaniesCount | Number of companies that are hiring
totalNumberOfJobs | Number of unique job postings in the endpoint
#### job
Attribute | Description
------------- | -------------
JobID | Unique ID for each job
JobTitle | Job title
Location | Location (can include remote)
Url | Link to the original job posting on the company's career page
DatePosted | Date and time in ISO 8601 format. The time zone is UTC.
Description | Description of the job opening in HTML format
CompanyName | Company name
Logo | URL to the company's logo image generated by CDN
Website | Link to the company's website

