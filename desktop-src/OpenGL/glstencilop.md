---
title: Funzione glStencilOp (Gl.h)
description: La funzione glStencilOp imposta le azioni di test degli stencil.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- Funzione glStencilOp OpenGL
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
ms.openlocfilehash: da899207456cece58216874c7540a032326e4180e9484590e2effd619eea72f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614335"
---
# <a name="glstencilop-function"></a>Funzione glStencilOp

La **funzione glStencilOp** imposta le azioni di test degli stencil.

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

*Fallire* 
</dt> <dd>

Azione da eseguire quando il test dello stencil ha esito negativo. Vengono accettate le sei costanti simboliche seguenti.



| Valore                                                                                                                                                | Significato                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**GL \_ KEEP**</dt> </dl>          | Mantiene il valore corrente.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**GL \_ ZERO**</dt> </dl>          | Imposta il valore del buffer dello stencil su zero.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**GL \_ REPLACE**</dt> </dl> | Imposta il valore del buffer degli stencil *su ref*, come specificato da **glStencilFunc.**<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**GL \_ INCR**</dt> </dl>          | Incrementa il valore corrente del buffer degli stencil. Si stringe al valore massimo rappresentabile senza segno.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**GL \_ DECR**</dt> </dl>          | Decrementa il valore corrente del buffer degli stencil. Si stringe a zero.<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ INVERT**</dt> </dl>    | Inverte bit per bit il valore corrente del buffer degli stencil.<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

Azione stencil quando il test dello stencil viene superato, ma il test di profondità ha esito negativo. Accetta le stesse costanti simboliche di *fail.*

</dd> <dt>

*zpass* 
</dt> <dd>

Azione stencil quando il test di stencil e il test di profondità superano o quando il test stencil viene superato e non è abilitato alcun buffer di profondità o test di profondità. Accetta le stesse costanti simboliche di con *esito negativo.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *fail,* *zfail* o *zpass* è qualsiasi valore diverso da sei valori costanti definiti.<br/>                                      |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Lo stencil, ad esempio z-buffering, abilita e disabilita il disegno per pixel.  È possibile disegnare nei piani degli stencil usando primitive di disegno OpenGL, quindi eseguire il rendering di geometria e immagini, usando i piani stencil per mascherare parti dello schermo. Gli stencil vengono in genere usati negli algoritmi di rendering multipass per ottenere effetti speciali, ad esempio decalcomanie, struttura e rendering geometrico a tinta unita.

Il test stencil elimina in modo condizionale un pixel in base al risultato di un confronto tra il valore nel buffer degli stencil e un valore di riferimento. Il test è abilitato con le chiamate [**glEnable**](glenable.md) [**e glDisable**](gldisable.md) con l'argomento GL STENCIL TEST e controllato \_ con \_ [**glStencilFunc**](glstencilfunc.md).

La **funzione glStencilOp** accetta tre argomenti che indicano cosa accade al valore dello stencil archiviato mentre lo stencil è abilitato. Se il test dello stencil ha esito negativo, non viene apportata alcuna modifica al buffer di colore o profondità del pixel e *fail* specifica cosa accade al contenuto del buffer degli stencil.

I valori del buffer degli stencil vengono considerati come interi senza segno. Se incrementati e decrementati, i valori vengono 0 e 2 *n* 1, dove *n* è il valore restituito dall'esecuzione di query GL \_ STENCIL \_ BITS.

Gli altri due argomenti per **glStencilOp** specificano le azioni del buffer degli stencil se i test successivi del buffer di profondità hanno esito positivo (*zpass*) o hanno esito negativo (*zfail*). Vedere [**glDepthFunc.**](gldepthfunc.md) Vengono specificati usando le stesse sei costanti simboliche di *fail*. Si noti *che zfail* viene ignorato quando non è presente alcun buffer di profondità o quando il buffer di profondità non è abilitato. In questi casi, *fail e* *zpass specificano l'azione* stencil rispettivamente quando il test degli stencil ha esito negativo e viene superato.

Inizialmente il test stencil è disabilitato. Se non è presente alcun buffer di stencil, non può verificarsi alcuna modifica dello stencil ed è come se i test degli stencil passano sempre, indipendentemente da qualsiasi chiamata a **glStencilOp.**

Le funzioni seguenti recuperano informazioni correlate **a glStencilOp:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ STENCIL \_ FAIL

**glGet** con argomento GL \_ STENCIL PASS DEPTH \_ \_ \_ PASS

**glGet con** argomento GL \_ STENCIL PASS DEPTH \_ \_ \_ FAIL

**glGet** con argomento GL \_ STENCIL \_ BITS

[**glIsEnabled con**](glisenabled.md) argomento GL \_ STENCIL \_ TEST

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

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





