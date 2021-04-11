---
description: La funzione GetClassIDFromBlob recupera un valore di identificatore di classe denominato da un BLOB.
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: Funzione GetClassIDFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128343"
---
# <a name="getclassidfromblob-function"></a>GetClassIDFromBlob (funzione)

La funzione **GetClassIDFromBlob** recupera un valore di identificatore di classe denominato da un BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per un BLOB.

</dd> <dt>

*pOwnerName* \[ in\]
</dt> <dd>

Puntatore al nome del proprietario del BLOB.

</dd> <dt>

*pCategoryName* \[ in\]
</dt> <dd>

Puntatore al nome della categoria BLOB.

</dd> <dt>

*pTagName* \[ in\]
</dt> <dd>

Puntatore al nome del tag BLOB.

</dd> <dt>

*pClsID* \[ out\]
</dt> <dd>

Puntatore all'identificatore di classe BLOB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.

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

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
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

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




