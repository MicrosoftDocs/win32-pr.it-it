---
description: Arresta Miracast sink, disattiva l'individuabilità e annulla la registrazione del callback.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Funzione WFDDisplaySinkStop (Wfdsink.h)
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
ms.openlocfilehash: a5e2da91e29535c1e2fd9553a2b6ec2bb0008e61f33cd55ebcda2746b93eb657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797931"
---
# <a name="wfddisplaysinkstop-function"></a>Funzione WFDDisplaySinkStop

Arresta Miracast sink, disattiva l'individuabilità e annulla la registrazione del callback. L'app deve chiamare questa operazione una volta all'arresto.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

## <a name="remarks"></a>Commenti

È previsto che l'app abbia sbloccato eventuali callback in corso prima di chiamare **WFDStopDisplaySink.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 10<br/>                                                                      |
| Fine del supporto server<br/>    | Windows Server 2016<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




