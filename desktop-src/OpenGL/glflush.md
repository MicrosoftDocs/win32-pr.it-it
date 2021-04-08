---
title: funzione glFlush (GL. h)
description: La funzione glFlush forza l'esecuzione delle funzioni OpenGL in tempo limitato.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- funzione glFlush OpenGL
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
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743874"
---
# <a name="glflush-function"></a>glFlush (funzione)

La funzione **glFlush** forza l'esecuzione delle funzioni OpenGL in tempo limitato.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Diverse implementazioni di OpenGL sono comandi del buffer in diverse posizioni, inclusi i buffer di rete e l'acceleratore grafico stesso. La funzione **glFlush** svuota tutti questi buffer, facendo sì che tutti i comandi rilasciati vengano eseguiti con la stessa velocità con cui vengono accettati dal motore di rendering effettivo. Sebbene questa esecuzione non venga completata in un determinato periodo di tempo, viene completata in un intervallo di tempo limitato.

Poiché qualsiasi programma OpenGL può essere eseguito in una rete o in un acceleratore che memorizza i comandi nel buffer, assicurarsi di chiamare **glFlush** in tutti i programmi che richiedono che tutti i comandi rilasciati in precedenza siano stati completati. Ad esempio, chiamare **glFlush** prima di attendere l'input dell'utente che dipende dall'immagine generata.

La funzione **glFlush** può restituire in qualsiasi momento. Non attende il completamento dell'esecuzione di tutte le funzioni OpenGL rilasciate in precedenza.

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

[**glFinish**](glfinish.md)
</dt> </dl>

 

 





