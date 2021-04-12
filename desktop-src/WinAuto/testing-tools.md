---
title: Strumenti di test
description: Vengono descritti gli strumenti per testare l'implementazione dell'accessibilità dell'applicazione per garantire che l'interfaccia utente sia completamente accessibile alle applicazioni client e agli utenti che accedono all'applicazione tramite la tastiera.
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- strumenti di test di accessibilità
- strumenti di test, accessibilità
- test di accessibilità
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce653adb2602b8fdd46bebb72d3a7607185ffd84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118367"
---
# <a name="testing-tools"></a>Strumenti di test

L'accesso a livello di codice e l'accesso tramite tastiera sono requisiti essenziali per supportare l'accessibilità nell'applicazione. Senza un accesso adeguato, molti utenti di Assistive Technology (AT), ad esempio l'utilità per la lettura dello schermo e gli utenti della tastiera su schermo, non sarebbero in grado di usare l'applicazione. Assicurarsi di testare accuratamente l'implementazione dell'accessibilità dell'applicazione per confermare che fornisca informazioni adeguate sugli elementi dell'interfaccia utente e che tutti gli scenari dell'applicazione possano essere eseguiti solo con la tastiera.

Oltre a verificare l'accesso a livello di codice, alcuni degli strumenti consentono di valutare l'implementazione dell'accesso alla tastiera dell'applicazione. Tuttavia, gli strumenti da soli non sono sufficienti. È importante verificare manualmente che tutti gli scenari possano essere eseguiti solo con la tastiera.

Per i requisiti a livello di codice e di tastiera, non è disponibile uno strumento che consente di verificare l'implementazione completa. Provare a usare un'ampia gamma di strumenti per verificare l'implementazione e, quando possibile, trovare gli utenti delle tecnologie per l'accesso facilitato, ad esempio gli utilità per la lettura dello schermo, per usare l'interfaccia utente.

In questa sezione vengono descritti gli strumenti disponibili per testare le implementazioni di Microsoft UI Automation (UIA) e Microsoft Active Accessibility (MSAA).

## <a name="tools"></a>Strumenti

[Informazioni dettagliate sull'accessibilità](https://accessibilityinsights.io/) : consente agli sviluppatori di individuare e correggere i problemi di accessibilità nei siti Web e nelle applicazioni Windows.

- [Accessibility Insights per il Web](https://accessibilityinsights.io/docs/web/overview) è un'estensione per Chrome e [Microsoft Edge Insider](https://www.microsoftedgeinsider.com) che consente agli sviluppatori di individuare e correggere i problemi di accessibilità nei siti e nelle app Web. Supporta due scenari principali:
  - **Fastpass** : processo semplificato in due passaggi che consente agli sviluppatori di identificare i problemi di accessibilità comuni e ad alto effetto in meno di cinque minuti.  
  - **Valutazione** : consente a chiunque di verificare che un sito Web sia conforme al 100% con gli standard e le linee guida per l'accessibilità. [Accessibility Insights](https://accessibilityinsights.io/) consente anche di esaminare gli elementi, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente (analogamente agli strumenti di [ispezione](/windows/desktop/winauto/inspect-objects) e [Accevent](/windows/desktop/winauto/accessible-event-watcher) legacy descritti nella sezione seguente).

- [Accessibility Insights per Windows](https://accessibilityinsights.io/docs/windows/overview) consente agli sviluppatori di individuare e risolvere i problemi di accessibilità nelle app di Windows. Lo strumento supporta tre scenari principali:
  - Il **controllo in tempo reale** consente agli sviluppatori di verificare che un elemento in un'app disponga delle proprietà di automazione interfaccia utente appropriate semplicemente passando il mouse sull'elemento o impostando lo stato attivo della tastiera.
  - **Fastpass** : processo semplificato in due passaggi che consente agli sviluppatori di identificare i problemi di accessibilità comuni e ad alto effetto in meno di cinque minuti.
  - La **risoluzione dei problemi** consente di diagnosticare e risolvere specifici problemi di accessibilità.

### <a name="legacy-testing-tools"></a>Strumenti di test legacy

Gli strumenti seguenti sono ancora disponibili nella Windows SDK e sono documentati qui per il supporto continuo, ma è consigliabile eseguire la transizione a [Insights di accessibilità](https://accessibilityinsights.io/).

- [**Watcher eventi accessibili**](accessible-event-watcher.md): lo strumento Monitoraggio eventi accessibili (accEvent) esamina i dati di accessibilità per convalidare gli elementi dell'interfaccia utente dell'applicazione, per assicurarsi che gli elementi dell'interfaccia utente generino eventi di automazione interfaccia utente e Active Accessibility Microsoft appropriati quando si verificano modifiche all'interfaccia AccEvent viene in genere usato per eseguire il debug dei problemi e per convalidare il corretto funzionamento dei controlli personalizzati ed estesi.

- [**Controllare**](inspect-objects.md): consente di visualizzare i dati di accessibilità in qualsiasi elemento dell'interfaccia utente. È particolarmente utile quando si estende un controllo comune o si crea un controllo personalizzato per assicurarsi che le proprietà e i pattern di controllo siano impostati correttamente.

- [**AccScope**](accscope.md): lo strumento AccScope consente agli sviluppatori di valutare visivamente l'accessibilità dell'applicazione durante le prime fasi di progettazione e sviluppo. AccScope consente di visualizzare il modo in cui un'app Reader usa le informazioni di automazione interfaccia utente fornite da un'app. Consente di visualizzare le aree in cui l'aggiunta di informazioni o il supporto per l'applicazione può migliorare l'accessibilità.

- [**Controllo di accessibilità**](ui-accessibility-checker.md)dell'interfaccia utente: lo strumento ACCCHECKER (UI Accessibility Checker) verifica che siano soddisfatti i requisiti di accessibilità chiave dell'interfaccia utente. AccChecker include controlli di verifica per l'automazione dell'interfaccia utente, Microsoft Active Accessibility e le applicazioni Rich Internet (ARIA) accessibili. Può fornire un controllo statico per la ricerca di errori, ad esempio nomi mancanti, problemi di struttura ad albero e altro ancora. Consente di verificare l'accesso a livello di codice e offre funzionalità avanzate per supportare l'automazione del test di accessibilità.

- [**Verifica automazione interfaccia**](ui-automation-verify.md)utente: verifica dell'automazione interfaccia utente (UIA Verify) è un Framework di test per test manuali e automatizzati dell'implementazione di un'applicazione o di un controllo dell'automazione dell'interfaccia utente. Consente inoltre di registrare i risultati del test. È possibile integrare l'applicazione nel codice di test ed eseguire verifiche regolari e automatizzate dei test o degli scenari di automazione dell'interfaccia utente. Questo strumento è utile per verificare che le modifiche apportate alle applicazioni con funzionalità stabilite non includano nuovi problemi o regressioni in aree oltre le nuove funzionalità.

### <a name="obsolete-tools"></a>Strumenti obsoleti

Gli strumenti di esplorazione **dell'interfaccia utente** e di **Esplora accessibili** sono obsoleti e non sono più disponibili. In alternativa, utilizzare [**ispezionare**](inspect-objects.md) o [**AccScope**](accscope.md) .

## <a name="related-topics"></a>Argomenti correlati

- [Hub per sviluppatori di accessibilità](https://developer.microsoft.com/windows/accessible-apps)
- [Accessibilità Microsoft](https://www.microsoft.com/accessibility/)