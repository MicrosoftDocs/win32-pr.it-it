---
title: Strumenti di test
description: Vengono descritti gli strumenti per testare l'implementazione dell'accessibilità dell'applicazione per garantire che l'interfaccia utente sia completamente accessibile alle applicazioni client e agli utenti che accedono all'applicazione tramite tastiera.
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- strumenti di test dell'accessibilità
- strumenti di test, accessibilità
- test dell'accessibilità
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcd5d8b0777eb80cf5b2935cc8652d328dfc219cb56bc654c1eeae0761bbd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133594"
---
# <a name="testing-tools"></a>Strumenti di test

L'accesso a livello di codice e l'accesso tramite tastiera sono requisiti fondamentali per supportare l'accessibilità nell'applicazione. Senza un accesso adeguato, molti utenti di assistive technology (AT), ad esempio utenti con utilità per la lettura dello schermo e tastiera su schermo, non sarebbero in grado di usare l'applicazione. Assicurarsi di testare accuratamente l'implementazione dell'accessibilità dell'applicazione per verificare che fornisce informazioni adeguate sugli elementi dell'interfaccia utente e che tutti gli scenari dell'applicazione possano essere eserciti solo con la tastiera.

Oltre a verificare l'accesso a livello di codice, alcuni degli strumenti consentono di valutare l'implementazione dell'accesso tramite tastiera dell'applicazione. Tuttavia, gli strumenti da soli non sono sufficienti. È importante verificare manualmente che tutti gli scenari possano essere evasi solo con la tastiera.

Per i requisiti a livello di codice e della tastiera, non è disponibile alcuno strumento in grado di verificare l'implementazione completa. Provare a usare un'ampia gamma di strumenti per verificare l'implementazione e, quando possibile, trovare gli utenti delle tecnologie di assistive, ad esempio le utilità per la lettura dello schermo, per usare l'interfaccia utente.

Questa sezione descrive gli strumenti disponibili per testare le implementazioni di Microsoft Automazione interfaccia utente (UIA) e Microsoft Active Accessibility (MSAA).

## <a name="tools"></a>Strumenti

[Accessibilità Insights:](https://accessibilityinsights.io/) consente agli sviluppatori di trovare e risolvere i problemi di accessibilità sia nei siti Web che nelle Windows applicazioni.

- [Accessibility Insights for Web](https://accessibilityinsights.io/docs/web/overview) è un'estensione per Chrome [e Microsoft Edge Insider](https://www.microsoftedgeinsider.com) che consente agli sviluppatori di trovare e risolvere i problemi di accessibilità nelle app Web e nei siti. Supporta due scenari principali:
  - **FastPass:** un processo leggero in due passaggi che consente agli sviluppatori di identificare i problemi comuni di accessibilità ad alto impatto in meno di cinque minuti.  
  - **Valutazione:** consente a chiunque di verificare che un sito Web sia conforme al 100% con gli standard e le linee guida per l'accessibilità. [L Insights](https://accessibilityinsights.io/) di accessibilità consente anche di esaminare Automazione interfaccia utente elementi, proprietà, pattern di controllo ed eventi ,analogamente agli strumenti legacy [Inspect](/windows/desktop/winauto/inspect-objects) e [AccEvent](/windows/desktop/winauto/accessible-event-watcher) descritti nella sezione seguente.

- [La Insights per Windows](https://accessibilityinsights.io/docs/windows/overview) consente agli sviluppatori di individuare e risolvere i problemi di accessibilità nelle Windows app. Lo strumento supporta tre scenari principali:
  - **Live Inspect** consente agli sviluppatori di verificare che un elemento in un'app abbia le proprietà Automazione interfaccia utente semplicemente passando il puntatore sull'elemento o impostando lo stato attivo della tastiera su di esso.
  - **FastPass:** un processo leggero in due passaggi che consente agli sviluppatori di identificare i problemi comuni di accessibilità ad alto impatto in meno di cinque minuti.
  - **La risoluzione** dei problemi consente di diagnosticare e correggere problemi di accessibilità specifici.

### <a name="legacy-testing-tools"></a>Strumenti di test legacy

Gli strumenti seguenti sono ancora disponibili in Windows SDK e sono documentati qui per il supporto continuo, ma è consigliabile passare a Accessibilità [Insights](https://accessibilityinsights.io/).

- [**Accessible Event Watcher**](accessible-event-watcher.md): lo strumento Accessible Event Watcher (AccEvent) esamina i dati di accessibilità per convalidare gli elementi dell'interfaccia utente dell'applicazione, per garantire che gli elementi dell'interfaccia utente generano eventi Microsoft Active Accessibility e Automazione interfaccia utente adeguati quando si verificano modifiche all'interfaccia utente. AccEvent viene in genere usato per eseguire il debug dei problemi e per convalidare il corretto funzionamento dei controlli personalizzati ed estesi.

- [**Inspect**](inspect-objects.md): Inspect consente di visualizzare i dati di accessibilità in qualsiasi elemento dell'interfaccia utente. È particolarmente utile, quando si estende un controllo comune o si crea un controllo personalizzato, per garantire che le proprietà e i pattern di controllo siano impostati correttamente.

- [**AccScope:**](accscope.md)lo strumento AccScope consente agli sviluppatori di valutare visivamente l'accessibilità dell'applicazione durante le fasi iniziali di progettazione e sviluppo. AccScope consente di visualizzare il modo in cui un'utilità per la lettura dello schermo Automazione interfaccia utente informazioni fornite da un'app. Può mostrare le aree in cui l'aggiunta di informazioni o supporto all'applicazione può migliorarne l'accessibilità.

- [**Verifica accessibilità interfaccia utente:**](ui-accessibility-checker.md)lo strumento Controllo accessibilità interfaccia utente verifica che siano soddisfatti i requisiti di accessibilità principali dell'interfaccia utente. AccChecker include i controlli di verifica per Automazione interfaccia utente, Microsoft Active Accessibility e LEA (Accessible Rich Internet Applications). Può fornire un controllo statico alla ricerca di errori, ad esempio nomi mancanti, problemi di albero e altro ancora. Consente di verificare l'accesso a livello di codice e offre funzionalità avanzate per supportare l'automazione dei test di accessibilità.

- [**Automazione interfaccia utente Verify**](ui-automation-verify.md): Automazione interfaccia utente Verify (UIA Verify) è un framework di test per test manuali e automatizzati dell'implementazione di un controllo o di un'applicazione di Automazione interfaccia utente. Può anche registrare i risultati del test. È possibile integrare l'applicazione nel codice di test ed eseguire normali test automatizzati o controlli spot Automazione interfaccia utente scenari. Questo strumento è utile per verificare che le modifiche alle applicazioni con funzionalità stabilite non presentino nuovi problemi o regressioni nelle aree oltre le nuove funzionalità.

### <a name="obsolete-tools"></a>Strumenti obsoleti

Gli **strumenti Accessible Explorer** e UI **Spy** sono obsoleti e non sono più disponibili. In [**alternativa,**](inspect-objects.md) usare Inspect [**o AccScope.**](accscope.md)

## <a name="related-topics"></a>Argomenti correlati

- [Hub per sviluppatori per l'accessibilità](https://developer.microsoft.com/windows/accessible-apps)
- [Accessibilità Di Microsoft](https://www.microsoft.com/accessibility/)