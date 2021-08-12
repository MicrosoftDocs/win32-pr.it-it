---
title: Funzione glPassThrough (Gl.h)
description: La funzione glPassThrough inserisce un marcatore nel buffer di feedback.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- Funzione glPassThrough OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5edf1b0fb2dbda1ef1e0a2c4b9ab67b8e7e6305998a8f5a6de9c461e4e148bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615418"
---
# <a name="glpassthrough-function"></a>Funzione glPassThrough

La **funzione glPassThrough** inserisce un marcatore nel buffer di feedback.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*token* 
</dt> <dd>

Valore del marcatore da inserire nel buffer di feedback. Viene indicato con il valore di identificazione univoco seguente.



| Valore                                                                                                                                                                                   | Significato                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**\_TOKEN \_ PASS-THROUGH GL \_**</dt> </dl> | Viene mantenuto **l'ordine dei comandi glPassThrough** rispetto alla specifica delle primitive grafiche.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Il feedback è una modalità di rendering OpenGL selezionata chiamando [**glRenderMode**](glrendermode.md) con GL \_ FEEDBACK. Quando OpenGL è in modalità feedback, nessun pixel viene prodotto dalla rasterizzazione. Le informazioni sulle primitive che sarebbero state rasterizzate vengono invece fornite all'applicazione da OpenGL. Per una descrizione del buffer di feedback e dei valori in esso presenti, vedere [**glFeedbackBuffer.**](glfeedbackbuffer.md)

La **funzione glPassThrough** inserisce un marcatore definito dall'utente nel buffer di feedback quando viene eseguito in modalità feedback. Il *parametro* token viene restituito come se fosse una primitiva.

La **funzione glPassThrough** viene ignorata se OpenGL non è in modalità feedback.

La funzione seguente recupera le informazioni correlate a **glPassThrough**:

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

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





