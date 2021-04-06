---
title: funzione glListBase (GL. h)
description: La funzione glListBase imposta la base dell'elenco di visualizzazione per glCallLists.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- funzione glListBase OpenGL
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
ms.openlocfilehash: c46af03477afc1b656df3a321fd8aa652b034b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963869"
---
# <a name="gllistbase-function"></a>glListBase (funzione)

La funzione **glListBase** imposta la base dell'elenco di visualizzazione per **glCallLists**.

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

Offset integer che verrà aggiunto agli offset [**glCallLists**](glcalllists.md) per generare i nomi degli elenchi di visualizzazione. Il valore iniziale è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glListBase** specifica una matrice di offset. I nomi degli elenchi di visualizzazione vengono generati aggiungendo *base* a ogni offset. Vengono eseguiti nomi che fanno riferimento a elenchi di visualizzazione validi; gli altri vengono ignorati.

La funzione seguente recupera le informazioni correlate a **glListBase**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con elenco GL \_ argomento \_ base

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> </dl>

 

 





