---
title: Oggetto RepetitionPattern
description: Oggetto di scripting che definisce la frequenza di esecuzione dell'attività e la durata della ripetizione del modello di ripetizione dopo l'avvio dell'attività.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- trigger Utilità di pianificazione , oggetto modello di ripetizione
- modello di ripetizione Utilità di pianificazione , oggetto
- Oggetto RepetitionPattern Utilità di pianificazione
- Oggetto RepetitionPattern Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06583aaef7f41a2752ace9c67599c1d299b72f87cb9984674994ede10d89525b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872396"
---
# <a name="repetitionpattern-object"></a>Oggetto RepetitionPattern

Oggetto di scripting che definisce la frequenza di esecuzione dell'attività e la durata della ripetizione del modello di ripetizione dopo l'avvio dell'attività.

## <a name="members"></a>Membri

**L'oggetto RepetitionPattern** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto RepetitionPattern** ha queste proprietà.



| Proprietà                                                                    | Tipo di accesso           | Descrizione                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Durata**](repetitionpattern-duration.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta la durata della ripetizione del criterio.<br/>                                                                                          |
| [**Intervallo**](repetitionpattern-interval.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta la quantità di tempo tra ogni riavvio dell'attività.<br/>                                                                       |
| [**StopAtDurationEnd**](repetitionpattern-stopatdurationend.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica se un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del criterio di ripetizione.<br/> |



 

## <a name="remarks"></a>Commenti

Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.

Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione pari a quattro minuti, l'attività verrà avviata cinque volte. Le cinque ripetizioni possono essere definite dal modello seguente.

1.  Un'attività inizia all'inizio del primo minuto.
2.  L'attività successiva inizia alla fine del primo minuto.
3.  L'attività successiva inizia alla fine del secondo minuto.
4.  L'attività successiva inizia alla fine del terzo minuto.
5.  L'attività successiva inizia alla fine del quarto minuto.

**Windows Server 2003, Windows XP e Windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione pari a un minuto e una durata di ripetizione pari a quattro minuti, l'attività verrà avviata quattro volte.

Quando si legge o si scrive codice XML per un'attività, il criterio di ripetizione viene specificato usando l'elemento [**Ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) dello schema Utilità di pianificazione schema.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questa proprietà, vedere [Daily Trigger Example (Scripting) .](daily-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione oggetti](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





