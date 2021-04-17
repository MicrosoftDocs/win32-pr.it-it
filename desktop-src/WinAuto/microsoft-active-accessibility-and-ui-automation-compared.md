---
title: Confronto tra Active Accessibility Microsoft e automazione interfaccia utente
description: In questo argomento vengono riepilogate le principali differenze tra Active Accessibility Microsoft e l'automazione dell'interfaccia utente.
ms.assetid: ba963e53-6fb8-4bc1-8883-62547f52b0e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c90c4bffd0646aea592e19adc51ca020b2c90d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300124"
---
# <a name="microsoft-active-accessibility-and-ui-automation-compared"></a>Confronto tra Active Accessibility Microsoft e automazione interfaccia utente

L'API di automazione di Windows è costituita da due tecnologie: Microsoft Active Accessibility e automazione interfaccia utente Microsoft. Microsoft Active Accessibility è la tecnologia di accessibilità legacy introdotta come componente aggiuntivo della piattaforma per Windows 95, mentre l'automazione dell'interfaccia utente è una tecnologia più recente e più idonea che consente di sovraentrare le limitazioni inerenti a Microsoft Active Accessibility.

In questo argomento vengono riepilogate le principali differenze tra Active Accessibility Microsoft e l'automazione dell'interfaccia utente. Include le sezioni seguenti:

-   [Principi di progettazione di base](#basic-design-principles)
-   [Proprietà e pattern di controllo](#properties-and-control-patterns)
-   [Ruoli MSAA e pattern di controllo di automazione interfaccia utente](#msaa-roles-and-ui-automation-control-patterns)
-   [Esplorazione del modello a oggetti](#object-model-navigation)
-   [Estendibilità del modello a oggetti](#object-model-extensibility)
-   [Transizione da MSAA](#transitioning-from-msaa)
-   [Scelta di Microsoft Active Accessibility, automazione interfaccia utente o IAccessibleEx](#choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex)
    -   [Nuove applicazioni e controlli](#new-applications-and-controls)
    -   [Implementazioni esistenti di Microsoft Active Accessibility](#existing-microsoft-active-accessibility-implementations)
-   [Argomenti correlati](#related-topics)

## <a name="basic-design-principles"></a>Principi di progettazione di base

Sebbene Microsoft Active Accessibility e l'automazione dell'interfaccia utente siano due tecnologie diverse, i principi di base della progettazione sono simili. Lo scopo di entrambe le tecnologie è esporre informazioni dettagliate sugli elementi dell'interfaccia utente utilizzati nelle applicazioni Windows. Gli sviluppatori di strumenti di accessibilità possono usare queste informazioni per creare software che rende le applicazioni in esecuzione in Windows più accessibili per gli utenti con disabilità di visione, udito o movimento.

Sia Microsoft Active Accessibility che automazione interfaccia utente espongono il modello a oggetti dell'interfaccia utente come albero gerarchico, con radice sul desktop. Microsoft Active Accessibility rappresenta gli elementi dell'interfaccia utente singoli come *oggetti accessibili* e l'automazione dell'interfaccia utente li rappresenta come *elementi di automazione*. Entrambi fanno riferimento allo strumento di accessibilità o al programma di automazione software come *client*. Tuttavia, Microsoft Active Accessibility si riferisce all'applicazione o al controllo che offre l'interfaccia utente per l'accessibilità come *Server*, mentre automazione interfaccia utente fa riferimento a questo come *provider*.

## <a name="properties-and-control-patterns"></a>Proprietà e pattern di controllo

Microsoft Active Accessibility offre un'unica interfaccia Component Object Model (COM) con un set di proprietà fisso e limitato. Automazione interfaccia utente offre un set più completo di proprietà, oltre a un set di interfacce estese denominate *pattern di controllo* per modificare gli oggetti accessibili nei modi in cui Microsoft Active Accessibility non può.

Per altre informazioni, vedere Cenni preliminari sulle [proprietà di automazione interfaccia](uiauto-propertiesoverview.md) utente e [Panoramica dei pattern di controllo di automazione interfaccia utente](uiauto-controlpatternsoverview.md)

## <a name="msaa-roles-and-ui-automation-control-patterns"></a>Ruoli MSAA e pattern di controllo di automazione interfaccia utente

Microsoft ha progettato il modello a oggetti di Microsoft Active Accessibility in un momento in cui è stato rilasciato Windows 95. Il modello è basato su "Roles" definito un decennio fa e non è possibile supportare nuovi comportamenti dell'interfaccia utente o unire due o più ruoli insieme. Non esiste, ad esempio, un modello a oggetti di testo per aiutare le tecnologie per l'accesso facilitato alla gestione di contenuti Web complessi. L'automazione dell'interfaccia utente supera queste limitazioni introducendo pattern di controllo che consentono agli oggetti di supportare più di un ruolo e il pattern di controllo del [testo](uiauto-implementingtextandtextrange.md) di automazione interfaccia utente offre un modello a oggetti di testo completo.

## <a name="object-model-navigation"></a>Esplorazione del modello a oggetti

Un altro limite di Microsoft Active Accessibility implica l'esplorazione del modello a oggetti. Microsoft Active Accessibility rappresenta l'interfaccia utente come una gerarchia di oggetti accessibili. I client passano da un oggetto accessibile a un altro usando le interfacce e i metodi disponibili dall'oggetto accessibile. I server possono esporre gli elementi figlio di un oggetto accessibile con proprietà dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o con l'interfaccia com [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) standard. I client, tuttavia, devono essere in grado di gestire entrambi gli approcci per qualsiasi server. Questa ambiguità implica operazioni aggiuntive per gli implementatori dei client e modelli a oggetti interrotti accessibili per gli implementatori di server.

Automazione interfaccia utente rappresenta l'interfaccia utente come albero gerarchico di elementi di automazione e fornisce una singola interfaccia per spostarsi nell'albero. I client possono personalizzare la visualizzazione degli elementi nell'albero per ambito e filtro.

## <a name="object-model-extensibility"></a>Estendibilità del modello a oggetti

Le funzioni e le proprietà di Microsoft Active Accessibility non possono essere estese senza suddividere o modificare la specifica dell'interfaccia com [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Il risultato è che il nuovo comportamento del controllo non può essere esposto tramite il modello a oggetti. tende a essere statica.

Con l'automazione dell'interfaccia utente, quando vengono creati nuovi elementi dell'interfaccia utente, gli sviluppatori di applicazioni possono introdurre proprietà personalizzate, pattern di controllo ed eventi per descrivere i nuovi elementi. Per altre informazioni, vedere [proprietà personalizzate, eventi e pattern di controllo](uiauto-custompropertieseventscontrolpatterns.md).

## <a name="transitioning-from-msaa"></a>Transizione da MSAA

Il Framework dell'API di automazione di Windows fornisce il supporto per la transizione da server Microsoft Active Accessibility a provider di automazione interfaccia utente. L'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) Abilita il supporto per specifiche proprietà di automazione interfaccia utente e pattern di controllo da aggiungere ai server Microsoft Active Accessibility legacy senza dover riscrivere l'intera implementazione. L'interfaccia **IAccessibleEx** consente inoltre ai client Microsoft Active Accessibility in-process di accedere direttamente alle interfacce del provider di automazione interfaccia utente, anziché tramite interfacce client di automazione interfaccia utente. Per ulteriori informazioni, vedere [l'interfaccia IAccessibleEx](iaccessibleex.md).

## <a name="choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex"></a>Scelta di Microsoft Active Accessibility, automazione interfaccia utente o IAccessibleEx

Questa sezione consente di determinare quale soluzione API di automazione di Windows utilizzare per implementare un prodotto di Assistive Technology o rendere accessibile l'applicazione ai prodotti di Assistive Technology.

### <a name="new-applications-and-controls"></a>Nuove applicazioni e controlli

Se si sviluppa una nuova applicazione o un nuovo controllo, Microsoft consiglia di usare l'automazione dell'interfaccia utente. Sebbene Microsoft Active Accessibility possa essere più facile da implementare a breve termine, le limitazioni inerenti a questa tecnologia, ad esempio il modello a oggetti di durata e l'impossibilità di supportare nuovi comportamenti dell'interfaccia utente o di unire i ruoli, rendono più difficile e costosa a lungo termine. Queste limitazioni diventano particolarmente evidenti quando si introducono nuovi controlli.

Il modello a oggetti di automazione interfaccia utente è più facile da usare ed è più flessibile rispetto a quello di Microsoft Active Accessibility. Gli elementi di automazione interfaccia utente riflettono l'evoluzione delle interfacce utente e gli sviluppatori possono definire pattern di controllo, proprietà ed eventi personalizzati di automazione interfaccia utente.

Microsoft Active Accessibility tende a funzionare lentamente per i client che hanno esaurito il processo. Per migliorare le prestazioni, gli sviluppatori di programmi per gli strumenti di accessibilità scelgono spesso di collegare ed eseguire i propri programmi nel processo dell'applicazione di destinazione: un approccio estremamente complesso e rischioso. L'automazione dell'interfaccia utente è molto più semplice da implementare per i client out-of-process e offre prestazioni e affidabilità molto migliori.

### <a name="existing-microsoft-active-accessibility-implementations"></a>Implementazioni esistenti di Microsoft Active Accessibility

Se si sta aggiornando un'applicazione o un controllo esistente basato su Active Accessibility Microsoft, è consigliabile aggiungere il supporto per l'automazione dell'interfaccia utente implementando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Assicurarsi prima di tutto che l'applicazione o il controllo soddisfi i requisiti seguenti:

-   La gerarchia di base di Microsoft Active Accessibility server degli oggetti accessibili deve essere ben organizzata e priva di errori. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) non è in grado di correggere problemi con le gerarchie di oggetti accessibili esistenti.
-   L'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) deve essere conforme alla specifica di Microsoft Active Accessibility e alla specifica di automazione interfaccia utente. Microsoft fornisce un set di strumenti per la convalida della conformità con entrambe le specifiche. Per altre informazioni, vedere [strumenti di test](testing-tools.md).

Se uno di questi requisiti non viene soddisfatto, provare a implementare automazione interfaccia utente in modo nativo. Se necessario, è possibile mantenere le implementazioni legacy di Microsoft Active Accessibility server per la compatibilità con le versioni precedenti. Dal punto di vista del client di automazione interfaccia utente, non esiste alcuna differenza tra i provider di automazione interfaccia utente e i server Microsoft Active Accessibility che implementano correttamente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Per ulteriori informazioni, vedere [l'interfaccia IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'API di automazione di Windows](windows-automation-api-overview.md)
</dt> <dt>

[Microsoft Active Accessibility](microsoft-active-accessibility.md)
</dt> <dt>

[Automazione interfaccia utente](entry-uiauto-win32.md)
</dt> <dt>

[Interfaccia IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 