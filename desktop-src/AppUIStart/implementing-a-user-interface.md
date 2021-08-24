---
title: Implementazione di un Interfaccia utente
description: Questa sezione descrive alcune delle attività associate all'implementazione di un'interfaccia utente per un Windows applizione.
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7967474781e180ab29a42fce6884cc391515eef0211107852659eace3490e712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702341"
---
# <a name="implementing-a-user-interface"></a>Implementazione di un Interfaccia utente

Questa sezione descrive alcune delle attività associate all'implementazione di un'interfaccia utente per un Windows applizione.

-   [Prototipo](#prototype)
-   [Costruire](#construct)
-   [Semplificare](#simplify)
    -   [Riduzione, riutilizzo, declutter](#reduce-reuse-declutter)
    -   [L'interfaccia utente migliore non è un'interfaccia utente](#the-best-ui-is-no-ui)
    -   [Meno interfaccia utente è un'interfaccia utente migliore](#less-ui-is-better-ui)
    -   [L'interfaccia utente coerente è un'interfaccia utente buona](#consistent-ui-is-good-ui)

## <a name="prototype"></a>Prototipo

Le interfacce utente devono essere progettate dall'elenco di scenari utente e requisiti identificati nel passaggio di analisi utente.

I prototipi possono essere semplici come gli sketch a matita o complessi come i mockup interattivi dello schermo. Mantenere tutto il lavoro precedente perché può essere utile quando si mostrano agli stakeholder le alternative che sono state considerate e spiegano perché sono state eliminate.

Provare a limitare al massimo questo passaggio a due o tre prototipi. I prototipi non devono essere esaustivi; devono solo simulare in modo efficace l'esperienza di uso dell'applicazione reale.

Illustrare i prototipi e tenere traccia dei commenti e suggerimenti degli utenti per identificare le tendenze generali di usabilità. Se possibile, eliminare i prototipi meno riusciti e incorporare il maggior feedback possibile in uno o più prototipi rimanenti. Ripetere questo processo in base al tempo e alle risorse consentite.

Sono disponibili vari strumenti di creazione di prototipi, tra cui [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) in Microsoft Expression Studio 3, l'editor di layout in Microsoft Visual Studio e persino Microsoft Paint.

## <a name="construct"></a>Costrutto

Quando si implementa l'interfaccia utente per un'applicazione, tenere presente quanto segue:

-   Struttura dei comandi

    Determinare se implementare una struttura di comandi tradizionale basata su menu e barre degli strumenti o una struttura di comandi alternativa basata Windows Ribbon Framework. Per altre informazioni, vedere [Menu,](../menurc/menus.md) [Barre degli strumenti](../controls/toolbar-control-reference.md)e Windows Ribbon [Framework.](../windowsribbon/-uiplat-windowsribbon-entry.md)

-   Windows finestre di dialogo

    In base alla progettazione dell'interfaccia utente e al lavoro di prototipazione, implementare le finestre dell'applicazione, incluse la finestra principale, le finestre figlio, le finestre di dialogo e le finestre di messaggio. Seguire le linee guida dell'esperienza utente per determinare gli stili e i controlli da usare nelle finestre e nelle finestre di dialogo. Per altre informazioni, vedere [Windows](../winmsg/windows.md), [Finestre di dialogo](../dlgbox/dialog-boxes.md)e Windows [controlli](../controls/window-controls.md).

-   Controlli personalizzati

    Creare nuovi controlli personalizzati solo se non è possibile ottenere la funzionalità desiderata da uno dei controlli Windows standard. I nuovi controlli personalizzati sono molto costosi da sviluppare e richiedono un lavoro aggiuntivo per renderli accessibili. Se l'applicazione richiede controlli personalizzati, assicurarsi che siano adeguatamente esposti alle tecnologie di assistive. Per altre informazioni, vedere [Controlli personalizzati e](../controls/user-controls-intro.md) API Windows [Automation](../winauto/windows-automation-api-portal.md).

-   Supporto per i dispositivi di input utente standard

    La maggior Windows applicazioni deve supportare l'input dell'utente tramite tastiera e mouse. La possibilità di spostarsi e accedere a tutte le funzionalità dell'applicazione solo tramite la tastiera è particolarmente importante per gli utenti con problemi di vista o con problemi di mobilità. Per altre informazioni, vedere [Input utente e](../inputdev/user-input.md) [eBook Engineering Software for Accessibility](https://www.microsoft.com/download/details.aspx?id=19262).

-   Stili di visualizzazione, animazioni ed effetti visivi

    Windows include diverse tecnologie che è possibile usare per aggiungere interesse visivo e impostare l'interfaccia utente a parte quella di altre applicazioni. Questi includono la specifica degli stili di visualizzazione dei controlli, l'aggiunta di animazioni agli elementi dell'interfaccia utente e l'implementazione di vari effetti visivi nell'interfaccia utente. Per altre informazioni, vedere [Stili di](../controls/themes-overview.md)visualizzazione , [Windows Animation Manager](../uianimation/-main-portal.md)e [Gestione finestre desktop](../dwm/dwm-overview.md).

## <a name="simplify"></a>Semplificare 

Un'esperienza utente efficace dipende dall'approccio, dalla prospettiva e dai presupposti dello sviluppatore durante il processo di progettazione. Per ottenere una conoscenza di base del modo in cui un'applicazione può essere usata dai destinatari di destinazione, è necessario avere la possibilità di pensare in modo ampio, oltre ai vincoli di ciò che soddisfa le esigenze dello sviluppatore. Investendo questo tempo, impegno e ricerca all'inizio di un progetto, alla fine si oderanno dividendi.

### <a name="reduce-reuse-declutter"></a>Riduzione, riutilizzo, declutter

Le funzionalità migliorano un prodotto solo se vengono effettivamente usate. In molti casi, la proliferazione di funzionalità può introdurre complessità con l'aggiunta di più icone, voci di menu, barre degli strumenti e finestre di dialogo che interferiscono con l'efficienza e la produttività anziché aggiungere valore.

### <a name="the-best-ui-is-no-ui"></a>L'interfaccia utente migliore non è un'interfaccia utente

L'interfaccia utente implica che l'utente deve interagire con l'applicazione per eseguire qualcosa. Nel caso ideale, non è necessaria alcuna interazione. Dal punto di vista dell'utente, funziona. Se è possibile aggiungere una funzionalità che rimuove in modo sicuro un'interazione dell'utente, migliora notevolmente l'esperienza utente.

### <a name="less-ui-is-better-ui"></a>Meno interfaccia utente è un'interfaccia utente migliore

In molti casi, non è possibile rimuovere completamente l'interazione dell'interfaccia utente dall'esperienza utente. Tuttavia, maggiore è la minore interazione dell'utente richiesta da un'applicazione.

Identificare le attività più comuni ed essenziali che gli utenti eseguiranno con l'applicazione e rendere tali funzioni più importanti nell'interfaccia utente. Relegare altre funzioni e attività a uno stato inferiore, visivamente, gerarchico o tramite impostazioni dell'applicazione facoltative e preferenze utente.

-   Sostituire anziché aggiungere

    La conservazione delle regole dell'interfaccia utente indica che si aggiunge qualcosa solo quando è possibile rimuovere qualcosa. Questa regola forza uno sviluppatore a pensare in modo critico a una nuova funzionalità considerando l'impatto della funzionalità sull'intera esperienza utente.

    Le nuove funzionalità non devono essere promosse perché sono nuove: non confondere il marketing con l'usabilità. Per consentire agli utenti di trovare nuove funzionalità nel prodotto, aggiungere una voce al menu **?** che descrive le modifiche apportate dopo l'ultima versione dell'applicazione.

-   L'utente è una risorsa limitata

    Più funzionalità vengono esposte in qualsiasi momento, più è difficile per un utente trovare le funzionalità necessarie.

-   È scortese interrompere

    Quando un'applicazione visualizza una finestra di dialogo, impone all'utente di arrestare qualsiasi operazione e prestare attenzione ad altro. Se possibile, rimuovere completamente la necessità di una finestra di dialogo evitando casi di errore e altre esperienze utente dannose. Per altre informazioni sulle linee guida per i messaggi, vedere [Messaggi](https://msdn.microsoft.com/library/dd535525.aspx).

-   Simple può essere potente

    Una semplice interfaccia utente non implica una mancanza di funzionalità. In genere, il risultato di un'interfaccia utente più semplice è una curva di apprendimento abbreviata, una maggiore efficienza e una maggiore produttività. Ciò consente a un utente di aumentare la propria competenza con l'applicazione.

### <a name="consistent-ui-is-good-ui"></a>L'interfaccia utente coerente è un'interfaccia utente buona

In genere, è consigliabile cercare coerenza in tutta l'interfaccia utente di un'applicazione. Fornendo un'interfaccia utente coerente, un utente può diventare più abile con un'applicazione in un tempo molto più breve. Sono in grado di applicare le conoscenze esistenti dell'applicazione a situazioni diverse e di usare funzionalità sconosciute con sicurezza.

In rari casi, la coerenza non offre alcun vantaggio all'utente e può persino peggiorare l'esperienza utente. Non rendere coerente l'interfaccia utente se tale coerenza comprova la possibilità di eseguire un'attività. La coerenza di per sé non garantisce l'usabilità. È un errore pensare che la coerenza nell'interfaccia possa portare a una buona progettazione.

Ad esempio, l'interfaccia utente dei videogiochi è in genere molto specifica per il tipo di gioco. Provare a progettare un'interfaccia utente generica che funzioni bene per due giochi specializzati, uno che richiede un timone e un altro che funziona meglio con un joystick e pulsanti, probabilmente non sarà efficace per entrambi i giochi. Nel migliore dei modi, è probabile che si o migliori un terreno intermedio che non sia adatto a nessuno dei due.

Avere dati validi sul modo in cui vengono usati gli elementi è la chiave per prendere questa decisione. Essere chiari sui vantaggi e i contro di ogni compromesso (velocità e affidabilità, facilità di apprendimento e competenza degli esperti, coerenza globale e ottimizzazione locale) e prendere le decisioni migliori per la funzionalità in relazione all'intero prodotto.

La progettazione sta scegliendo come non riuscire: ottimizzare per una cosa significa non riuscire in un'altra. La chiave per una buona progettazione dell'interfaccia utente è la possibilità di decidere quali caratteristiche dell'applicazione sono le più importanti e quali possono essere tagliate.

 

 