---
title: funzione glStencilOp (GL. h)
description: La funzione glStencilOp imposta le azioni di test dello stencil.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- funzione glStencilOp OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302190"
---
# <a name="glstencilop-function"></a>glStencilOp (funzione)

La funzione **glStencilOp** imposta le azioni di test dello stencil.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*esito negativo* 
</dt> <dd>

Azione da intraprendere quando il test di stencil ha esito negativo. Vengono accettate le sei costanti simboliche seguenti.



| Valore                                                                                                                                                | Significato                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**\_conservazione GL**</dt> </dl>          | Mantiene il valore corrente.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**\_zero GL**</dt> </dl>          | Imposta il valore del buffer dello stencil su zero.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**\_sostituzione GL**</dt> </dl> | Imposta il valore del buffer dello stencil su *ref*, come specificato da **glStencilFunc**.<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**\_incr GL**</dt> </dl>          | Incrementa il valore del buffer dello stencil corrente. Si blocca al valore unsignable massimo rappresentabile.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**\_Decr GL**</dt> </dl>          | Decrementa il valore del buffer dello stencil corrente. Morsetti a zero.<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ invertiti**</dt> </dl>    | Bit per bit il valore del buffer dello stencil corrente viene invertito.<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

Azione dello stencil quando il test di stencil viene superato, ma il test di profondità non riesce. Accetta le stesse costanti simboliche di *Fail.*

</dd> <dt>

*zpass* 
</dt> <dd>

Azione stencil quando il test di stencil e il test di profondità superano o quando il test di stencil viene superato e non è stato abilitato alcun buffer di profondità o test di profondità. Accetta le stesse costanti simboliche di *Fail*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Fail*, *zfail* o *ZPass* è un valore qualsiasi diverso da sei valori costanti definiti.<br/>                                      |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La creazione di stencil, ad esempio il buffer *z*, Abilita e Disabilita il disegno in base ai singoli pixel. Si disegnano i piani stencil usando le primitive di disegno OpenGL, quindi si esegue il rendering di geometria e immagini, usando i piani degli stencil per mascherare parti dello schermo. Lo stencil viene in genere usato negli algoritmi di rendering multipass per ottenere effetti speciali, ad esempio decalcomanie, struttura e rendering di geometria continua costruttiva.

Il test di stencil Elimina in modo condizionale un pixel in base al risultato di un confronto tra il valore nel buffer dello stencil e un valore di riferimento. Il test è abilitato con le chiamate [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con il test di stencil GL degli argomenti \_ \_ e controllato con [**glStencilFunc**](glstencilfunc.md).

La funzione **glStencilOp** accetta tre argomenti che indicano cosa accade al valore dello stencil archiviato mentre è abilitato lo stencil. Se il test di stencil ha esito negativo, non viene apportata alcuna modifica ai buffer di colore o profondità del pixel e l'operazione ha *esito negativo* indica cosa accade al contenuto del buffer dello stencil.

I valori del buffer dello stencil vengono considerati come interi senza segno. Quando viene incrementato e decrementato, i valori vengono fissati a 0 e 2 *n* 1, dove *n* è il valore restituito dall'esecuzione di una query sui bit dello \_ stencil GL \_ .

Gli altri due argomenti per **glStencilOp** specificano le azioni del buffer dello stencil dovrebbero avere esito positivo dei test del buffer di profondità (*ZPass*) o Fail (*zfail*). Vedere [**glDepthFunc**](gldepthfunc.md). Vengono specificati con le stesse sei costanti simboliche di *non riuscite*. Si noti che *zfail* viene ignorato quando non è presente alcun buffer di profondità o quando il buffer di profondità non è abilitato. In questi casi, *Fail* e *ZPass* specificano l'azione dello stencil quando il test di stencil ha esito negativo e passa rispettivamente.

Inizialmente il test di stencil è disabilitato. Se non è presente alcun buffer dello stencil, non può verificarsi alcuna modifica dello stencil ed è come se i test di stencil fossero sempre passati, indipendentemente da qualsiasi chiamata a **glStencilOp**.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glStencilOp**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con stencil GL \_ argomento \_ non riuscito

**glGet** con passaggio di \_ \_ profondità del passaggio dello stencil di \_ argomento GL \_

**glGet** con errore di \_ \_ profondità di passaggio dello stencil GL \_ argomento \_

**glGet** con \_ bit stencil GL \_ argomento

[**glIsEnabled**](glisenabled.md) con \_ test stencil GL \_ argomento

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





