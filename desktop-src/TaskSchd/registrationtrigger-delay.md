---
title: RegistrationTrigger.Delay - proprietà
description: Per la creazione di script, ottiene o imposta la quantità di tempo tra la registrazione dell'attività e l'avvio dell'attività.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Proprietà Delay Utilità di pianificazione
- Proprietà Delay Utilità di pianificazione , oggetto RegistrationTrigger
- Proprietà RegistrationTrigger Utilità di pianificazione , Delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd5b2176f6274ad0e4b0f413edbe595d97c95ecef6d48b076b9ae9a5ff81c0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072631"
---
# <a name="registrationtriggerdelay-property"></a>RegistrationTrigger.Delay - proprietà

Per la creazione di script, ottiene o imposta la quantità di tempo tra la registrazione dell'attività e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="syntax"></a>Sintassi


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>Valore proprietà

Intervallo di tempo tra la registrazione del sistema e l'avvio dell'attività.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, il ritardo di avvio viene specificato usando l'elemento [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) dello schema Utilità di pianificazione di avvio.

Se un'attività con un trigger di registrazione ritardata viene registrata e il computer in cui è registrata l'attività viene arrestato o riavviato durante il ritardo, prima dell'esecuzione dell'attività, l'attività non verrà eseguita e il ritardo andrà perso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





