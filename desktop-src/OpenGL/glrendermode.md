---
title: funzione glRenderMode (GL. h)
description: La funzione glRenderMode imposta la modalità di rasterizzazione.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- funzione glRenderMode OpenGL
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
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121450"
---
# <a name="glrendermode-function"></a>glRenderMode (funzione)

La funzione **glRenderMode** imposta la modalità di rasterizzazione.

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

Modalità di rasterizzazione. Vengono accettati i tre valori seguenti. Il valore predefinito è GL \_ Render.



| Valore                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**\_rendering GL**</dt> </dl>       | Modalità di rendering. Le primitive vengono rasterizzate e producono frammenti di pixel, che vengono scritti nel framebuffer. Si tratta della modalità normale e anche della modalità predefinita.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**\_selezione GL**</dt> </dl>       | Modalità di selezione. Non viene prodotto alcun frammento di pixel e non viene apportata alcuna modifica al contenuto del framebuffer. Al contrario, un record dei nomi delle primitive che sarebbero stati disegnati se la modalità di rendering era GL \_ Render viene restituito in un buffer Select, che deve essere creato (vedere [**glSelectBuffer**](glselectbuffer.md)) prima di immettere la modalità di selezione.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**\_feedback GL**</dt> </dl> | Modalità di feedback. Non viene prodotto alcun frammento di pixel e non viene apportata alcuna modifica al contenuto del framebuffer. Al contrario, le coordinate e gli attributi dei vertici che sarebbero stati disegnati avevano la modalità di rendering GL \_ Render sono restituiti in un buffer di feedback, che è necessario creare (vedere [**glFeedbackBuffer**](glfeedbackbuffer.md)) prima di immettere la modalità di feedback.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è uno dei tre valori accettati.<br/>                                                                                     |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata con l'argomento GL \_ Select prima che [**glSelectBuffer**](glselectbuffer.md) venisse chiamato almeno una volta.<br/>       |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata con l'argomento GL \_ feedback prima che [**glBeedbackBuffer**](glfeedbackbuffer.md) venisse chiamato almeno una volta.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>       |



## <a name="remarks"></a>Commenti

La funzione **glRenderMode** accetta un argomento, *mode*, che può assumere uno dei tre valori predefiniti precedenti.

Il valore restituito della funzione **glRenderMode** è determinato dalla modalità di rendering nel momento in cui viene chiamato **glRenderMode** , anziché in base alla *modalità*. I valori restituiti per le tre modalità di rendering sono i seguenti.



| Valore        | Significato                                                                 |
|--------------|-------------------------------------------------------------------------|
| \_rendering GL   | Zero.                                                                   |
| \_selezione GL   | Numero di record di hit Transfer trasferiti nel buffer di selezione.             |
| \_feedback GL | Numero di valori (non vertici) trasferiti al buffer di feedback. |



 

Per informazioni dettagliate sull'operazione di selezione e feedback, vedere [**glSelectBuffer**](glselectbuffer.md) e [**glFeedbackBuffer**](glfeedbackbuffer.md) .

Se viene generato un errore, **glRenderMode** restituisce zero indipendentemente dalla modalità di rendering corrente.

La funzione seguente recupera le informazioni correlate a **glRenderMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con modalità di \_ rendering GL argomento \_

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

[**Remo**](glend.md)
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

 

 





