---
title: Oggetto RepetitionPattern
description: Oggetto di script che definisce la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- trigger Utilità di pianificazione, oggetto modello di ripetizione
- modello di ripetizione Utilità di pianificazione, oggetto
- Utilità di pianificazione oggetto RepetitionPattern
- Oggetto RepetitionPattern Utilità di pianificazione, descritto
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
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475976"
---
# <a name="repetitionpattern-object"></a>Oggetto RepetitionPattern

Oggetto di script che definisce la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.

## <a name="members"></a>Membri

L'oggetto **RepetitionPattern** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **RepetitionPattern** dispone di queste proprietà.



| Proprietà                                                                    | Tipo di accesso           | Descrizione                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](repetitionpattern-duration.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta il tempo di ripetizione del pattern.<br/>                                                                                          |
| [**Interval**](repetitionpattern-interval.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta la quantità di tempo che intercorre tra il riavvio dell'attività.<br/>                                                                       |
| [**StopAtDurationEnd**](repetitionpattern-stopatdurationend.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica se un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del criterio di ripetizione.<br/> |



 

## <a name="remarks"></a>Commenti

Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.

Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata cinque volte. Le cinque ripetizioni possono essere definite dal modello seguente.

1.  Un'attività viene avviata all'inizio del primo minuto.
2.  L'attività successiva inizia alla fine del primo minuto.
3.  L'attività successiva inizia alla fine del secondo minuto.
4.  L'attività successiva inizia alla fine del terzo minuto.
5.  L'attività successiva inizia alla fine del quarto minuto.

**Windows Server 2003, Windows XP e windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata quattro volte.

Durante la lettura o la scrittura di codice XML per un'attività, il modello di ripetizione viene specificato utilizzando l'elemento di [**ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) dello schema di utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questa proprietà, vedere [esempio di trigger giornalieri (scripting)](daily-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Utilità di pianificazione](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





