---
description: Windows risparmio energia rende i computer immediatamente accessibili agli utenti toccando un pulsante o un tasto.
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Windows Risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7335b521b22b762468d2b542ea3c4fdbfcacb798860d4997f4a512d8135bcf46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032721"
---
# <a name="windows-power-management"></a>Windows Risparmio energia

Windows risparmio energia rende i computer immediatamente accessibili agli utenti toccando un pulsante o un tasto. Garantisce inoltre che tutti gli elementi del sistema, ovvero applicazioni, dispositivi e interfaccia utente, possano sfruttare i notevoli miglioramenti apportati alla tecnologia e alle funzionalità di risparmio energia.

Il Windows operativo usa l'hardware per il risparmio energia per  mettere il computer in uno stato di sospensione a basso consumo invece di arrestarsi completamente, in modo che il sistema possa riprendere rapidamente a funzionare. Il sistema operativo entra automaticamente nello stato di sospensione quando il computer è inattivo o quando l'utente preme un pulsante per indicare che la sessione di lavoro corrente è stata attiva. Per l'utente, il sistema sembra essere disattivato. Mentre è in stato di sospensione, il processore del computer non esegue codice e non viene eseguita alcuna operazione per l'utente. Tuttavia, gli eventi nel sistema da entrambi i dispositivi hardware e l'orologio in tempo reale possono essere abilitati per fare in modo che il sistema eserciti lo stato di sospensione (ovvero la "riattivazione") e torni rapidamente allo stato di lavoro.

Quando il computer è in stato di sospensione, l'hardware del computer, il sistema e le applicazioni in esecuzione nel computer devono essere in grado di rispondere immediatamente all'interruttore di alimentazione, agli eventi di comunicazione e ad altre azioni. Se tutte le applicazioni gestiscono correttamente le transizioni dello stato di alimentazione, l'utente percepirà un sistema più elegante e integrato. Le applicazioni che non gestiscono queste transizioni possono avere esito negativo quando l'alimentazione viene spenta e quindi accesa, a causa della perdita di dati o di una dipendenza da un dispositivo che potrebbe essere stato rimosso.

Di seguito sono riportati i vantaggi del risparmio Windows risparmio energia:

-   Elimina i ritardi di avvio e arresto. Il computer non deve eseguire un avvio completo del sistema quando esce dallo stato di sospensione o un arresto completo del sistema quando l'utente avvia lo stato di sospensione.
-   Consente l'esecuzione di attività automatizzate mentre il computer è in stato di sospensione. Il Utilità di pianificazione consente all'utente di pianificare l'esecuzione delle applicazioni. Gli eventi pianificati possono essere eseguiti anche quando il sistema è in stato di sospensione. L Utilità di pianificazione usa [timer waitable](/windows/desktop/Sync/waitable-timer-objects) per garantire che il sistema sia pronto quando è pianificata l'esecuzione dell'applicazione. Per altre informazioni, vedere il file della Guida incluso nel Utilità di pianificazione.
-   Abilita il risparmio energia per dispositivo. I dispositivi non in uso possono risparmiare energia immettendo lo stato di sospensione.
-   Migliora l'efficienza energetica. L'efficienza energetica è particolarmente importante nei computer portatili. La riduzione del consumo di energia del sistema si traduce direttamente in costi di energia inferiori e una durata maggiore della batteria.
-   Consente agli utenti di creare [combinazioni per il](power-schemes.md)risparmio di energia, impostare avvisi e specificare le opzioni della batteria tramite l Opzioni risparmio energia appliazione in Pannello di controllo. Il sistema operativo coordina tutte le attività di risparmio energia, in base alle impostazioni dei criteri di risparmio energia. Per altre informazioni, vedere il file della Guida incluso nell'Opzioni risparmio energia predefinita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> <dt>

[Utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
