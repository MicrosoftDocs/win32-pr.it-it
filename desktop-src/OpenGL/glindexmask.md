---
title: funzione glIndexMask (GL. h)
description: La funzione glIndexMask controlla la scrittura di singoli bit nei buffer di indice dei colori.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- funzione glIndexMask OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301165"
---
# <a name="glindexmask-function"></a>glIndexMask (funzione)

La funzione **glIndexMask** controlla la scrittura di singoli bit nei buffer di indice dei colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maschera* 
</dt> <dd>

Maschera di bit per abilitare e disabilitare la scrittura di singoli bit nei buffer di indice dei colori. Inizialmente, la maschera corrisponde a tutti gli altri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glIndexMask** controlla la scrittura di singoli bit nei buffer di indice dei colori. I *n* bit meno significativi della *maschera*, dove *1* è il numero di bit in un buffer di indice dei colori, specificare una maschera. Ogni volta che viene visualizzato un oggetto nella maschera, il bit corrispondente nel buffer dell'indice dei colori (o buffer) viene reso scrivibile. Quando viene visualizzato uno zero, il bit è protetto da scrittura.

Questa maschera viene utilizzata solo in modalità di indice dei colori e influiscono solo sui buffer attualmente selezionati per la scrittura (vedere [**glDrawBuffer**](gldrawbuffer.md)). Inizialmente, tutti i bit sono abilitati per la scrittura.

La funzione seguente recupera le informazioni correlate a **glIndexMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ index \_ WRITEMASK

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

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





