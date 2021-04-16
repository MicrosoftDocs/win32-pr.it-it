---
description: Caricamento di un grafico da un processo esterno
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Caricamento di un grafico da un processo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564201"
---
# <a name="loading-a-graph-from-an-external-process"></a>Caricamento di un grafico da un processo esterno

GraphEdit può caricare un grafo di filtro creato da un processo esterno. Con questa funzionalità è possibile visualizzare esattamente il grafico del filtro compilato dall'applicazione, con una quantità minima di codice aggiuntivo nell'applicazione.

> [!Note]  
> Questa funzionalità richiede Windows 2000, Windows XP o versione successiva.

 

> [!Note]  
> A partire da Windows Vista, è necessario registrare proppage.dll per abilitare questa funzionalità. Proppage.dll è incluso nel Windows SDK.

 

L'applicazione deve registrare l'istanza del grafico di filtro nella tabella degli oggetti in esecuzione (ROT). Il ROT è una tabella di ricerca accessibile a livello globale che tiene traccia degli oggetti in esecuzione. Gli oggetti vengono registrati nel ROT per moniker. Per connettersi al grafo, GraphEdit Cerca i moniker per i moniker il cui nome visualizzato corrisponde a un formato particolare:


```C++
!FilterGraph X pid Y
```



dove *X* è l'indirizzo esadecimale del gestore del grafico del filtro e *Y* è l'ID del processo, anche in formato esadecimale.

Quando l'applicazione crea il grafico di filtro per la prima volta, chiamare la funzione seguente:


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



Questa funzione crea un moniker e una nuova voce ROT per il grafico dei filtri. Il primo parametro è un puntatore al grafico dei filtri. Il secondo parametro riceve un valore che identifica la nuova voce ROT. Prima che l'applicazione rilasci il grafo del filtro, chiamare la funzione seguente per rimuovere la voce ROT. Il parametro *pdwRegister* è l'identificatore restituito dalla funzione AddToRot.


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



Nell'esempio di codice seguente viene illustrato come chiamare queste funzioni. In questo esempio, il codice che aggiunge e rimuove le voci ROT viene compilato in modo condizionale, in modo che sia incluso solo nelle build di debug.


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



Per visualizzare il grafico di filtro in GraphEdit, eseguire l'applicazione e GraphEdit allo stesso tempo. Nel menu **file** GraphEdit fare clic su **Connetti a grafo remoto...** Nella finestra di dialogo **Connetti al grafico** selezionare l'ID del processo (PID) dell'applicazione e fare clic su **OK**. GraphEdit carica il grafico del filtro e lo Visualizza. Non usare altre funzionalità di GraphEdit in questo grafico. potrebbero verificarsi risultati imprevisti. Ad esempio, non aggiungere o rimuovere filtri oppure arrestare e avviare il grafo. Chiudere GraphEdit prima di uscire dall'applicazione.

> [!Note]  
> L'applicazione potrebbe raggiungere varie asserzioni quando viene chiusa. che possono essere tuttavia ignorati.

 

Nella figura seguente viene illustrata la finestra **di dialogo Connetti al grafico** .

![Connetti a grafico](images/gedit-spy.png)

Quando GraphEdit carica il grafo, viene eseguito nel contesto dell'applicazione di destinazione. Pertanto, GraphEdit potrebbe bloccarsi perché è in attesa del thread. Questo può verificarsi, ad esempio, se si esegue il codice istruzione per istruzione nel debugger.

Questa funzionalità deve essere utilizzata solo nelle build di debug dell'applicazione, non nelle compilazioni finali, perché consente ad altre applicazioni di visualizzare o controllare il grafico del filtro.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>Connessione a un grafo remoto dalla riga di comando

GraphEdit supporta un'opzione della riga di comando per caricare automaticamente un grafo remoto all'avvio. La sintassi è:


```C++
GraphEdt -a moniker
```



dove *moniker* è un moniker creato mediante la funzione AddToRot, descritto in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Simulazione della creazione di grafici con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



