---
title: funzione glViewport (GL. h)
description: La funzione glViewport imposta il viewport.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- funzione glViewport OpenGL
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
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556678"
---
# <a name="glviewport-function"></a>glViewport (funzione)

La funzione **glViewport** imposta il viewport.

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

Larghezza del riquadro di visualizzazione. Quando un contesto OpenGL viene collegato per la prima volta a una finestra, la *larghezza* e l' *altezza* vengono impostate sulle dimensioni della finestra.

</dd> <dt>

*height* 
</dt> <dd>

Altezza del riquadro di visualizzazione. Quando un contesto OpenGL viene collegato per la prima volta a una finestra, la *larghezza* e l' *altezza* vengono impostate sulle dimensioni della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | La *larghezza* o l' *altezza* è negativa.<br/>                                                                                   |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glViewport** specifica la trasformazione affine di *x* e *y* dalle coordinate del dispositivo normalizzate alle coordinate della finestra. Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) sono coordinate del dispositivo normalizzate. Le coordinate della finestra (*x*<sub>w</sub> , *y*<sub>w</sub> ) vengono quindi calcolate come indicato di seguito:

![Equazione che mostra il calcolo delle coordinate della finestra.](images/view01.png)

La larghezza e l'altezza del viewport vengono automaticamente fissate a un intervallo che dipende dall'implementazione di. Viene eseguita una query su questo intervallo chiamando **glGet** con argomento GL \_ Max \_ viewport \_ Dim.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glViewport**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con viewport GL argomento \_

**glGet** con l'argomento \_ numero massimo di \_ finestre di visualizzazione \_ Dim

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
</dt> </dl>

 

 





