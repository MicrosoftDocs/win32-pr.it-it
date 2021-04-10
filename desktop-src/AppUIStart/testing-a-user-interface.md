---
title: Test di un'interfaccia utente
description: In questa sezione vengono descritte in dettaglio alcune attività associate al test di un'interfaccia utente per un'applicazione Windows.
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e86282c03502642541c0ea1318b8ccaf6d16b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963373"
---
# <a name="testing-a-user-interface"></a>Test di un'interfaccia utente

In questa sezione vengono descritte in dettaglio alcune attività associate al test di un'interfaccia utente per un'applicazione Windows.

-   [Introduzione](#introduction)
-   [Test di usabilità](#usability-testing)
-   [Test di accessibilità](#accessibility-testing)

## <a name="introduction"></a>Introduzione

Per determinare completamente l'efficacia e l'usabilità complessiva di un'interfaccia utente dell'applicazione, è necessario verificarlo. Il test espone quanto è facile o difficile usare l'interfaccia utente per i destinatari più ampi possibile. Il tempo necessario per testare un'applicazione è molto utile.

Questo argomento è incentrato su tre scenari di test principali: usabilità generale, accessibilità e automazione.

## <a name="usability-testing"></a>Test di usabilità

I test di usabilità offrono la possibilità di valutare un prodotto studiando il modo in cui gli utenti reali utilizzano effettivamente il prodotto. Questa analisi garantisce che i presupposti chiave degli utenti e delle progettazioni di interfacce desiderate siano supportati (o contestati) con dati reali. Solo raccogliendo questi dati empirici è possibile scoprire in che modo l'interfaccia utente di un prodotto soddisfa le esigenze e le aspettative degli utenti.

Osservando l'interazione dell'utente con il prodotto e ascoltando il feedback degli utenti, vengono identificate funzionalità importanti che potrebbero essere difficili da trovare e usare. In base a questi risultati, le modifiche possono essere apportate all'interfaccia utente come richiesto. È quasi impossibile compilare un prodotto utile senza un certo livello di test di usabilità, perché i risultati rappresentano la base per prendere decisioni migliori sul prodotto e migliorare l'esperienza utente complessiva.

Il test di usabilità fornisce un recupero significativo solo quando è ben integrato nell'intero ciclo di vita del progetto. Un unico studio sull'usabilità può identificare i problemi, ma senza test di completamento è difficile determinare se le soluzioni hanno risolto tali problemi o ne sono state introdotte di nuove.

Gli scenari principali per i test di usabilità sono:

-   Se sei un fornitore di prodotti software, il testing degli utenti reali del tuo prodotto significa che stai valutando la progettazione. In base alla modalità di progettazione dell'applicazione, gli utenti possono completare le attività necessarie? Il testing di utenti reali che eseguono attività reali può anche evidenziare se le linee guida dell'interfaccia utente che seguono si trovano nel contesto del prodotto e quando la coerenza aiuta o impedisce la possibilità di un utente di svolgere il proprio lavoro.
-   Se si è un acquirente di prodotti software, è possibile eseguire test di usabilità per valutare un prodotto per l'acquisto. Ad esempio, l'azienda potrebbe prendere in considerazione l'acquisto di un prodotto per i dipendenti 20000. Prima che l'azienda spenda il denaro, è necessario assicurarsi che il prodotto in questione possa aiutare i dipendenti a lavorare meglio. I test di usabilità possono essere utili anche per verificare se l'applicazione proposta segue le linee guida di stile dell'interfaccia utente pubblicate (interne o esterne). È preferibile usare le linee guida dell'interfaccia utente come origine ausiliaria, anziché primaria, per prendere decisioni di acquisto.

Per altre informazioni, vedere [usabilità in pratica: test di usabilità](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing).

## <a name="accessibility-testing"></a>Test di accessibilità

Il test di accessibilità comprende due aree della progettazione dell'interfaccia utente: il supporto per gli utenti con disabilità e l'accesso a livello di codice da Framework di test automatizzati.

Verificare che un'applicazione sia accessibile agli utenti con disabilità comporta i test per:

-   Conformità: l'applicazione è conforme a diversi requisiti legali relativi all'accessibilità?
-   Efficacia: è possibile usare l'applicazione per gli utenti con disabilità?
-   Utilità: l'applicazione espone funzionalità appropriate per gli utenti con particolari esigenze?
-   Soddisfazione: in che modo l'applicazione viene percepita dagli utenti con particolari esigenze?

Il test di questi aspetti di un'applicazione può essere eseguito tramite un controllo di accessibilità, che prevede una revisione manuale dell'applicazione da parte di un esperto di accessibilità e uno studio di usabilità mirato per gli utenti disabilitati e i dispositivi di Assistive Technology.

Sebbene apparentemente non correlato, esiste una stretta correlazione tra i requisiti di accesso a livello di codice dei framework di test automatizzati e quelli dei dispositivi di Assistive Technology. Il supporto di uno ha il vantaggio aggiuntivo di abilitare l'altro. Per ulteriori informazioni sull'accessibilità e l'automazione dei test nelle applicazioni Windows, vedere [accessibilità](/windows/desktop/accessibility), [strumenti di test](/windows/desktop/WinAuto/testing-tools)e l'API di [automazione di Windows](/windows/desktop/WinAuto/windows-automation-api-portal).

 

 