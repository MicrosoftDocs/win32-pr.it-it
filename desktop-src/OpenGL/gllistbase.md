---
title: Funzione glListBase (Gl.h)
description: La funzione glListBase imposta la base dell'elenco di visualizzazione per glCallLists.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- Funzione glListBase OpenGL
topic_type:
- apiref
api_name:
- glListBase
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ba7cbe7b179184efa739ac3492f4e74b36f56abe0f02498a0e1a688b85183a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938518"
---
# <a name="gllistbase-function"></a>Funzione glListBase

La **funzione glListBase** imposta la base dell'elenco di visualizzazione **per glCallLists**.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glListBase(
   GLuint base
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*base* 
</dt> <dd>

Offset intero che verrà aggiunto agli offset [**glCallLists**](glcalllists.md) per generare i nomi degli elenchi visualizzati. Il valore iniziale è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glListBase** specifica una matrice di offset. I nomi degli elenchi visualizzati vengono generati aggiungendo *base* a ogni offset. I nomi che fanno riferimento a elenchi di visualizzazione validi vengono eseguiti; altri vengono ignorati.

La funzione seguente recupera le informazioni correlate a **glListBase**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ LIST \_ BASE

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





