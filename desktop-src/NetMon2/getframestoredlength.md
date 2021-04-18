---
description: La funzione GetFrameStoredLength restituisce la lunghezza del frame.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: Funzione GetFrameStoredLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315462"
---
# <a name="getframestoredlength-function"></a>GetFrameStoredLength (funzione)

La funzione **GetFrameStoredLength** restituisce la lunghezza del frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è la lunghezza del frame archiviato.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameStoredLength** .

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

[GetFrameLength](getframelength.md)
</dt> </dl>

 

 




