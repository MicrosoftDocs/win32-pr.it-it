---
title: Ripetizione di un'attività
description: Utilità di pianificazione possibile eseguire un'attività un numero qualsiasi di volte dopo l'attivazione di un trigger.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- modello di ripetizione Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7039b57bdc6cc7f53125e74b8a6fda7d017106cd44c66d2535f7fdf27505a960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759357"
---
# <a name="repeating-a-task"></a>Ripetizione di un'attività

Utilità di pianificazione possibile eseguire un'attività un numero qualsiasi di volte dopo l'attivazione di un trigger. A tale scopo, il trigger definisce un modello di ripetizione che indica Utilità di pianificazione quanto tempo deve continuare a ripetere l'attività e l'intervallo di tempo tra ogni ripetizione di attività.

## <a name="repetition-pattern"></a>Modello di ripetizione

La figura seguente mostra un modello di ripetizione con una durata di 60 minuti e un intervallo di 25 minuti. Tenere presente che in questo caso, Utilità di pianificazione esegue l'attività quando il trigger viene attivato, esegue nuovamente l'attività dopo 25 minuti, quindi esegue di nuovo l'attività dopo 50 minuti a seconda dell'impostazione della proprietà [**StopAtDurationEnd di IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) per lo scripting). Se la **proprietà StopAtDurationEnd** è impostata su True, Utilità di pianificazione arresta l'ultima istanza dell'attività se è ancora in esecuzione dopo 60 minuti. Se la **proprietà StopAtDurationEnd** è impostata su False, l'ultima istanza dell'attività viene eseguita indipendentemente dalla durata.

![modello di ripetizione trigger](images/repetition-pattern.png)

Se si registra un'attività che contiene un trigger con un intervallo di ripetizione pari a un minuto e una durata di ripetizione pari a quattro minuti, l'attività verrà avviata cinque volte. Le cinque ripetizioni possono essere definite nel modello seguente:

1.  Un'attività inizia all'inizio del primo minuto.
2.  L'attività successiva inizia alla fine del primo minuto.
3.  L'attività successiva inizia alla fine del secondo minuto.
4.  L'attività successiva inizia alla fine del terzo minuto.
5.  L'attività successiva inizia alla fine del quarto minuto.

**Windows Server 2003, Windows XP e Windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione pari a un minuto e una durata di ripetizione pari a quattro minuti, l'attività verrà avviata quattro volte.

## <a name="objects-interfaces-and-xml-elements"></a>Oggetti, interfacce ed elementi XML

Per lo sviluppo di script, il modello di ripetizione viene definito usando [**l'oggetto RepetitionPattern.**](repetitionpattern.md)

Per lo sviluppo in C++, il modello di ripetizione è definito [**dall'interfaccia IRepetitionPattern.**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern)

Durante la lettura o la scrittura di codice XML per un'attività, il modello di ripetizione viene specificato [**nell'elemento Ripetizione.**](taskschedulerschema-repetition-triggerbasetype-element.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger di attività](task-triggers.md)
</dt> </dl>

 

 




