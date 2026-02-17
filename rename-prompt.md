You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/595cb6ccb56826a802ed411cef875f0e.css",
    "context": {
      "path": "css/595cb6ccb56826a802ed411cef875f0e.css"
    }
  },
  {
    "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css",
    "context": {
      "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css",
    "context": {
      "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/0d80095142116c9205bbe6ba033c7f90.webp",
    "context": {
      "refs": [
        {
          "alt": "Master Data Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1856ddf31c92956adf856fb8ea94f77b.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e67c3fdfcd30ad2dd805481ef7c02be.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/36cda96908b71012c3fc4ba5f3e8c3e4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/37e7088b0083ada97e6e23c0397f5765.webp",
    "context": {
      "refs": [
        {
          "alt": "Actionable Insights",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/404a309dd986f51cd2f93f6028603094.webp",
    "context": {
      "refs": [
        {
          "alt": "Business Intelligence",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4a0d3064282ef955dbb3cdd9ab15d78f.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5764e1fcd93676b98374ca0775784fbf.webp",
    "context": {
      "refs": [
        {
          "alt": "HR Service Delivery (HRSD)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6137f02952d09fdd6b7b796df1f51bb8.webp",
    "context": {
      "refs": [
        {
          "alt": "Customer Service Management (CSM)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6414cf8d7a43206495cbc3caebbf0232.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/645301a1d9804987f358397a90022511.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6d0123f9df533e5884b51ea23efd201d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6ff892c88442c651683908353641951a.webp",
    "context": {
      "refs": [
        {
          "alt": "Why Choose RAMIN IT for ServiceNow?",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b983b3a639a4ac919afd62d168b0641.webp",
    "context": {
      "refs": [
        {
          "alt": "Data Quality",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c58c4f075f0c67098903cdad1218f7d.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8fdb1714cea5cd7d44ac592e95348676.webp",
    "context": {
      "refs": [
        {
          "alt": "Data Governance",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9868a209a88a3b5e3eaf38793204054b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aed873d36a3caed7e1b3e005c8c6a638.webp",
    "context": {
      "refs": [
        {
          "alt": "Procurement Service Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b61cb1358c535db6a1b2a4506ad3d184.webp",
    "context": {
      "refs": [
        {
          "alt": "Seamless Integration",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bd75f1b43b722bd6f7700017e5286374.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bdd3c4e88549c307d764b6f1b51757d9.webp",
    "context": {
      "refs": [
        {
          "alt": "IT Service Management (ITSM)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c89e480fe6375984aba94764bebfe76b.webp",
    "context": {
      "refs": [
        {
          "alt": "Field Service Management (FSM)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c922cff746e90301a9f639a14f40dc41.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d03cb282a8685f096623f69e9977aa02.webp",
    "context": {
      "refs": [
        {
          "alt": "Facilities Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e50a13282e58412387cd55d072c99468.webp",
    "context": {
      "refs": [
        {
          "alt": "Intelligent Automation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f286f962eec997ad3be7c7b984a9af59.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f798cbdb954a5abc1f0eee2b4afd7d14.webp",
    "context": {
      "refs": [
        {
          "alt": "IT Service Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8db8ae9252461e060d7f6d96d274f84.webp",
    "context": {
      "refs": [
        {
          "alt": "Data Analysis",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "RAMIN IT | IT Consulting \u201cServices & Solutions\u201d firm",
      "first_heading": "We Are RAMIN IT"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "servicenow-practice.html",
    "context": {
      "title": "ServiceNow Practice | Modernize Your Business with ServiceNow Implementation",
      "first_heading": "Modernize Your Business with ServiceNow Implementation"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.