---
title: funzione glGetPixelMapfv (GL. h)
description: Le funzioni glGetPixelMapfv, glGetPixelMapuiv e glGetPixelMapusv restituiscono la mappa pixel specificata. | funzione glGetPixelMapfv (GL. h)
ms.assetid: b09f4799-8e36-4d4f-90d8-4a8ed3d15718
keywords:
- funzione glGetPixelMapfv OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f73fb817c347832dfc6a09636173641e5c869b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886119"
---
# <a name="glgetpixelmapfv-function"></a>glGetPixelMapfv (funzione)

Le funzioni **glGetPixelMapfv**, [**glGetPixelMapuiv**](glgetpixelmapuiv.md)e [**glGetPixelMapusv**](glgetpixelmapusv.md) restituiscono la mappa pixel specificata.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetPixelMapfv(
   GLenum  map,
   GLfloat *values
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*map* 
</dt> <dd>

Nome della mappa dei pixel da restituire. I valori accettati sono GL \_ pixel \_ Map \_ i to \_ \_ i, GL \_ pixel \_ Map \_ S \_ to \_ S, GL \_ pixel \_ Map \_ i \_ to \_ R, GL \_ pixel \_ Map \_ i \_ to \_ g, GL \_ pixel \_ Map \_ i \_ a \_ b, GL \_ pixel \_ Map \_ i \_ to \_ a, GL \_ pixel \_ Map \_ r \_ to \_ r, GL \_ pixel map \_ \_ g \_ to \_ g, GL \_ pixel map \_ \_ B \_ to \_ b e \_ GL \_ pixel \_ \_ \_ Map a.

</dd> <dt>

*valori* 
</dt> <dd>

Restituisce il contenuto della mappa pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *mapping* non è un valore accettato.<br/>                                                                                           |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Per una descrizione dei valori accettabili per il parametro *Map* , vedere [**glPixelMap**](glpixelmap.md) . La funzione **glGetPixelMap** restituisce in *valori* il contenuto della mappa pixel specificata in *Map*. Usare i mapping dei pixel durante l'esecuzione di [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)e [**glTexImage2D**](glteximage2d.md) per eseguire il mapping degli indici di colore, degli stencil, dei componenti dei colori e dei componenti di profondità ad altri valori.

I valori interi senza segno, se richiesti, vengono mappati linearmente dalla rappresentazione a virgola fissa o a virgola mobile interna, in modo che 1,0 sia mappata al valore integer rappresentabile più grande e 0,0 venga eseguito il mapping a zero. I valori restituiti Unsigned Integer non sono definiti se il valore della mappa non è compreso nell'intervallo \[ 0, 1 \] .

Per determinare la dimensione richiesta della *mappa*, chiamare [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con la costante simbolica appropriata.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto dei *valori*.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glGetPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ pixel \_ Map \_ i \_ to \_ i \_ size

**glGet** con argomento \_ \_ di mapping GL pixel per la \_ \_ \_ \_ dimensione s

**glGet** con argomento GL \_ pixel \_ Map \_ I \_ to \_ R \_ size

**glGet** con argomento GL \_ pixel \_ mapping \_ I \_ a \_ G \_ size

**glGet** con argomento GL \_ pixel \_ Map \_ I \_ a \_ B \_ size

**glGet** con argomento GL \_ pixel \_ mappa \_ I \_ a \_ una \_ dimensione

**glGet** con argomento GL \_ pixel \_ Map \_ r \_ to \_ r \_ size

**glGet** con argomento GL \_ pixel \_ mappa \_ g \_ a \_ g \_ size

**glGet** con argomento GL \_ pixel \_ mappa \_ b \_ a \_ b \_ dimensioni

**glGet** con argomento GL \_ pixel \_ mappa \_ a \_ \_ una \_ dimensione

**glGet** con argomento \_ tabella di \_ mappa pixel max \_ \_

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

 

 





