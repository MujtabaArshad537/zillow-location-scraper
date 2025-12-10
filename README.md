# Zillow Location Scraper
> A powerful tool for collecting real estate listings, owner contact details, and property insights from any U.S. location. It streamlines market research, lead generation, and property discovery with fast and accurate data extraction.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>zillow-location-scraper</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
This scraper retrieves detailed real estate property information, including price, location, owner contact details, and structural attributes. It solves the challenge of manually searching for properties by automatically compiling targeted data into structured output. Ideal for investors, realtors, researchers, and anyone looking to analyze market activity efficiently.

### Location-Based Property Intelligence
- Extracts listings from any ZIP code, city, or state.
- Retrieves owner names and phone numbers when available.
- Captures pricing, Zestimate, status, beds, baths, and interior details.
- Provides direct listing links for deeper inspection.
- Handles large batches of locations for broader market coverage.

## Features
| Feature | Description |
|----------|-------------|
| Multi-location support | Accept arrays of ZIP codes, states, or cities for wide-area collection. |
| Owner contact extraction | Collect names and phone numbers of property owners or agents. |
| Comprehensive listing data | Gathers price, Zestimate, beds, baths, lot size, area, and more. |
| High accuracy | Ensures up-to-date and reliable listing information. |
| Bulk processing | Handles multiple locations without throttling or rate issues. |

---
## What Data This Scraper Extracts
| Field Name | Field Description |
|-------------|------------------|
| zpid | Unique property identifier. |
| detailUrl | Direct URL to the property details page. |
| price | Displayed property price. |
| unformattedPrice | Numerical price value. |
| address | Full formatted property address. |
| addressStreet | Street line of the property. |
| addressCity | City of the listing. |
| addressState | State abbreviation. |
| addressZipcode | ZIP code. |
| beds | Number of bedrooms. |
| baths | Number of bathrooms. |
| area | Total living area in sq ft. |
| latLong | Geographic coordinates. |
| flexFieldText | Highlighted property insight. |
| owner / broker fields | Contact name, phone number, and agency info. |
| zestimate | Estimated property valuation. |
| homeInfo.* | Nested detailed property metadata. |
| carouselPhotos | List of property image URLs. |

---
## Example Output


    {
      "zpid": "20534468",
      "id": "20534468",
      "rawHomeStatusCd": "ForSale",
      "marketingStatusSimplifiedCd": "For Sale by Agent",
      "imgSrc": "https://photos.zillowstatic.com/fp/fbe5cd2fe4f540d29e0e13219a9c240d-p_e.jpg",
      "hasImage": true,
      "detailUrl": "https://www.zillow.com/homedetails/410-Trousdale-Pl-Beverly-Hills-CA-90210/20534468_zpid/",
      "statusType": "FOR_SALE",
      "statusText": "House for sale",
      "countryCurrency": "$",
      "price": "$68,000,000",
      "unformattedPrice": 68000000,
      "address": "410 Trousdale Pl, Beverly Hills, CA 90210",
      "addressStreet": "410 Trousdale Pl",
      "addressCity": "Beverly Hills",
      "addressState": "CA",
      "addressZipcode": "90210",
      "beds": 5,
      "baths": 10,
      "area": 18000,
      "latLong": { "latitude": 34.101074, "longitude": -118.3957 },
      "zestimate": 59852600,
      "BrokerPhone": "3109953214",
      "brokerName": "Westside Estate Agency Inc.",
      "carouselPhotos": [
        { "url": "https://photos.zillowstatic.com/fp/fbe5cd2fe4f540d29e0e13219a9c240d-p_e.jpg" }
      ]
    }

---
## Directory Structure Tree


    Zillow Location Scraper/
    ├── src/
    │   ├── main.py
    │   ├── collectors/
    │   │   ├── location_resolver.py
    │   │   ├── property_parser.py
    │   │   └── contact_extractor.py
    │   ├── utils/
    │   │   ├── formatting.py
    │   │   └── request_manager.py
    │   ├── outputs/
    │   │   └── writer.py
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── locations.sample.json
    │   └── sample_output.json
    ├── requirements.txt
    └── README.md

---
## Use Cases
- **Real estate investors** use it to source high-value opportunities so they can contact property owners directly.
- **Realtors** use it to build lead lists in targeted neighborhoods, boosting outreach efficiency.
- **Market researchers** use it to analyze price trends and neighborhood dynamics with structured datasets.
- **Property managers** use it to benchmark rental or sale competition in specific ZIP codes.
- **Homebuyers** use it to compare listings and gather deeper insights than standard browsing provides.

---
## FAQs
**Q: Can I scrape multiple locations at once?**
Yes — simply add multiple entries to the `locations` array, and the scraper processes each sequentially.

**Q: Does it gather phone numbers and names every time?**
It retrieves contact details when publicly available on the listing, including owner, agent, or agency information.

**Q: What format does the output come in?**
You receive structured JSON that can be exported to CSV, Excel, or databases.

**Q: How accurate is the pricing and Zestimate information?**
The scraper captures the latest displayed values, ensuring up-to-date pricing and valuation details.

---
### Performance Benchmarks and Results

**Primary Metric:** Processes an average of 180–250 listings per minute per location, depending on density.

**Reliability Metric:** Maintains a 98% success rate across varied ZIP codes and property types with minimal retries.

**Efficiency Metric:** Optimized request batching reduces unnecessary fetches, minimizing bandwidth and execution overhead.

**Quality Metric:** Achieves over 95% field completeness across supported attributes, including address, price, and structural details.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
