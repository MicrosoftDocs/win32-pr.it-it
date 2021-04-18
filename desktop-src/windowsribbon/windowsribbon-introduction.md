---
title: Introduzione al framework della barra multifunzione di Windows
description: Windows Ribbon Framework è un sofisticato sistema di presentazione dei comandi che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Barra multifunzione di Windows, Framework
- Barra multifunzione, Framework
- Barra multifunzione di Windows, informazioni
- Barra multifunzione, informazioni
- Barra multifunzione di Windows, componenti
- Barra multifunzione, componenti
- Barra multifunzione di Windows, visualizzazioni
- Barra multifunzione, visualizzazioni
- Barra multifunzione di Windows, architettura
- Barra multifunzione, architettura
- Barra multifunzione di Windows, API
- Barra multifunzione, API
- Barra multifunzione di Windows, sicurezza
- Barra multifunzione, sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac5c3acccf1c48a54f93b1752729067e63e4c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104568046"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Introduzione al framework della barra multifunzione di Windows

Windows Ribbon Framework è un sofisticato sistema di presentazione dei comandi che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.

-   [Nuovo paradigma di comando](#a-new-command-paradigm)
-   [Visualizzazioni](#views)
    -   [Visualizzazione della barra multifunzione](#the-ribbon-view)
    -   [Visualizzazione ContextPopup](#the-contextpopup-view)
-   [Architettura della barra multifunzione](#ribbon-architecture)
    -   [API della barra multifunzione](#the-ribbon-apis)
    -   [Sicurezza e privacy](#security-and-privacy)
    -   [Accessibilità e localizzazione](#accessibility-and-localization)
-   [Conclusione](#conclusion)
-   [Argomenti correlati](#related-topics)

## <a name="a-new-command-paradigm"></a>Nuovo paradigma di comando

Il Framework della barra multifunzione è una raccolta di API Microsoft Win32 che supportano un host di nuove funzionalità dell'interfaccia utente per gli sviluppatori Windows.

Questo framework completo di comandi dell'interfaccia utente moderna offre:

-   Implementazione semplificata per nuove applicazioni del Framework della barra multifunzione e migrazione semplice di applicazioni Win32 esistenti.
-   Aspetto e comportamento coerenti per tutte le applicazioni della barra multifunzione.
-   Conformità alle linee guida dell'interfaccia utente di Windows per un'esperienza di Windows di prima classe tramite gli standard di accessibilità, il supporto per lo stile di visualizzazione (tema), le regolazioni a contrasto elevato automatico e la consapevolezza dei punti per pollice (dpi).

Il Framework della barra multifunzione è costituito da due componenti principali dell'interfaccia utente:

-   Barra dei comandi della barra multifunzione, costituita dalla barra di accesso rapido (QAT) che espone ed evidenzia vari comandi della barra multifunzione come specificato dall'utente o dall'applicazione, nonché da una riga di tabulazione che contiene il menu dell'applicazione, le schede standard o contestuali e un pulsante?.
-   Sistema di menu di scelta rapida completo.

Una combinazione di XML dichiarativo e interfacce COM native viene utilizzata per separare la presentazione e le funzionalità di questi componenti.

## <a name="views"></a>Viste

I componenti principali dell'interfaccia utente del Framework della barra multifunzione, la barra dei comandi della barra multifunzione e il sistema del menu di scelta rapida, sono differenziati strutturalmente attraverso le *visualizzazioni*. Il Framework supporta due visualizzazioni: la visualizzazione della [**barra multifunzione**](windowsribbon-element-ribbon.md) e la visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) .

### <a name="the-ribbon-view"></a>Visualizzazione della barra multifunzione

L'interfaccia utente della visualizzazione della [**barra**](windowsribbon-element-ribbon.md) multifunzione è la caratteristica principale del Framework della barra multifunzione e fornisce l'esperienza utente di nuova generazione per la presentazione di comandi nelle applicazioni Windows.

La barra multifunzione è una barra dei comandi che espone le funzionalità principali di un'applicazione tramite una serie di schede nella parte superiore di una finestra dell'applicazione. È simile alla funzionalità e all'aspetto dell'interfaccia utente di Microsoft Office 2007 Fluent. La barra multifunzione fornisce un contrappunto intuitivo al processo di valutazione e di errore di individuazione dei comandi tipico dei sistemi di menu standard di Windows. Ottimizzato per migliorare l'efficienza e l'individuabilità, la barra multifunzione semplifica la ricerca, la comprensione e l'uso dei comandi con i clic del mouse e le sequenze di tasti minime attraverso un sistema di controlli standard, raccolte e anteprime in tempo reale.

Nell'immagine seguente viene illustrata l'implementazione del Framework della barra multifunzione in Paint per Windows 7.

![screenshot che illustra l'implementazione della barra multifunzione in Paint per Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>Visualizzazione ContextPopup

La visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) , tramite il controllo [popup del contesto](windowsribbon-controls-contextpopup.md) , fornisce un sistema di menu di scelta rapida più completo rispetto a quello disponibile con le applicazioni Windows precedenti. Un popup del contesto può essere distribuito solo a supporto di una barra multifunzione, un popup del contesto autonomo non è supportato dal framework della barra multifunzione.

## <a name="ribbon-architecture"></a>Architettura della barra multifunzione

A differenza del modello di sviluppo dell'interfaccia utente Windows tradizionale basato sul controllo, lo sviluppo dell'interfaccia utente di Windows Ribbon Framework è basato sul concetto più astratto di comandi. Concentrandosi sui comandi associati ai controlli, anziché sui controlli stessi, il Framework è in grado di regolare automaticamente l'interfaccia utente come richiesto in risposta allo stato di esecuzione dei comandi recuperato dall'applicazione host della barra multifunzione.

Un'applicazione che usa il Framework della barra multifunzione espone i comandi senza essere vincolati dai dettagli relativi alla rappresentazione del comando nell'interfaccia utente. Questa operazione viene a volte definita modello di interfaccia utente basata su finalità. Il [**tipo di comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), le relative proprietà e le relative risorse definiscono lo scopo del comando per l'applicazione. Ad esempio, l'input del mouse, l'input da tastiera o persino l'agitazione di un dispositivo giroscopico possono comportare l'esecuzione dello stesso comando. l'applicazione è interessata solo all'esecuzione del comando, non alla modalità di chiamata.

Il Framework della barra multifunzione offre questa flessibilità separando la funzionalità dalla presentazione con due strutture di sviluppo distinte, ovvero un linguaggio di markup basato su Extensible Application Markup Language (XAML) per dichiarare i controlli e il layout visivo di un'implementazione della barra multifunzione e interfacce basate su COM C++ per inizializzare il Framework e gestire gli eventi in fase di esecuzione. Questa distinzione consente a sviluppatori e progettisti di interfaccia utente di essere esclusivamente responsabili dell'aspetto di un'applicazione Ribbon, mentre la funzionalità di base rimane il dominio dei tecnici software.

Per ulteriori informazioni, vedere informazioni sui [comandi e sui controlli](windowsribbon-commandscontrols.md).

### <a name="the-ribbon-apis"></a>API della barra multifunzione

Le API della barra multifunzione forniscono le connessioni necessarie tra una visualizzazione e l'applicazione host della barra multifunzione. Queste API sono costituite dalle interfacce e dalle chiavi delle proprietà seguenti:

-   Set di interfacce COM implementate dal framework della barra multifunzione per eseguire i servizi dell'interfaccia utente.

    

    | Interfaccia                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Definisce i metodi per la funzionalità di base della vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Definisce i metodi che supportano la funzionalità di base delle visualizzazioni della [**barra multifunzione**](windowsribbon-element-ribbon.md) e [**ContextPopup**](windowsribbon-element-contextpopup.md) .                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Definisce i metodi per specificare le impostazioni e le proprietà per una visualizzazione della [**barra multifunzione**](windowsribbon-element-ribbon.md) .                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet****](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Definisce un metodo per il recupero del valore identificato da una chiave della proprietà. Questa interfaccia viene implementata dal framework della barra multifunzione e viene implementata anche dall'applicazione host per ogni elemento dell'oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) di una raccolta di elementi.<br/> Quando viene implementato dall'applicazione host, il metodo definito da questa interfaccia viene utilizzato per recuperare un valore della chiave della proprietà per l'elemento selezionato in [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).<br/> |
    | [IUICollection****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Definisce i metodi per modificare dinamicamente i controlli basati su raccolte, ad esempio le [raccolte](ribbon-controls-galleries.md)qat e basate su raccolte della barra multifunzione in fase di esecuzione.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Definisce il metodo per il recupero di un'immagine da visualizzare nell'interfaccia utente della barra multifunzione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Definisce il metodo factory per la creazione di un oggetto [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) .                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Set di interfacce COM implementate dall'applicazione host della barra multifunzione che il Framework chiama in risposta alle modifiche dell'interfaccia utente.

    

    | Interfaccia                                                                                  | Descrizione                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Definisce i metodi del punto di ingresso di callback dell'applicazione per il Framework della barra multifunzione.                               |
    | [IUICommandHandler****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Definisce i metodi per la raccolta di informazioni sui comandi e la gestione degli eventi di comando dal framework della barra multifunzione. |
    | [IUICollectionChangedEvent****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Definisce il metodo richiesto per gestire le modifiche apportate a una raccolta in fase di esecuzione.                                   |

    

     

-   Set di chiavi di proprietà che definiscono le proprietà dell'interfaccia utente di cui l'applicazione ha il controllo a livello di codice.

    

    | Tipo di chiave della proprietà                                                  | Descrizione                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Raccolta](windowsribbon-reference-properties-collection.md)    | Definisce le proprietà per i controlli basati su raccolte della barra multifunzione. |
    | [Selezione colori](windowsribbon-reference-properties-colorpicker.md) | Definisce le proprietà per i controlli selezione colori della barra multifunzione.     |
    | [Carattere](windowsribbon-reference-properties-fontcontrol.md)         | Definisce le proprietà per la barra multifunzione FontControl.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Definisce le proprietà globali per il Framework della barra multifunzione.      |
    | [Risorsa](windowsribbon-reference-properties-resource.md)        | Definisce le proprietà delle risorse della barra multifunzione.                      |
    | [Barra multifunzione](windowsribbon-reference-properties-ribbon.md)            | Definisce le proprietà di visualizzazione della barra multifunzione.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Definisce le proprietà per il contesto o lo stato del controllo della barra multifunzione.  |

    

     

### <a name="security-and-privacy"></a>Sicurezza e privacy

La DLL del Framework della barra multifunzione (uiribbon.dll) viene eseguita in-process e ha gli stessi privilegi dell'applicazione host. La barra multifunzione accetta solo le informazioni fornite dall'applicazione host come input o input dell'utente da controlli strettamente vincolati, ad esempio la casella combinata casella di selezione e modificabile.

Inoltre, il Framework non archivia in modo permanente le informazioni eccetto quelle fornite dall'applicazione host o raccolte (come autorizzato dall'utente finale) tramite il programma di esperienza utente Windows per il consenso esplicito.

### <a name="accessibility-and-localization"></a>Accessibilità e localizzazione

Per fornire un'interfaccia utente altamente accessibile, il Framework della barra multifunzione implementa Microsoft Active Accessibility. Popolando automaticamente le proprietà rilevanti di Microsoft Active Accessibility con informazioni valide e utili, il Framework riduce significativamente il carico degli sviluppatori per offrire un'esperienza inclusiva per tutti gli utenti.

Per altre informazioni sull'accessibilità nel framework della barra multifunzione, vedere [uso di Active Accessibility nell'interfaccia utente di Office Fluent di 2007](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Inoltre, il Framework della barra multifunzione è una funzionalità di Windows e, di conseguenza, è localizzato per tutte le lingue supportate da Windows. Gli sviluppatori, tuttavia, sono responsabili della localizzazione delle proprie risorse specifiche dell'applicazione.

## <a name="conclusion"></a>Conclusione

La barra multifunzione è una forma nuova e accattivante della presentazione dei comandi che gli sviluppatori, i progettisti e i progettisti di applicazioni devono considerare durante la progettazione e la compilazione di nuove applicazioni o l'aggiornamento di quelle esistenti.

Il [Forum di sviluppo della barra multifunzione di Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni che implementano il Framework della barra multifunzione di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](windowsribbon-schema.md)
</dt> <dt>

[Linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

