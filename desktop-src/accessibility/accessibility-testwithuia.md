---
description: Panoramica dell'uso di automazione interfaccia utente e di altri strumenti per testare le app.
title: Test per l'accessibilità
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0d589c9b7bd598c0829ff9941ab2facabfaf10d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127582"
---
# <a name="testing-for-accessibility"></a>Test per l'accessibilità

L'accesso a livello di codice e l'accesso tramite tastiera sono requisiti essenziali per supportare l'accessibilità nell'applicazione. Il test dell'accessibilità delle applicazioni Windows, degli strumenti di Assistive Technology (AT) e dei framework dell'interfaccia utente è fondamentale per garantire un'esperienza utente efficace per gli utenti con diverse disabilità e limitazioni (tra cui visione, apprendimento, destrezza/mobilità e disabilità di lingua/comunicazione) o chi preferisce semplicemente utilizzare una tastiera.

Senza un accesso adeguato a, ad esempio lettori schermo e tastiere sullo schermo, gli utenti con visione, apprendimento, destrezza/mobilità e disabilità o limitazioni di lingua/comunicazione (e utenti che preferiscono semplicemente utilizzare la tastiera) non sarebbero in grado di utilizzare l'applicazione.

In questa sezione vengono descritti i vari strumenti che è possibile utilizzare per testare l'implementazione dell'accessibilità delle applicazioni Windows e Web.

> [!NOTE]
> È anche importante eseguire test manuali per verificare l'accesso tramite tastiera all'applicazione.

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

- [Ispeziona](/windows/desktop/winauto/inspect-objects): consente di visualizzare i dati di accessibilità di qualsiasi elemento dell'interfaccia utente. È particolarmente utile per garantire che le proprietà e i pattern di controllo siano impostati correttamente quando si estende un controllo comune o si crea un controllo personalizzato.
- [Monitoraggio eventi accessibili (accEvent)](/windows/desktop/winauto/accessible-event-watcher): esamina i dati di accessibilità per convalidare gli elementi dell'interfaccia utente dell'applicazione e verificare che gli elementi dell'interfaccia utente generino gli eventi di Microsoft Active Accessibility e di automazione interfaccia utente appropriati AccEvent viene in genere usato per eseguire il debug dei problemi e per convalidare il corretto funzionamento dei controlli personalizzati ed estesi.
- [AccScope](/windows/desktop/winauto/accscope): consente la valutazione visiva dell'accessibilità di un'applicazione durante le fasi iniziali di progettazione e sviluppo. AccScope consente di visualizzare il modo in cui un'applicazione per la lettura dello schermo usa le informazioni di automazione interfaccia utente fornite da un'app e Mostra dove l'aggiunta di informazioni o il supporto per l'applicazione può migliorare l'accessibilità.
- [Controllo di accessibilità dell'interfaccia utente](/windows/desktop/winauto/ui-accessibility-checker): verifica che i requisiti di accessibilità chiave dell'interfaccia utente in un'applicazione vengano realizzati. AccChecker include controlli di verifica per l'automazione dell'interfaccia utente, Microsoft Active Accessibility e le applicazioni Rich Internet (ARIA) accessibili. Può fornire un controllo statico degli errori, ad esempio nomi mancanti, problemi di struttura ad albero e altro ancora. Consente di verificare l'accesso programmatico e include funzionalità avanzate per l'automazione dei test di accessibilità.
- [Verifica automazione interfaccia utente](/windows/desktop/winauto/ui-automation-verify): un Framework per test manuali e automatizzati dell'implementazione di automazione interfaccia utente in un controllo o in un'applicazione (i risultati possono essere registrati). È possibile integrare l'applicazione nel codice di test ed eseguire verifiche regolari e automatizzate dei test o degli scenari di automazione dell'interfaccia utente. Questo strumento è utile per verificare che le modifiche apportate alle applicazioni con funzionalità stabilite non includano nuovi problemi o regressioni in aree oltre le nuove funzionalità.
