---
title: Tecnologie dell'interfaccia utente
description: In questo argomento viene fornita una breve panoramica delle tecnologie Microsoft per lo sviluppo di interfacce utente per le applicazioni basate su Windows.
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d9343672d064cf073ea8018758b90083f440bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963372"
---
# <a name="user-interface-technologies"></a>Tecnologie dell'interfaccia utente

In questo argomento viene fornita una breve panoramica delle tecnologie Microsoft per lo sviluppo di interfacce utente per le applicazioni basate su Windows. Fornisce le informazioni necessarie per determinare se utilizzare una determinata tecnologia e identifica la posizione in cui è possibile reperire ulteriori informazioni.

In questo argomento vengono descritte le tecnologie seguenti:

-   [Tecnologie dell'interfaccia utente per le applicazioni non gestite](#user-interface-technologies-for-unmanaged-applications)
    -   [Controlli Windows](#windows-controls)
    -   [Stili di visualizzazione](#visual-styles)
    -   [Framework della barra multifunzione di Windows](#windows-ribbon-framework)
    -   [Gestione animazioni Windows](#windows-animation-manager)
    -   [Gestione finestre desktop](#desktop-window-manager)
    -   [API di automazione di Windows](#windows-automation-api)
    -   [Speech API](#speech-api)
    -   [API Magnification](#magnification-api)
    -   [Compilatore di risorse](#resource-compiler)
-   [Tecnologie dell'interfaccia utente per le applicazioni gestite](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Expression Blend 3 + SketchFlow](/windows)
    -   [Automazione interfaccia utente per le applicazioni gestite](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>Tecnologie dell'interfaccia utente per le applicazioni non gestite

In questa sezione vengono descritte le tecnologie Microsoft per lo sviluppo di interfacce utente per le applicazioni Windows non gestite. Queste tecnologie sono destinate agli sviluppatori C/C++ esperti che hanno familiarità con i concetti di programmazione di WindowsAPI e che usano Microsoft Windows Software Development Kit (SDK). Alcune tecnologie hanno prerequisiti aggiuntivi, ad esempio la conoscenza dei problemi di programmazione grafica o la familiarità con le nozioni di base della programmazione Component Object Model (COM).

### <a name="windows-controls"></a>Controlli Windows

I controlli Windows sono elementi dell'interfaccia utente utilizzati insieme a un'altra finestra (in genere una finestra o una finestra di dialogo client) per consentire all'utente di interagire con un'applicazione. Molti degli elementi che costituiscono l'interfaccia utente di un'applicazione tradizionale basata su Windows sono i controlli Windows, inclusi elementi quali menu, barre di scorrimento, pulsanti, caselle di riepilogo, visualizzazioni albero e così via.

I controlli Windows sono supportati da tutte le versioni di Windows. Tuttavia, poiché i componenti della fase di esecuzione che supportano i controlli si sono evoluti nel tempo, alcuni controlli e funzionalità introdotti nelle versioni successive non sono supportati nelle versioni precedenti. Le applicazioni devono rilevare le versioni e utilizzare solo le funzionalità disponibili.

Usare i controlli di Windows se si vuole creare un'interfaccia utente tradizionale per un'applicazione basata su Windows non gestita eseguita in un'ampia gamma di versioni di Windows.

Per ulteriori informazioni, vedere [controlli Windows](../controls/window-controls.md).

### <a name="visual-styles"></a>Stili di visualizzazione

Gli stili di visualizzazione sono specifiche per l'aspetto dei controlli. Uno stile di visualizzazione, ad esempio, può definire l'aspetto complessivo dei controlli e consentire agli sviluppatori di software di configurare l'interfaccia visiva di tali controlli per coordinarsi con l'aspetto di un'applicazione. Inoltre, gli stili di visualizzazione forniscono un meccanismo che consente a tutte le applicazioni basate su Windows di standardizzare l'aspetto di un'applicazione.

Gli stili di visualizzazione sono supportati in Windows XP e versioni successive e influiscono solo sull'aspetto dei controlli Windows standard e dei controlli comuni di Microsoft Win32.

È consigliabile usare gli stili di visualizzazione se è necessario modificare l'aspetto dei controlli Windows standard e dei controlli comuni in modo che corrispondano all'aspetto dell'interfaccia utente dell'applicazione.

Per altre informazioni, vedere [stili di visualizzazione](../controls/themes-overview.md).

### <a name="windows-ribbon-framework"></a>Framework della barra multifunzione di Windows

Il Framework della barra multifunzione di Windows è un sistema avanzato per la presentazione di comandi per applicazioni basate su Windows. È costituito da una barra dei comandi della barra multifunzione che espone le funzionalità principali di un'applicazione tramite una serie di schede nella parte superiore di una finestra dell'applicazione e un sistema di menu di scelta rapida. Il Framework della barra multifunzione di Windows è supportato nelle versioni di Windows seguenti:

-   Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Vista
-   Windows 7 e versioni successive
-   Windows Server 2008 R2
-   Windows Server 2008 con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Server 2008

È consigliabile utilizzare il Framework della barra multifunzione di Windows se si desidera implementare un'interfaccia utente di comando che rappresenta un'alternativa ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.

Il Framework della barra multifunzione di Windows è destinato agli sviluppatori esperti nella programmazione COM.

Per altre informazioni, vedere [Framework della barra multifunzione di Windows](../windowsribbon/-uiplat-windowsribbon-entry.md).

### <a name="windows-animation-manager"></a>Gestione animazioni Windows

Windows Animation Manager supporta l'animazione degli elementi dell'interfaccia utente fornendo un potente motore di animazione e un'interfaccia a livello di codice standardizzata. La piattaforma semplifica lo sviluppo e la manutenzione delle sequenze di animazione dell'interfaccia utente e consente agli sviluppatori di implementare animazioni dell'interfaccia utente coerenti e intuitive. L'animazione Windows può essere usata con qualsiasi piattaforma grafica, tra cui Direct2D, Microsoft Direct3D o Windows GDI+.

Windows Animation Framework è supportato in Windows Vista con aggiornamento della piattaforma per Windows VistaWindows vista con SP2 e aggiornamento della piattaforma per Windows Vista e Windows 7 e versioni successive.

È consigliabile utilizzare Gestione animazioni di Windows se si desidera aggiungere sequenze di animazione all'interfaccia utente di un'applicazione basata su Windows non gestita.

Per ulteriori informazioni, vedere [Windows Animation Manager](../uianimation/-main-portal.md).

### <a name="desktop-window-manager"></a>Gestione finestre desktop

Gestione finestre desktop (DWM) è un componente della fase di esecuzione di Windows che supporta la composizione del desktop, una funzionalità introdotta in Windows Vista. Grazie alla composizione del desktop, DWM Abilita gli effetti visivi nell'interfaccia utente, ad esempio i frame della finestra Glass, le animazioni di transizione delle finestre 3D, Windows Flip e Windows Flip3D e il supporto ad alta risoluzione.

DWM espone un'API per il controllo di molti degli effetti visivi associati alla composizione desktop. Ad esempio, un'applicazione può visualizzare le anteprime, applicare un effetto translucido e sfocato all'area client delle finestre di primo livello, controllare gli effetti della trasparenza e della transizione usati nell'area non client di Windows e così via.

DWM è supportato in Windows Vista e Windows Server 2008.

È consigliabile utilizzare DWM se l'applicazione deve accedere e controllare gli effetti visivi associati alla composizione desktop.

Per ulteriori informazioni, vedere [Gestione finestre desktop](../dwm/dwm-overview.md).

### <a name="windows-automation-api"></a>API di automazione di Windows

L'API di automazione di Windows consente agli sviluppatori di creare applicazioni accessibili al più ampio pubblico possibile, tra cui persone con disabilità di visione, udito o movimento. L'API funziona esponendo informazioni sugli elementi che costituiscono un'interfaccia utente dell'applicazione. Le applicazioni di Assistive Technology, ad esempio gli utilità per la lettura dello schermo, possono utilizzare le informazioni per presentare l'interfaccia utente in modo che possa essere utilizzata da utenti con particolari esigenze.

L'API di automazione di Windows è costituita da due Framework API distinti, Microsoft Active Accessibility e automazione interfaccia utente Microsoft. Microsoft Active Accessibility è un'API legacy introdotta in Windows 95 come componente aggiuntivo per la piattaforma. Automazione interfaccia utente è il successore di Microsoft Active Accessibility e è un'implementazione di Windows della specifica di automazione interfaccia utente.

Il supporto completo per Microsoft Active Accessibility è integrato in Windows XP e Windows Server 2003. Microsoft Active Accessibility è inoltre supportato in Windows NT 4,0 con Service Pack 6 (SP6) e versioni successive e Windows 98. Automazione interfaccia utente è supportata nei sistemi operativi seguenti: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows Server 2008 e Windows Server 2008 R2.

Se l'applicazione contiene controlli personalizzati o altre funzionalità dell'interfaccia utente personalizzate, è necessario usare l'API di automazione di Windows per assicurarsi che i controlli e le funzionalità personalizzati siano completamente accessibili. In generale, gli sviluppatori necessitano di un livello moderato di informazioni sugli oggetti e le interfacce COM, sulla programmazione Unicode e sull'API Windows.

Per altre informazioni, vedere [API di automazione di Windows](../winauto/windows-automation-api-portal.md).

### <a name="speech-api"></a>Speech API

Microsoft Speech API (SAPI) fornisce un'interfaccia di alto livello tra un'applicazione e un motore di sintesi vocale. SAPI implementa tutti i dettagli di basso livello necessari per controllare e gestire le operazioni in tempo reale di diversi motori di riconoscimento vocale.

I due tipi di base dei motori SAPI sono i sistemi di sintesi vocale e di riconoscimento vocale. I sistemi TTS sintetizzano stringhe di testo e file nell'audio vocale usando le voci sintetiche. I riconoscitori di sintesi vocale convertono l'audio parlato in file e stringhe di testo leggibili.

È consigliabile usare SAPI se si vuole implementare un'interfaccia utente che consente all'utente di interagire con l'applicazione tramite il riconoscimento vocale e vocale, oltre ai dispositivi di input standard come la tastiera, il mouse e la visualizzazione.

Per ulteriori informazioni, vedere [Microsoft Speech API (SAPI) 5,4](/previous-versions/windows/desktop/ee125663(v=vs.85)).

### <a name="magnification-api"></a>API Magnification

L'API di ingrandimento (MAPI) viene usata per ingrandire parti dello schermo e per applicare gli effetti dei colori e altre trasformazioni. Questa API è destinata principalmente alle applicazioni di tecnologia per l'accesso facilitato che ingrandiscono le parti dello schermo per facilitarne la visualizzazione.

MAPI è supportato in Windows Vista, Windows 7, Windows Server 2008 e Windows Server 2008 R2. È destinato agli sviluppatori che hanno familiarità con i concetti di programmazione grafica.

Per altre informazioni, vedere [API di ingrandimento](/previous-versions/windows/desktop/magapi/entry-magapi-sdk).

### <a name="resource-compiler"></a>Compilatore di risorse

Il compilatore di risorse di Microsoft Windows è uno strumento di sviluppo di applicazioni usato per aggiungere l'interfaccia utente e altre risorse a un'applicazione basata su Windows. Una risorsa è costituita da dati non eseguibili usati da un'applicazione e include elementi quali finestre di dialogo, menu, stringhe, cursori, icone, bitmap e così via. Il compilatore di risorse è incluso in Microsoft Visual Studio e Windows SDK.

Per altre informazioni, vedere [-resource (opzioni del compilatore C#)](../menurc/resource-compiler.md).

## <a name="user-interface-technologies-for-managed-applications"></a>Tecnologie dell'interfaccia utente per le applicazioni gestite

In questa sezione vengono descritte le tecnologie Microsoft per lo sviluppo di interfacce utente per le applicazioni Windows gestite eseguite nel contesto del .NET Framework. Per ulteriori informazioni, vedere [sviluppo di .NET](/previous-versions/ff361664(v=vs.100)).

### <a name="windows-forms"></a>Windows Forms

Windows Form è un Application Programming Interface grafico per la creazione di applicazioni Windows gestite basate sulla .NET Framework. In Windows Form, un modulo è una superficie visiva in cui vengono visualizzate le informazioni per l'utente e tramite cui si riceve l'input dall'utente.

Per compilare applicazioni di Windows Form, è possibile aggiungere controlli ai moduli e sviluppare risposte alle azioni dell'utente, ad esempio clic del mouse o pressioni dei tasti. Un controllo è un elemento discreto dell'interfaccia utente che Visualizza i dati o accetta input di dati. Windows Form contiene diversi controlli che possono essere inseriti nei form, ad esempio i controlli che visualizzano caselle di testo, pulsanti, caselle di riepilogo a discesa, pulsanti di opzione e persino pagine Web. Windows Form supporta anche la creazione di controlli personalizzati.

Per ulteriori informazioni, vedere [Windows Form](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)).

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) è il successore di [Windows Form](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)). WPF è un sistema di presentazione per la compilazione e il rendering di interfacce utente in applicazioni client basate su Windows e applicazioni ospitate da browser. L'elemento principale di WPF è un motore di rendering vettoriale e indipendente dalla risoluzione compilato per sfruttare i vantaggi dei moderni componenti hardware grafici. Oltre a questo elemento principale, WPF offre un set completo di funzionalità per lo sviluppo di applicazioni che includono Extensible Application Markup Language (XAML), controlli, data binding, layout, grafica 2D e 3D, animazioni, stili, modelli, documenti, supporti, testo e tipografia.

WPF è incluso in .NET Framework, per consentire la compilazione di applicazioni che incorporano altri elementi della libreria di classi .NET Framework. WPF è supportato in Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2 ed è disponibile anche per Windows XP con Service Pack 2 (SP2) e Windows Server 2003.

Per ulteriori informazioni, vedere [Windows Presentation Foundation](/dotnet/framework/wpf/).

### <a name="silverlight"></a>Silverlight

Microsoft Silverlight è una potente piattaforma di sviluppo per la creazione di applicazioni multimediali e applicazioni aziendali avanzate per il Web, il desktop e i dispositivi mobili.

In base alla .NET Framework, il plug-in Silverlight gratuito funziona su più browser, dispositivi e sistemi operativi per portare nuove interattività sul Web. Grazie a numerose opzioni di layout e stile, protocolli di comunicazione avanzati, accesso affidabile ai dati e supporto per l'interazione dell'utente e i supporti ad alta definizione, Silverlight consente di creare esperienze clienti veloci, uniformi e visivamente complesse. Le applicazioni Silverlight possono essere sviluppate rapidamente con la piattaforma Web Microsoft, Visual Studio ed Expression Studio.

Per ulteriori informazioni, vedere [Microsoft Silverlight](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95)).

### <a name="expression-blend-3--sketchflow"></a>Expression Blend 3 + SketchFlow

Expression Blend 3 + SketchFlow è uno strumento visivo per la progettazione, la creazione di prototipi e la creazione di interfacce utente sofisticate per applicazioni desktop e Web WPF e Silverlight. È possibile compilare un'applicazione disegnando forme, disegnando controlli quali pulsanti e caselle di riepilogo, facendo in modo che i componenti dell'applicazione rispondano ai clic del mouse e ad altri input dell'utente e applicando lo stile a tutti gli elementi per l'aspetto.

Per ulteriori informazioni, vedere la pagina relativa [al prototipo con SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)).

### <a name="ui-automation-for-managed-applications"></a>Automazione interfaccia utente per le applicazioni gestite

Automazione interfaccia utente è un Framework di accessibilità per Windows, disponibile in tutti i sistemi operativi che supportano WPF.

Automazione interfaccia utente consente l'accesso a livello di codice alla maggior parte degli elementi dell'interfaccia utente sul desktop, consentendo a prodotti di Assistive Technology quali utilità per la lettura dello schermo di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente per mezzo di input standard. Automazione interfaccia utente consente inoltre l'interazione degli script di test automatizzati con l'interfaccia utente.

Per altre informazioni, vedere [automazione interfaccia utente per le applicazioni gestite](/dotnet/framework/ui-automation/).

 

 