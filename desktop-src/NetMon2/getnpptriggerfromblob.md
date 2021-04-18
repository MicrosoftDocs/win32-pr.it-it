---
description: La funzione GetNPPTriggerFromBlob Recupera il trigger dal BLOB specificato.
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: Funzione GetNPPTriggerFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 11622078354012de4796ddd43a698ac812951742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305901"
---
# <a name="getnpptriggerfromblob-function"></a>GetNPPTriggerFromBlob (funzione)

La funzione **GetNPPTriggerFromBlob** Recupera il trigger dal blob specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*pTrigger* \[ out\]
</dt> <dd>

Puntatore al valore del trigger.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle per un BLOB di errori che specifica il punto in cui si è verificato l'errore (se presente) nel BLOB originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="remarks"></a>Commenti

Le informazioni sul trigger sono archiviate nella categoria **trigger** del BLOB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




