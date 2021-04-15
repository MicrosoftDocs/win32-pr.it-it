---
title: funzione glPolygonStipple (GL. h)
description: La funzione glPolygonStipple imposta il pattern punteggiatura del poligono.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- funzione glPolygonStipple OpenGL
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
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477236"
---
# <a name="glpolygonstipple-function"></a>glPolygonStipple (funzione)

La funzione **glPolygonStipple** imposta il pattern punteggiatura del poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maschera* 
</dt> <dd>

Un puntatore a un modello di stipple 32x32 che verrà decompresso dalla memoria nello stesso modo in cui [**glDrawPixels**](gldrawpixels.md) decomprime i pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glPolygonStipple** imposta il pattern punteggiatura del poligono. Poligono punteggiatura, ad esempio la linea punteggiatura (vedere [**glLineStipple**](gllinestipple.md)), maschera alcuni frammenti prodotti dalla rasterizzazione, creando un modello. Punteggiatura è indipendente dall'anti-aliasing del poligono.

Il parametro *mask* è un puntatore a un modello stipple 32x32 che viene archiviato in memoria esattamente come i dati pixel forniti a **glDrawPixels** con *altezza* e *larghezza* uguali a 32, un *formato* pixel di indice dei \_ colori GL e il \_ *tipo* di dati della \_ bitmap GL. Ovvero, il modello stipple è rappresentato come una matrice 32x32 di indici di colore a 1 bit compressi in byte senza segno. I parametri della funzione [**glPixelStore**](glpixelstore-functions.md) , ad esempio GL \_ unpack \_ swap \_ bytes e GL \_ depack \_ LSB \_ First, influiscono sul montaggio dei bit in un modello stipple. Tuttavia, le operazioni di trasferimento dei pixel, ovvero MAIUSC, offset e mappa pixel, non vengono applicate all'immagine di stipple.

Polygon punteggiatura è abilitato e disabilitato con [**glEnable**](glenable.md) e **glDisable** usando l'argomento GL \_ Polygon \_ stipple. Se abilitata, un frammento di poligono rasterizzato con le coordinate della finestra *x*<sub>w</sub> e *y*<sub>w</sub> viene inviato alla fase successiva di OpenGL se e solo se il bit (*x*<sub>w</sub> mod 32) nella riga (*y*<sub>w</sub> mod 32) del modello stipple è uno. Quando il poligono punteggiatura è disabilitato, è come se il modello stipple fosse tutti quelli.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glPolygonStipple**:

[**glGetPolygonStipple**](glgetpolygonstipple.md)

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Polygon \_ stipple

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

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





