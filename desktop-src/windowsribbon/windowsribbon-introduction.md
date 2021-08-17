---
title: Introduzione al framework Windows ribbon
description: Visualizzare la pagina di destinazione per il framework della barra multifunzione Windows, un'alternativa ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows Barra multifunzione, framework
- Barra multifunzione, framework
- Windows Barra multifunzione, informazioni su
- Barra multifunzione, informazioni su
- Windows Barra multifunzione, componenti
- Barra multifunzione, componenti
- Windows Barra multifunzione, visualizzazioni
- Barra multifunzione, visualizzazioni
- Windows Barra multifunzione, architettura
- Barra multifunzione, architettura
- Windows Barra multifunzione, API
- Barra multifunzione, API
- Windows Barra multifunzione, sicurezza
- Barra multifunzione, sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65576d90abb68b0efddf850f4855633f4b362d8cb21ce6f6f85f7924085e8810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850644"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Introduzione al framework Windows ribbon

Il framework Windows della barra multifunzione è un sistema di presentazione dei comandi ricco che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.

-   [Un nuovo paradigma di comando](#a-new-command-paradigm)
-   [Visualizzazioni](#views)
    -   [Visualizzazione barra multifunzione](#the-ribbon-view)
    -   [Visualizzazione ContextPopup](#the-contextpopup-view)
-   [Architettura della barra multifunzione](#ribbon-architecture)
    -   [API della barra multifunzione](#the-ribbon-apis)
    -   [Sicurezza e privacy](#security-and-privacy)
    -   [Accessibilità e localizzazione](#accessibility-and-localization)
-   [Conclusione](#conclusion)
-   [Argomenti correlati](#related-topics)

## <a name="a-new-command-paradigm"></a>Un nuovo paradigma di comando

Il framework della barra multifunzione è una raccolta di API Win32 Microsoft che supportano una serie di nuove funzionalità dell'interfaccia utente per Windows sviluppatori.

Questo framework di comandi dell'interfaccia utente moderno offre:

-   Implementazione semplice per le nuove applicazioni del framework ribbon e migrazione semplice delle applicazioni Win32 esistenti.
-   Aspetto e comportamento coerenti tra le applicazioni della barra multifunzione.
-   Conformità alle linee guida Windows'interfaccia utente per un'esperienza Windows di prima classe tramite standard di accessibilità, supporto dello stile di visualizzazione (tema), regolazioni automatiche del contrasto elevato e riconoscimento di punti per pollice (dpi) elevati.

Il framework della barra multifunzione è costituito da due componenti principali dell'interfaccia utente:

-   La barra dei comandi della barra multifunzione, costituita dalla barra di accesso rapido che espone ed evidenzia vari comandi della barra multifunzione, come specificato dall'utente o dall'applicazione, e da una riga di scheda contenente il menu dell'applicazione, le schede standard o contestuali e un pulsante della Guida.
-   Un sistema di menu di scelta rapida ricco.

Una combinazione di interfacce COM native e XML dichiarative viene usata per separare la presentazione e la funzionalità di questi componenti.

## <a name="views"></a>Viste

I componenti principali dell'interfaccia utente del framework della barra multifunzione, la barra dei comandi della barra multifunzione e il sistema di menu di scelta rapida, sono differenziati strutturalmente tramite *Visualizzazioni*. Il framework supporta due visualizzazioni: la [**visualizzazione barra**](windowsribbon-element-ribbon.md) multifunzione e la [**visualizzazione ContextPopup.**](windowsribbon-element-contextpopup.md)

### <a name="the-ribbon-view"></a>Visualizzazione barra multifunzione

L'interfaccia [**utente**](windowsribbon-element-ribbon.md) della visualizzazione barra multifunzione è la funzionalità principale del framework della barra multifunzione e offre l'esperienza utente di nuova generazione per la presentazione di comandi nelle Windows applicazioni.

La barra multifunzione è una barra dei comandi che espone le principali funzionalità di un'applicazione tramite una serie di schede nella parte superiore di una finestra dell'applicazione. È simile per funzionalità e aspetto all'interfaccia Microsoft Office 2007 Fluent 2007. La barra multifunzione offre un punto di contrasto intuitivo al processo di valutazione ed errore dell'individuazione dei comandi tipico dei sistemi di menu Windows standard. Ottimizzata per l'efficienza e l'individuabilità, la barra multifunzione facilita la ricerca, la comprensione e l'uso dei comandi con un numero minimo di clic del mouse e sequenze di tasti tramite un sistema di controlli standard, raccolte e anteprima live.

L'immagine seguente illustra l'implementazione del framework della barra multifunzione in Paint per Windows 7.

![Screenshot che mostra l'implementazione della barra multifunzione in paint per Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>Visualizzazione ContextPopup

La [**visualizzazione ContextPopup,**](windowsribbon-element-contextpopup.md) tramite il controllo [Popup](windowsribbon-controls-contextpopup.md) di contesto, fornisce un sistema di menu di scelta rapida più completo rispetto a quello disponibile con le applicazioni Windows precedenti. Un popup di contesto può essere distribuito solo in supporto di una barra multifunzione, un popup di contesto autonomo non è supportato dal framework della barra multifunzione.

## <a name="ribbon-architecture"></a>Architettura della barra multifunzione

A differenza del modello di sviluppo dell'interfaccia utente basato su controlli Windows, lo sviluppo dell'interfaccia utente del framework della barra multifunzione Windows è basato sul concetto più astratto di Comandi. Concentrandosi sui comandi associati ai controlli, anziché sui controlli stessi, il framework è in grado di regolare automaticamente l'interfaccia utente in base alle esigenze in risposta allo stato di esecuzione del comando recuperato dall'applicazione host della barra multifunzione.

Un'applicazione che usa il framework della barra multifunzione espone i comandi senza essere ingombrati con i dettagli del modo in cui tale comando viene rappresentato nell'interfaccia utente. Questo modello viene talvolta definito modello di interfaccia utente basato sulle finalità. Il [**tipo di comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), le relative proprietà e le relative risorse definiscono la finalità del comando per l'applicazione. Ad esempio, l'input del mouse, l'input da tastiera o persino l'agitazione di un dispositivo giroscopico può comportare l'esecuzione dello stesso comando che l'applicazione è interessata solo all'esecuzione del comando, non al modo in cui è stato richiamato.

Il framework della barra multifunzione offre questa flessibilità separando la funzionalità dalla presentazione con due strutture di sviluppo distinte: un linguaggio di markup basato su Extensible Application Markup Language (XAML) per dichiarare i controlli e il layout visivo di un'implementazione della barra multifunzione e interfacce basate su COM C++ per inizializzare il framework e gestire gli eventi in fase di esecuzione. Questa distinzione consente agli sviluppatori e ai progettisti dell'interfaccia utente di essere esclusivamente responsabili dell'aspetto di un'applicazione barra multifunzione, mentre le funzionalità di base rimangono il dominio dei tecnici software.

Per altre informazioni, vedere [Informazioni su comandi e controlli](windowsribbon-commandscontrols.md).

### <a name="the-ribbon-apis"></a>API della barra multifunzione

Le API della barra multifunzione forniscono le connessioni necessarie tra una visualizzazione e l'applicazione host della barra multifunzione. Queste API sono costituite da interfacce e chiavi di proprietà seguenti:

-   Set di interfacce COM implementate dal framework della barra multifunzione per eseguire i servizi dell'interfaccia utente.

    

    | Interfaccia                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Definisce i metodi per la funzionalità principale della [**visualizzazione ContextPopup.**](windowsribbon-element-contextpopup.md)                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Definisce i metodi che supportano le funzionalità principali della barra [**multifunzione**](windowsribbon-element-ribbon.md) e [**delle visualizzazioni ContextPopup.**](windowsribbon-element-contextpopup.md)                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Definisce i metodi per specificare le impostazioni e le proprietà per una [**visualizzazione barra**](windowsribbon-element-ribbon.md) multifunzione.                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet****](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Definisce un metodo per recuperare il valore identificato da una chiave di proprietà. Questa interfaccia viene implementata dal framework della barra multifunzione e viene implementata anche dall'applicazione host per ogni elemento nell'oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) di una raccolta di elementi.<br/> Quando viene implementato dall'applicazione host, il metodo definito da questa interfaccia viene usato per recuperare un valore della chiave di proprietà per l'elemento selezionato in [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).<br/> |
    | [IUICollection****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Definisce i metodi per la modifica dinamica dei controlli basati su raccolta, ad esempio la QAT della barra multifunzione e [le raccolte](ribbon-controls-galleries.md)basate su raccolta, in fase di esecuzione.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Definisce il metodo per recuperare un'immagine da visualizzare nell'interfaccia utente della barra multifunzione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Definisce il metodo factory per la creazione di un [**oggetto IUIImage.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Set di interfacce COM implementate dall'applicazione host della barra multifunzione che il framework chiama in risposta alle modifiche dell'interfaccia utente.

    

    | Interfaccia                                                                                  | Descrizione                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Definisce i metodi del punto di ingresso di callback dell'applicazione per il framework della barra multifunzione.                               |
    | [IUICommandHandler****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Definisce i metodi per la raccolta di informazioni sui comandi e la gestione degli eventi Command dal framework della barra multifunzione. |
    | [IUICollectionChangedEvent****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Definisce il metodo necessario per gestire le modifiche a una raccolta in fase di esecuzione.                                   |

    

     

-   Set di chiavi di proprietà che definiscono le proprietà dell'interfaccia utente su cui l'applicazione ha il controllo a livello di codice.

    

    | Tipo di chiave di proprietà                                                  | Descrizione                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Raccolta](windowsribbon-reference-properties-collection.md)    | Definisce le proprietà per i controlli basati su raccolta della barra multifunzione. |
    | [Selezione colori](windowsribbon-reference-properties-colorpicker.md) | Definisce le proprietà per i controlli selezione colori della barra multifunzione.     |
    | [Font](windowsribbon-reference-properties-fontcontrol.md)         | Definisce le proprietà per l'oggetto FontControl della barra multifunzione.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Definisce le proprietà globali per il framework della barra multifunzione.      |
    | [Risorsa](windowsribbon-reference-properties-resource.md)        | Definisce le proprietà delle risorse della barra multifunzione.                      |
    | [Barra multifunzione](windowsribbon-reference-properties-ribbon.md)            | Definisce le proprietà della visualizzazione barra multifunzione.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Definisce le proprietà per lo stato o il contesto del controllo Barra multifunzione.  |

    

     

### <a name="security-and-privacy"></a>Sicurezza e privacy

La DLL del framework della barra multifunzione (uiribbon.dll) viene eseguita in-process e ha gli stessi privilegi dell'applicazione host. La barra multifunzione accetta solo ciò che l'applicazione host fornisce come input o input utente da controlli strettamente vincolati, ad esempio la casella di selezione e la casella combinata modificabile.

Inoltre, il framework non archivia in modo permanente tutte le informazioni tranne quelle fornite dall'applicazione host o raccolte (come autorizzato dall'utente finale) tramite il programma Windows Customer Experience Program.

### <a name="accessibility-and-localization"></a>Accessibilità e localizzazione

Per fornire un'interfaccia utente altamente accessibile, il framework della barra multifunzione implementa Microsoft Active Accessibility. Popolando automaticamente le proprietà Microsoft Active Accessibility con informazioni valide e utili, il framework riduce significativamente l'onere per gli sviluppatori di offrire un'esperienza inclusiva a tutti gli utenti.

Per altre informazioni sull'accessibilità nel framework della barra multifunzione, vedere Working [with Active Accessibility in the 2007 Office Fluent Interfaccia utente](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Inoltre, il framework della barra multifunzione è Windows funzionalità e, di conseguenza, è localizzato per tutte le lingue supportate Windows. Gli sviluppatori, tuttavia, sono responsabili della localizzazione delle proprie risorse dell'applicazione specifiche.

## <a name="conclusion"></a>Conclusione

La barra multifunzione è una nuova e coinvolgente forma di presentazione dei comandi che sviluppatori, architetti e progettisti di applicazioni devono prendere in considerazione quando si progettano e compilano nuove applicazioni o si aggiornano quelle esistenti.

Il [Windows di sviluppo della](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) barra multifunzione è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni che implementano il framework Windows Ribbon.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](windowsribbon-schema.md)
</dt> <dt>

[Linee guida per l'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

