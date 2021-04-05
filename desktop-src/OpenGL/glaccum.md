---
title: funzione glAccum (GL. h)
description: La funzione glAccum opera sul buffer di accumulo.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- funzione glAccum OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741946"
---
# <a name="glaccum-function"></a>glAccum (funzione)

La funzione **glAccum** opera sul buffer di accumulo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*op* 
</dt> <dd>

Operazione del buffer di accumulo. Le costanti simboliche accettate sono le seguenti.



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**\_Accue GL**</dt> </dl>    | Ottiene R, G, B e un valore dal buffer attualmente selezionato per la lettura (vedere [**glReadBuffer**](glreadbuffer.md)). Ogni valore di componente è diviso per 2 *n*  1, dove *n* è il numero di bit allocati a ogni componente colore nel buffer attualmente selezionato. Il risultato è un valore a virgola mobile nell'intervallo compreso tra \[ 0 \] e 1, moltiplicato per *valore* e aggiunto al componente pixel corrispondente nel buffer di accumulo, aggiornando in tal modo il buffer di accumulo.<br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**\_carico GL**</dt> </dl>       | Simile a GL \_ accut, ad eccezione del fatto che il valore corrente nel buffer di accumulo non viene utilizzato nel calcolo del nuovo valore. Ovvero i valori R, G, B e quelli del buffer attualmente selezionato sono divisi per 2 *n*  1, moltiplicati per *valore* e quindi archiviati nella cella corrispondente del buffer di accumulo, sovrascrivendo il valore corrente.<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**Aggiunta di GL \_**</dt> </dl>          | Aggiunge un *valore* a ogni R, G, B e a nel buffer di accumulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**\_mult**</dt> </dl>       | Moltiplica ogni R, G, B e a nel buffer di accumulo per *valore* e restituisce il componente ridimensionato alla posizione del buffer di accumulo corrispondente.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**\_return GL**</dt> </dl> | Trasferisce i valori del buffer di accumulo al buffer dei colori o ai buffer attualmente selezionati per la scrittura. Ogni R, G, B e un componente viene moltiplicato per *valore*, quindi moltiplicato per 2 *n*  1, fissato all'intervallo \[ 0, 2 *n*  1 \] e archiviato nella cella del buffer di visualizzazione corrispondente. Le uniche operazioni di frammento applicate a questo trasferimento sono proprietà pixel, Scissor, dithering e colore writemasks.<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

Valore a virgola mobile utilizzato nell'operazione del buffer di accumulo. Il parametro *op* determina il modo in cui viene usato il *valore* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *op* non è un valore accettato.<br/>                                                                                                                                            |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | Non è stato rilevato alcun buffer di accumulo o la funzione **glAccum** è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Il buffer di accumulo è un buffer di colori a intervalli estesi. Non viene eseguito il rendering delle immagini. Al contrario, le immagini sottoposte a rendering in uno dei buffer dei colori vengono aggiunte al contenuto del buffer di accumulo dopo il rendering. È possibile creare effetti quali l'anti-aliasing (di punti, linee e poligoni), la sfocatura del movimento e la profondità del campo accumulando immagini generate con matrici di trasformazione diverse.

Ogni pixel nel buffer di accumulo è costituito da valori rosso, verde, blu e alfa. Il numero di bit per componente nel buffer di accumulo dipende dall'implementazione di. È possibile esaminare questo numero chiamando [**glGetIntegerv**](glgetintegerv.md) quattro volte, con gli argomenti GL \_ accut \_ Red \_ bits, GL \_ accut \_ Green \_ bits, GL \_ accuy \_ Blue \_ bits e GL \_ accuy \_ Alpha \_ bits, rispettivamente. Indipendentemente dal numero di bit per componente, tuttavia, l'intervallo di valori archiviati da ogni componente è \[ 1,? 1 \] . I pixel del buffer di accumulo sono mappati uno-a-uno con i pixel del framebuffer.

La funzione **glAccum** opera sul buffer di accumulo. Il primo argomento, *op*, è una costante simbolica che seleziona un'operazione del buffer di accumulo. Il secondo argomento, *value*, è un valore a virgola mobile da usare in tale operazione. Sono state specificate cinque operazioni: GL \_ accut, GL \_ Load, GL \_ Add, GL \_ mult e GL \_ return.

Tutte le operazioni del buffer di accumulo sono limitate all'area della casella a forbice corrente e vengono applicate in modo identico ai componenti rosso, verde, blu e alfa di ogni pixel. Il contenuto di un componente pixel del buffer di accumulo non è definito se l'operazione **glAccum** restituisce un valore non compreso nell'intervallo \[ 1, 1 \] .

Per cancellare il buffer di accumulo, usare la funzione [**glClearAccum**](glclearaccum.md) per specificare R, G, B e un valore per impostarlo su e rilasciare una funzione [**glClear**](glclear.md) con il buffer di accumulo abilitato.

Solo i pixel all'interno della casella Scissor corrente vengono aggiornati da qualsiasi operazione **glAccum** .

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glAccum** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento contabilità GL \_ \_ Red \_ BITS

**glGet** con argomento GL \_ accut \_ Green \_ BITS

**glGet** con argument GL \_ \_ Blue \_ BITS

**glGet** con argomento GL \_ accuy \_ Alpha \_ BITS

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





