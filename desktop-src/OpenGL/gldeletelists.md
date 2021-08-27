---
title: Funzione glDeleteLists (Gl.h)
description: La funzione glDeleteLists elimina un gruppo contiguo di elenchi di visualizzazione.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- Funzione glDeleteLists OpenGL
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
ms.openlocfilehash: 6ec0ffac68119f6f2080ef6ca96ec63fbd35176d3541464a89b6c31f4941b4c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081661"
---
# <a name="gldeletelists-function"></a>Funzione glDeleteLists

La **funzione glDeleteLists** elimina un gruppo contiguo di elenchi di visualizzazione.

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

Nome intero del primo elenco di visualizzazione da eliminare.

</dd> <dt>

*range* 
</dt> <dd>

Numero di elenchi visualizzati da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *L'intervallo* era negativo.<br/>                                                                                                      |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glDeleteLists** causa l'eliminazione di un gruppo contiguo di elenchi di visualizzazione. Il *parametro list* è il nome del primo elenco visualizzato da eliminare e *range* è il numero di elenchi visualizzati da eliminare. Tutti gli elenchi visualizzati *d* con   =  *l'elenco d*  =    +  *list range* - 1 vengono eliminati.

Tutti i percorsi di archiviazione allocati agli elenchi di visualizzazione specificati vengono liberati e i nomi sono disponibili per il riutilizzo in un secondo momento. I nomi all'interno dell'intervallo a cui non è associato un elenco di visualizzazione vengono ignorati. Se *range* è zero, non accade nulla.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





