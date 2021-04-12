---
title: Implementazione di un'interfaccia utente
description: In questa sezione vengono descritte alcune delle attività associate all'implementazione di un'interfaccia utente per un'applicazione Windows.
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941458e046a85dc6e27a684d8aa3a7ea609e889
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338271"
---
# <a name="implementing-a-user-interface"></a>Implementazione di un'interfaccia utente

In questa sezione vengono descritte alcune delle attività associate all'implementazione di un'interfaccia utente per un'applicazione Windows.

-   [Prototipo](#prototype)
-   [Costruire](#construct)
-   [Semplificare](#simplify)
    -   [Ridurre, riutilizzare, declutter](#reduce-reuse-declutter)
    -   [L'interfaccia utente migliore non è interfaccia utente](#the-best-ui-is-no-ui)
    -   [Una minore interfaccia utente è migliore interfaccia utente](#less-ui-is-better-ui)
    -   [Interfaccia utente coerente è un'interfaccia utente corretta](#consistent-ui-is-good-ui)

## <a name="prototype"></a>Prototipo

Le interfacce utente (UI) devono essere progettate dall'elenco degli scenari utente e dei requisiti identificati nel passaggio analisi utente.

I prototipi possono essere semplici come gli schizzi a matita o complessi come mockup di schermate interattive. Tenere tutto il lavoro precedente, in quanto può essere utile quando si mostrano le alternative interessate e spiegano perché sono state eliminate.

Provare a limitare questo passaggio a due o tre prototipi. Non è necessario che i prototipi siano completi; è sufficiente simulare in modo efficace l'esperienza di utilizzo dell'applicazione reale.

Illustra i prototipi e tieni traccia dei commenti e suggerimenti degli utenti per identificare le tendenze generali di usabilità. Se possibile, rimuovere i prototipi meno riusciti e incorporare il maggior numero possibile di commenti e suggerimenti in uno o più dei prototipi rimanenti. Ripetere questo processo come tempo e le risorse consentono.

Sono disponibili diversi strumenti di prototipazione, tra cui [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) in Microsoft Expression Studio 3, editor di layout in Microsoft Visual Studio e anche Microsoft Paint.

## <a name="construct"></a>Costrutto

Quando si implementa l'interfaccia utente per un'applicazione, tenere presente quanto segue:

-   Struttura dei comandi

    Determinare se implementare una struttura di comandi tradizionale basata su menu e barre degli strumenti o una struttura di comando alternativa basata sul Framework della barra multifunzione di Windows. Per ulteriori informazioni, vedere i [menu](../menurc/menus.md), le [barre degli strumenti](../controls/toolbar-control-reference.md)e il [Framework della barra multifunzione di Windows](../windowsribbon/-uiplat-windowsribbon-entry.md).

-   Finestre e finestre di dialogo

    In base al lavoro di progettazione e creazione di prototipi dell'interfaccia utente, implementare le finestre delle applicazioni, incluse la finestra principale, le finestre figlio, le finestre di dialogo e le finestre di messaggio. Seguire le linee guida per l'esperienza utente per determinare gli stili e i controlli da usare nelle finestre di dialogo e. Per ulteriori informazioni, vedere [finestre](../winmsg/windows.md), finestre di [dialogo](../dlgbox/dialog-boxes.md)e [controlli Windows](../controls/window-controls.md).

-   Controlli personalizzati

    Creare nuovi controlli personalizzati solo se non è possibile ottenere la funzionalità desiderata da uno dei controlli Windows standard. I nuovi controlli personalizzati sono molto costosi da sviluppare e richiedono un lavoro aggiuntivo per renderli accessibili. Se l'applicazione richiede controlli personalizzati, assicurarsi che siano esposti adeguatamente alle tecnologie per l'accesso facilitato. Per altre informazioni, vedere [controlli personalizzati](../controls/user-controls-intro.md) e [API di automazione di Windows](../winauto/windows-automation-api-portal.md).

-   Supporto per i dispositivi di input utente standard

    La maggior parte delle applicazioni Windows deve supportare l'input dell'utente tramite la tastiera e il mouse. La possibilità di esplorare e accedere a tutte le funzionalità dell'applicazione tramite la tastiera è particolarmente importante per gli utenti con problemi di visione o con problemi di mobilità. Per ulteriori informazioni, vedere l' [input dell'utente](../inputdev/user-input.md) e il [software tecnico per l'accessibilità](https://www.microsoft.com/download/details.aspx?id=19262).

-   Stili visivi, animazioni e effetti visivi

    Windows include diverse tecnologie che è possibile utilizzare per aggiungere un interesse visivo e impostare l'interfaccia utente in modo diverso da quello di altre applicazioni. Che includono la specifica degli stili visivi dei controlli, l'aggiunta di animazioni agli elementi dell'interfaccia utente e l'implementazione di vari effetti visivi nell'interfaccia utente. Per ulteriori informazioni, vedere [stili visivi](../controls/themes-overview.md), [Gestione animazioni Windows](../uianimation/-main-portal.md)e [Gestione finestre desktop](../dwm/dwm-overview.md).

## <a name="simplify"></a>Semplificare 

Un'esperienza utente corretta dipende dall'approccio, dalla prospettiva e dalle ipotesi dello sviluppatore durante il processo di progettazione. Il raggiungimento di una conoscenza di base del modo in cui un'applicazione può essere utilizzata dai destinatari di destinazione richiede la possibilità di pensare a grandi linee, oltre ai vincoli di ciò che soddisfa le esigenze dello sviluppatore. Investendo questo tempo, sforzo e ricerca all'inizio di un progetto, i dividendi saranno pagati alla fine.

### <a name="reduce-reuse-declutter"></a>Ridurre, riutilizzare, declutter

Le funzionalità migliorano un prodotto solo se vengono effettivamente usate. In molti casi, la proliferazione delle funzionalità può comportare complessità con l'aggiunta di più icone, voci di menu, barre degli strumenti e finestre di dialogo che interferiscono con efficienza e produttività, anziché aggiungere valore.

### <a name="the-best-ui-is-no-ui"></a>L'interfaccia utente migliore non è interfaccia utente

L'interfaccia utente implica che l'utente deve interagire con l'applicazione per fare in modo che si verifichi un evento. Nel caso ideale, non è necessaria alcuna interazione. Dal punto di vista dell'utente, funziona semplicemente. Se è possibile aggiungere una funzionalità che rimuove in modo sicuro un'interazione dell'utente, migliora significativamente l'esperienza utente.

### <a name="less-ui-is-better-ui"></a>Una minore interfaccia utente è migliore interfaccia utente

In molti casi, non è possibile rimuovere completamente l'interazione dell'interfaccia utente dall'esperienza utente. Tuttavia, l'interazione dell'utente minore richiesta da un'applicazione è migliore.

Identificare le attività più comuni ed essenziali che verranno eseguite dagli utenti con l'applicazione e rendere le funzioni più importanti nell'interfaccia utente. Relegare altre funzioni e attività allo stato inferiore in modo visivo, gerarchico o tramite impostazioni facoltative dell'applicazione e preferenze dell'utente.

-   Sostituisci anziché Aggiungi

    La conservazione degli Stati delle regole dell'interfaccia utente che si aggiungono solo quando è possibile eliminare un elemento. Questa regola impone agli sviluppatori di pensare in modo critico a una nuova funzionalità, considerando l'effetto che la funzionalità ha sull'intera esperienza utente.

    Le nuove funzionalità non devono essere promosse perché sono nuove: non confondere il marketing con l'usabilità. Per consentire agli utenti di trovare nuove funzionalità nel prodotto, aggiungere un elemento al **menu?** che descrive le modifiche apportate dall'ultima versione dell'applicazione.

-   L'utente è una risorsa limitata

    Più sono le funzionalità esposte in un momento specifico, più difficile è che un utente possa trovare la funzionalità necessaria.

-   È scortese interrompere

    Quando un'applicazione visualizza una finestra di dialogo, impone all'utente di arrestare qualunque altra cosa stia facendo e di prestare attenzione a un altro elemento. Se possibile, rimuovere completamente la necessità di una finestra di dialogo evitando i casi di errore e altre esperienze utente di disturbo. Per ulteriori informazioni sulle linee guida per i messaggi, vedere [messaggi](https://msdn.microsoft.com/library/dd535525.aspx).

-   Semplice può essere potente

    Una semplice interfaccia utente non implica alcuna funzionalità. In genere, il risultato di un'interfaccia utente più semplice è una curva di apprendimento abbreviata, una maggiore efficienza e una maggiore produttività. Questo consente a un utente di migliorare le proprie competenze con l'applicazione.

### <a name="consistent-ui-is-good-ui"></a>Interfaccia utente coerente è un'interfaccia utente corretta

In genere, è consigliabile tentare la coerenza nell'intera interfaccia utente di un'applicazione. Fornire un'interfaccia utente coerente consente a un utente di acquisire maggiore dimestichezza con un'applicazione in tempi molto più brevi. Sono in grado di applicare le proprie conoscenze esistenti dell'applicazione a situazioni diverse e di usare una funzionalità non familiare con fiducia.

In rari casi, la coerenza non offre alcun vantaggio per l'utente e può anche peggiorare l'esperienza utente. Non rendere coerente l'interfaccia utente se la coerenza non è in grado di eseguire un'attività. La coerenza non garantisce l'usabilità. Si tratta di un errore a pensare che la coerenza nell'interfaccia provocherà una progettazione corretta.

Ad esempio, l'interfaccia utente del gioco video è in genere molto specifica per il tipo di gioco. Il tentativo di progettare un'interfaccia utente generica che funziona bene per due giochi specializzati, uno che richiede una rotellina di sterzata e un altro che funziona meglio con un joystick e pulsanti, probabilmente non riuscirà per entrambi i giochi. È probabile che si ottenga una posizione intermedia che non è ottimale per nessuno dei due.

La presenza di dati appropriati sulle modalità di utilizzo è la chiave per prendere questa decisione. È possibile chiarire i vantaggi e gli svantaggi di ogni compromesso (velocità e affidabilità, facilità di apprendimento rispetto alla competenza degli esperti, coerenza globale rispetto all'ottimizzazione locale) e prendere le decisioni migliori per la funzionalità in relazione all'intero prodotto.

La progettazione è la scelta della modalità di errore: l'ottimizzazione per un elemento comporta un errore in un altro. La chiave per una buona progettazione dell'interfaccia utente è la possibilità di decidere quali caratteristiche dell'applicazione sono le più importanti e quali possono essere tagliate.

 

 