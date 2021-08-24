---
title: Funzione glGetPixelMapusv (Gl.h)
description: Le funzioni glGetPixelMapfv, glGetPixelMapuiv e glGetPixelMapusv restituiscono la mappa pixel specificata. | Funzione glGetPixelMapusv (Gl.h)
ms.assetid: 68b71f9b-5666-4183-aeb8-4c9f09bc5d9c
keywords:
- Funzione glGetPixelMapusv OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f879da92c9c31b4f44a7e65d8648f94c94fcfaaa8ab3a9d88a39ffc15bd57e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494131"
---
# <a name="glgetpixelmapusv-function"></a>Funzione glGetPixelMapusv

Le [**funzioni glGetPixelMapfv**](glgetpixelmapfv.md), [**glGetPixelMapuiv**](glgetpixelmapuiv.md)e **glGetPixelMapusv** restituiscono la mappa pixel specificata.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetPixelMapusv(
   GLenum   map,
   GLushort *values
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*map* 
</dt> <dd>

Nome della mappa pixel da restituire. I valori accettati sono GL \_ PIXEL MAP I TO \_ \_ \_ \_ I, GL PIXEL MAP S \_ TO \_ \_ \_ \_ S, GL PIXEL MAP \_ I TO \_ \_ \_ \_ R, GL PIXEL MAP I \_ TO \_ \_ \_ \_ G, GL PIXEL MAP \_ I TO \_ \_ \_ \_ B, GL PIXEL MAP I \_ TO \_ \_ \_ \_ A, GL PIXEL MAP R \_ TO \_ \_ \_ \_ R, GL PIXEL MAP G \_ TO \_ \_ \_ \_ G, GL PIXEL MAP \_ B TO B e GL PIXEL MAP A \_ \_ \_ \_ \_ \_ \_ \_ \_ A.

</dd> <dt>

*Valori* 
</dt> <dd>

Restituisce il contenuto della mappa pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *map* non è un valore accettato.<br/>                                                                                           |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Per una descrizione dei valori accettabili per il parametro *map,* vedere [**glPixelMap.**](glpixelmap.md) La **funzione glGetPixelMap** restituisce in *valori* il contenuto della mappa pixel specificata in *map*. Usare mappe pixel durante l'esecuzione di [**glReadPixels,**](glreadpixels.md) [**glDrawPixels,**](gldrawpixels.md) [**glCopyPixels,**](glcopypixels.md) [**glTexImage1D**](glteximage1d.md)e [**glTexImage2D**](glteximage2d.md) per eseguire il mapping di indici di colore, indici di stencil, componenti di colore e componenti di profondità ad altri valori.

I valori interi senza segno, se richiesti, vengono mappati in modo lineare dalla rappresentazione interna fissa o a virgola mobile in modo che 1.0 esee 1.0 sia mappato al valore integer rappresentabile più grande e 0,0 sia mappato a zero. I valori integer senza segno restituiti non sono definiti se il valore della mappa non è compreso nell'intervallo \[ 0,1. \]

Per determinare le dimensioni richieste della *mappa,* chiamare [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con la costante simbolica appropriata.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto dei *valori*.

Le funzioni seguenti recuperano informazioni correlate **a glGetPixelMap**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet con** argomento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





