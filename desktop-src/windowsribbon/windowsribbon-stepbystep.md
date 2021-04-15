---
title: Creazione di un'applicazione Ribbon
description: Il Framework della barra multifunzione di Windows è costituito da due piattaforme di sviluppo distinte, ma dipendenti, un linguaggio di markup basato su Extensible Application Markup Language (XAML) per dichiarare controlli e il relativo layout visivo e un set di interfacce basato su C++ Component Object Model (COM) per definire la funzionalità del comando e gli hook dell'applicazione. Questa divisione del lavoro all'interno dell'architettura del Framework della barra multifunzione richiede che uno sviluppatore che desidera sfruttare le funzionalità dell'interfaccia utente avanzate offerte dal Framework debba progettare e descrivere l'interfaccia utente nel markup, quindi utilizzare le interfacce COM del Framework della barra multifunzione per connettere il Framework all'applicazione host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Barra multifunzione di Windows, creazione di applicazioni
- Barra multifunzione, creazione di applicazioni
- Barra multifunzione di Windows, roadmap
- Barra multifunzione, roadmap
- Barra multifunzione di Windows, markup
- Barra multifunzione, markup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399448"
---
# <a name="creating-a-ribbon-application"></a>Creazione di un'applicazione Ribbon

Il Framework della barra multifunzione di Windows è costituito da due piattaforme di sviluppo distinte e dipendenti, ovvero un linguaggio di markup basato su Extensible Application Markup Language (XAML) per dichiarare controlli e il relativo layout visivo e un set di interfacce basato su C++ Component Object Model (COM) per definire le funzionalità dei comandi e gli hook dell'applicazione. Questa divisione del lavoro all'interno dell'architettura del Framework della barra multifunzione richiede che uno sviluppatore che desidera sfruttare le funzionalità dell'interfaccia utente avanzate offerte dal Framework debba progettare e descrivere l'interfaccia utente nel markup, quindi utilizzare le interfacce COM del Framework della barra multifunzione per connettere il Framework all'applicazione host.

-   [Roadmap della barra multifunzione](#ribbon-roadmap)
-   [Scrivere il markup](#write-the-markup)
    -   [Compilare il markup](#compile-the-markup)
-   [Compilare l'applicazione](#build-the-application)
    -   [Inizializza la barra multifunzione](#initialize-the-ribbon)
    -   [Collegare il markup all'applicazione](#link-the-markup-to-the-application)
    -   [Compilare l'applicazione](#link-the-markup-to-the-application)
-   [Aggiornamenti ed esecuzioni in fase di esecuzione](#run-time-updates-and-executions)
-   [Supporto OLE](#ole-support)
-   [Argomenti correlati](#related-topics)

## <a name="ribbon-roadmap"></a>Roadmap della barra multifunzione

Gli aspetti visivi di un'applicazione Ribbon, ad esempio i controlli visualizzati e la posizione in cui vengono inseriti, vengono dichiarati nel markup (vedere [dichiarazione di comandi e controlli con markup della barra multifunzione](windowsribbon-schema.md)). La logica del comando dell'applicazione, ad esempio cosa accade quando viene premuto un pulsante, viene implementata nel codice.

Il processo di implementazione di una barra multifunzione e di incorporarlo in un'applicazione Windows richiede quattro attività di base: scrivere il markup, compilare il markup, scrivere il codice e compilare e collegare l'intera applicazione.

Il diagramma seguente illustra il flusso di lavoro per una tipica implementazione della barra multifunzione.

![diagramma che illustra il flusso di lavoro per una tipica implementazione della barra multifunzione.](images/overviews/ribbonroadmap.png)

Le sezioni seguenti descrivono questo processo in modo più dettagliato.

## <a name="write-the-markup"></a>Scrivere il markup

Una volta progettata l'interfaccia utente della barra multifunzione, la prima attività per uno sviluppatore di applicazioni consiste nel descrivere l'interfaccia utente con il markup della barra multifunzione.

> [!IMPORTANT]
> Il file dello schema di markup del Framework della barra multifunzione, UICC. xsd, viene installato con Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4,0. Utilizzando il percorso di installazione standard, il file si trova nella cartella% ProgramFiles% \\ Microsoft \\ SDK \\ \[ numero versione Windows \] \\ bin a cui è possibile fare riferimento da molti editor XML per fornire suggerimenti e completamento automatico.

 

Controlli della barra multifunzione, comandi della barra multifunzione (elementi indipendenti dal controllo che forniscono la funzionalità di base per i controlli della barra multifunzione) e tutti i layout di controllo e le relazioni visive sono dichiarati nel La struttura del markup della barra multifunzione enfatizza la distinzione tra i controlli della barra multifunzione e i comandi attraverso due gerarchie di nodi primari: un albero di [comandi e risorse](windowsribbon-reference-elements-command.md) e una struttura di [visualizzazioni](windowsribbon-reference-elements-view.md) .

Tutti i contenitori e le azioni esposti dalla barra multifunzione sono dichiarati nell'albero [comandi e risorse](windowsribbon-reference-elements-command.md) . Ogni elemento Command è associato a un set di risorse, come richiesto dalla progettazione dell'interfaccia utente.

Dopo aver creato i comandi per un'applicazione, è necessario dichiarare i controlli nell'albero delle [visualizzazioni](windowsribbon-reference-elements-view.md) e associare ogni controllo a un comando per esporre la funzionalità del comando. Il Framework della barra multifunzione determina il posizionamento effettivo dei controlli in base alla gerarchia dei controlli dichiarata qui.

Nell'esempio di codice riportato di seguito viene illustrato come dichiarare un controllo Button, con etichetta Exit Application e come associarlo a un comando Exit.


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
> Sebbene sia possibile utilizzare qualsiasi estensione di file per il file di markup della barra multifunzione, XML è l'estensione consigliata utilizzata nella documentazione.

 

### <a name="compile-the-markup"></a>Compilare il markup

Dopo aver creato il file di markup della barra multifunzione, è necessario compilarlo in un formato binario tramite il compilatore di markup della barra multifunzione, il compilatore di comandi dell'interfaccia utente (UICC), incluso in Windows Software Development Kit (SDK). Un riferimento a questo file binario viene passato al metodo [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante l'inizializzazione del Framework della barra multifunzione dall'applicazione host.

UICC può essere eseguito direttamente da una finestra della riga di comando o aggiunto come "passaggio di compilazione personalizzato" in Visual Studio.

La figura seguente mostra il compilatore di markup UICC nella finestra della shell CMD di Windows 7 SDK.

![screenshot che mostra uicc.exe in una finestra della riga di comando.](images/overviews/screenshot-intentcl-commandline.png)

La figura seguente mostra UICC aggiunto come un'istruzione di compilazione personalizzata in Visual Studio.

![screenshot che mostra uicc.exe aggiunto come istruzione di compilazione personalizzata in Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

UICC genera tre file: una versione binaria del markup (. BML), un'intestazione di definizione ID (file h) per esporre gli elementi di markup all'applicazione host della barra multifunzione e uno [script di definizione delle risorse](../menurc/about-resource-files.md) (file RC) per collegare le risorse di tipo stringa e immagine della barra multifunzione all'applicazione host in fase di compilazione.

Per informazioni più dettagliate sulla compilazione del markup del Framework della barra multifunzione, vedere [compilazione del markup della barra](windowsribbon-intentcl.md)multifunzione.

## <a name="build-the-application"></a>Compilare l'applicazione

Una volta che l'interfaccia utente preliminare per un'applicazione Ribbon è stata progettata e implementata nel markup, è necessario scrivere il codice dell'applicazione che inizializza il Framework, usa il markup e associa i comandi dichiarati nel markup ai gestori di comandi appropriati nell'applicazione.

> [!IMPORTANT]
>
> Poiché il Framework della barra multifunzione è basato su COM, è consigliabile che i progetti Ribbon usino l' \_ \_ operatore uuidof () per fare riferimento ai GUID per le interfacce del Framework della barra multifunzione (IID). Nei casi in cui non è possibile usare l' \_ \_ operatore uuidof (), ad esempio quando viene usato un compilatore non Microsoft o l'applicazione host è basata su C, il IID deve essere definito dall'applicazione perché non è contenuto in UUID. lib.
>
> Se i IID sono definiti dall'applicazione, è necessario usare i GUID specificati in UIRibbon. idl.
>
> UIRibbon. idl viene fornito come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) e si trova nel percorso di installazione standard di% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ include.

 

### <a name="initialize-the-ribbon"></a>Inizializza la barra multifunzione

Il diagramma seguente illustra i passaggi necessari per implementare una semplice applicazione della barra multifunzione.

![diagramma che illustra i passaggi necessari per implementare una semplice implementazione della barra multifunzione.](images/overviews/initializationsteps.png)

I passaggi seguenti descrivono in dettaglio come implementare una semplice applicazione della barra multifunzione.

1.  CoCreateInstance

    L'applicazione chiama la funzione standard COM CoCreateInstance con l'ID classe del Framework della barra multifunzione per ottenere un puntatore al Framework.

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

    

2.  Initialize (HWND, IUIApplication \* )

    L'applicazione chiama [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passando due parametri: l'handle per la finestra di primo livello che conterrà la barra multifunzione e un puntatore all'implementazione di [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) che consente al Framework di eseguire i callback all'applicazione.

    > \[! Importante\]  
    > Il Framework della barra multifunzione viene inizializzato come un Apartment a thread singolo (STA).

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI (istanza, resourceName)

    L'applicazione chiama [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) per associare la risorsa di markup. Il primo parametro di questa funzione è un handle per l'istanza dell'applicazione Ribbon. Il secondo parametro è il nome della risorsa di markup binario che è stata compilata in precedenza. Passando il markup binario al framework della barra multifunzione, l'applicazione segnala la struttura della barra multifunzione e il modo in cui devono essere disposti i controlli. Fornisce inoltre al Framework un manifesto di comandi da esporre, ad esempio incolla, taglia, trova, che vengono utilizzati dal framework quando vengono eseguiti callback correlati al comando in fase di esecuzione.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  Callback [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

    Una volta completati i passaggi da 1 a 3, il Framework della barra multifunzione sa quali comandi esporre nella barra multifunzione. Tuttavia, il Framework necessita ancora di due elementi prima che la barra multifunzione sia completamente funzionante: un modo per indicare all'applicazione quando vengono eseguiti i comandi e un modo per ottenere le risorse o le proprietà del comando in fase di esecuzione. Se, ad esempio, una casella combinata viene visualizzata nell'interfaccia utente, il Framework deve richiedere gli elementi con cui popolare la casella combinata.

    Queste due parti di funzionalità vengono gestite tramite l'interfaccia [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) . In particolare, per ogni comando dichiarato nel markup binario (vedere il passaggio 3 precedente), il Framework chiama [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) per chiedere all'applicazione un oggetto **IUICommandHandler** per tale comando

    > [!Note]  
    > L'interfaccia [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) consente di associare un gestore di comando a uno o più comandi.

     

Come minimo, l'applicazione deve implementare gli stub dei metodi [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) che restituiscono E \_ NOTIMPL, come illustrato nell'esempio seguente.


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

A questo punto, i file di risorse di markup devono essere collegati all'applicazione host includendo un riferimento al file di definizione delle risorse di markup, che contiene un riferimento al file di intestazione di markup, nel file di risorse dell'applicazione. Ad esempio, un'applicazione denominata RibbonApp con un file di risorse denominato ribbonUI. RC richiede la riga seguente nel file RibbonApp. RC.


```C++
#include "ribbonUI.rc"
```



A seconda del compilatore e del linker utilizzati, è possibile che anche lo script di definizione della risorsa richieda la compilazione prima che l'applicazione Ribbon possa essere compilata. Lo strumento da riga di comando del [compilatore di risorse (RC)](../menurc/using-rc-the-rc-command-line-.md) fornito con Microsoft Visual Studio e il Windows SDK può essere utilizzato per questa attività.

### <a name="compile-the-application"></a>Compilare l'applicazione

Una volta compilata l'applicazione Ribbon, è possibile eseguirla e testare l'interfaccia utente. Se l'interfaccia utente richiede la modifica e non vi sono modifiche ai gestori di comandi associati nel codice dell'applicazione principale, modificare il file di origine di markup, ricompilare il markup con UICC.exe e collegare i nuovi file di risorse di markup. Quando l'applicazione viene riavviata, viene visualizzata l'interfaccia utente modificata.

Tutto questo è possibile senza modificare il codice dell'applicazione principale, ovvero un miglioramento significativo dello sviluppo e della distribuzione di applicazioni standard.

## <a name="run-time-updates-and-executions"></a>Aggiornamenti ed esecuzioni in fase di esecuzione

La struttura di comunicazione in fase di esecuzione del Framework della barra multifunzione è basata su un modello di push e pull o di un chiamante bidirezionale.

Questo modello consente al Framework di informare l'applicazione quando viene eseguito un comando e consente al Framework e all'applicazione di eseguire query, aggiornare e invalidare i valori delle proprietà e le risorse della barra multifunzione. Questa funzionalità viene fornita tramite una serie di interfacce e metodi.

Il Framework esegue il pull delle informazioni aggiornate sulla proprietà dall'applicazione Ribbon tramite il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) . Un ID di comando e una chiave di proprietà, che identifica la proprietà del comando da aggiornare, vengono passati al metodo che quindi restituisce, o effettua il push, un valore per la chiave della proprietà nel Framework.

Il Framework chiama [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando viene eseguito un comando, identificando sia l'ID del comando sia il tipo di esecuzione che si è verificata ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)). Questo è il punto in cui l'applicazione specifica la logica di esecuzione per un comando.

Il diagramma seguente illustra la comunicazione di run-time per l'esecuzione dei comandi tra il Framework e l'applicazione.

![diagramma che mostra un esempio della comunicazione di run-time tra il Framework della barra multifunzione e un'applicazione host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> L'implementazione delle funzioni [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) e [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) non è necessaria per visualizzare inizialmente una barra multifunzione in un'applicazione. Tuttavia, questi metodi sono necessari per garantire che l'applicazione funzioni correttamente quando i comandi vengono eseguiti dall'utente.

 

## <a name="ole-support"></a>Supporto OLE

Un'applicazione Ribbon può essere configurata come server OLE per supportare l'attivazione OLE fuori sede.

Gli oggetti creati in un'applicazione server OLE mantengono l'associazione con l'applicazione server quando vengono inseriti (incollati o posizionati) in un'applicazione client OLE (o contenitore). Nell'attivazione OLE fuori sede, facendo doppio clic sull'oggetto nell'applicazione client viene aperta un'istanza dedicata dell'applicazione server e viene caricato l'oggetto per la modifica. Quando l'applicazione server viene chiusa, tutte le modifiche apportate all'oggetto vengono riflesse nell'applicazione client.

> [!Note]  
> Il Framework della barra multifunzione non supporta l'attivazione OLE sul posto. Impossibile modificare gli oggetti creati in un server OLE basato su barra multifunzione dall'interno dell'applicazione client OLE. È necessaria un'istanza esterna dedicata dell'applicazione server.


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](./windowsribbon-schema.md)
</dt> <dt>

[Linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




