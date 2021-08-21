---
title: Funzione glPolygonStipple (Gl.h)
description: La funzione glPolygonStipple imposta il modello di stippling poligono.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- Funzione glPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f9098ab91af5f258f97e0878ae8cbcb19863ec3bc82765c2664683830539fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614907"
---
# <a name="glpolygonstipple-function"></a>Funzione glPolygonStipple

La **funzione glPolygonStipple** imposta il modello di stippling poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Maschera* 
</dt> <dd>

Puntatore a un modello a stipple 32x32 che verrà decompresso dalla memoria nello stesso modo in cui [**glDrawPixels**](gldrawpixels.md) decomprime i pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glPolygonStipple** imposta il modello di stippling poligono. Lo stippling dei poligoni, ad esempio lo stippling delle linee (vedere [**glLineStipple),**](gllinestipple.md)maschera alcuni frammenti prodotti dalla rasterizzazione, creando un modello. Stippling è indipendente dall'antialiasing poligonale.

Il parametro *mask* è un puntatore a un modello a stipple 32x32 archiviato in memoria  proprio  come i dati pixel forniti a **glDrawPixels** con altezza e larghezza pari a 32, un formato *pixel* di GL COLOR INDEX e il tipo di dati \_ GL \_  \_ BITMAP. Ciò significa che il modello di punta è rappresentato come matrice 32x32 di indici di colore a 1 bit compressi in byte senza segno. I parametri della funzione [**glPixelStore,**](glpixelstore-functions.md) ad esempio GL UNPACK SWAP BYTES e \_ GL \_ \_ \_ UNPACK \_ LSB \_ FIRST, influiscono sull'assemblaggio dei bit in un modello di base. Le operazioni di trasferimento dei pixel (spostamento, offset e mappa pixel) non vengono tuttavia applicate all'immagine della punta.

Lo stippling poligono è abilitato e disabilitato con [**glEnable**](glenable.md) **e glDisable** usando l'argomento GL \_ POLYGON \_ STIPPLE. Se abilitata, un frammento poligono rasterizzato con coordinate della finestra *x*<sub>w</sub> e *y*<sub>w</sub> viene inviato alla fase successiva di OpenGL se e solo se il bit (*x*<sub>w</sub> mod 32)th nella riga (*y*<sub>w</sub> mod 32)th del modello di stipla è uno. Quando l'stippling poligono è disabilitato, è come se il modello di stilo fosse tutto uno.

Le funzioni seguenti recuperano informazioni correlate **a glPolygonStipple:**

[**glGetPolygonStipple**](glgetpolygonstipple.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ POLYGON \_ STIPPLE

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

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





