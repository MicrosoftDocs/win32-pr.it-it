---
title: Funzione UninitializeNapAgentNotifier (NapUtil.h)
description: Annulla la sottoscrizione del processo chiamante dalle notifiche di modifica dello stato napAgent e dalle notifiche di modifica dello stato di quarantena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- Funzione UninitializeNapAgentNotifier NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b474ea95dcb2e3bd5c756cefa825463f3384e798492ccdcf794641a16fbfc450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065261"
---
# <a name="uninitializenapagentnotifier-function"></a>Funzione UninitializeNapAgentNotifier

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione UninitializeNapAgentNotifier** annulla la sottoscrizione del processo chiamante dalle notifiche di modifica dello stato di NapAgent e dalle notifiche di modifica dello stato di quarantena. Queste notifiche vengono fornite dal servizio NapAgent.

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* \[ Pollici\]
</dt> <dd>

Valore [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) che specifica il tipo di notifiche del servizio da cui annullare la sottoscrizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non ha valori restituiti.

## <a name="remarks"></a>Commenti

Questa funzione non è thread-safe.

Ogni processo sottoscritto per le notifiche del servizio NapAgent del tipo *specificato* deve chiamare **UninitializeNapAgentNotifier** per annullare la sottoscrizione alle notifiche. Se un processo è sottoscritto a più di un tipo di notifica, deve chiamare **UninitializeNapAgentNotifier** una volta per ogni tipo di notifica.

Questa funzione avrà esito negativo automaticamente se il processo non ha chiamato in precedenza [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) per il tipo di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





