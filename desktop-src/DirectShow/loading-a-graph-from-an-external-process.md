---
description: Caricamento di Graph da un processo esterno
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Caricamento di Graph da un processo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e92fdaebb9ce3cb6615153daf66a8991477bf76e16ac3298e8e8b2fb59d74b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831057"
---
# <a name="loading-a-graph-from-an-external-process"></a>Caricamento di Graph da un processo esterno

GraphEdit può caricare un grafo di filtro creato da un processo esterno. Con questa funzionalità è possibile visualizzare esattamente il grafico dei filtri compilato dall'applicazione, con una quantità minima di codice aggiuntivo nell'applicazione.

> [!Note]  
> Questa funzionalità richiede Windows 2000, Windows XP o versione successiva.

 

> [!Note]  
> A partire da Windows Vista, è necessario registrare proppage.dll per abilitare questa funzionalità. Proppage.dll è incluso in Windows SDK.

 

L'applicazione deve registrare l'istanza del grafo del filtro nella tabella degli oggetti in esecuzione (ROT, Running Object Table). ROT è una tabella di ricerca accessibile a livello globale che tiene traccia degli oggetti in esecuzione. Gli oggetti vengono registrati nel moniker ROT. Per connettersi al grafo, GraphEdit cerca i moniker ROT il cui nome visualizzato corrisponde a un formato specifico:


```C++
!FilterGraph X pid Y
```



dove *X* è l'indirizzo esadecimale di Filter Graph Manager e *Y* è l'ID processo, anche in formato esadecimale.

Quando l'applicazione crea per la prima volta il grafico dei filtri, chiamare la funzione seguente:


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



Questa funzione crea un moniker e una nuova voce ROT per il grafico dei filtri. Il primo parametro è un puntatore al grafico dei filtri. Il secondo parametro riceve un valore che identifica la nuova voce ROT. Prima che l'applicazione rilasci il grafico dei filtri, chiamare la funzione seguente per rimuovere la voce ROT. Il *parametro pdwRegister* è l'identificatore restituito dalla funzione AddToRot.


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



Nell'esempio di codice seguente viene illustrato come chiamare queste funzioni. In questo esempio il codice che aggiunge e rimuove le voci ROT viene compilato in modo condizionale, in modo che sia incluso solo nelle compilazioni di debug.


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



Per visualizzare il grafico dei filtri in GraphEdit, eseguire contemporaneamente l'applicazione e GraphEdit. Nel menu GraphEdit **File (Modifica file)** **fare clic Connessione su Remote Graph...** Nella finestra **Connessione di Graph** selezionare l'ID processo (pid) dell'applicazione e fare clic su **OK.** GraphEdit carica il grafico dei filtri e lo visualizza. Non usare altre funzionalità GraphEdit in questo grafo, perché potrebbe causare risultati imprevisti. Ad esempio, non aggiungere o rimuovere filtri o arrestare e avviare il grafico. Chiudere GraphEdit prima di uscire dall'applicazione.

> [!Note]  
> L'applicazione potrebbe avere diverse asserzioni all'uscita. che possono essere tuttavia ignorati.

 

La figura seguente mostra la **finestra Connessione to Graph** .

![connettersi al grafo](images/gedit-spy.png)

Quando GraphEdit carica il grafo, viene eseguito nel contesto dell'applicazione di destinazione. GraphEdit potrebbe pertanto bloccarsi perché è in attesa del thread. Ad esempio, questa operazione può verificarsi se si esegue un'istruzione alla volta nel codice nel debugger.

Questa funzionalità deve essere usata solo nelle build di debug dell'applicazione, non nelle build di vendita al dettaglio, perché consente ad altre applicazioni di visualizzare o controllare il grafico dei filtri.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>Connessione a un Graph remoto dalla riga di comando

GraphEdit supporta un'opzione della riga di comando per caricare automaticamente un grafo remoto all'avvio. La sintassi è:


```C++
GraphEdt -a moniker
```



dove *moniker è* un moniker creato usando la funzione AddToRot, descritta in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Simulazione Graph compilazione con GraphModifica](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



