---
title: funzione glDeleteLists (GL. h)
description: La funzione glDeleteLists Elimina un gruppo contiguo di elenchi di visualizzazione.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- funzione glDeleteLists OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301798"
---
# <a name="gldeletelists-function"></a>glDeleteLists (funzione)

La funzione **glDeleteLists** Elimina un gruppo contiguo di elenchi di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*list* 
</dt> <dd>

Nome intero del primo elenco visualizzato da eliminare.

</dd> <dt>

*range* 
</dt> <dd>

Numero di elenchi di visualizzazione da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | l' *intervallo* è negativo.<br/>                                                                                                      |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glDeleteLists** causa l'eliminazione di un gruppo contiguo di elenchi di visualizzazione. Il parametro *List* è il nome del primo elenco visualizzato da eliminare e *Range* indica il numero di elenchi di visualizzazione da eliminare. Tutti gli elenchi di visualizzazione *d* con *List*  =  *d*  =  *List*  +  *Range* -1 vengono eliminati.

Tutte le posizioni di archiviazione allocate agli elenchi di visualizzazione specificati vengono liberate e i nomi sono disponibili per essere riutilizzati in un secondo momento. I nomi compresi nell'intervallo che non dispongono di un elenco di visualizzazione associato vengono ignorati. Se *Range* è zero, non viene eseguita alcuna operazione.

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

[**Remo**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**Pagina di**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





