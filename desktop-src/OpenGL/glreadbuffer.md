---
title: funzione glReadBuffer (GL. h)
description: La funzione glReadBuffer seleziona un'origine del buffer dei colori per i pixel.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- funzione glReadBuffer OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302191"
---
# <a name="glreadbuffer-function"></a>glReadBuffer (funzione)

La funzione **glReadBuffer** seleziona un'origine del buffer dei colori per i pixel.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Buffer dei colori. I valori accettati sono GL \_ front \_ Left, GL \_ front \_ right, GL \_ back \_ Left, GL \_ back \_ right, GL \_ Front, GL back, GL \_ \_ Left, GL \_ right e GL \_ aux *i*, dove *i* è compreso tra 0 e GL \_ aux \_ buffers 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è uno dei dodici o più valori accettati.<br/>                                                             |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | la *modalità* specifica un buffer che non esiste.<br/>                                                                             |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glReadBuffer** specifica un buffer dei colori come origine per i comandi successivi [**glReadPixels**](glreadpixels.md) e [**glCopyPixels**](glcopypixels.md) . Il parametro *mode* accetta uno dei dodici o più valori predefiniti. (GL \_ AUX0 tramite GL \_ AUX3 sono sempre definiti. In un sistema completamente configurato, GL front \_ , GL \_ Left e GL \_ front left hanno \_ tutti il nome del buffer di inizio sinistro, GL \_ front \_ right e GL \_ right denominano il buffer anteriore destro e GL \_ back \_ Left e GL \_ tornano il nome del buffer di back-left.

Le configurazioni con doppio buffer non stereo hanno solo un buffer a sinistra e in primo piano. Le configurazioni con buffer singolo hanno un buffer anteriore sinistro e anteriore destro se stereo e solo un buffer anteriore sinistro se non stereo. Non è possibile specificare un buffer inesistente per **glReadBuffer**.

Per impostazione predefinita, la modalità è di *tipo* GL \_ front in configurazioni con buffer singolo e GL viene \_ nuovamente in configurazioni con doppio buffer.

La funzione seguente recupera le informazioni correlate a **glReadBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con buffer di \_ lettura argomento GL \_

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





