# Database structure
   
![image](https://github.com/kubade123/gg-midterm/assets/86041365/f2ca25b1-9782-470f-b32f-b8cf6d8739b5)

In this version i'm still using models to define my databases (I haven't connected it to an external database)  
There are two models, videos and products. I include comment as one of the video's property.

# API Structure
## GET /videos
- **URL Params**  
  None
- **Data Params**  
  None
- **Headers**  
  Content-Type: application/json
- **Success Response:**  
- **Code:** 200  
  **Content:**
  ```
  {
    "status": "success",
    "message": "Berikut adalah list video",
    "videoList": [
        {
            "id": 1,
            "title": "video handphone",
            "thumbnail": "https://presisi.co/assets/images/news/2020/11/5fbbba6ca47541606138476-sudah.jpg"
        },
        {
            "id": 2,
            "title": "video processor",
            "thumbnail": "https://laptopnesia.com/wp-content/uploads/2018/07/Urutan-Processor-Intel-1.png"
        }
    ]
  }
   ```
- **Error Response:**  
     - **Code:** 404  
       **Content:**
   ```
   {
      status: 'Fail',
      message: 'List video kosong',
    }
    ```
## GET /videos/:id
- **URL Params**  
  _Required_: ```id=[integer]```
- **Data Params**  
  None
- **Headers**  
  Content-Type: application/json
- **Success Response:**  
- **Code:** 200    
  **Content:**
   ```
     {
       "status": "success",
       "videoThumbnail": "https://cdn0-production-images-kly.akamaized.net/5QbQKELPuya1JOcIC_Fbn7aa2Ss=/1200x900/smart/filters:quality(75):strip_icc():format(jpeg)/kly-media-production/medias/824785/original/047593200_1425897043-HyperX_Cloud_headset_black_Cloud-headset-model_08_08_04_2014_01_34-650x419.jpg",
       "productList": [
           {
               "id": 104,
               "videoId": 3,
               "title": "HyperX Cloud II Wireless",
               "productLink": "https://www.tokopedia.com/hyperxofficial/hyperx-cloud-ii-wireless-gaming-headset",
               "price": 2490000
           },
           {
               "id": 105,
               "videoId": 3,
               "title": "HyperX Cloud Alpha S",
               "productLink": "https://www.tokopedia.com/hyperxofficial/hyperx-cloud-alpha-s-gaming-headset-blue",
               "price": 1600000
           }
       ],
       "commentList": [
           {
               "username": "siijo_123",
               "comment": "pelan-pelan pak sopir",
               "createdAt": "27-07-2023 08:45:00"
           }
       ]
   }
   ```  
- **Error Response:**  
     - **Code:** 404
     - **Content:**
  ```
   {
      status: 'Fail',
      message: 'Product tidak ditemukan',
    }
   ```
     OR
  ```
       {
      status: 'Fail',
      message: 'Video tidak ditemukan',
    }
  ```
  
## GET /products/:videoId
- **URL Params**  
  None
- **Data Params**  
  None
- **Headers**  
  Content-Type: application/json
- **Success Response:**  
- **Code**  
  **Content:**  
- **Error Response:**  
     - **Code:**
 

## GET /videos/:id/comments
- **URL Params**  
  None
- **Data Params**  
  None
- **Headers**  
  Content-Type: application/json
- **Success Response:**  
- **Code**  
  **Content:**  
- **Error Response:**  
     - **Code:**
 

## GET /videos/:id/comments
- **URL Params**  
  None
- **Data Params**  
  None
- **Headers**  
  Content-Type: application/json
- **Success Response:**  
- **Code**  
  **Content:**  
- **Error Response:**  
     - **Code:**



2. API structure
3. List API request and response
4. How to run guide

