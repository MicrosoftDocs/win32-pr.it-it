---
title: Creazione di un'applicazione barra multifunzione
description: Il framework della barra multifunzione di Windows è costituito da due piattaforme di sviluppo distinte, ma dipendenti, un linguaggio di markup basato su Extensible Application Markup Language (XAML) per dichiarare i controlli e il relativo layout visivo e un set di interfacce basato su C++ Component Object Model (COM) per definire la funzionalità dei comandi e gli hook dell'applicazione. Questa divisione del lavoro all'interno dell'architettura del framework della barra multifunzione richiede che uno sviluppatore che voglia sfruttare le funzionalità avanzate dell'interfaccia utente offerte dal framework deve progettare e descrivere l'interfaccia utente nel markup e quindi usare le interfacce COM del framework della barra multifunzione per connettere il framework all'applicazione host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Windows barra multifunzione, creazione di applicazioni
- barra multifunzione, creazione di applicazioni
- Windows Barra multifunzione, roadmap
- Barra multifunzione, roadmap
- Windows barra multifunzione, markup
- barra multifunzione, markup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3cc3395b2fe53759152f5d0244c6546c08832bda190035a918af6049a99811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850027"
---
# <a name="creating-a-ribbon-application"></a>Creazione di un'applicazione barra multifunzione

Il framework della barra multifunzione Windows è costituito da due piattaforme di sviluppo distinte, ma dipendenti: un linguaggio di markup basato su Extensible Application Markup Language (XAML) per dichiarare i controlli e il relativo layout visivo e un set di interfacce basato su C++ Component Object Model (COM) per definire la funzionalità dei comandi e gli hook dell'applicazione. Questa divisione del lavoro all'interno dell'architettura del framework della barra multifunzione richiede che uno sviluppatore che voglia sfruttare le funzionalità avanzate dell'interfaccia utente offerte dal framework deve progettare e descrivere l'interfaccia utente nel markup e quindi usare le interfacce COM del framework della barra multifunzione per connettere il framework all'applicazione host.

-   [Roadmap della barra multifunzione](#ribbon-roadmap)
-   [Scrivere il markup](#write-the-markup)
    -   [Compilare il markup](#compile-the-markup)
-   [Compilare l'applicazione](#build-the-application)
    -   [Inizializzare la barra multifunzione](#initialize-the-ribbon)
    -   [Collegare il markup all'applicazione](#link-the-markup-to-the-application)
    -   [Compilare l'applicazione](#link-the-markup-to-the-application)
-   [Aggiornamenti ed esecuzioni in fase di esecuzione](#run-time-updates-and-executions)
-   [Supporto OLE](#ole-support)
-   [Argomenti correlati](#related-topics)

## <a name="ribbon-roadmap"></a>Roadmap della barra multifunzione

Gli aspetti visivi di un'applicazione barra multifunzione, ad esempio quali controlli vengono visualizzati e dove vengono posizionati, vengono dichiarati nel markup (vedere Dichiarazione di comandi e controlli con markup della barra [multifunzione).](windowsribbon-schema.md) La logica dei comandi dell'applicazione, ad esempio ciò che accade quando viene premuto un pulsante, viene implementata nel codice.

Il processo di implementazione di una barra multifunzione e incorporarlo in un'applicazione Windows richiede quattro attività di base: scrivere il markup, compilare il markup, scrivere il codice e compilare e collegare l'intera applicazione.

Il diagramma seguente illustra il flusso di lavoro per un'implementazione tipica della barra multifunzione.

![diagramma che mostra il flusso di lavoro per un'implementazione tipica della barra multifunzione.](images/overviews/ribbonroadmap.png)

Le sezioni seguenti descrivono questo processo in modo più dettagliato.

## <a name="write-the-markup"></a>Scrivere il markup

Dopo aver progettato l'interfaccia utente della barra multifunzione, la prima attività per uno sviluppatore di applicazioni è descrivere l'interfaccia utente con il markup della barra multifunzione.

> [!IMPORTANT]
> Il file dello schema di markup del framework della barra multifunzione, UICC.xsd, viene installato con Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4.0. Usando il percorso di installazione standard, il file si trova nella cartella Bin %ProgramFiles% Microsoft SDKs Windows version number dove molti editor XML possono fare riferimento a questo file per fornire suggerimenti e completamento \\ \\ \\ \[ \] \\ automatico.

 

I controlli della barra multifunzione, i comandi della barra multifunzione (gli elementi indipendenti dai controlli che forniscono la funzionalità di base per i controlli della barra multifunzione) e tutte le relazioni tra layout dei controlli e oggetti visivi vengono dichiarati nel markup. La struttura del markup della barra multifunzione evidenzia la distinzione tra i controlli barra multifunzione e i comandi tramite due gerarchie di nodi primarie: un albero [Comandi](windowsribbon-reference-elements-command.md) e risorse e [un](windowsribbon-reference-elements-view.md) albero Visualizzazioni.

Tutti i contenitori e le azioni esposti dalla barra multifunzione vengono dichiarati [nell'albero Comandi e](windowsribbon-reference-elements-command.md) risorse. Ogni elemento Command è associato a un set di risorse, come richiesto dalla progettazione dell'interfaccia utente.

Dopo aver creato i comandi per un'applicazione, dichiarare i controlli nell'albero [visualizzazioni](windowsribbon-reference-elements-view.md) e associare ogni controllo a un comando per esporre la funzionalità Comando. Il framework della barra multifunzione determina il posizionamento effettivo dei controlli in base alla gerarchia dei controlli dichiarata qui.

L'esempio di codice seguente illustra come dichiarare un controllo Button, con etichetta Exit application, e associarlo a un comando Exit.


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> Anche se è possibile usare qualsiasi estensione di file per il file di markup della barra multifunzione, .xml è l'estensione consigliata usata in tutta la documentazione.

 

### <a name="compile-the-markup"></a>Compilare il markup

Dopo la creazione, il file di markup della barra multifunzione deve essere compilato in un formato binario dal compilatore di markup della barra multifunzione UI Command Compiler (UICC), incluso in Windows Software Development Kit (SDK). Un riferimento a questo file binario viene passato al [**metodo IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante l'inizializzazione del framework della barra multifunzione dall'applicazione host.

UICC può essere eseguito direttamente da una finestra della riga di comando o aggiunto come "Istruzione di compilazione personalizzata" in Visual Studio.

L'immagine seguente mostra il compilatore di markup UICC nella Windows shell CMD di SDK 7.

![Screenshot che mostra uicc.exe in una finestra della riga di comando.](images/overviews/screenshot-intentcl-commandline.png)

L'immagine seguente mostra UICC aggiunto come istruzione di compilazione personalizzata in Visual Studio.

![Screenshot che mostra uicc.exe aggiunta come istruzione di compilazione personalizzata in Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

UICC genera tre file: una versione binaria del markup (BML), un'intestazione di definizione ID (file con estensione h) per esporre gli elementi di markup all'applicazione host della barra multifunzione e uno [script](../menurc/about-resource-files.md) di definizione delle risorse (file con estensione rc) per collegare le risorse immagine e stringa della barra multifunzione all'applicazione host in fase di compilazione.

Per altri dettagli sulla compilazione del markup del framework della barra multifunzione, vedere [Compilazione del markup della barra multifunzione.](windowsribbon-intentcl.md)

## <a name="build-the-application"></a>Compilare l'applicazione

Dopo che l'interfaccia utente preliminare per un'applicazione della barra multifunzione è stata progettata e implementata nel markup, è necessario scrivere il codice dell'applicazione che inizializza il framework, usa il markup e associa i comandi dichiarati nel markup ai gestori di comandi appropriati nell'applicazione.

> [!IMPORTANT]
>
> Poiché il framework della barra multifunzione è basato su COM, è consigliabile che i progetti barra multifunzione usino \_ l'operatore uuidof() per fare riferimento ai GUID per le interfacce del framework della barra \_ multifunzione (IID). Nei casi in cui non è possibile usare l'operatore uuidof(), ad esempio quando viene usato un compilatore non Microsoft o l'applicazione host è basata su C, gli IID devono essere definiti dall'applicazione perché non sono contenuti \_ \_ in uuid.lib.
>
> Se gli IID sono definiti dall'applicazione, è necessario usare i GUID specificati in UIRibbon.idl.
>
> UIRibbon.idl viene fornito come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) ed è disponibile nel percorso di installazione standard %ProgramFiles% Microsoft \\ SDKs \\ Windows \\ v7.0 \\ Include.

 

### <a name="initialize-the-ribbon"></a>Inizializzare la barra multifunzione

Il diagramma seguente illustra i passaggi necessari per implementare una semplice applicazione della barra multifunzione.

![diagramma che illustra i passaggi necessari per implementare una semplice implementazione della barra multifunzione.](images/overviews/initializationsteps.png)

I passaggi seguenti descrivono in dettaglio come implementare una semplice applicazione barra multifunzione.

1.  Cocreateinstance

    L'applicazione chiama la funzione Com CoCreateInstance standard con l'ID di classe del framework della barra multifunzione per ottenere un puntatore al framework.

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  Initialize(hwnd, IUIApplication \* )

    L'applicazione chiama [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)passando due parametri: l'handle alla finestra di primo livello che conterrà la barra multifunzione e un puntatore all'implementazione [**di IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) che consente al framework di eseguire callback all'applicazione.

    > \[! Importante\]  
    > Il framework della barra multifunzione viene inizializzato come apartment a thread singolo (STA).

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI(instance, resourceName)

    L'applicazione chiama [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) per associare la risorsa di markup. Il primo parametro di questa funzione è un handle per l'istanza dell'applicazione della barra multifunzione. Il secondo parametro è il nome della risorsa di markup binario compilata in precedenza. Passando il markup binario al framework della barra multifunzione, l'applicazione segnala che cos'è la struttura della barra multifunzione e come devono essere disposti i controlli. Fornisce inoltre al framework un manifesto dei comandi da esporre (ad esempio Incolla, Taglia, Trova), che vengono usati dal framework quando esegue callback correlati al comando in fase di esecuzione.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  Callback [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

    Al termine dei passaggi da 1 a 3, il framework della barra multifunzione sa quali comandi esporre nella barra multifunzione. Tuttavia, il framework necessita ancora di due elementi prima che la barra multifunzione sia completamente funzionante: un modo per indicare all'applicazione quando vengono eseguiti i comandi e un modo per ottenere le risorse di comando, o le proprietà, in fase di esecuzione. Ad esempio, se una casella combinata deve essere visualizzata nell'interfaccia utente, il framework deve richiedere gli elementi con cui popolare la casella combinata.

    Queste due funzionalità vengono gestite tramite [**l'interfaccia IUICommandHandler.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) In particolare, per ogni comando dichiarato nel markup binario (vedere il passaggio 3 precedente), il framework chiama [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) per chiedere all'applicazione un oggetto **IUICommandHandler** per tale comando

    > [!Note]  
    > [**L'interfaccia IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) consente a un gestore command di essere associato a uno o più comandi.

     

Come minimo, l'applicazione è necessaria per implementare stub di metodi [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) che restituiscono E \_ NOTIMPL, come illustrato nell'esempio seguente.


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a>Collegare il markup all'applicazione

A questo punto, i file di risorse di markup devono essere collegati all'applicazione host includendo un riferimento al file di definizione delle risorse di markup (che contiene un riferimento al file di intestazione del markup) nel file di risorse dell'applicazione. Ad esempio, un'applicazione denominata RibbonApp con un file di risorse denominato ribbonUI.rc richiede la riga seguente nel file RibbonApp.rc.


```C++
#include "ribbonUI.rc"
```



A seconda del compilatore e del linker in uso, lo script di definizione delle risorse può richiedere anche la compilazione prima di poter compilare l'applicazione della barra multifunzione. Per questa attività è possibile usare lo strumento da riga di comando del compilatore di risorse [(RC)](../menurc/using-rc-the-rc-command-line-.md) fornito con Microsoft Visual Studio e Windows SDK.

### <a name="compile-the-application"></a>Compilare l'applicazione

Dopo aver compilato l'applicazione della barra multifunzione, è possibile eseguirla e testare l'interfaccia utente. Se l'interfaccia utente richiede modifiche e non sono presenti modifiche ai gestori command associati nel codice dell'applicazione principale, modificare il file di origine del markup, ricompilare il markup con UICC.exe e collegare i nuovi file di risorse di markup. Quando l'applicazione viene riavviata, viene visualizzata l'interfaccia utente modificata.

Tutto questo è possibile senza toccare il codice principale dell'applicazione, un miglioramento significativo rispetto allo sviluppo e alla distribuzione standard delle applicazioni.

## <a name="run-time-updates-and-executions"></a>Aggiornamenti ed esecuzioni in fase di esecuzione

La struttura di comunicazione in fase di esecuzione del framework della barra multifunzione si basa su un modello push e pull, o chiamante bidirezionale.

Questo modello consente al framework di informare l'applicazione quando viene eseguito un comando e consente sia al framework che all'applicazione di eseguire query, aggiornare e invalidare i valori delle proprietà e le risorse della barra multifunzione. Questa funzionalità viene fornita tramite una serie di interfacce e metodi.

Il framework esegue il pull delle informazioni sulle proprietà aggiornate dall'applicazione della barra multifunzione tramite il metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) Un ID comando e una chiave di proprietà, che identifica la proprietà Command da aggiornare, vengono passati al metodo che restituisce o esegue il push di un valore per tale chiave di proprietà nel framework.

Il framework chiama [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando viene eseguito un comando, identificando sia l'ID comando che il tipo di esecuzione che si è verificato ([**\_ UI EXECUTIONVERB).**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) Qui l'applicazione specifica la logica di esecuzione per un comando.

Il diagramma seguente illustra la comunicazione in fase di esecuzione per l'esecuzione di comandi tra il framework e l'applicazione.

![diagramma che mostra un esempio di comunicazione in fase di esecuzione tra il framework della barra multifunzione e un'applicazione host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> L'implementazione [**delle funzioni IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) e [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) non è necessaria per visualizzare inizialmente una barra multifunzione in un'applicazione. Tuttavia, questi metodi sono necessari per garantire che l'applicazione funzioni correttamente quando i comandi vengono eseguiti dall'utente.

 

## <a name="ole-support"></a>Supporto OLE

Un'applicazione barra multifunzione può essere configurata come server OLE per supportare l'attivazione OLE sul posto.

Gli oggetti creati in un'applicazione server OLE mantengono l'associazione con l'applicazione server quando vengono inseriti (incollati o inseriti) in un'applicazione client OLE (o contenitore). Nell'attivazione OLE sul posto, facendo doppio clic sull'oggetto nell'applicazione client viene aperta un'istanza dedicata dell'applicazione server e viene caricato l'oggetto per la modifica. Quando l'applicazione server viene chiusa, tutte le modifiche apportate all'oggetto vengono riflesse nell'applicazione client.

> [!Note]  
> Il framework della barra multifunzione non supporta l'attivazione OLE sul posto. Gli oggetti creati in un server OLE basato sulla barra multifunzione non possono essere modificati dall'interno dell'applicazione client OLE. È necessaria un'istanza esterna dedicata dell'applicazione server.


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](./windowsribbon-schema.md)
</dt> <dt>

[Linee guida per l'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




