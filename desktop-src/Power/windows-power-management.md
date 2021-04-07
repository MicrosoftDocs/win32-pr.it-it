---
description: Il risparmio energia di Windows rende i computer immediatamente accessibili agli utenti al tocco di un pulsante o di una chiave.
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Risparmio energia di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abb3a040f8da8e2deb242a2aa607a9448d31c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881709"
---
# <a name="windows-power-management"></a>Risparmio energia di Windows

Il risparmio energia di Windows rende i computer immediatamente accessibili agli utenti al tocco di un pulsante o di una chiave. Garantisce inoltre che tutti gli elementi del sistema, ovvero applicazioni, dispositivi e interfaccia utente, possano sfruttare i numerosi miglioramenti apportati alla tecnologia e alle funzionalità di risparmio energia.

Il sistema operativo Windows utilizza l'hardware di gestione del risparmio energia per impostare il computer in uno *stato di sospensione* a basso consumo anziché arrestarsi completamente, in modo che il sistema possa riprendere rapidamente a funzionare. Il sistema operativo entrerà automaticamente nello stato di sospensione quando il computer è inattivo o quando l'utente preme un pulsante per indicare che la sessione di lavoro corrente è finita. Per l'utente, il sistema sembra essere disattivato. Durante lo stato di sospensione, il processore del computer non esegue il codice e non viene eseguito alcun lavoro per l'utente. Tuttavia, gli eventi nel sistema da entrambi i dispositivi hardware e l'orologio in tempo reale possono essere abilitati in modo che il sistema esca dallo stato di sospensione (ovvero "riattivazione") e torni rapidamente allo stato di lavoro.

Quando il computer è in stato di sospensione, l'hardware del computer, il sistema e le applicazioni in esecuzione nel computer devono essere in grado di rispondere immediatamente al commutire di alimentazione, agli eventi di comunicazione e ad altre azioni. Se tutte le applicazioni gestiscono correttamente le transizioni di stato di alimentazione, l'utente percepirà un sistema più elegante e integrato. Le applicazioni che non gestiscono queste transizioni possono avere esito negativo quando l'alimentazione è spenta e poi accesa a causa di una perdita di dati o di una dipendenza da un dispositivo che potrebbe essere stato rimosso.

Di seguito sono riportati i vantaggi del risparmio energia di Windows:

-   Elimina i ritardi di avvio e arresto. Quando l'utente avvia lo stato di sospensione, il computer non deve eseguire un avvio completo del sistema quando si chiude lo stato di sospensione o un arresto completo del sistema.
-   Consente l'esecuzione di attività automatiche mentre il computer è in stato di sospensione. Il Utilità di pianificazione consente all'utente di pianificare l'esecuzione delle applicazioni; gli eventi pianificati possono essere eseguiti anche quando il sistema è in stato di sospensione. Il Utilità di pianificazione utilizza i [timer in attesa](/windows/desktop/Sync/waitable-timer-objects) per garantire che il sistema sia pronto quando è pianificata l'esecuzione dell'applicazione. Per ulteriori informazioni, vedere il file della Guida incluso nel Utilità di pianificazione.
-   Abilita la gestione del risparmio energia per ogni dispositivo. I dispositivi che non sono in uso possono risparmiare energia entrando nello stato di sospensione.
-   Migliora l'efficienza energetica. L'efficienza energetica è particolarmente importante nei computer portatili. La riduzione del consumo di energia del sistema si traduce direttamente in costi energetici inferiori e durata della batteria superiore.
-   Consente agli utenti di creare combinazioni per il [risparmio di energia](power-schemes.md), impostare gli avvisi e specificare le opzioni della batteria tramite l'applicazione Opzioni risparmio energia nel pannello di controllo. Il sistema operativo coordina tutte le attività di risparmio energia, in base alle impostazioni di criteri di risparmio energia. Per ulteriori informazioni, vedere il file della Guida incluso nell'applicazione Opzioni risparmio energia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> <dt>

[Utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
