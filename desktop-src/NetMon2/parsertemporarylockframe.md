---
description: La funzione ParserTemporaryLockFrame blocca un frame quando immette un parser e sblocca il frame quando la funzione esce dal parser.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Funzione ParserTemporaryLockFrame (Netmon. h)
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
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317101"
---
# <a name="parsertemporarylockframe-function"></a>ParserTemporaryLockFrame (funzione)

La funzione **ParserTemporaryLockFrame** blocca un frame quando immette un parser e sblocca il frame quando la funzione esce dal parser.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame a cui punta il parser.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore al primo byte di dati nel frame.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

I parser non devono chiamare la funzione **LockFrame** . Se un parser acquisisce un blocco e quindi genera un errore o viene restituito senza sbloccare il frame, il parser lascia il sistema in uno stato in cui non può modificare i protocolli né tagliare o copiare frame. I parser devono usare la funzione **ParserTemporaryLockFrame** , che concede un blocco solo durante il contesto della voce della funzione nel parser. All'uscita dal parser, viene rilasciato il blocco del frame. Di conseguenza, il puntatore sarà valido solo dopo la restituzione del parser dalla chiamata alla funzione **AttachProperties** o **RecognizeFrame** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




