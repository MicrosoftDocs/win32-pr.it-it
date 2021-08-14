---
title: Funzione glFlush (Gl.h)
description: La funzione glFlush forza l'esecuzione di funzioni OpenGL nel tempo finito.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- Funzione glFlush OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece5f0aa96140b6fa16b5fbde1a857f1e14f1570ad7fc734626a27ac660a65ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360408"
---
# <a name="glflush-function"></a>Funzione glFlush

La **funzione glFlush** forza l'esecuzione di funzioni OpenGL nel tempo finito.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Diverse implementazioni di OpenGL consentono di eseguire il buffer dei comandi in diverse posizioni, inclusi i buffer di rete e l'acceleratore grafico stesso. La **funzione glFlush** svuota tutti questi buffer, causando l'esecuzione di tutti i comandi emessi non appena vengono accettati dal motore di rendering effettivo. Anche se questa esecuzione potrebbe non essere completata in un determinato periodo di tempo, viene completata in un periodo di tempo limitato.

Poiché qualsiasi programma OpenGL può essere eseguito in rete o su un acceleratore che bufferi i comandi, assicurarsi di chiamare **glFlush** in tutti i programmi che richiedono che tutti i comandi eseguiti in precedenza siano stati completati. Ad esempio, chiamare **glFlush prima** di attendere l'input dell'utente che dipende dall'immagine generata.

La **funzione glFlush** può restituire in qualsiasi momento. Non attende il completamento dell'esecuzione di tutte le funzioni OpenGL rilasciate in precedenza.

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

[**glFinish**](glfinish.md)
</dt> </dl>

 

 





