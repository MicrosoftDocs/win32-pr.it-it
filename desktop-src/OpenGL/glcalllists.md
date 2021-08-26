---
title: Funzione glCallLists (Gl.h)
description: La funzione glCallLists esegue un elenco di elenchi di visualizzazione.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- Funzione glCallLists OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e15c382b23558786443f03f57349b2504ad251301e3e195885e276d7dbebe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082111"
---
# <a name="glcalllists-function"></a>Funzione glCallLists

La **funzione glCallLists** esegue un elenco di elenchi di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero di elenchi di visualizzazione da eseguire.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di valori negli *elenchi*. Vengono accettate le costanti simboliche seguenti.



| Valore                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Il *parametro lists* viene considerato come una matrice di byte con segno, ognuno nell'intervallo compreso tra -128 e 127.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | Il *parametro lists* viene considerato come una matrice di byte senza segno, ognuno nell'intervallo compreso tra 0 e 255.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Il *parametro lists* viene considerato come una matrice di interi con segno a 2 byte, ognuno nell'intervallo compreso tra -32768 e 32767.<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | Il *parametro lists* viene considerato come una matrice di interi senza segno a 2 byte, ognuno nell'intervallo compreso tra 0 e 65535.<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | Il *parametro lists* viene considerato come una matrice di interi con segno a 4 byte.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | Il *parametro lists* viene considerato come una matrice di interi senza segno a 4 byte.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Il *parametro lists* viene considerato come una matrice di valori a virgola mobile a 4 byte.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ BYTE**</dt> </dl>                      | Il *parametro lists* viene considerato come una matrice di byte senza segno. Ogni coppia di byte specifica un singolo nome dell'elenco di visualizzazione. Il valore della coppia viene calcolato come 256 volte il valore senza segno del primo byte più il valore senza segno del secondo byte.<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL \_ 3 \_ BYTE**</dt> </dl>                      | Il *parametro lists* viene considerato come una matrice di byte senza segno. Ogni tripletta di byte specifica un singolo nome di elenco visualizzato. Il valore della tripletta viene calcolato come 65536 volte il valore senza segno del primo byte, più 256 volte il valore senza segno del secondo byte, più il valore senza segno del terzo byte.<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**GL \_ 4 \_ BYTE**</dt> </dl>                      | Il *parametro lists* viene considerato come una matrice di byte senza segno. Ogni quadruplo di byte specifica un singolo nome di elenco visualizzato. Il valore del quadruplet viene calcolato come 16777216 volte il valore senza segno del primo byte, più 65536 volte il valore senza segno del secondo byte, più 256 volte il valore senza segno del terzo byte più il valore senza segno del quarto byte.<br/> |



 

</dd> <dt>

*Elenchi* 
</dt> <dd>

Indirizzo di una matrice di offset dei nomi nell'elenco di visualizzazione. Il tipo di puntatore è void perché gli offset possono essere byte, short, ints o float, a seconda del valore di *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione glCallLists** determina l'esecuzione di ogni elenco di visualizzazione nell'elenco dei *nomi* passati come elenchi. Di conseguenza, le funzioni salvate in ogni elenco di visualizzazione vengono eseguite in ordine, come se fossero state chiamate senza usare un elenco di visualizzazione. I nomi degli elenchi visualizzati che non sono stati definiti vengono ignorati.

La **funzione glCallLists** offre un modo efficiente per eseguire gli elenchi di visualizzazione. Il *parametro n* specifica il numero di elenchi con vari formati di nome (specificati dal parametro *di* tipo) **che glCallLists** esegue.

L'elenco dei nomi degli elenchi visualizzati non ha terminazione Null. n *specifica* invece quanti nomi devono essere prelevati dagli *elenchi*.

La [**funzione glListBase**](gllistbase.md) rende disponibile un livello aggiuntivo di riferimento indiretto. La **funzione glListBase** specifica un offset senza segno che viene aggiunto a ogni nome dell'elenco visualizzato specificato *negli* elenchi prima dell'esecuzione di tale elenco.

La **funzione glCallLists** può essere visualizzata all'interno di un elenco di visualizzazione. Per evitare la possibilità di ricorsione infinita risultante da elenchi di visualizzazione che si chiamano tra loro, viene inserito un limite al livello di annidamento degli elenchi di visualizzazione durante l'esecuzione dell'elenco di visualizzazione. Questo limite deve essere almeno 64 e dipende dall'implementazione.

Lo stato OpenGL non viene salvato e ripristinato in una chiamata a **glCallLists.** Di conseguenza, le modifiche apportate allo stato OpenGL durante l'esecuzione degli elenchi di visualizzazione rimangono al termine dell'esecuzione. Usare [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md) per mantenere lo stato OpenGL tra **le chiamate glCallLists.**

È possibile eseguire elenchi di visualizzazione tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md), purché l'elenco di visualizzazione includa solo le funzioni consentite in questo intervallo.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glCallLists:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ LIST \_ BASE

**glGet** con argomento GL \_ MAX \_ LIST \_ NESTING

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

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glListBase**](gllistbase.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





