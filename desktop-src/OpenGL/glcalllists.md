---
title: funzione glCallLists (GL. h)
description: La funzione glCallLists esegue un elenco di elenchi di visualizzazione.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- funzione glCallLists OpenGL
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
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964358"
---
# <a name="glcalllists-function"></a>glCallLists (funzione)

La funzione **glCallLists** esegue un elenco di elenchi di visualizzazione.

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

Tipo di valori negli *elenchi*. Vengono accettate le seguenti costanti simboliche.



| Valore                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_byte GL**</dt> </dl>                                | Il parametro *lists* viene considerato come una matrice di byte con segno, ognuno nell'intervallo compreso tra-128 e 127.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte senza segno GL \_**</dt> </dl>    | Il parametro *lists* viene considerato come una matrice di byte senza segno, ognuno nell'intervallo compreso tra 0 e 255.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**\_short GL**</dt> </dl>                             | Il parametro *lists* viene considerato come una matrice di interi con segno a 2 byte, ognuno nell'intervallo compreso tra-32768 e 32767.<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**\_short senza segno GL \_**</dt> </dl> | Il parametro *lists* viene considerato come una matrice di interi senza segno a 2 byte, ognuno nell'intervallo compreso tra 0 e 65535.<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Il parametro *lists* viene considerato come una matrice di interi con segno a 4 byte.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ senza segno \_ int**</dt> </dl>       | Il parametro *lists* viene considerato come una matrice di interi senza segno a 4 byte.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | Il parametro *lists* viene considerato come una matrice di valori a virgola mobile a 4 byte.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ byte**</dt> </dl>                      | Il parametro *lists* viene considerato come una matrice di byte senza segno. Ogni coppia di byte specifica un singolo nome di elenco visualizzato. Il valore della coppia viene calcolato come 256 volte il valore senza segno del primo byte e il valore senza segno del secondo byte.<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL \_ 3 \_ byte**</dt> </dl>                      | Il parametro *lists* viene considerato come una matrice di byte senza segno. Ogni tripletta di byte specifica un singolo nome di elenco visualizzato. Il valore della terna viene calcolato come 65536 volte il valore senza segno del primo byte, più 256 volte il valore senza segno del secondo byte, più il valore senza segno del terzo byte.<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**GL \_ 4 \_ byte**</dt> </dl>                      | Il parametro *lists* viene considerato come una matrice di byte senza segno. Ogni quadruplo di byte specifica un solo nome di elenco visualizzato. Il valore del quadruplo viene calcolato come 16777216 volte il valore senza segno del primo byte, più 65536 volte il valore senza segno del secondo byte, più 256 volte il valore senza segno del terzo byte, più il valore senza segno del quarto byte.<br/> |



 

</dd> <dt>

*elenchi* 
</dt> <dd>

Indirizzo di una matrice di offset del nome nell'elenco di visualizzazione. Il tipo di puntatore è void perché gli offset possono essere byte, Shorts, int o float, a seconda del valore di *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **glCallLists** causa l'esecuzione di ogni elenco di visualizzazione nell'elenco di nomi passati come *elenchi* . Di conseguenza, le funzioni salvate in ogni elenco di visualizzazione vengono eseguite in ordine, come se fossero chiamate senza usare un elenco di visualizzazione. I nomi degli elenchi di visualizzazione che non sono stati definiti vengono ignorati.

La funzione **glCallLists** fornisce un mezzo efficace per l'esecuzione degli elenchi di visualizzazione. Il parametro *n* specifica il numero di elenchi con diversi formati di nome (specificati dal parametro di *tipo* ) **glCallLists** executes.

L'elenco dei nomi degli elenchi di visualizzazione non è con terminazione null. Viene invece *specificato il* numero di nomi che devono essere presi dagli *elenchi*.

La funzione [**glListBase**](gllistbase.md) rende disponibile un ulteriore livello di riferimento indiretto. La funzione **glListBase** specifica un offset senza segno aggiunto a ogni nome di elenco visualizzato specificato negli *elenchi* prima dell'esecuzione dell'elenco di visualizzazione.

La funzione **glCallLists** può essere visualizzata all'interno di un elenco di visualizzazione. Per evitare la possibilità di una ricorsione infinita risultante da elenchi di visualizzazione che si richiamano, viene applicato un limite al livello di annidamento degli elenchi di visualizzazione durante l'esecuzione dell'elenco di visualizzazione. Questo limite deve essere almeno 64 e dipende dall'implementazione di.

Lo stato OpenGL non viene salvato e ripristinato tramite una chiamata a **glCallLists**. Pertanto, le modifiche apportate allo stato OpenGL durante l'esecuzione degli elenchi di visualizzazione rimangono al termine dell'esecuzione. Usare [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md) per mantenere lo stato OpenGL tra le chiamate **glCallLists** .

È possibile eseguire gli elenchi di visualizzazione tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md), purché nell'elenco di visualizzazione siano incluse solo le funzioni consentite in questo intervallo.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glCallLists** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con elenco GL \_ argomento \_ base

**glGet** con elenco di \_ \_ \_ nidificazione elenco massimo argomenti

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

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**Pagina di**](glislist.md)
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

 

 





