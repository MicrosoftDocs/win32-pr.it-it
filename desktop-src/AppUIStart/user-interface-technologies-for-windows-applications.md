---
title: Interfaccia utente tecnologie
description: In questo argomento viene fornito un breve sondaggio sulle tecnologie Microsoft per lo sviluppo di Windows applicazioni basate su applicazioni.
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a36bbf73d5b319e04ba2b02570c6fce4124a9ec6d54fcec201e77c4c9487dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702321"
---
# <a name="user-interface-technologies"></a>Interfaccia utente tecnologie

In questo argomento viene fornito un breve sondaggio sulle tecnologie Microsoft per lo sviluppo di Windows applicazioni basate su applicazioni. Fornisce le informazioni necessarie per determinare se usare una determinata tecnologia e identifica la posizione in cui è possibile trovare altre informazioni.

In questo argomento vengono descritte le tecnologie seguenti:

-   [Interfaccia utente tecnologie per le applicazioni non gestite](#user-interface-technologies-for-unmanaged-applications)
    -   [Windows Controlli](#windows-controls)
    -   [Stili di visualizzazione](#visual-styles)
    -   [Windows Framework della barra multifunzione](#windows-ribbon-framework)
    -   [Windows Gestione animazione](#windows-animation-manager)
    -   [Gestione finestre desktop](#desktop-window-manager)
    -   [API di automazione di Windows](#windows-automation-api)
    -   [Speech API](#speech-api)
    -   [API Magnification](#magnification-api)
    -   [Compilatore di risorse](#resource-compiler)
-   [Interfaccia utente tecnologie per le applicazioni gestite](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Expression Blend 3 + SketchFlow](/windows)
    -   [Automazione interfaccia utente per le applicazioni gestite](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>Interfaccia utente tecnologie per le applicazioni non gestite

Questa sezione descrive le tecnologie Microsoft per lo sviluppo di interfacce utente per applicazioni Windows non gestite. Queste tecnologie sono destinate a sviluppatori C/C++ esperti che hanno familiarità con i concetti di programmazione WindowsAPI e che usano Microsoft Windows Software Development Kit (SDK). Alcune tecnologie hanno prerequisiti aggiuntivi, ad esempio la conoscenza dei problemi di programmazione grafica o la conoscenza delle nozioni di base della programmazione Component Object Model (COM).

### <a name="windows-controls"></a>Windows Controlli

Windows controlli sono elementi dell'interfaccia utente usati in combinazione con un'altra finestra (in genere una finestra client o una finestra di dialogo) per consentire all'utente di interagire con un'applicazione. Molti degli elementi che costituiscono l'interfaccia utente di un'applicazione tradizionale basata su Windows sono controlli Windows, inclusi elementi quali menu, barre di scorrimento, pulsanti, caselle di riepilogo, visualizzazioni albero e così via.

Windows sono supportati da tutte le versioni di Windows. Tuttavia, poiché i componenti di run-time che supportano i controlli si sono evoluti nel tempo, alcuni controlli e funzionalità introdotti nelle versioni successive non sono supportati nelle versioni precedenti. Le applicazioni devono rilevare le versioni e usare solo le funzionalità disponibili.

È consigliabile usare Windows se si vuole creare un'interfaccia utente tradizionale per un'applicazione basata su Windows non gestita che viene eseguita in un'ampia gamma di Windows versioni.

Per altre informazioni, vedere [Windows controlli](../controls/window-controls.md).

### <a name="visual-styles"></a>Stili di visualizzazione

Gli stili di visualizzazione sono specifiche per l'aspetto dei controlli. Ad esempio, uno stile di visualizzazione può definire l'aspetto complessivo dei controlli e consentire agli sviluppatori di software di configurare l'interfaccia visiva di tali controlli per coordinarsi con l'aspetto di un'applicazione. Inoltre, gli stili di visualizzazione forniscono un meccanismo per tutte Windows applicazioni basate Windows standardizzare l'aspetto di un'applicazione.

Gli stili di visualizzazione sono supportati Windows XP e versioni successive e influiscono solo sull'aspetto dei controlli Windows standard e dei controlli comuni Microsoft Win32.

È consigliabile usare gli stili di visualizzazione se è necessario modificare l'aspetto dei controlli Windows standard e dei controlli comuni in modo che corrispondano all'aspetto dell'interfaccia utente dell'applicazione.

Per altre informazioni, vedere [Stili di visualizzazione.](../controls/themes-overview.md)

### <a name="windows-ribbon-framework"></a>Windows Framework della barra multifunzione

Il framework Windows ribbon è un sistema di presentazione dei comandi Windows applicazioni basate su più applicazioni. È costituita da una barra dei comandi della barra multifunzione che espone le principali funzionalità di un'applicazione tramite una serie di schede nella parte superiore di una finestra dell'applicazione e un sistema di menu di scelta rapida. Il framework Windows ribbon è supportato nelle versioni Windows seguenti:

-   Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Vista
-   Windows 7 e versioni successive
-   Windows Server 2008 R2
-   Windows Server 2008 con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Server 2008

È consigliabile usare Windows framework della barra multifunzione se si vuole implementare un'interfaccia utente dei comandi alternativa ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.

Il Windows della barra multifunzione è destinato agli sviluppatori esperti di programmazione COM.

Per altre informazioni, vedere Windows [Ribbon Framework.](../windowsribbon/-uiplat-windowsribbon-entry.md)

### <a name="windows-animation-manager"></a>Windows Gestione animazione

Il Windows Animation Manager supporta l'animazione degli elementi dell'interfaccia utente fornendo un potente motore di animazione e un'interfaccia programmatica standardizzata. La piattaforma semplifica lo sviluppo e la manutenzione delle sequenze di animazione dell'interfaccia utente e consente agli sviluppatori di implementare animazioni dell'interfaccia utente coerenti e intuitive. Windows L'animazione può essere usata con qualsiasi piattaforma grafica, tra cui Direct2D, Microsoft Direct3D o Windows GDI+.

Il framework di animazione Windows è supportato in Windows Vista con l'aggiornamento della piattaforma per Windows VistaWindows Vista con SP2 e l'aggiornamento della piattaforma per Windows Vista e Windows 7 e versioni successive.

È consigliabile usare Windows Animation Manager se si vogliono aggiungere sequenze di animazione all'interfaccia utente di un'applicazione basata su Windows non gestita.

Per altre informazioni, vedere Windows [Animation Manager.](../uianimation/-main-portal.md)

### <a name="desktop-window-manager"></a>Gestione finestre desktop

Gestione finestre desktop (DWM) è un componente Windows di esecuzione che supporta la composizione desktop, una funzionalità introdotta in Windows Vista. Tramite la composizione desktop, DWM consente gli effetti visivi nell'interfaccia utente, ad esempio fotogrammi di finestre di effetto, animazioni di transizione di finestra 3D, Windows capovolgimento e Windows Flip3D e supporto ad alta risoluzione.

DWM espone un'API per controllare molti degli effetti visivi associati alla composizione del desktop. Ad esempio, un'applicazione può visualizzare anteprime, applicare un effetto traslucido e sfocato all'area client delle finestre di primo livello, controllare gli effetti di trasparenza e transizione usati nell'area non client delle finestre e così via.

DWM è supportato in Windows Vista e Windows Server 2008.

È consigliabile usare DWM se l'applicazione deve accedere e controllare gli effetti visivi associati alla composizione del desktop.

Per altre informazioni, vedere [Gestione finestre desktop](../dwm/dwm-overview.md).

### <a name="windows-automation-api"></a>API di automazione di Windows

L Windows API di Automazione di Windows consente agli sviluppatori di creare applicazioni accessibili al pubblico più ampio possibile, incluse le persone con problemi di vista, udito o movimento. L'API funziona esponendo informazioni sugli elementi che costituiscono un'interfaccia utente dell'applicazione. Le applicazioni di assistive technology, ad esempio le utilità per la lettura dello schermo, possono usare le informazioni per presentare l'interfaccia utente in modo che possa essere usata da persone con disabilità.

L Windows API di Automazione è costituita da due framework API separati, Microsoft Active Accessibility e Microsoft Automazione interfaccia utente. Microsoft Active Accessibility è un'API legacy introdotta in Windows 95 come componente aggiuntivo della piattaforma. Automazione interfaccia utente è il successore di Microsoft Active Accessibility ed è un'implementazione Windows della specifica Automazione interfaccia utente.

Il supporto completo Microsoft Active Accessibility è integrato in Windows XP e Windows Server 2003. Microsoft Active Accessibility è supportato anche in Windows NT 4.0 con Service Pack 6 (SP6) e versioni successive e Windows 98. Automazione interfaccia utente è supportato nei sistemi operativi seguenti: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows Server 2008 e Windows Server 2008 R2.

Se l'applicazione contiene controlli personalizzati o altre funzionalità dell'interfaccia utente personalizzate, è necessario usare l'API di automazione di Windows per assicurarsi che i controlli e le funzionalità personalizzati siano completamente accessibili. In generale, gli sviluppatori necessitano di un livello moderato di conoscenza degli oggetti e delle interfacce COM, di Unicode e Windows api.

Per altre informazioni, vedere API [Windows Automation.](../winauto/windows-automation-api-portal.md)

### <a name="speech-api"></a>Speech API

Microsoft Speech API (SAPI) offre un'interfaccia di alto livello tra un'applicazione e i motori vocali. SAPI implementa tutti i dettagli di basso livello necessari per controllare e gestire le operazioni in tempo reale dei vari motori vocali.

I due tipi di base di motori SAPI sono sistemi di sintesi vocale (TTS) e sistemi di riconoscimento vocale. I sistemi TTS sintetizzano file e stringhe di testo in audio parlato usando voci sintetiche. I riconoscitori vocali convertono l'audio parlato umano in file e stringhe di testo leggibili.

È consigliabile usare SAPI se si vuole implementare un'interfaccia utente che consenta all'utente di interagire con l'applicazione tramite TTS e riconoscimento vocale, oltre ai dispositivi di input standard, ad esempio tastiera, mouse e visualizzazione.

Per altre informazioni, vedere [Microsoft Speech API (SAPI) 5.4](/previous-versions/windows/desktop/ee125663(v=vs.85)).

### <a name="magnification-api"></a>API Magnification

L'API di ingrandimento (MAPI) viene usata per ingrandire parti dello schermo e per applicare effetti di colore e altre trasformazioni. Questa API è destinata principalmente alle applicazioni di assistive technology che ingrandisce parti dello schermo per facilitarne la visualizzazione.

MAPI è supportato in Windows Vista, Windows 7, Windows Server 2008 e Windows Server 2008 R2. È destinato agli sviluppatori che hanno familiarità con i concetti di programmazione grafica.

Per altre informazioni, vedere [API ingrandimento.](/previous-versions/windows/desktop/magapi/entry-magapi-sdk)

### <a name="resource-compiler"></a>Compilatore di risorse

Microsoft Windows Resource Compiler è uno strumento di sviluppo di applicazioni usato per aggiungere l'interfaccia utente e altre risorse a un'Windows basata su risorse. Una risorsa è qualsiasi dato non eseguibile usato da un'applicazione e include elementi quali finestre di dialogo, menu, stringhe, cursori, icone, bitmap e così via. Il compilatore di risorse è incluso Microsoft Visual Studio e Windows SDK.

Per altre informazioni, vedere [-resource (opzioni del compilatore C#)](../menurc/resource-compiler.md).

## <a name="user-interface-technologies-for-managed-applications"></a>Interfaccia utente tecnologie per le applicazioni gestite

Questa sezione descrive le tecnologie Microsoft per lo sviluppo di informazioni utente per applicazioni Windows gestite eseguite nel contesto del .NET Framework. Per altre informazioni, vedere [Sviluppo .NET.](/previous-versions/ff361664(v=vs.100))

### <a name="windows-forms"></a>Windows Forms

Windows Forms è un'interfaccia grafica di programmazione delle applicazioni per la creazione di applicazioni Windows gestite basate sul .NET Framework. In Windows Form un modulo è una superficie visiva in cui vengono visualizzate informazioni all'utente e tramite cui si riceve l'input dell'utente.

È possibile Windows applicazioni Form aggiungendo controlli ai moduli e sviluppando risposte alle azioni dell'utente, ad esempio clic del mouse o pressione del tasto. Un controllo è un elemento discreto dell'interfaccia utente che visualizza i dati o accetta l'input di dati. Windows Form contiene diversi controlli che possono essere inseriti nei form, ad esempio i controlli che visualizzano caselle di testo, pulsanti, caselle di riepilogo a discesa, pulsanti di opzione e persino pagine Web. Windows I form supportano anche la creazione di controlli personalizzati.

Per altre informazioni, vedere [Windows Forms.](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100))

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) è il successore di [Windows Form.](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)) WPF è un sistema di presentazione per la compilazione e il rendering di interfacce utente in applicazioni client basate su Windows e in applicazioni ospitate da browser. L'elemento principale di WPF è un motore di rendering vettoriale e indipendente dalla risoluzione compilato per sfruttare i vantaggi dei moderni componenti hardware grafici. Oltre a questo elemento principale, WPF offre un set completo di funzionalità per lo sviluppo di applicazioni che includono Extensible Application Markup Language (XAML), controlli, data binding, layout, grafica 2D e 3D, animazioni, stili, modelli, documenti, supporti, testo e tipografia.

WPF è incluso in .NET Framework, per consentire la compilazione di applicazioni che incorporano altri elementi della libreria di classi .NET Framework. WPF è supportato in Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2 ed è disponibile anche per Windows XP con Service Pack 2 (SP2) e Windows Server 2003.

Per altre informazioni, vedere [Windows Presentation Foundation](/dotnet/framework/wpf/).

### <a name="silverlight"></a>Silverlight

Microsoft Silverlight è una potente piattaforma di sviluppo per la creazione di applicazioni multimediali e applicazioni aziendali complesse per dispositivi Web, desktop e mobili.

In base al .NET Framework, il plug-in Silverlight gratuito funziona in più browser, dispositivi e sistemi operativi per portare nuova interattività sul Web. Con opzioni di layout e stile estese, protocolli di comunicazione potenti, accesso ai dati affidabile e supporto per l'interazione dell'utente e supporti ad alta definizione, Silverlight consente di creare esperienze dei clienti veloci, uniformi e visivamente avanzate. Le applicazioni Silverlight possono essere sviluppate rapidamente con Piattaforma Web Microsoft, Visual Studio ed Expression Studio.

Per altre informazioni, vedere [Microsoft Silverlight.](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95))

### <a name="expression-blend-3--sketchflow"></a>Expression Blend 3 + SketchFlow

Expression Blend 3 + SketchFlow è uno strumento visivo per la progettazione, la creazione di prototipi e la creazione di interfacce utente sofisticate per applicazioni Desktop e Web WPF e Silverlight. È possibile compilare un'applicazione disegnando forme, disegnando controlli quali pulsanti e caselle di riepilogo, facendo in modo che le parti dell'applicazione rispondano ai clic del mouse e ad altri input dell'utente e stilizzando tutto in modo univoco.

Per altre informazioni, vedere [Creazione di prototipi con SketchFlow.](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30))

### <a name="ui-automation-for-managed-applications"></a>Automazione interfaccia utente per le applicazioni gestite

Automazione interfaccia utente è un framework di accessibilità per Windows, disponibile in tutti i sistemi operativi che supportano WPF.

Automazione interfaccia utente consente l'accesso a livello di codice alla maggior parte degli elementi dell'interfaccia utente sul desktop, consentendo ai prodotti assistive technology come le utilità per la lettura dello schermo di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente con mezzi diversi dall'input standard. Automazione interfaccia utente consente anche agli script di test automatizzati di interagire con l'interfaccia utente.

Per altre informazioni, vedere [Automazione interfaccia utente per le applicazioni gestite.](/dotnet/framework/ui-automation/)

 

 