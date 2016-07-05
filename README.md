# Facebook Album Fetcher API

A simple API to fetch Facebook Page Album and Photos

## Create Facebook App - Follow [this](http://www.codeofaninja.com/2013/02/facebook-appId-and-appSecret.html) tutorial

	appId: somerandomkey
	appSecret: somerandomkey

## Generate Access Token

	https://graph.facebook.com/oauth/access_token?client_id=APP_ID&client_secret=APP_SECRET&grant_type=client_credentials
	
## Fetch Albums

	https://graph.facebook.com/v2.3/FACEBOOK_PAGE_ID/albums?fields=id,name,description,link,cover_photo,count&access_token=ACCESS_TOKEN

### Sample Output

	{
	   "data": [
	      {
	         "id": "542528065929026",
	         "name": "Timeline Photos",
	         "link": "https://www.facebook.com/album.php?fbid=542528065929026&id=542323912616108&aid=1073741828",
	         "cover_photo": {
	            "created_time": "2016-06-30T14:43:22+0000",
	            "name": "We're preparing materials for API Development class. \n\nIn this class you will learn fundamental of the API, How to develop API from scratch and of course, develop API with awesome Laravel framework!\n\ninsyaAllah, first class expected in 3 weeks time!\n\nLaravel knowledge is compulsary!\n\n#cleaniquecoders\n#api\n#laravel",
	            "id": "595651460616686"
	         },
	         "count": 54
	      },
	   ],
	   "paging": {
	      "cursors": {
	         "before": "NTQyNTI4MDY1OTI5MDI2",
	         "after": "NTQyMzI0MzcyNjE2MDYy"
	      }
	   }
	}

## Display Photo

	https://graph.facebook.com/v2.3/COVER_PHOTO_ID/picture?access_token=ACCESS_TOKEN
