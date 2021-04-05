---
title: funzione glSelectBuffer (GL. h)
description: La funzione glSelectBuffer stabilisce un buffer per i valori della modalità di selezione.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- funzione glSelectBuffer OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740039"
---
# <a name="glselectbuffer-function"></a>glSelectBuffer (funzione)

La funzione **glSelectBuffer** stabilisce un buffer per i valori della modalità di selezione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*size* 
</dt> <dd>

Dimensione del *buffer*.

</dd> <dt>

*buffer* 
</dt> <dd>

Restituisce i dati di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | la *dimensione* è negativa.<br/>                                                                                                       |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata mentre la modalità di rendering era GL \_ Select.<br/>                                                              |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glSelectBuffer** ha due parametri: *buffer* è un puntatore a una matrice di interi senza segno e *size* indica la dimensione della matrice. Il parametro *buffer* restituisce i valori dallo stack dei nomi (vedere [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) quando la modalità di rendering è GL \_ Select (vedere [**glRenderMode**](glrendermode.md)). La funzione **glSelectBuffer** deve essere eseguita prima dell'abilitazione della modalità di selezione e non deve essere eseguita mentre la modalità di rendering è GL \_ Select.

La selezione viene utilizzata da un programmatore per determinare quali primitive vengono disegnate in una determinata area di una finestra. L'area è definita dalle matrici Modelview e Perspective correnti.

In modalità di selezione non viene prodotto alcun frammento di pixel dalla rasterizzazione. Al contrario, se una primitiva interseca il volume di ritaglio definito dal tronco di visualizzazione e i piani di ritaglio definiti dall'utente, questa primitiva causa un riscontro della selezione. Con i poligoni, non si verifica alcun hit se il poligono viene raccolto. Quando viene apportata una modifica allo stack dei nomi o quando viene chiamato [**glRenderMode**](glrendermode.md) , un record di hit viene copiato nel *buffer* se si verificano dei riscontri dall'ultimo evento di questo tipo (una modifica dello stack del nome o una chiamata **glRenderMode** ). Il record di hit è costituito dal numero di nomi nello stack dei nomi al momento dell'evento. seguito dai valori minimo e massimo di profondità di tutti i vertici raggiunti dall'evento precedente; seguito dal contenuto dello stack dei nomi, il nome inferiore prima.

Viene eseguito il mapping dei valori di profondità restituiti in modo che il valore di Unsigned Integer più grande corrisponda alla profondità della coordinata finestra 1,0 e zero corrisponda alla 0,0 profondità della coordinata

Un indice interno nel *buffer* viene reimpostato su zero ogni volta che viene immessa la modalità di selezione. Ogni volta che un record di hit viene copiato nel *buffer*, l'indice viene incrementato in modo che punti alla cella appena oltre la fine del blocco di namesthat è, alla cella successiva disponibile. Se il record di hit supera il numero di posizioni rimanenti nel *buffer*, la quantità di dati che è possibile adattare viene copiata e viene impostato il flag di overflow. Se lo stack dei nomi è vuoto quando viene copiato un record di hit, il record è costituito da zero seguito dai valori minimo e massimo di profondità.

La modalità di selezione è stata chiusa chiamando **glRenderMode** con un argomento diverso da GL \_ Select. Quando **glRenderMode** viene chiamato mentre la modalità di rendering è GL \_ Select, restituisce il numero di record di hit copiati nel *buffer*, reimposta il flag di overflow e il puntatore del buffer di selezione e inizializza lo stack dei nomi come vuoto. Se è stato impostato il bit di overflow quando è stato chiamato **glRenderMode** , viene restituito un numero di record di hit negativo.

Il contenuto del *buffer* non è definito fino a quando non viene chiamato [**glRenderMode**](glrendermode.md) con un argomento diverso da GL \_ Select.

Le  / primitive e le chiamate a [**glRasterPos**](glrasterpos-functions.md) di glBegin **glEnd** possono causare riscontri.

La funzione seguente recupera le informazioni correlate a **glSelectBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack nome GL \_

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

[**Remo**](glend.md)
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





