---
title: funzione glNewList (GL. h)
description: Le funzioni glNewList e glEndList creano o sostituiscono un elenco di visualizzazione. | funzione glNewList (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- funzione glNewList OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321644"
---
# <a name="glnewlist-function"></a>glNewList (funzione)

Le funzioni **glNewList** e [**glEndList**](glendlist.md) creano o sostituiscono un elenco di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*list* 
</dt> <dd>

Nome dell'elenco di visualizzazione.

</dd> <dt>

*mode* 
</dt> <dd>

Modalità di compilazione. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <dt>**\_compilazione GL**</dt> </dl>                                       | I comandi sono semplicemente compilati.<br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <dt>**\_compilazione \_ ed \_ esecuzione GL**</dt> </dl> | I comandi vengono eseguiti Man mano che vengono compilati nell'elenco di visualizzazione.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *List* è zero.<br/>                                                                                                           |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Gli elenchi di visualizzazione sono gruppi di comandi OpenGL archiviati per l'esecuzione successiva. Gli elenchi di visualizzazione vengono creati con **glNewList**. Tutti i comandi successivi vengono inseriti nell'elenco di visualizzazione, nell'ordine emesso, fino a quando non viene chiamato **glEndList** .

La funzione **glNewList** ha due parametri. Il primo parametro, *List*, è un numero intero positivo che diventa il nome univoco per l'elenco di visualizzazione. I nomi possono essere creati e riservati con [**glGenLists**](glgenlists.md) e sono stati testati per l'univocità con l'indisponibilità [**.**](glislist.md) Il secondo parametro, *mode*, è una costante simbolica che può assumere uno dei due valori precedenti.

Alcuni comandi non vengono compilati nell'elenco di visualizzazione, ma vengono eseguiti immediatamente, indipendentemente dalla modalità elenco di visualizzazione. Questi comandi sono [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**Glis**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)e tutte le routine [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .

Analogamente, [**glTexImage2D**](glteximage2d.md) e [**glTexImage1D**](glteximage1d.md) vengono eseguiti immediatamente e non vengono compilati nell'elenco di visualizzazione quando il primo argomento è la trama del proxy GL \_ \_ \_ 2D o GL proxy texture \_ \_ \_ 1D, rispettivamente.

Quando viene rilevata la funzione **glEndList** , la definizione dell'elenco di visualizzazione viene completata associando l'elenco all' *elenco* dei nomi univoci (specificato nel comando **glNewList** ). Se un elenco di visualizzazione con l' *elenco dei* nomi esiste già, viene sostituito solo quando viene chiamato **glEndList** .

Le funzioni [**glCallList**](glcalllist.md) e [**glCallLists**](glcalllists.md) possono essere immesse negli elenchi di visualizzazione. I comandi nell'elenco di visualizzazione o negli elenchi eseguiti da **glCallList** o **glCallLists** non sono inclusi nell'elenco di visualizzazione creato, anche se la modalità di creazione dell'elenco è la \_ compilazione e l'esecuzione di GL \_ \_ .

La funzione seguente recupera le informazioni correlate a **glNewList**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glEndList**](glendlist.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**Pagina di**](glislist.md)
</dt> </dl>

 

 





