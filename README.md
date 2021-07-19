# notes-app-back-end
 [Notes app](http://notesapp-v1.dicodingacademy.com/) back end server RESTful API project from Dicoding's Belajar Membuat Aplikasi Back-End untuk Pemula course

## Project Criteria (CRUD):
1. **Create Notes**

    Notes saved in JavaScript array in server memory using `'/notes'` path route and `POST` method.

    * Client request body JSON data:
        ```js
        {
            "title": "Judul Catatan",
            "tags": ["Tag 1", "Tag 2"],
            "body": "Konten catatan"
        }
        ```

    * Notes data in saved array:
        ```js
        {
            id: string,
            title: string,
            createdAt: string,
            updatedAt: string,
            tags: array of string,
            body: string,
        },
        ```

    If saved successfully, server gives response code **201 (created)** and return data in JSON:
    ```js
    {
        "status": "success",
        "message": "Catatan berhasil ditambahkan",
        "data": {
            "noteId": "<noteid>"
        }
    }
    ```
    If failed, server gives response code **500** and return data in JSON:
    ```js
    {
        "status": "error",
        "message": "Catatan gagal untuk ditambahkan"
    }
    ```

2. **Show saved notes**

    Show all or specific saved notes data using `GET` method.
    * Show all -- path `'/notes'`
    * Show specific note by id -- path `'/notes/{id}'`

3. **Update saved notes**

    Change/update saved notes data using `PUT` method.

4. **Delete notes**

    Delete saved notes using `DELETE` method.


## Project structure:
* **server.js** : make, config, and run HTTP server using Hapi.
* **routes.js** : server routing config.
* **handler.js** : handler functions used in **routes**.
* **notes.js** : notes data in object array.