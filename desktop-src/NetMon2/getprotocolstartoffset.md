---
description: Restituisce l'offset di un protocollo specificato nel frame.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Funzione GetProtocolStartOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305896"
---
# <a name="getprotocolstartoffset-function"></a>GetProtocolStartOffset (funzione)

La funzione **GetProtocolStartOffset** restituisce l'offset di un protocollo specificato nel frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* 
</dt> <dd>

Handle per il frame.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nome del protocollo, ad esempio TCP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un offset **DWORD** all'inizio del protocollo in cui viene eseguita la ricerca di un valore restituito pari a zero indica che il protocollo è il primo protocollo nel frame.

Se la funzione ha esito negativo, il protocollo non si trova nel frame, il valore restituito è-1.

## <a name="remarks"></a>Commenti

Quando viene fornito l'handle a un frame, questa funzione restituisce l'offset a un protocollo specificato nel frame. Per determinare, ad esempio, se il frame è un frame DNS, il parser DNS richiede l'indirizzo di porta del protocollo TCP. Il parser DNS chiamerà questa funzione con TCP come valore *ProtocolName* . Se il frame viene riconosciuto dal protocollo TCP, viene restituito l'offset delle **parole** dall'inizio del frame all'inizio del frame TCP. Se non è presente alcun protocollo TCP, il valore restituito è zero.

Questa funzione trova l'inizio di un protocollo in un frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




