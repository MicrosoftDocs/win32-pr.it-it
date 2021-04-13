---
title: Proprietà RegistrationTrigger. Delay
description: Per gli script, ottiene o imposta la quantità di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto RegistrationTrigger
- Utilità di pianificazione oggetto RegistrationTrigger, proprietà delay
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
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518603"
---
# <a name="registrationtriggerdelay-property"></a>Proprietà RegistrationTrigger. Delay

Per gli script, ottiene o imposta la quantità di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="syntax"></a>Sintassi


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>Valore proprietà

Intervallo di tempo tra il momento in cui il sistema viene registrato e l'avvio dell'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, il ritardo di avvio viene specificato utilizzando l'elemento [**delay**](taskschedulerschema-delay-registrationtriggertype-element.md) dello schema utilità di pianificazione.

Se un'attività con un trigger di registrazione ritardata viene registrata e il computer in cui è registrata l'attività viene arrestato o riavviato durante il ritardo, prima dell'esecuzione dell'attività, l'attività non verrà eseguita e il ritardo andrà perso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





