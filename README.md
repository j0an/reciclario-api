Reciclario API
==============

API para el sitio Reciclario.com.ar para el #BaHAckatonVerde del GCBA.

Reciclario.com.ar es una guía con información sobre residuos, que hacer con ellos y cuales son las mejores formas de desecharlos/reutilizarlos para minimizar el impacto ambiental de cada persona.

Creamos una API publica para acceder a esta información y asi desarrollar aplicaciones que ayuden a educar/concientizar.


## Endpoints

### Listado de residuos reciclables/no reciclables/compostables/otros

```
GET http://reciclario.com.ar/?json=get_posts&post_type=reciclable
GET http://reciclario.com.ar/?json=get_posts&post_type=no_reciclable
GET http://reciclario.com.ar/?json=get_posts&post_type=compostable
GET http://reciclario.com.ar/?json=get_posts&post_type=otras
```

### Busqueda de residuos
```
GET http://reciclario.com.ar/?json=get_search_results&search=film
```

#### Response
```
{
    "status": "ok",
    "count": 10,
    "count_total": 12,
    "pages": 2,
    "posts": [{
            "id": 882,
            "type": "compostable",
            "url": "http://reciclario.com.ar/?compostable=yerba-mate",
            "title": "Yerba Mate",
            "title_plain": "Yerba Mate",
            "content": "<h2>¿ES COMPOSTABLE?</h2>\n<p>La yerba mate es compostable y resulta un buen alimento para las lombrices si se tienen, además de que con sus vitaminas y minerales enriquece la tierra.</p>\n<h2>¿CÓMO LA SEPARO PARA FACILITAR SU COMPOSTAJE?</h2>\n<p>Si la yerba está muy húmeda puede aportar exceso de agua al compost, lo cuál es perjudicial para el compostaje. Se la puede dejar secar un poco antes de arrojarla al compost.</p>\n<h2></h2>\n",
            "excerpt": "<p>¿ES COMPOSTABLE? La yerba mate es compostable y resulta un buen alimento para las lombrices si se tienen, además de que con sus vitaminas y minerales enriquece la tierra. ¿CÓMO&#8230;</p>\n",
            "date": "2013-09-16 12:01:43",
            "modified": "2013-09-16 12:01:43",
            "attachments": [{
                "id": 883,
                "mime_type": "image/jpeg",
                "images": {
                    "full": {
                        "url": "http://reciclario.com.ar/wp-content/uploads/yerba.jpg",
                        "width": 500,
                        "height": 340
                    },
                    "thumbnail": {
                        "url": "http://reciclario.com.ar/wp-content/uploads/yerba-150x150.jpg",
                        "width": 150,
                        "height": 150
                    },
                    "medium": {
                        "url": "http://reciclario.com.ar/wp-content/uploads/yerba-300x204.jpg",
                        "width": 300,
                        "height": 204
                    },
                    "large": {
                        "url": "http://reciclario.com.ar/wp-content/uploads/yerba.jpg",
                        "width": 500,
                        "height": 340
                    }
                }
            }]
     }]
     ...
}
```