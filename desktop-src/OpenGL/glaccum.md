---
title: Funzione glAccum (Gl.h)
description: La funzione glAccum opera sul buffer di accumulo.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- Funzione glAccum OpenGL
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
ms.openlocfilehash: 0820d27bf6aff05916eb179e4dfd0b51a0746e2c6e5a6f4e5f3bdfe8f3e6d91a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082261"
---
# <a name="glaccum-function"></a>Funzione glAccum

La **funzione glAccum** opera sul buffer di accumulo.

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

Operazione di accumulo del buffer. Le costanti simboliche accettate sono le seguenti.



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**GL \_ ACCUM**</dt> </dl>    | Ottiene i valori R, G, B e A dal buffer attualmente selezionato per la lettura (vedere [**glReadBuffer**](glreadbuffer.md)). Ogni valore del componente è diviso per 2 *n*  1, dove *n* è il numero di bit allocati a ogni componente colore nel buffer attualmente selezionato. Il risultato è un valore a virgola mobile nell'intervallo 0,1, moltiplicato per valore e aggiunto al componente pixel corrispondente nel buffer di accumulo, aggiornando così il buffer di \[ \] accumulo. <br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**GL \_ LOAD**</dt> </dl>       | Simile a GL ACCUM, ad eccezione del fatto che il valore corrente nel buffer di accumulo non \_ viene usato nel calcolo del nuovo valore. Ciò significa che i valori R, G, B e A del buffer attualmente selezionato vengono divisi per 2 *n*  1, moltiplicati per il valore *e* quindi archiviati nella cella del buffer di accumulo corrispondente, sovrascrivendo il valore corrente.<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**GL \_ ADD**</dt> </dl>          | Aggiunge *valore* a ogni R, G, B e A nel buffer di accumulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**GL \_ MULT**</dt> </dl>       | Moltiplica ogni R, G, B e A  nel buffer di accumulo per valore e restituisce il componente ridimensionato alla posizione corrispondente del buffer di accumulo.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**GL \_ RETURN**</dt> </dl> | Trasferisce i valori del buffer di accumulo nel buffer dei colori o nei buffer attualmente selezionati per la scrittura. Ogni componente R, G, B e A viene moltiplicato per il valore *,* quindi moltiplicato per 2 *n*  1, fissato all'intervallo \[ 0, 2 *n*  1 e archiviato nella cella del buffer di visualizzazione \] corrispondente. Le uniche operazioni di frammento applicate a questo trasferimento sono la proprietà dei pixel, la scissor, il dithering e le maschera di scrittura dei colori.<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

Valore a virgola mobile utilizzato nell'operazione di accumulo del buffer. Il *parametro op* determina come *viene* usato il valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *op* non è un valore accettato.<br/>                                                                                                                                            |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | Non è presente alcun buffer di accumulo o è stata chiamata la funzione **glAccum** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Il buffer di accumulo è un buffer di colore a intervallo esteso. Non viene eseguito il rendering delle immagini al suo interno. Al contrario, le immagini di cui viene eseguito il rendering in uno dei buffer di colore vengono aggiunte al contenuto del buffer di accumulo dopo il rendering. È possibile creare effetti come l'anti-aliasing (di punti, linee e poligoni), la sfocatura del movimento e la profondità del campo accumulando immagini generate con matrici di trasformazione diverse.

Ogni pixel nel buffer di accumulo è costituito da valori rosso, verde, blu e alfa. Il numero di bit per componente nel buffer di accumulo dipende dall'implementazione. È possibile esaminare questo numero chiamando [**glGetIntegerv**](glgetintegerv.md) quattro volte, rispettivamente con gli argomenti GL \_ ACCUM \_ RED \_ BITS, GL \_ ACCUM \_ GREEN \_ BITS, GL \_ ACCUM BLUE BITS e GL \_ \_ \_ ACCUM ALPHA \_ \_ BITS. Indipendentemente dal numero di bit per componente, tuttavia, l'intervallo di valori archiviati da ogni componente è \[ 1,?1 \] . I pixel del buffer di accumulo vengono mappati uno a uno con pixel framebuffer.

La **funzione glAccum** opera sul buffer di accumulo. Il primo argomento, *op*, è una costante simbolica che seleziona un'operazione di buffer di accumulo. Il secondo argomento, *value*, è un valore a virgola mobile da usare in tale operazione. Vengono specificate cinque operazioni: GL \_ ACCUM, GL \_ LOAD, GL \_ ADD, GL \_ MULT e GL \_ RETURN.

Tutte le operazioni di buffer di accumulo sono limitate all'area della casella di forbice corrente e vengono applicate in modo identico ai componenti rosso, verde, blu e alfa di ogni pixel. Il contenuto di un componente pixel del buffer di accumulo non è definito se **l'operazione glAccum** comporta un valore non compreso nell'intervallo \[ 1,1. \]

Per cancellare il buffer di accumulo, usare la funzione [**glClearAccum**](glclearaccum.md) per specificare i valori R, G, B e A su cui impostarlo ed eseguire una funzione [**glClear**](glclear.md) con il buffer di accumulo abilitato.

Solo i pixel all'interno della casella di forbice corrente vengono aggiornati da qualsiasi **operazione glAccum.**

Le funzioni seguenti recuperano informazioni correlate alla **funzione glAccum:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ ACCUM \_ RED \_ BITS

**glGet** con argomento GL \_ ACCUM \_ GREEN \_ BITS

**glGet** con argomento GL \_ ACCUM \_ BLUE \_ BITS

**glGet** con argomento GL \_ ACCUM \_ ALPHA \_ BITS

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





