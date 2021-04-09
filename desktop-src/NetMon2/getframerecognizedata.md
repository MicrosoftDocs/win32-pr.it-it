---
description: La funzione GetFrameRecognizeData restituisce una tabella di strutture RECOGNIZEDATA. Ognuna di queste strutture contiene un identificatore di protocollo e un offset che punta all'inizio del protocollo specificato nei dati.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Funzione GetFrameRecognizeData (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966467"
---
# <a name="getframerecognizedata-function"></a>GetFrameRecognizeData (funzione)

La funzione **GetFrameRecognizeData** restituisce una tabella di strutture **RECOGNIZEDATA** . Ognuna di queste strutture contiene un identificatore di protocollo e un offset che punta all'inizio del protocollo specificato nei dati.

## <a name="syntax"></a>Sintassi


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
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

Se la funzione ha esito positivo, il valore restituito è un puntatore a una struttura **RECOGNIZEDATATABLE** .

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameRecognizeData** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




