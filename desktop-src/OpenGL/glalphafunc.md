---
title: funzione glAlphaFunc (GL. h)
description: La funzione glAlphaFunc consente all'applicazione di impostare la funzione di test alfa.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- funzione glAlphaFunc OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301806"
---
# <a name="glalphafunc-function"></a>glAlphaFunc (funzione)

La funzione **glAlphaFunc** consente all'applicazione di impostare la funzione di test alfa.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*func* 
</dt> <dd>

Funzione di confronto alfa. Di seguito sono riportate le costanti simboliche accettate e i relativi significati.



| Valore                                                                                                                                                   | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ mai**</dt> </dl>          | Non viene mai passato.<br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**\_meno GL**</dt> </dl>             | Passa se il valore alfa in ingresso è minore del valore di riferimento.<br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ uguale**</dt> </dl>          | Passa se il valore alfa in ingresso è uguale al valore di riferimento.<br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passa se il valore alfa in ingresso è minore o uguale al valore di riferimento.<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**maggiore di GL \_**</dt> </dl>    | Passa se il valore alfa in ingresso è maggiore del valore di riferimento.<br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**\_NOTEQUAL GL**</dt> </dl> | Passa se il valore alfa in ingresso non è uguale al valore di riferimento.<br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passa se il valore alfa in ingresso è maggiore o uguale al valore di riferimento.<br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ Always**</dt> </dl>       | Passa sempre. Questo è il valore predefinito.<br/>                                                 |



 

</dd> <dt>

*ref* 
</dt> <dd>

Valore di riferimento a cui vengono confrontati i valori alfa in ingresso. Questo valore viene fissato nell'intervallo compreso tra 0 e 1, dove 0 rappresenta il valore alfa più basso possibile e 1 il valore massimo possibile. Il riferimento predefinito è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Func* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Il test alfa Elimina i frammenti a seconda del risultato di un confronto tra i valori alfa dei frammenti in ingresso e un valore di riferimento costante. La funzione **glAlphaFunc** specifica il riferimento e la funzione di confronto. Il confronto viene eseguito solo se è abilitato il test alfa. (Per altre informazioni su GL \_ \_Test alfa, vedere [**glEnable**](glenable.md).

I parametri *Func* e *ref* specificano le condizioni in base alle quali viene disegnato il pixel. Il valore alfa in ingresso viene confrontato con *ref* utilizzando la funzione specificata da *Func*. Se il confronto passa, il frammento in ingresso viene disegnato, condizionale nei test dello stencil e del buffer di profondità successivi. Se il confronto ha esito negativo, non viene apportata alcuna modifica al framebuffer nella posizione in cui si trova il pixel.

La funzione **glAlphaFunc** opera su tutte le Scritture in pixel, incluse quelle derivanti dalla conversione dell'analisi di punti, linee, poligoni e bitmap e dalle operazioni di copia e di copia dei pixel. La funzione **glAlphaFunc** non influisce sulle operazioni di cancellazione dello schermo.

Il test alfa viene eseguito solo in modalità RGBA.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glAlphaFunc** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Alpha \_ test \_ Func

**glGet** con argomento \_ ref di \_ test di Alpha \_

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Alpha \_ test

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





