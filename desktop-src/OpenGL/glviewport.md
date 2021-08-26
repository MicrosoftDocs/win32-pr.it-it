---
title: Funzione glViewport (Gl.h)
description: La funzione glViewport imposta il viewport.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- Funzione glViewport OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70fc727265ce4af1db2be808ae7eee3f59246874659a815c66292bcab3d7ecfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035407"
---
# <a name="glviewport-function"></a>Funzione glViewport

La **funzione glViewport** imposta il viewport.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Angolo inferiore sinistro del rettangolo del viewport, in pixel. Il valore predefinito è (0,0).

</dd> <dt>

*y* 
</dt> <dd>

Angolo inferiore sinistro del rettangolo del viewport, in pixel. Il valore predefinito è (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Larghezza del riquadro di visualizzazione. Quando un contesto OpenGL viene collegato per  la prima volta a una *finestra,* la larghezza e l'altezza vengono impostate alle dimensioni di tale finestra.

</dd> <dt>

*height* 
</dt> <dd>

Altezza del riquadro di visualizzazione. Quando un contesto OpenGL viene collegato per  la prima volta a una *finestra,* la larghezza e l'altezza vengono impostate alle dimensioni di tale finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | La *larghezza o* *l'altezza* erano negative.<br/>                                                                                   |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glViewport** specifica la trasformazione affine di *x* e *y* dalle coordinate del dispositivo normalizzate alle coordinate della finestra. Lasciare che (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) siano coordinate del dispositivo normalizzate. Le coordinate della finestra (*x*<sub>w</sub> , *y*<sub>w</sub> ) vengono quindi calcolate come segue:

![Equazione che mostra il calcolo delle coordinate della finestra.](images/view01.png)

La larghezza e l'altezza del viewport vengono invisibile all'utente a un intervallo che dipende dall'implementazione. Questo intervallo viene sottoposto a query chiamando **glGet con** l'argomento GL \_ MAX \_ VIEWPORT \_ DIMS.

Le funzioni seguenti recuperano informazioni correlate a **glViewport**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ VIEWPORT

**glGet con** argomento GL \_ MAX \_ VIEWPORT \_ DIMS

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
</dt> </dl>

 

 





