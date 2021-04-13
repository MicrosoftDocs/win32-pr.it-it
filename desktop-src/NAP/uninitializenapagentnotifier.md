---
title: Funzione UninitializeNapAgentNotifier (NapUtil. h)
description: Annulla la sottoscrizione del processo chiamante dalle notifiche di modifica dello stato NapAgent e quarantena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- NAP funzione UninitializeNapAgentNotifier
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
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400486"
---
# <a name="uninitializenapagentnotifier-function"></a>UninitializeNapAgentNotifier (funzione)

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La funzione **UninitializeNapAgentNotifier** Annulla la sottoscrizione del processo chiamante dalle notifiche di modifica dello stato di napagent e dalla quarantena. Queste notifiche vengono fornite dal servizio NapAgent.

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo* \[ di in\]
</dt> <dd>

Valore [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) che specifica il tipo di notifiche del servizio da cui annullare la sottoscrizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione non è thread-safe.

Ogni processo sottoscritto per le notifiche del servizio NapAgent del *tipo* specificato deve chiamare **UninitializeNapAgentNotifier** per annullare la sottoscrizione alle notifiche. Se un processo viene sottoscritto a più di un tipo di notifica, deve chiamare **UninitializeNapAgentNotifier** una volta per ogni tipo di notifica.

Questa funzione avrà esito negativo automaticamente se il processo non era stato precedentemente chiamato [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) per il tipo di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





