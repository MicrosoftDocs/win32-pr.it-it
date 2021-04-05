---
title: funzione glGenLists (GL. h)
description: La funzione glGenLists genera un set contiguo di elenchi di visualizzazione vuoti.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- funzione glGenLists OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740479"
---
# <a name="glgenlists-function"></a>glGenLists (funzione)

La funzione **glGenLists** genera un set contiguo di elenchi di visualizzazione vuoti.

## <a name="syntax"></a>Sintassi


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*range* 
</dt> <dd>

Numero di elenchi di visualizzazione vuoti contigui da generare.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | l' *intervallo* è negativo.<br/>                                                                                                      |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGenLists** ha un argomento, *Range*. Restituisce un integer *n* *tale da visualizzare elenchi di visualizzazione* vuoti contigui, denominati *n*, *n* + 1,. . ., *n* + (*intervallo* -1), vengono creati. Se *Range* è zero, se non sono disponibili gruppi di nomi contigui di *intervallo* o se viene generato un errore, non viene generato alcun elenco di visualizzazione e viene restituito zero.

La funzione seguente recupera le informazioni correlate a **glGenLists**:

[**Pagina di**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**Pagina di**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





