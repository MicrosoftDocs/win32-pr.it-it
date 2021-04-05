---
title: funzione glBitmap (GL. h)
description: La funzione glBitmap disegna una bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- funzione glBitmap OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048470"
---
# <a name="glbitmap-function"></a>glBitmap (funzione)

La funzione **glBitmap** disegna una bitmap.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*width* 
</dt> <dd>

Larghezza in pixel dell'immagine bitmap.

</dd> <dt>

*height* 
</dt> <dd>

Altezza in pixel dell'immagine bitmap.

</dd> <dt>

*xorig* 
</dt> <dd>

Posizione *x* dell'origine nell'immagine bitmap. L'origine viene misurata dall'angolo inferiore sinistro della bitmap, con le direzioni giuste e verso l'alto sono gli assi positivi.

</dd> <dt>

*yorig* 
</dt> <dd>

Posizione *y* dell'origine nell'immagine bitmap. L'origine viene misurata dall'angolo inferiore sinistro della bitmap, con le direzioni giuste e verso l'alto sono gli assi positivi.

</dd> <dt>

*xmove* 
</dt> <dd>

Offset *x* da aggiungere alla posizione raster corrente dopo che la bitmap è stata disegnata.

</dd> <dt>

*ymove* 
</dt> <dd>

Offset *y* da aggiungere alla posizione raster corrente dopo che la bitmap è stata disegnata.

</dd> <dt>

*bitmap* 
</dt> <dd>

Indirizzo dell'immagine bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | la *larghezza* o l' *altezza* è negativa.<br/>                                                                                           |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Una bitmap è un'immagine binaria. Quando viene disegnata, la bitmap viene posizionata in relazione alla posizione raster corrente e i pixel framebuffer corrispondenti a 1S nella bitmap vengono scritti usando il colore o l'indice raster corrente. I pixel del buffer dei frame corrispondenti agli zeri nella bitmap non vengono modificati.

L'immagine bitmap viene interpretata come dati di immagine per la funzione [**glDrawPixels**](gldrawpixels.md) , con *larghezza* e *altezza* corrispondenti agli argomenti di larghezza e altezza della funzione e con il *tipo* impostato su GL \_ bitmap e *Format* impostato su GL \_ Color \_ index. Le modalità specificate utilizzando [**glPixelStore**](glpixelstore-functions.md) influiscono sull'interpretazione dei dati dell'immagine bitmap. le modalità specificate tramite [**glPixelTransfer**](glpixeltransfer.md) non sono disponibili.

Se la posizione raster corrente non è valida, **glBitmap** viene ignorato. In caso contrario, l'angolo inferiore sinistro dell'immagine bitmap viene posizionato alle coordinate della finestra seguenti:

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?

*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?

In queste coordinate (*x*<sub>r</sub> , *y*<sub>r</sub> ) è la posizione raster e (*x*? , *y*? ) è l'origine della bitmap. I frammenti vengono quindi generati per ogni pixel corrispondente a 1 nell'immagine bitmap. Questi frammenti vengono generati usando la coordinata *z*, il colore o l'indice dei colori e le coordinate correnti della trama raster. Vengono quindi trattati come se fossero stati generati da un punto, una linea o un poligono, tra cui il mapping di trama, la nebbia e tutte le operazioni per frammento, ad esempio Alpha e test di profondità.

Dopo che la bitmap è stata disegnata, le coordinate *x* e *y* della posizione raster corrente sono offset da *XMOVE* e *ymove*. Non viene apportata alcuna modifica alla coordinata *z* della posizione raster corrente o al colore raster, all'indice o alle coordinate di trama correnti.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glBitmap** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position

 

**glGet** con argomento GL \_ Current \_ \_ color raster

 

**glGet** con argomento GL \_ Current \_ \_ index raster

 

**glGet** con argomento con \_ \_ coordinate di \_ trama \_ raster correnti

 

**glGet** con argomento GL \_ Current \_ raster \_ position \_ valido

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





