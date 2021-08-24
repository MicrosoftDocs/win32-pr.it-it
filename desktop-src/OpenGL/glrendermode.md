---
title: Funzione glRenderMode (Gl.h)
description: La funzione glRenderMode imposta la modalità di rasterizzazione.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- Funzione glRenderMode OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93eb3c7e2d7f4a6d261632e0f010cf0e1c7a2410a5a8364a6cf1fd65f36ada99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777931"
---
# <a name="glrendermode-function"></a>Funzione glRenderMode

La **funzione glRenderMode** imposta la modalità di rasterizzazione.

## <a name="syntax"></a>Sintassi


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Modalità di rasterizzazione. Vengono accettati i tre valori seguenti. Il valore predefinito è GL \_ RENDER.



| Valore                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**RENDERING \_ GL**</dt> </dl>       | Modalità di rendering. Le primitive vengono rasterizzate, producendo frammenti di pixel, scritti nel framebuffer. Si tratta della modalità normale e anche della modalità predefinita.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**GL \_ SELECT**</dt> </dl>       | Modalità di selezione. Non vengono prodotti frammenti di pixel e non viene apportata alcuna modifica al contenuto del buffer frame. Viene invece restituito un record dei nomi delle primitive che verrebbero disegnate se la modalità di rendering fosse GL RENDER in un buffer di selezione, che deve essere creato \_ (vedere [**glSelectBuffer**](glselectbuffer.md)) prima che venga attivata la modalità di selezione.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**COMMENTI E SUGGERIMENTI DI GL \_**</dt> </dl> | Modalità feedback. Non vengono prodotti frammenti di pixel e non viene apportata alcuna modifica al contenuto del buffer frame. Al contrario, le coordinate e gli attributi dei vertici che sarebbero stati disegnati se la modalità di rendering fosse GL RENDER vengono restituiti in un buffer di feedback, che deve essere creato \_ (vedere [**glFeedbackBuffer**](glfeedbackbuffer.md)) prima che venga attivata la modalità feedback.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *mode* non è uno dei tre valori accettati.<br/>                                                                                     |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata con l'argomento GL \_ SELECT prima della chiamata di [**glSelectBuffer**](glselectbuffer.md) almeno una volta.<br/>       |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata con l'argomento GL \_ FEEDBACK [**prima che glBeedbackBuffer**](glfeedbackbuffer.md) venga chiamato almeno una volta.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>       |



## <a name="remarks"></a>Commenti

La **funzione glRenderMode** accetta un solo argomento, *mode*, che può presupporre uno dei tre valori predefiniti precedenti.

Il valore restituito della **funzione glRenderMode** è determinato dalla modalità di rendering al momento della chiamata di **glRenderMode,** anziché dalla *modalità*. I valori restituiti per le tre modalità di rendering sono i seguenti.



| Valore        | Significato                                                                 |
|--------------|-------------------------------------------------------------------------|
| RENDERING \_ GL   | Zero.                                                                   |
| GL \_ SELECT   | Numero di record di hit trasferiti nel buffer di selezione.             |
| COMMENTI E SUGGERIMENTI DI GL \_ | Numero di valori (non vertici) trasferiti nel buffer di feedback. |



 

Per altri dettagli [**relativi all'operazione di**](glselectbuffer.md) selezione e feedback, vedere glSelectBuffer e [**glFeedbackBuffer.**](glfeedbackbuffer.md)

Se viene generato un errore, **glRenderMode** restituisce zero indipendentemente dalla modalità di rendering corrente.

La funzione seguente recupera le informazioni correlate **a glRenderMode**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ RENDER \_ MODE

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

[**glEnd**](glend.md)
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





