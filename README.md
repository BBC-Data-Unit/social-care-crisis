# Social care in crisis

![](https://ichef.bbci.co.uk/news/976/cpsprodpb/23ED/production/_130579190_lily4lookingatcamera-top.jpg.webp)

In July and November 2023, The Shared Data Unit (SDU) looked at how delays for care assessments were contributing to patients remaining in hospital despite being classed as well enough to be discharged. 

The first set of stories, in July, focused on [the scale of those dying - at least 1,300 people - waiting for a care package to start during the last financial year](https://www.bbc.co.uk/news/uk-wales-66260332).

The second stories, In November, [looked at the large proportion of patients - around 60% - who were having to stay in hospital at the end of each day despite being classed as fit to leave](https://www.bbc.co.uk/news/uk-england-67125440).

## Methodology

For the first set of stories we sent Freedom of Information requests to every local authority in the UK asking two sets of questions. In Northern Ireland, health and social care trusts handle care. 

The first set asked authorities how many individual domiciliary care contracts had been handed back to the authority in 2021-22 and in 2022-23. We also asked for the reasons behind those hand-backs, though these were not handed over in a form that could be easily shared.

The second set of questions asked councils to provide the median wait times for an initial care assessment and for a care package to start. We also asked them to provide the longest individual waits they had on record for both and whether any individuals had died waiting for a package to start.

We also asked those same councils (and health boards in Northern Ireland) how long people waited on average for an initial care assessment over the past two financial years and how long they waited for a care package to start following the assessment.

Only 83 out of the 211 authorities (39%) collected the data in a way that could be retrieved under the Freedom of Information Act. Most (59%) of replying authorities did not answer the questions fully but provided at least partial responses.

For the second set of stories we compiled and analysed data from [NHS 'situation reports' (sitreps) that stated the numbers of patients discharged each day, and the numbers of patients who "no longer meet the criteria to reside" but who were still not discharged](https://www.england.nhs.uk/statistics/statistical-work-areas/discharge-delays-acute-data/). This involved writing Python code to fetch, combine, filter and clean 12 separate monthly datasets, before further analysis was conducted in spreadsheets and R. 

The analysis then allowed us to identify trusts with particularly high or low rates of non-discharged patients, to look at regional patterns and change over time, and to conduct further reporting to find out more about those patterns.

The methodology for each set of stories is outlined in an associated briefing pack or website. 

* [Briefing pack: Social Care in Crisis](https://docs.google.com/document/d/1QvJ7k_eiLa7dZDor7HI6UXAevQ9Tfy9bEfVqCEFAHD8/edit) ([PDF copy](https://github.com/BBC-Data-Unit/social-care-crisis/blob/main/Social%20Care%20in%20Crisis.pdf))
* [Briefing website: Why are hospitals unable to discharge patients?](https://hospitaldischarges.github.io/website/index.html)

## Data

* [Data: Social Care in Crisis](https://docs.google.com/spreadsheets/d/11md8PJ-8FdRFxuiOvUq0Lte03n2y3XCWuTCC2cWeaEY/edit#gid=492937083) ([Excel export](https://github.com/BBC-Data-Unit/social-care-crisis/blob/main/Social%20care%20in%20crisis.xlsx))

## Scripts

As well as the Python notebook to gather, combine and clean the data on discharges, R notebooks were used to create a bespoke analysis for 120 separate trusts, and publish that as a webpage with a page detailing the picture at each trust. The code for those notebooks is available in this repo at the links below.

* [Python notebook used to download, combine, filter, clean and export data on discharges](https://github.com/BBC-Data-Unit/social-care-crisis/blob/main/scripts/sitreps_cleaning.ipynb)
* [R notebook that generates the homepage for the story website](https://github.com/BBC-Data-Unit/social-care-crisis/blob/main/scripts/index.Rmd)
* [R notebook that generates a 'template' page for each hospital trust](https://github.com/BBC-Data-Unit/social-care-crisis/blob/main/scripts/01templateHD.Rmd)
* [R notebook that 'renders' that template into 120 different markdown files - one for each hospital trust](https://github.com/BBC-Data-Unit/social-care-crisis/blob/main/scripts/03render.Rmd)
* [R notebook that renders those 120 markdown files as HTML versions](https://github.com/BBC-Data-Unit/social-care-crisis/blob/main/scripts/04renderhtml.Rmd)
* [R notebook that cleans those HTML files and adds extra elements such as navigation, charts, etc.](https://github.com/BBC-Data-Unit/social-care-crisis/blob/main/scripts/05cleaning.Rmd)

## Partner usage

Usage for the first story in July included:

* All About Newtown: [Older people 'being let down' across Wales](https://allaboutnewtown.wales/story/older-people-across-wales-waiting-longer-for-social-care-assessments)
* Caerphilly Observer: [Caerphilly: 34 people died waiting for council-arranged care packages](https://caerphilly.observer/news/1024883/34-people-died-waiting-for-council-arranged-care-packages/)
* Care Appointments: [‘Pretty miserable’ situation for people in need of social care with lengthy 
delays reported](https://careappointments.com/care-news/england/197568/pretty-miserable-situation-for-people-in-need-of-social-care-with-lengthy-delays-reported/)"
* Head Topics: [Long waits for care leave patients 'stuck in bed'](https://headtopics.com/uk/long-waits-for-care-leave-patients-stuck-in-bed-41700373)
* Home Care Insight: [Isle of Wight Council refuses to share ‘crucial’ social care data](https://www.homecareinsight.co.uk/isle-of-wight-council-refuses-to-share-crucial-social-care-data/)
* Island Echo (Isle of Wight): [SOCIAL CARE IN CRISIS BUT COUNCIL REFUSE TO PROVIDE DATA IN RESPONSE TO FOI 
REQUEST](https://www.islandecho.co.uk/social-care-in-crisis-but-council-refuse-to-provide-data-in-response-to-foi-request/)
* Lancashire Telegraph: [Blackburn with Darwen resident waits 616 days for care assessment](https://www.lancashiretelegraph.co.uk/news/23686751.blackburn-darwen-resident-waits-616-days-care-assessment/)
* Macclesfield Nub News: [Macclesfield: Cheshire East Council refused to respond on wait times in 
social care](https://macclesfield.nub.news/news/local-news/macclesfield-cheshire-east-council-refused-to-respond-on-wait-times-in-social-care-193249)
* Macclesfield Nub News: [More than 30 people died waiting for a care package in Caerphilly](https://www.southwalesargus.co.uk/news/23686518.30-people-died-waiting-care-package-caerphilly/)
* Metro News: [Barry: Woman, 96, stuck in hospital for 11 months waiting for carers | UK 
News](https://metro.co.uk/2023/07/31/barry-woman-96-stuck-in-hospital-for-11-months-waiting-for-carers-19219031/https://metro.co.uk/2023/07/31/barry-woman-96-stuck-in-hospital-for-11-months-waiting-for-carers-19219031/)
* National World: [Brits are dying while waiting for social care, investigation finds](https://www.nationalworld.com/health/social-care-brits-dying-waiting-carers-hands-tied-investigation-finds-4237262)
* [Pitman Blog](https://pitmanblog.co.uk/caregiver-shortage-woman-stuck-in-hospital-for-11-months-2/)
* South Wales Argus: [More than 30 people died waiting for a care package in Caerphilly](https://www.southwalesargus.co.uk/news/23686518.30-people-died-waiting-care-package-gwent/)
* South Wales Argus: [Councils speak after people died waiting for care in South Wales](https://www.southwalesargus.co.uk/news/23693927.councils-speak-people-died-waiting-care-south-wales/)
* STV News: [UK deaths while waiting for care package tops 1,300 over past year, new 
research reveals](https://news.stv.tv/scotland/uk-deaths-while-waiting-for-care-package-tops-1300-over-past-year-new-research-reveals)
* Wales Online: [Welsh council has worst social care waiting times in whole of UK](https://www.walesonline.co.uk/news/wales-news/welsh-council-worst-social-care-27426956)
* Yahoo! News: [Social care: People dying while waiting for care as councils and carers 
"have their hands tied"](https://uk.news.yahoo.com/social-care-people-dying-while-074556695.html?guccounter=1&guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAAI6bm6CUefYkhdQHe6cA4n9qQ37FO_K-x8GW8VdZy9Z77AUjVxiPcUs05bihwzsSvYZRMZtOrgMgjxlHqsQ-Sq4kf4ZxoCpWa1j4s5BpaTgh0ZDAKct1a_tZnTYcQzMgeJtWnx_r49Jb3owmLl215BUbvyc65nJK9S2Gbwp7BD3S)

Usage for the second story includes:

* BBC North West: [Hospital discharges: Getting patients home has become a 'real challenge'](https://www.bbc.co.uk/news/uk-england-merseyside-67345936)
* Ireland Live: [Number of patients who faced delayed discharge rose in September](https://www.ireland-live.ie/news/scotland/1342285/number-of-patients-who-faced-delayed-discharge-rose-in-september.html)
* Northern Echo: [Durham and Darlington patients stuck in hospital unnecessarily](https://www.thenorthernecho.co.uk/news/23908453.durham-darlington-patients-stuck-hospital-unnecessarily/)
* Planet Radio: [Study shows extent of hospital 'bed blocking' across North Yorkshire](https://planetradio.co.uk/hits-radio/north-yorkshire/news/concern-over-bed-blocking-figures-in-north-yorkshire-hospitals/)
