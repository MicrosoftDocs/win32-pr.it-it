---
title: funzione glGetPolygonStipple (GL. h)
description: La funzione glGetPolygonStipple restituisce il pattern stipple del poligono.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- funzione glGetPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873461"
---
# <a name="glgetpolygonstipple-function"></a>glGetPolygonStipple (funzione)

La funzione **glGetPolygonStipple** restituisce il pattern stipple del poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maschera* 
</dt> <dd>

Restituisce il pattern stipple.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetPolygonStipple** restituisce un modello stipple poligono 32x32 tramite il parametro *mask* . Il modello viene compresso in memoria come se fosse stato chiamato [**glReadPixels**](glreadpixels.md) con *altezza* e *larghezza* di 32, il *tipo* di \_ bitmap GL e il *formato* dell'indice dei \_ colori GL \_ e il modello stipple fosse archiviato in un buffer di indice colori 32x32 interno. Diversamente da **glReadPixels**, tuttavia, le operazioni di trasferimento dei pixel (spostamento, offset e mappa pixel) non vengono applicate all'immagine stipple restituita.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto della *maschera*.

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

[**Remo**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





