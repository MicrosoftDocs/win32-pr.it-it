---
title: funzione glStencilFunc (GL. h)
description: La funzione glStencilFunc imposta la funzione e il valore di riferimento per il test di stencil.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- funzione glStencilFunc OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302706"
---
# <a name="glstencilfunc-function"></a>glStencilFunc (funzione)

La funzione **glStencilFunc** imposta la funzione e il valore di riferimento per il test di stencil.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*func* 
</dt> <dd>

Funzione di test. I seguenti otto token sono validi.



| Valore                                                                                                                                                   | Significato                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ mai**</dt> </dl>          | Ha sempre esito negativo.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**\_meno GL**</dt> </dl>             | Passa se (  &  *maschera* di riferimento) < (maschera di *stencil*  &  ).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passa se (*ref*  &  *mask*) = (  &  *maschera* di stencil).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**maggiore di GL \_**</dt> </dl>    | Passa se (  &  *maschera* di riferimento) > (maschera di *stencil*  &  ).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passa se (*ref*  &  *mask*) = (  &  *maschera* di stencil).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ uguale**</dt> </dl>          | Passa se (*ref*  &  *mask*) = (  &  *maschera* di stencil).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**\_NOTEQUAL GL**</dt> </dl> | Passa se (*ref*  &  *mask*)? (*stencil*  &  *mask*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ Always**</dt> </dl>       | Passa sempre.<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

Valore di riferimento per il test di stencil. Il parametro *ref* viene bloccato nell'intervallo \[ 0, 2 *n* 1 \] , dove *n* è il numero di bitplane nel buffer dello stencil.

</dd> <dt>

*maschera* 
</dt> <dd>

Maschera che è **e** ed è il valore di riferimento e il valore dello stencil archiviato al termine del test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Func* non è uno degli otto valori accettati.<br/>                                                                           |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La creazione di stencil, ad esempio il buffer *z*, Abilita e Disabilita il disegno in base ai singoli pixel. Si disegnano i piani stencil usando le primitive di disegno OpenGL, quindi si esegue il rendering di geometria e immagini, usando i piani degli stencil per mascherare parti dello schermo. Lo stencil viene in genere usato negli algoritmi di rendering multipass per ottenere effetti speciali, ad esempio decalcomanie, struttura e rendering di geometria continua costruttiva.

Il test di stencil Elimina in modo condizionale un pixel in base al risultato di un confronto tra il valore di riferimento e il valore nel buffer dello stencil. Il test è abilitato da [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con il test di stencil GL degli argomenti \_ \_ . Le azioni eseguite in base al risultato del test dello stencil vengono specificate con [**glStencilOp**](glstencilop.md).

Il parametro *Func* è una costante simbolica che determina la funzione di confronto dello stencil. Accetta uno degli otto valori indicati sopra. Il parametro *ref* è un valore di riferimento integer utilizzato nel confronto tra stencil. Viene premuto nell'intervallo \[ 0, 2 *n* 1 \] , dove *n* è il numero di bitplane nel buffer dello stencil. Il parametro *mask* è bit per bit **e** ed è il valore di riferimento e il valore dello stencil archiviato, con i valori **e che** partecipano al confronto.

Se *stencil* rappresenta il valore archiviato nella posizione del buffer dello stencil corrispondente, l'elenco precedente mostra l'effetto di ogni funzione di confronto che può essere specificata da *Func*. Solo se il confronto ha esito positivo è il pixel passato alla fase successiva nel processo di rasterizzazione (vedere [**glStencilOp**](glstencilop.md)). Tutti i test considerano i valori degli *stencil* come interi senza segno nell'intervallo \[ 0, 2 *n* 1 \] , dove *n* è il numero di bitplane nel buffer dello stencil.

Inizialmente, il test di stencil è disabilitato. Se non è presente alcun buffer dello stencil, non può verificarsi alcuna modifica dello stencil ed è come se il test di stencil venisse sempre superato.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glStencilFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argument GL \_ stencil \_ Func

**glGet** con \_ \_ maschera valore stencil GL \_ argomento

**glGet** con argomento \_ ref dello stencil GL \_

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

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





