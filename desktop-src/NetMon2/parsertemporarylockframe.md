---
description: La funzione ParserTemporaryLockFrame blocca un frame quando entra in un parser e lo sblocca quando la funzione esce dal parser.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Funzione ParserTemporaryLockFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 47a8c02a29007084161897e34bd3ba6fbe3b5f53460aaced2acaf8e4924d67f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364387"
---
# <a name="parsertemporarylockframe-function"></a>Funzione ParserTemporaryLockFrame

La **funzione ParserTemporaryLockFrame** blocca un frame quando entra in un parser e lo sblocca quando la funzione esce dal parser.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle al frame a cui punta il parser.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore al primo byte di dati nel frame.

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

I parser non devono chiamare la **funzione LockFrame.** Se un parser accetta un blocco e quindi genera un errore o restituisce un errore senza sbloccare il frame, il parser lascia il sistema in uno stato in cui non può modificare protocolli o tagliare o copiare frame. I parser devono usare **la funzione ParserTemporaryLockFrame,** che concede un blocco solo durante il contesto della voce della funzione nel parser. All'uscita dal parser, viene rilasciato il blocco per tale frame. Di conseguenza, il puntatore sarà valido solo dopo il ritorno del parser dalla chiamata alla **funzione AttachProperties** **o RecognizeFrame.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




