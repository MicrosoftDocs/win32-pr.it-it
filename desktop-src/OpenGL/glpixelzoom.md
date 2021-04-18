---
title: funzione glPixelZoom (GL. h)
description: La funzione glPixelZoom specifica i fattori di zoom pixel.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- funzione glPixelZoom OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320426"
---
# <a name="glpixelzoom-function"></a>glPixelZoom (funzione)

La funzione **glPixelZoom** specifica i fattori di zoom pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*XFactor* 
</dt> <dd>

Fattore di zoom *x* per le operazioni di scrittura in pixel.

</dd> <dt>

*yfactor* 
</dt> <dd>

Il fattore di zoom *y* per le operazioni di scrittura in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glPixelZoom** specifica i valori per i fattori di zoom *x* e *y* . Durante l'esecuzione di [**glDrawPixels**](gldrawpixels.md) o [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) è la posizione raster corrente e un dato elemento si trova nella riga *n* e *m* del rettangolo pixel, quindi i pixel i cui centri si trovano nel rettangolo con angoli

![Equazione che mostra le posizioni in cui i pixel sono candidati per la sostituzione.](images/pix05.png)

sono candidati per la sostituzione. Vengono modificati anche tutti i pixel il cui centro si trova sul bordo inferiore o sinistro dell'area rettangolare.

I fattori di zoom pixel non sono limitati ai valori positivi. I fattori di zoom negativi riflettono l'immagine risultante sulla posizione raster corrente.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glPixelZoom**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Zoom \_ X

**glGet** con argomento GL \_ Zoom \_ Y

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> </dl>

 

 





