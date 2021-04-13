---
title: Ripetizione di un'attività
description: Utilità di pianificazione possibile eseguire un'attività un numero qualsiasi di volte in cui viene attivato un trigger.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- modello di ripetizione Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331228"
---
# <a name="repeating-a-task"></a>Ripetizione di un'attività

Utilità di pianificazione possibile eseguire un'attività un numero qualsiasi di volte in cui viene attivato un trigger. A tale scopo, il trigger definisce uno schema di ripetizione che indica Utilità di pianificazione per quanto tempo deve continuare a ripetere l'attività e l'intervallo di tempo tra ogni ripetizione dell'attività.

## <a name="repetition-pattern"></a>Modello di ripetizione

Nella figura seguente viene illustrato un modello di ripetizione con una durata di 60 minuti e un intervallo di 25 minuti. Tenere presente che, in questo caso, Utilità di pianificazione esegue l'attività quando viene attivato il trigger, esegue nuovamente l'attività dopo 25 minuti, quindi esegue nuovamente l'attività dopo 50 minuti a seconda dell'impostazione della [**Proprietà StopAtDurationEnd di IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) per lo scripting). Se la proprietà **StopAtDurationEnd** è impostata su True, utilità di pianificazione arresta l'ultima istanza dell'attività se è ancora in esecuzione dopo 60 minuti. Se la proprietà **StopAtDurationEnd** è impostata su false, l'ultima istanza dell'attività viene eseguita indipendentemente dalla durata.

![modello di ripetizione trigger](images/repetition-pattern.png)

Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata cinque volte. Le cinque ripetizioni possono essere definite dal modello seguente:

1.  Un'attività viene avviata all'inizio del primo minuto.
2.  L'attività successiva inizia alla fine del primo minuto.
3.  L'attività successiva inizia alla fine del secondo minuto.
4.  L'attività successiva inizia alla fine del terzo minuto.
5.  L'attività successiva inizia alla fine del quarto minuto.

**Windows Server 2003, Windows XP e windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata quattro volte.

## <a name="objects-interfaces-and-xml-elements"></a>Oggetti, interfacce ed elementi XML

Per lo sviluppo di script, il modello di ripetizione viene definito utilizzando l'oggetto [**RepetitionPattern**](repetitionpattern.md) .

Per lo sviluppo in C++, il modello di ripetizione viene definito dall'interfaccia [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .

Durante la lettura o la scrittura di codice XML per un'attività, il modello di ripetizione viene specificato nell'elemento di [**ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger attività](task-triggers.md)
</dt> </dl>

 

 




