---
description: Restituisce una stringa che si trova in una posizione specificata all'interno di un BLOB.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: Funzione GetStringFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484324"
---
# <a name="getstringfromblob-function"></a>GetStringFromBlob (funzione)

La funzione **GetStringFromBlob** restituisce una stringa che si trova in una posizione specificata all'interno di un BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*pOwnerName* \[ in\]
</dt> <dd>

Sezione del **proprietario** del BLOB in cui si trova la stringa.

</dd> <dt>

*pCategoryName* \[ in\]
</dt> <dd>

Sezione di **categoria** BLOB in cui si trova la stringa.

</dd> <dt>

*pTagName* \[ in\]
</dt> <dd>

**Tag** della stringa richiesta.

</dd> <dt>

*ppString* \[ out\]
</dt> <dd>

Puntatore a una variabile che punta alla stringa restituita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

Se il **proprietario**, la **categoria** o i dati del **tag** specificati non esiste, la funzione restituisce la **voce del BLOB NMERR non \_ \_ \_ \_ \_ esiste**.

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

[SetStringInBlob](setstringinblob.md)
</dt> <dt>

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

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




