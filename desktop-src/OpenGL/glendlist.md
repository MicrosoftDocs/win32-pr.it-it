---
title: Funzione glEndList (Gl.h)
description: Le funzioni glNewList e glEndList creano o sostituiscono un elenco di visualizzazione. | Funzione glEndList (Gl.h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- Funzione glEndList OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad75f62b3b049f2244b6e701f69654d110c559b337c0d4bb72da75af93f954f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081521"
---
# <a name="glendlist-function"></a>Funzione glEndList

Le [**funzioni glNewList**](glnewlist.md) e **glEndList** creano o sostituiscono un elenco di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | **glEndList è** stato chiamato senza **un glNewList** precedente o se **glnewlist** è stato chiamato durante la definizione di un elenco di visualizzazione.<br/> |



## <a name="remarks"></a>Commenti

Gli elenchi di visualizzazione sono gruppi di comandi OpenGL archiviati per l'esecuzione successiva. Gli elenchi di visualizzazione vengono creati con [**glNewList**](glnewlist.md). Tutti i comandi successivi vengono inseriti nell'elenco di visualizzazione, nell'ordine emesso, fino a quando non viene chiamato **glEndList.**

La [**funzione glNewList**](glnewlist.md) ha due parametri. Il primo parametro, *list*, è un numero intero positivo che diventa il nome univoco per l'elenco di visualizzazione. I nomi possono essere creati e riservati con [**glGenLists**](glgenlists.md) e testati per l'univocità [**con glIsList**](glislist.md). Il secondo parametro, *mode*, è una costante simbolica che può presupporre uno dei due valori precedenti.

Alcuni comandi non vengono compilati nell'elenco di visualizzazione, ma vengono eseguiti immediatamente, indipendentemente dalla modalità elenco di visualizzazione. Questi comandi sono [**glColorPointer,**](glcolorpointer.md) [**glDeleteLists,**](gldeletelists.md) [**glDisableClientState,**](gldisableclientstate.md) [**glEdgeFlagPointer,**](gledgeflagpointer.md) [**glEnableClientState,**](glenableclientstate.md) [**glFeedbackBuffer,**](glfeedbackbuffer.md) [**glFinish,**](glfinish.md) [**glFlush,**](glflush.md) [**glGenLists,**](glgenlists.md) [**glIndexPointer,**](glindexpointer.md) [**glInterleavedArrays,**](glinterleavedarrays.md) [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer e**](glvertexpointer.md)tutte le routine [**glGet.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

Analogamente, [**glTexImage2D**](glteximage2d.md) e [**glTexImage1D**](glteximage1d.md) vengono eseguiti immediatamente e non compilati nell'elenco di visualizzazione quando il primo argomento è GL \_ PROXY TEXTURE 2D o GL PROXY TEXTURE \_ \_ \_ \_ \_ 1D, rispettivamente.

Quando viene rilevata la funzione **glEndList,** la definizione dell'elenco di visualizzazione viene completata associando l'elenco all'elenco di nomi univoci *(specificato* nel [**comando glNewList).**](glnewlist.md) Se esiste già un elenco di visualizzazione con *nome,* viene sostituito solo quando viene chiamato **glEndList.**

Le [**funzioni glCallList**](glcalllist.md) [**e glCallLists**](glcalllists.md) possono essere immesse negli elenchi di visualizzazione. I comandi nell'elenco di visualizzazione o negli elenchi eseguiti da **glCallList** o **glCallLists** non sono inclusi nell'elenco di visualizzazione creato, anche se la modalità di creazione dell'elenco è GL \_ COMPILE AND \_ \_ EXECUTE.

La funzione seguente recupera le informazioni correlate a [**glNewList**](glnewlist.md):

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MATRIX \_ MODE

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





