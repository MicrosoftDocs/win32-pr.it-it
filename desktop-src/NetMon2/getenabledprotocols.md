---
description: La funzione GetEnabledProtocols restituisce una tabella di tutti i protocolli contrassegnati come Enabled.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Funzione GetEnabledProtocols (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305912"
---
# <a name="getenabledprotocols-function"></a>GetEnabledProtocols (funzione)

La funzione **GetEnabledProtocols** restituisce una tabella di tutti i protocolli contrassegnati come Enabled.

## <a name="syntax"></a>Sintassi


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ in\]
</dt> <dd>

Handle per l'acquisizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore a una struttura [PROTOCOLTABLE](protocoltable.md) che elenca tutti i protocolli abilitati nell'acquisizione.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetEnabledProtocols** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PROTOCOLTABLE](protocoltable.md)
</dt> </dl>

 

 




