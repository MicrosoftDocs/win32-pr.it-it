---
title: funzione glDepthFunc (GL. h)
description: La funzione glDepthFunc specifica il valore usato per i confronti del buffer di profondità.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- funzione glDepthFunc OpenGL
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
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475844"
---
# <a name="gldepthfunc-function"></a>glDepthFunc (funzione)

La funzione **glDepthFunc** specifica il valore usato per i confronti del buffer di profondità.

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

Specifica la funzione di confronto di profondità. Vengono accettate le seguenti costanti simboliche.



| Valore                                                                                                                                                   | Significato                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ mai**</dt> </dl>          | Non viene mai passato.<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**\_meno GL**</dt> </dl>             | Passa se il valore *z* in ingresso è minore del valore *z* archiviato. Si tratta del valore predefinito.<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**\_LEQUAL GL**</dt> </dl>       | Passa se il valore z in ingresso è minore o uguale al valore z archiviato.<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ uguale**</dt> </dl>          | Passa se il valore z in ingresso è uguale al valore z archiviato.<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**maggiore di GL \_**</dt> </dl>    | Passa se il valore z in ingresso è maggiore del valore z archiviato.<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**\_NOTEQUAL GL**</dt> </dl> | Passa se il valore z in entrata non è uguale al valore z archiviato.<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**\_GEQUAL GL**</dt> </dl>       | Passa se il valore z in ingresso è maggiore o uguale al valore z archiviato.<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ Always**</dt> </dl>       | Passa sempre.<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glDepthFunc** specifica la funzione utilizzata per confrontare ogni valore di pixel *z* in ingresso con il valore *z* presente nel buffer di profondità. Il confronto viene eseguito solo se è abilitato il test di profondità. (Vedere [**glEnable**](glenable.md) con l'argomento GL \_ TEST di profondità \_ .

Inizialmente, il test di profondità è disabilitato.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glDepthFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Depth \_ Func

[**glIsEnabled**](glisenabled.md) con il \_ test di profondità di argomento GL \_

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

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





