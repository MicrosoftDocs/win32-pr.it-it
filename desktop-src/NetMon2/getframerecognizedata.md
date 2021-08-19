---
description: La funzione GetFrameRecognizeData restituisce una tabella di strutture RECOGNIZEDATA. Ognuna di queste strutture contiene un identificatore di protocollo e un offset che punta all'inizio del protocollo specificato nei dati.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Funzione GetFrameRecognizeData (Netmon.h)
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
ms.openlocfilehash: 2b04472e0fee0238677a6592cace0d1c7fbe078635ac85b92ff8922c68da3c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366499"
---
# <a name="getframerecognizedata-function"></a>Funzione GetFrameRecognizeData

La **funzione GetFrameRecognizeData** restituisce una tabella di **strutture RECOGNIZEDATA.** Ognuna di queste strutture contiene un identificatore di protocollo e un offset che punta all'inizio del protocollo specificato nei dati.

## <a name="syntax"></a>Sintassi


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per un frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore a una **struttura RECOGNIZEDATATABLE.**

Se la funzione non ha esito positivo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare la **funzione GetFrameRecognizeData.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




