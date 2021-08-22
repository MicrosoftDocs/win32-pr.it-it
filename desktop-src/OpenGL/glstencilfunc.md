---
title: Funzione glStencilFunc (Gl.h)
description: La funzione glStencilFunc imposta la funzione e il valore di riferimento per il test degli stencil.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- Funzione glStencilFunc OpenGL
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
ms.openlocfilehash: e529bd83cff8ffb25c8853b7d896926e63982370387f7e2fb5d2ca30a394c1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491511"
---
# <a name="glstencilfunc-function"></a>Funzione glStencilFunc

La **funzione glStencilFunc** imposta la funzione e il valore di riferimento per il test degli stencil.

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

Funzione di test. Gli otto token seguenti sono validi.



| Valore                                                                                                                                                   | Significato                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ NEVER**</dt> </dl>          | Ha sempre esito negativo.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | Passa se (*ref*  &  *mask*) < (*stencil*  &  *mask*).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Passa se (*ref*  &  *mask*) = (*stencil*  &  *mask*).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ GREATER**</dt> </dl>    | Passa se (*ref*  &  *mask*) > (*stencil*  &  *mask*).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Passa se (*ref*  &  *mask*) = (*stencil*  &  *mask*).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ EQUAL**</dt> </dl>          | Passa se (*ref*  &  *mask*) = (*stencil*  &  *mask*).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | Passa se (*ref*  &  *mask*) ? (*stencil*  &  *mask*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ ALWAYS**</dt> </dl>       | Passa sempre .<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

Valore di riferimento per il test dello stencil. Il *parametro ref* è limitato all'intervallo \[ 0, 2 *n* 1, dove n è il numero di \] bitplane nel buffer degli stencil. 

</dd> <dt>

*Maschera* 
</dt> <dd>

Maschera che è **AND ed** con il valore di riferimento e il valore dello stencil archiviato al termine del test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *func* non è uno degli otto valori accettati.<br/>                                                                           |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Lo stencil, ad esempio z-buffering, abilita e disabilita il disegno per pixel.  È possibile disegnare nei piani degli stencil usando primitive di disegno OpenGL, quindi eseguire il rendering di geometria e immagini, usando i piani stencil per mascherare parti dello schermo. Gli stencil vengono in genere usati negli algoritmi di rendering multipass per ottenere effetti speciali, ad esempio decalcomanie, struttura e rendering geometrico a tinta unita.

Il test stencil elimina in modo condizionale un pixel in base al risultato di un confronto tra il valore di riferimento e il valore nel buffer degli stencil. Il test è abilitato da [**glEnable**](glenable.md) e [**glDisable con**](gldisable.md) l'argomento GL \_ STENCIL \_ TEST. Le azioni eseguite in base al risultato del test stencil vengono specificate con [**glStencilOp.**](glstencilop.md)

Il *parametro func* è una costante simbolica che determina la funzione di confronto degli stencil. Accetta uno degli otto valori illustrati in precedenza. Il *parametro ref* è un valore di riferimento integer usato nel confronto degli stencil. È limitato all'intervallo \[ 0, 2 *n* 1 , dove n è il numero di \] bitplane nel buffer degli stencil.  Il *parametro mask* è AND bit per bit con il valore di riferimento e il valore dello stencil archiviato, con i valori ed **AND** che partecipano al confronto. 

Se *stencil* rappresenta il valore archiviato nella posizione del buffer degli stencil corrispondente, l'elenco precedente mostra l'effetto di ogni funzione di confronto che può essere specificata da *func*. Solo se il confronto ha esito positivo è il pixel passato alla fase successiva del processo di rasterizzazione (vedere [**glStencilOp).**](glstencilop.md) Tutti i *test trattano* i valori degli stencil come interi senza segno nell'intervallo \[ 0, 2 *n* 1, dove n è il numero di bitplani nel \] buffer degli stencil. 

Inizialmente, il test degli stencil è disabilitato. Se non è presente alcun buffer di stencil, non è possibile apportare alcuna modifica allo stencil ed è come se il test degli stencil fosse sempre superato.

Le funzioni seguenti recuperano informazioni correlate **a glStencilFunc:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ STENCIL \_ FUNC

**glGet con** argomento GL \_ STENCIL VALUE \_ \_ MASK

**glGet** con argomento GL \_ STENCIL \_ REF

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

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





