---
title: Funzione glReadBuffer (Gl.h)
description: La funzione glReadBuffer seleziona un'origine del buffer dei colori per i pixel.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- Funzione glReadBuffer OpenGL
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
ms.openlocfilehash: 3a25e9a799185b1a509510abb81617895fbbd0624d8816110e4c2ba8e4a7c1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937951"
---
# <a name="glreadbuffer-function"></a>Funzione glReadBuffer

La **funzione glReadBuffer** seleziona un'origine del buffer dei colori per i pixel.

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

Buffer dei colori. I valori accettati sono GL FRONT LEFT, GL FRONT RIGHT, GL BACK LEFT, GL BACK RIGHT, GL FRONT, GL LEFT, GL RIGHT e GL AUX i, dove i è compreso tra 0 e \_ \_ \_ \_ GL \_ \_ \_ \_ \_ \_ \_ \_ \_   \_ AUX \_ BUFFERS 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *mode* non è uno dei dodici (o più) valori accettati.<br/>                                                             |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *mode* ha specificato un buffer che non esiste.<br/>                                                                             |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glReadBuffer** specifica un buffer dei colori come origine per i comandi [**glReadPixels**](glreadpixels.md) e [**glCopyPixels**](glcopypixels.md) successivi. Il *parametro mode* accetta uno dei dodici o più valori predefiniti. (GL \_ Da AUX0 a GL \_ AUX3 sono sempre definiti. In un sistema completamente configurato, GL FRONT, GL LEFT e GL FRONT LEFT deno tutti il buffer anteriore sinistro, GL FRONT RIGHT e GL RIGHT deno il buffer anteriore destro e GL BACK LEFT e GL BACK deno il \_ \_ buffer \_ \_ \_ \_ \_ \_ \_ \_ back-left.

Le configurazioni con doppio buffer nonstereo hanno solo un buffer anteriore sinistro e un buffer back-left. Le configurazioni con buffer singolo hanno un buffer anteriore sinistro e un buffer anteriore destro se stereo e solo un buffer anteriore sinistro se nonstereo. È un errore specificare un buffer inesistente in **glReadBuffer**.

Per impostazione predefinita, *la modalità* è GL FRONT nelle configurazioni a buffer singolo e GL BACK \_ nelle \_ configurazioni a doppio buffer.

La funzione seguente recupera informazioni correlate a **glReadBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ READ \_ BUFFER

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





