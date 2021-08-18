---
title: Funzione glIndexMask (Gl.h)
description: La funzione glIndexMask controlla la scrittura di singoli bit nei buffer dell'indice dei colori.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- Funzione glIndexMask OpenGL
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
ms.openlocfilehash: f8e022bb3cbb5be5ac15049b5e8bc128d2ac7e100d5bcec6a87988dd2d14c5d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012199"
---
# <a name="glindexmask-function"></a>Funzione glIndexMask

La **funzione glIndexMask** controlla la scrittura di singoli bit nei buffer dell'indice dei colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Maschera* 
</dt> <dd>

Maschera di bit per abilitare e disabilitare la scrittura di singoli bit nei buffer dell'indice dei colori. Inizialmente, la maschera è tutte quelle.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glIndexMask** controlla la scrittura di singoli bit nei buffer dell'indice dei colori. Gli n bit *meno* significativi della *maschera*, dove *1* è il numero di bit in un index buffer colore, specificare una maschera. Ogni volta che viene visualizzato un oggetto nella maschera, il bit corrispondente nel index buffer (o buffer) viene reso scrivibile. Se viene visualizzato uno zero, il bit è protetto da scrittura.

Questa maschera viene usata solo in modalità di indicizzazione dei colori e influisce solo sui buffer attualmente selezionati per la scrittura (vedere [**glDrawBuffer**](gldrawbuffer.md)). Inizialmente, tutti i bit sono abilitati per la scrittura.

La funzione seguente recupera le informazioni correlate a **glIndexMask:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ INDEX \_ WRITEMASK

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

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





