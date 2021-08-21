---
title: Funzione glBitmap (Gl.h)
description: La funzione glBitmap disegna una bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- Funzione glBitmap OpenGL
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
ms.openlocfilehash: 8da90b8e592f8cd9d1702c7810990042b3929ef40e70814e8fb7d3326d902cb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082231"
---
# <a name="glbitmap-function"></a>Funzione glBitmap

La **funzione glBitmap** disegna una bitmap.

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

Posizione *x* dell'origine nell'immagine bitmap. L'origine viene misurata dall'angolo inferiore sinistro della bitmap, con gli assi positivi verso destra e verso l'alto.

</dd> <dt>

*yorig* 
</dt> <dd>

Posizione *y* dell'origine nell'immagine bitmap. L'origine viene misurata dall'angolo inferiore sinistro della bitmap, con gli assi positivi verso destra e verso l'alto.

</dd> <dt>

*xmove* 
</dt> <dd>

Offset *x* da aggiungere alla posizione raster corrente dopo il disegnato della bitmap.

</dd> <dt>

*ymove* 
</dt> <dd>

Offset *y* da aggiungere alla posizione raster corrente dopo il disegnato della bitmap.

</dd> <dt>

*bitmap* 
</dt> <dd>

Indirizzo dell'immagine bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *width* o *height* è negativo.<br/>                                                                                           |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Una bitmap è un'immagine binaria. Quando viene disegnata, la bitmap viene posizionata rispetto alla posizione raster corrente e i pixel framebuffer corrispondenti a 1 nella bitmap vengono scritti usando il colore o l'indice raster corrente. I pixel del buffer di frame corrispondenti agli zeri nella bitmap non vengono modificati.

L'immagine bitmap viene interpretata come dati di immagine  per  la funzione [**glDrawPixels,**](gldrawpixels.md) con larghezza e altezza corrispondenti agli argomenti width e height di tale funzione e con *tipo* impostato su GL BITMAP e format impostato su \_ GL COLOR  \_ \_ INDEX. Le modalità specificate tramite [**glPixelStore**](glpixelstore-functions.md) influiscono sull'interpretazione dei dati delle immagini bitmap. le modalità specificate con [**glPixelTransfer**](glpixeltransfer.md) non lo fanno.

Se la posizione raster corrente non è valida, **glBitmap viene** ignorato. In caso contrario, l'angolo inferiore sinistro dell'immagine bitmap viene posizionato in corrispondenza delle coordinate della finestra seguenti:

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?

*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?

In queste coordinate (*x*<sub>r</sub> , *y*<sub>r</sub> ) è la posizione raster e (*x*? ? , *y*? ) è l'origine della bitmap. I frammenti vengono quindi generati per ogni pixel corrispondente a 1 nell'immagine bitmap. Questi frammenti vengono generati usando la coordinata *z* corrente, il colore o l'indice dei colori e le coordinate correnti della trama raster. Vengono quindi trattati come se fossero stati generati da un punto, una linea o un poligono, tra cui mapping di trame, fogging e tutte le operazioni per frammento, ad esempio il test alfa e di profondità.

Dopo aver disegnato la bitmap, *le coordinate x* e *y* della posizione raster corrente vengono offset da *xmove* *e ymove*. Non viene apportata alcuna modifica alla *coordinata z* della posizione raster corrente o alle coordinate correnti del colore raster, dell'indice o della trama.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glBitmap:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ CURRENT \_ RASTER \_ POSITION

 

**glGet con** argomento GL \_ CURRENT \_ RASTER \_ COLOR

 

**glGet con** argomento GL \_ CURRENT \_ RASTER \_ INDEX

 

**glGet con** argomento GL \_ CURRENT \_ RASTER TEXTURE \_ \_ COORDS

 

**glGet con** argomento GL \_ CURRENT \_ RASTER POSITION \_ \_ VALID

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





