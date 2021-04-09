---
description: La funzione GetProtocolFromName restituisce un handle per un protocollo di un nome specificato.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: Funzione GetProtocolFromName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750074"
---
# <a name="getprotocolfromname-function"></a>GetProtocolFromName (funzione)

La funzione **GetProtocolFromName** restituisce un handle per un protocollo di un nome specificato.

## <a name="syntax"></a>Sintassi


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolName* \[ in\]
</dt> <dd>

Nome del protocollo (ad esempio, IP).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle del protocollo.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetProtocolFromName** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




