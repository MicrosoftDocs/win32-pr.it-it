---
title: funzione glGetError (GL. h)
description: La funzione glGetError restituisce informazioni sull'errore.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- funzione glGetError OpenGL
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
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964775"
---
# <a name="glgeterror-function"></a>glGetError (funzione)

La funzione **glGetError** restituisce informazioni sull'errore.

## <a name="syntax"></a>Sintassi


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

La funzione **glGetError** restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                           | Descrizione                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | È stato specificato un valore non accettabile per un argomento enumerato. La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.<br/>         |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | Un argomento numerico non è compreso nell'intervallo. La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.<br/>                                    |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | L'operazione specificata non è consentita nello stato corrente. La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.<br/>           |
| <dl> <dt>**GL \_ nessun \_ errore**</dt> </dl>          | Non è stato registrato alcun errore. Il valore di questa costante simbolica è sicuramente zero.<br/>                                                                         |
| <dl> <dt>**\_overflow dello stack GL \_**</dt> </dl>    | Questa funzione provocherebbe un overflow dello stack. La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.<br/>                            |
| <dl> <dt>**\_underflow dello stack GL \_**</dt> </dl>   | Questa funzione provocherebbe un underflow dello stack. La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.<br/>                           |
| <dl> <dt>**\_ \_ \_ memoria INsufficiente per GL**</dt> </dl>    | Memoria insufficiente per l'esecuzione della funzione. Lo stato di OpenGL non è definito, ad eccezione dello stato dei flag di errore, dopo la registrazione di questo errore.<br/> |



 

Si noti che **glGetError** restituisce l' \_ operazione GL non valida \_ se viene chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).

## <a name="remarks"></a>Commenti

A ogni errore rilevabile viene assegnato un codice numerico e un nome simbolico. Quando si verifica un errore, il flag di errore viene impostato sul valore del codice di errore appropriato. Non vengono registrati altri errori fino a quando non viene chiamato **glGetError** , viene restituito il codice di errore e il flag viene reimpostato su GL \_ senza \_ errori. Se una chiamata a **glGetError** restituisce GL \_ No \_ Error, non sono stati rilevati errori dall'ultima chiamata a **glGetError** o dall'inizializzazione di OpenGL.

Per consentire le implementazioni distribuite, è possibile che siano presenti diversi flag di errore. Se un singolo flag di errore ha registrato un errore, viene restituito il valore di tale flag e tale flag viene reimpostato su GL \_ senza \_ errori quando viene chiamato **glGetError** . Se più di un flag ha registrato un errore, **glGetError** restituisce e cancella un valore di flag di errore arbitrario. Se tutti i flag di errore devono essere reimpostati, è sempre necessario chiamare **glGetError** in un ciclo fino a quando non viene restituito GL \_ nessun \_ errore.

Inizialmente, tutti i flag di errore sono impostati su GL \_ nessun \_ errore.

Quando viene impostato un flag di errore, i risultati di un'operazione OpenGL sono indefiniti solo se si \_ \_ \_ è verificata una memoria insufficiente. In tutti gli altri casi, la funzione che genera l'errore viene ignorata e non ha alcun effetto sullo stato OpenGL o sul contenuto del framebuffer.

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
</dt> </dl>

 

 





