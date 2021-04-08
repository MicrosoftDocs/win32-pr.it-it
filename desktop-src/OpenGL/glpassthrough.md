---
title: funzione glPassThrough (GL. h)
description: La funzione glPassThrough inserisce un marcatore nel buffer di feedback.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- funzione glPassThrough OpenGL
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
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741135"
---
# <a name="glpassthrough-function"></a>glPassThrough (funzione)

La funzione **glPassThrough** inserisce un marcatore nel buffer di feedback.

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

Valore del marcatore da inserire nel buffer di feedback. Viene indicato con il seguente valore di identificazione univoco.



| Valore                                                                                                                                                                                   | Significato                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**\_token pass- \_ through per GL \_**</dt> </dl> | Viene mantenuto l'ordine dei comandi **glPassThrough** rispetto alla specifica delle primitive grafiche.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Il feedback è una modalità di rendering OpenGL selezionata chiamando [**glRenderMode**](glrendermode.md) con \_ feedback GL. Quando OpenGL è in modalità di feedback, nessun pixel viene prodotto dalla rasterizzazione. Al contrario, le informazioni sulle primitive che sarebbero state rasterizzate vengono riportate all'applicazione da OpenGL. Per una descrizione del buffer di feedback e dei relativi valori, vedere [**glFeedbackBuffer**](glfeedbackbuffer.md) .

La funzione **glPassThrough** inserisce un marcatore definito dall'utente nel buffer di feedback quando viene eseguito in modalità di feedback. Il parametro *token* viene restituito come se fosse una primitiva.

La funzione **glPassThrough** viene ignorata se OpenGL non è in modalità di feedback.

La funzione seguente recupera le informazioni correlate a **glPassThrough**:

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

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





