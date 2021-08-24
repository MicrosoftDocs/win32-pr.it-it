---
title: Funzione glSelectBuffer (Gl.h)
description: La funzione glSelectBuffer stabilisce un buffer per i valori della modalità di selezione.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- Funzione glSelectBuffer OpenGL
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
ms.openlocfilehash: 17c40030c34ece43f4e24ac6937c35400fed7ab7acc005e99c653b233e08b69e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519821"
---
# <a name="glselectbuffer-function"></a>Funzione glSelectBuffer

La **funzione glSelectBuffer** stabilisce un buffer per i valori della modalità di selezione.

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

*Buffer* 
</dt> <dd>

Restituisce i dati di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *size* è negativo.<br/>                                                                                                       |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata mentre la modalità di rendering era GL \_ SELECT.<br/>                                                              |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glSelectBuffer** ha due parametri: *buffer* è un puntatore a una matrice di interi senza segno e *size* indica le dimensioni della matrice. Il *parametro buffer* restituisce valori dallo stack di nomi (vedere [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) quando la modalità di rendering è GL \_ SELECT (vedere [**glRenderMode**](glrendermode.md)). La **funzione glSelectBuffer** deve essere emessa prima che sia abilitata la modalità di selezione e non deve essere emessa mentre la modalità di rendering è GL \_ SELECT.

La selezione viene usata da un programmatore per determinare quali primitive vengono disegnate in un'area di una finestra. L'area è definita dalla visualizzazione modello corrente e dalle matrici prospettica.

In modalità di selezione non vengono prodotti frammenti di pixel dalla rasterizzazione. Se invece una primitiva interseca il volume di ritaglio definito dal frustum di visualizzazione e dai piani di ritaglio definiti dall'utente, questa primitiva causa un hit della selezione. Con i poligoni, non si verifica alcun hit se il poligono viene selezionato. Quando viene apportata una modifica allo stack di nomi o quando viene chiamato [**glRenderMode,**](glrendermode.md) un record di hit viene copiato nel *buffer* se si sono verificati riscontri dall'ultimo evento di questo tipo (una modifica dello stack dei nomi o una **chiamata glRenderMode).** Il record di hit è costituito dal numero di nomi nello stack di nomi al momento dell'evento. seguito dai valori di profondità minima e massima di tutti i vertici che hanno raggiunto l'evento precedente; seguito dal contenuto dello stack del nome, il nome in basso.

Viene eseguito il mapping dei valori di profondità restituiti in modo che il valore intero senza segno più grande corrisponda alla profondità delle coordinate della finestra 1,0 e zero corrisponda alla profondità delle coordinate della finestra 0,0.

Un indice interno nel *buffer* viene reimpostato su zero ogni volta che viene attivata la modalità di selezione. Ogni volta che un record di hit viene copiato nel *buffer*, l'indice viene incrementato in modo che punti alla cella appena oltre la fine del blocco di nomi, cio' alla cella successiva disponibile. Se il record di passaggi è maggiore del numero di posizioni rimanenti nel *buffer,* viene copiata la quantità di dati che può contenere e viene impostato il flag di overflow. Se lo stack di nomi è vuoto quando viene copiato un record di hit, tale record è costituito da zero seguito dai valori di profondità minimo e massimo.

La modalità di selezione viene chiusa chiamando **glRenderMode** con un argomento diverso da GL \_ SELECT. Ogni **volta che glRenderMode** viene chiamato mentre la modalità di rendering è GL SELECT, restituisce il numero di record di hit copiati nel \_ *buffer,* reimposta il flag di overflow e il puntatore del buffer di selezione e inizializza lo stack dei nomi come vuoto. Se il bit di overflow è stato impostato quando è stato chiamato **glRenderMode,** viene restituito un numero negativo di record di hit.

Il contenuto del *buffer non* è definito finché [**glRenderMode non**](glrendermode.md) viene chiamato con un argomento diverso da GL \_ SELECT.

Le **primitive glBegin** / **glEnd** e le chiamate [**a glRasterPos**](glrasterpos-functions.md) possono comportare riscontri.

La funzione seguente recupera le informazioni correlate a **glSelectBuffer**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ NAME STACK \_ \_ DEPTH

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

[**glEnd**](glend.md)
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

 

 





