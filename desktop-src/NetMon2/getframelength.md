---
description: La funzione GetFrameLength restituisce la lunghezza del frame.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: Funzione GetFrameLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305906"
---
# <a name="getframelength-function"></a>GetFrameLength (funzione)

La funzione **GetFrameLength** restituisce la lunghezza del frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per un frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è la lunghezza del frame in byte.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameLength** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




