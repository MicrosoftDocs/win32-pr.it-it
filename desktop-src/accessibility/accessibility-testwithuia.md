---
description: Panoramica di come usare Automazione interfaccia utente e altri strumenti per testare le app.
title: Test per l'accessibilità
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0cc1d118c84e2689b6cf329da29bb518a566fb8588c311229be17fcd28825ddc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896581"
---
# <a name="testing-for-accessibility"></a>Test per l'accessibilità

L'accesso a livello di codice e l'accesso tramite tastiera sono requisiti critici per il supporto dell'accessibilità nell'applicazione. Testare l'accessibilità delle applicazioni Windows, degli strumenti di assistive technology (AT) e dei framework dell'interfaccia utente è fondamentale per garantire un'esperienza utente ottimale per gli utenti con varie disabilità e limitazioni (inclusi visione, apprendimento, complessità/mobilità e disabilità di linguaggio/comunicazione) o per coloro che preferiscono semplicemente usare una tastiera.

Senza un accesso adeguato tramite AT, ad esempio utilità per la lettura dello schermo e tastiere su schermo, gli utenti con visione, apprendimento, mobilità e disabilità di linguaggio/comunicazione o limitazioni (e gli utenti che preferiscono semplicemente usare la tastiera) non sarebbero in grado di usare l'applicazione.

In questa sezione vengono descritti i vari strumenti che è possibile usare per testare l'implementazione dell'accessibilità delle applicazioni Windows e Web.

> [!NOTE]
> È anche importante eseguire test manuali per verificare l'accesso tramite tastiera all'applicazione.

## <a name="tools"></a>Strumenti

[Accessibilità Insights: consente](https://accessibilityinsights.io/) agli sviluppatori di individuare e risolvere i problemi di accessibilità sia nei siti Web che Windows applicazioni.

- [Accessibility Insights for Web](https://accessibilityinsights.io/docs/web/overview) è un'estensione per Chrome e [Microsoft Edge Insider](https://www.microsoftedgeinsider.com) che consente agli sviluppatori di individuare e risolvere i problemi di accessibilità in siti e app Web. Supporta due scenari principali:
  - **FastPass:** processo leggero in due passaggi che consente agli sviluppatori di identificare i problemi comuni di accessibilità ad alto impatto in meno di cinque minuti.  
  - **Valutazione:** consente a chiunque di verificare che un sito Web sia 100% conforme agli standard e alle linee guida di accessibilità. [Il Insights](https://accessibilityinsights.io/) accessibilità consente anche di esaminare Automazione interfaccia utente elementi, proprietà, pattern di controllo ed eventi (in modo simile agli strumenti legacy [Inspect](/windows/desktop/winauto/inspect-objects) e [AccEvent](/windows/desktop/winauto/accessible-event-watcher) descritti nella sezione seguente).

- [I Insights per Windows](https://accessibilityinsights.io/docs/windows/overview) consentono agli sviluppatori di individuare e risolvere i problemi di accessibilità nelle Windows app. Lo strumento supporta tre scenari principali:
  - **Live Inspect consente** agli sviluppatori di verificare che un elemento in un'app abbia le proprietà Automazione interfaccia utente semplicemente passando il puntatore sull'elemento o impostando lo stato attivo della tastiera su di esso.
  - **FastPass:** processo leggero in due passaggi che consente agli sviluppatori di identificare i problemi comuni di accessibilità ad alto impatto in meno di cinque minuti.
  - **La risoluzione** dei problemi consente di diagnosticare e risolvere problemi di accessibilità specifici.

### <a name="legacy-testing-tools"></a>Strumenti di test legacy

Gli strumenti seguenti sono ancora disponibili in Windows SDK e sono documentati qui per il supporto continuo, ma è consigliabile passare a [Accessibilità Insights](https://accessibilityinsights.io/).

- [Inspect](/windows/desktop/winauto/inspect-objects): consente di visualizzare i dati di accessibilità di qualsiasi elemento dell'interfaccia utente. È particolarmente utile per garantire che le proprietà e i pattern di controllo vengano impostati correttamente durante l'estensione di un controllo comune o la creazione di un controllo personalizzato.
- [Accessible Event Watcher (AccEvent):](/windows/desktop/winauto/accessible-event-watcher)esamina i dati di accessibilità per convalidare gli elementi dell'interfaccia utente dell'applicazione e assicurarsi che gli elementi dell'interfaccia utente Microsoft Active Accessibility e Automazione interfaccia utente eventi dell'interfaccia utente. AccEvent viene in genere usato per eseguire il debug dei problemi e per convalidare il corretto funzionamento dei controlli personalizzati ed estesi.
- [AccScope:](/windows/desktop/winauto/accscope)consente la valutazione visiva dell'accessibilità di un'applicazione durante le prime fasi di progettazione e sviluppo. AccScope consente di visualizzare il modo in cui un'utilità per la lettura dello schermo usa le Automazione interfaccia utente fornite da un'app e mostra dove l'aggiunta di informazioni o supporto all'applicazione può migliorarne l'accessibilità.
- [Verifica accessibilità interfaccia utente:](/windows/desktop/winauto/ui-accessibility-checker)verifica che siano soddisfatti i requisiti di accessibilità principali dell'interfaccia utente in un'applicazione. AccChecker include controlli di verifica per Automazione interfaccia utente, Microsoft Active Accessibility e LEA (Accessible Rich Internet Applications). Può fornire un controllo statico degli errori, ad esempio nomi mancanti, problemi di albero e altro ancora. Consente di verificare l'accesso a livello di codice e include funzionalità avanzate per l'automazione dei test di accessibilità.
- [Automazione interfaccia utente verifica:](/windows/desktop/winauto/ui-automation-verify)framework per il test manuale e automatizzato dell'implementazione Automazione interfaccia utente in un controllo o in un'applicazione (i risultati possono essere registrati). È possibile integrare l'applicazione nel codice di test ed eseguire test regolari e automatizzati o controlli spot degli scenari Automazione interfaccia utente test. Questo strumento è utile per verificare che le modifiche apportate alle applicazioni con funzionalità stabilite non presentino nuovi problemi o regressioni in aree oltre le nuove funzionalità.
