---
title: Funzione glDepthFunc (Gl.h)
description: La funzione glDepthFunc specifica il valore usato per i confronti tra buffer di profondità e buffer.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- Funzione glDepthFunc OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229b269e8d9677e0ffdedffb3d91029a473292082409830ac26490bf34680075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617037"
---
# <a name="gldepthfunc-function"></a>Funzione glDepthFunc

La **funzione glDepthFunc** specifica il valore usato per i confronti tra buffer di profondità e buffer.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*func* 
</dt> <dd>

Specifica la funzione di confronto della profondità. Vengono accettate le costanti simboliche seguenti.



| Valore                                                                                                                                                   | Significato                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ NEVER**</dt> </dl>          | Non passa mai.<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | Passa se il valore *z* in ingresso è minore del valore *z* archiviato. Si tratta del valore predefinito.<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Passa se il valore z in ingresso è minore o uguale al valore z archiviato.<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ UGUALE**</dt> </dl>          | Passa se il valore z in ingresso è uguale al valore z archiviato.<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ MAGGIORE**</dt> </dl>    | Passa se il valore z in ingresso è maggiore del valore z archiviato.<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | Passa se il valore z in ingresso non è uguale al valore z archiviato.<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Passa se il valore z in ingresso è maggiore o uguale al valore z archiviato.<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ ALWAYS**</dt> </dl>       | Passa sempre .<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glDepthFunc** specifica la funzione usata per confrontare ogni valore *z* in pixel in ingresso con il valore *z* presente nel buffer di profondità. Il confronto viene eseguito solo se è abilitato il test di profondità. Vedere [**glEnable con**](glenable.md) l'argomento GL \_ TEST \_ DI PROFONDITÀ.

Inizialmente, il test di profondità è disabilitato.

Le funzioni seguenti recuperano informazioni correlate a **glDepthFunc**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ DEPTH \_ FUNC

[**glIsEnabled con**](glisenabled.md) argomento GL \_ DEPTH \_ TEST

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

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





