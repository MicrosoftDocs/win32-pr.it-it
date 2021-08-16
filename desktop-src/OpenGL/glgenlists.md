---
title: Funzione glGenLists (Gl.h)
description: La funzione glGenLists genera un set contiguo di elenchi di visualizzazione vuoti.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- Funzione glGenLists OpenGL
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
ms.openlocfilehash: 7a916b163f2ec04e51da06263aed0f76f5e4dd6b51b7eca9fdbca8965644fdd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360398"
---
# <a name="glgenlists-function"></a>Funzione glGenLists

La **funzione glGenLists** genera un set contiguo di elenchi di visualizzazione vuoti.

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

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *l'intervallo* era negativo.<br/>                                                                                                      |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGenLists** ha un argomento, *intervallo*. Restituisce un numero intero *n* tale che *l'intervallo* di elenchi di visualizzazione vuoti contigui, *denominati n*, *n* + 1, . . ., *n* + (*intervallo* - 1), vengono creati. Se *range* è zero, se non è disponibile alcun gruppo di nomi *contigui* di intervallo o se viene generato un errore, non viene generato alcun elenco di visualizzazione e viene restituito zero.

La funzione seguente recupera le informazioni correlate a **glGenLists**:

[**glIsList**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





