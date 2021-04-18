---
description: La funzione GetFrameTimeStamp restituisce il timestamp di un frame specificato.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Funzione GetFrameTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312835"
---
# <a name="getframetimestamp-function"></a>GetFrameTimeStamp (funzione)

La funzione **GetFrameTimeStamp** restituisce il timestamp di un frame specificato.

## <a name="syntax"></a>Sintassi


```C++
__int64 WINAPI GetFrameTimeStamp(
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

Se la funzione ha esito positivo, il valore restituito è il timestamp del frame in microsecondi.

Se la funzione ha esito negativo, il valore restituito è meno uno (-1).

## <a name="remarks"></a>Commenti

La funzione **GetFrameTimeStamp** restituisce un timestamp che mostra il tempo trascorso tra l'inizio del processo di acquisizione e la registrazione del frame.

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameTimeStamp** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




