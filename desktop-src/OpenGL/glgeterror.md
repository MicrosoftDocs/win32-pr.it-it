---
title: Funzione glGetError (Gl.h)
description: La funzione glGetError restituisce informazioni sull'errore.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- Funzione glGetError OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212a76930e87d5a83c32a2f6707def8e2af40b89c5ede621ec0c31159d3aa0c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962401"
---
# <a name="glgeterror-function"></a>Funzione glGetError

La **funzione glGetError** restituisce informazioni sull'errore.

## <a name="syntax"></a>Sintassi


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

La **funzione glGetError** restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                           | Descrizione                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | Per un argomento enumerato viene specificato un valore inammissibile. La funzione offesa viene ignorata, senza alcun effetto collaterale diverso dall'impostazione del flag di errore.<br/>         |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | Un argomento numerico non è compreso nell'intervallo. La funzione offesa viene ignorata, senza alcun effetto collaterale diverso dall'impostazione del flag di errore.<br/>                                    |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | L'operazione specificata non è consentita nello stato corrente. La funzione offesa viene ignorata, senza alcun effetto collaterale diverso dall'impostazione del flag di errore.<br/>           |
| <dl> <dt>**GL \_ NO \_ ERROR**</dt> </dl>          | Non è stato registrato alcun errore. Il valore di questa costante simbolica è garantito come zero.<br/>                                                                         |
| <dl> <dt>**OVERFLOW DELLO STACK GL \_ \_**</dt> </dl>    | Questa funzione causerebbe un overflow dello stack. La funzione offesa viene ignorata, senza alcun effetto collaterale diverso dall'impostazione del flag di errore.<br/>                            |
| <dl> <dt>**UNDERFLOW \_ DELLO STACK \_ GL**</dt> </dl>   | Questa funzione causerebbe un underflow dello stack. La funzione offesa viene ignorata, senza alcun effetto collaterale diverso dall'impostazione del flag di errore.<br/>                           |
| <dl> <dt>**MEMORIA \_ \_ INSUFFICIENTE \_**</dt> </dl>    | La memoria disponibile non è sufficiente per eseguire la funzione. Lo stato di OpenGL non è definito, ad eccezione dello stato dei flag di errore, dopo la registrazione di questo errore.<br/> |



 

Si noti **che glGetError** restituisce GL INVALID OPERATION se viene chiamato tra una \_ chiamata a \_ [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).

## <a name="remarks"></a>Commenti

A ogni errore rilevabile vengono assegnati un codice numerico e un nome simbolico. Quando si verifica un errore, il flag di errore viene impostato sul valore del codice di errore appropriato. Non vengono registrati altri errori finché non viene chiamato **glGetError,** non viene restituito il codice di errore e il flag viene reimpostato su GL \_ NO \_ ERROR. Se una chiamata a **glGetError** restituisce GL NO ERROR, non si è verificato alcun errore rilevabile dall'ultima chiamata a glGetError o dall'inizializzazione \_ \_ di OpenGL. 

Per consentire le implementazioni distribuite, possono essere presenti diversi flag di errore. Se un singolo flag di errore ha registrato un errore, viene restituito il valore di tale flag e tale flag viene reimpostato su GL NO ERROR quando viene chiamato \_ \_ **glGetError.** Se più flag hanno registrato un errore, **glGetError** restituisce e cancella un valore di flag di errore arbitrario. Se tutti i flag di errore devono essere reimpostati, è necessario chiamare **sempre glGetError** in un ciclo finché non restituisce GL \_ NO \_ ERROR.

Inizialmente, tutti i flag di errore sono impostati su GL \_ NO \_ ERROR.

Quando viene impostato un flag di errore, i risultati di un'operazione OpenGL non sono definiti solo se si è verificata l'eccezione GL \_ OUT \_ OF \_ MEMORY. In tutti gli altri casi, la funzione che genera l'errore viene ignorata e non ha alcun effetto sul contenuto dello stato OpenGL o del framebuffer.

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
</dt> </dl>

 

 





