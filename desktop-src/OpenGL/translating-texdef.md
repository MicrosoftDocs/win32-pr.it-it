---
title: Conversione di texdef
description: L'esempio di codice seguente è una definizione di trama di IRIS GL
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Porting di IRIS GL, trama
- porting da IRIS GL, trama
- porting in OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
- Porting di IRIS GL, texdef
- porting da IRIS GL, texdef
- porting in OpenGL da IRIS GL, texdef
- Porting OpenGL da IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856810"
---
# <a name="translating-texdef"></a>Conversione di texdef

L'esempio di codice seguente è una definizione di trama di IRIS GL:


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



Nell'esempio precedente, **texdef** specifica il filtro del \_ punto TX sia come ingrandimento che come filtro di riduzione a icona e TX \_ Ripeti come meccanismo di wrapping. Specifica anche l'immagine della trama, **ovvero \_ granito**.

In OpenGL, [**glTexImage**](glteximage1d.md) specifica l'immagine e [glTexParameter](gltexparameter-functions.md) imposta la proprietà. Per tradurre le definizioni delle trame IRIS GL, sostituire la funzione **textdef** con **glTexImage** e una o più chiamate a **glTexParameter**.

Il codice di IRIS GL precedente ha un aspetto simile al seguente quando viene convertito in OpenGL:


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



La tabella seguente elenca i parametri di trama di IRIS GL e i parametri OpenGL equivalenti.



| Parametro trama IRIS GL | Parametro trama OpenGL                                  |
|---------------------------|-----------------------------------------------------------|
| \_MINFILTER TX             | \_ \_ Filtro minimo trama \_ GL                                  |
| \_MAGFILTER TX             | \_ \_ filtro mag trama di contabilità \_                                  |
| TX \_ wrap, TX \_ Wrap \_ S     | \_wrapping di trama GL \_ \_                                      |
| TX \_ wrap, TX \_ Wrap \_ T     | \_ \_ \_ \_ \_ colore bordo trama TGL \_ trama a capo<br/> |



 

La tabella seguente elenca i valori possibili dei parametri di trama di IRIS GL e i parametri OpenGL equivalenti.



| Parametro trama IRIS GL | Parametro trama OpenGL     |
|---------------------------|------------------------------|
| \_punto TX                 | GL \_ più vicino                  |
| \_BIlineare TX              | \_linea GL                   |
| \_punto MIPMAP \_ TX         | GL \_ più vicino \_ MIPMAP \_ più vicino |
| TX \_ MIPMAP \_ bilinear      | \_MIPMAP lineare \_ \_ più vicino  |
| \_MIPMAP \_ lineare TX        | GL \_ più vicino \_ MIPMAP \_ lineare  |
| \_TRIlineare TX             | \_MIPMAP lineare \_ lineare \_   |



 

 

 





