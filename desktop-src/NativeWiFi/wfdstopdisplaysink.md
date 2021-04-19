---
description: Arresta la modalità di sink Miracast, disattiva l'individuabilità e Annulla la registrazione del callback.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Funzione WFDDisplaySinkStop (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309442"
---
# <a name="wfddisplaysinkstop-function"></a>WFDDisplaySinkStop (funzione)

Arresta la modalità di sink Miracast, disattiva l'individuabilità e Annulla la registrazione del callback. L'app dovrebbe chiamarla una volta all'arresto.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

## <a name="remarks"></a>Commenti

Si prevede che l'app abbia sbloccato tutti i callback in corso prima di chiamare **WFDStopDisplaySink**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 10<br/>                                                                      |
| Fine del supporto server<br/>    | Windows Server 2016<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




