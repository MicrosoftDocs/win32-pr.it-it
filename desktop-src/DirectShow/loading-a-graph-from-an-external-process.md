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
# <a name="loading-a-graph-from-an-external-process"></a><span data-ttu-id="af43b-103">Caricamento di un grafico da un processo esterno</span><span class="sxs-lookup"><span data-stu-id="af43b-103">Loading a Graph From an External Process</span></span>

<span data-ttu-id="af43b-104">GraphEdit può caricare un grafo di filtro creato da un processo esterno.</span><span class="sxs-lookup"><span data-stu-id="af43b-104">GraphEdit can load a filter graph created by an external process.</span></span> <span data-ttu-id="af43b-105">Con questa funzionalità è possibile visualizzare esattamente il grafico del filtro compilato dall'applicazione, con una quantità minima di codice aggiuntivo nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="af43b-105">With this feature, you can see exactly what filter graph your application builds, with only a minimal amount of additional code in your application.</span></span>

> [!Note]  
> <span data-ttu-id="af43b-106">Questa funzionalità richiede Windows 2000, Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="af43b-106">This feature requires Windows 2000, Windows XP, or later.</span></span>

 

> [!Note]  
> <span data-ttu-id="af43b-107">A partire da Windows Vista, è necessario registrare proppage.dll per abilitare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="af43b-107">Starting in Windows Vista, you must register proppage.dll to enable this feature.</span></span> <span data-ttu-id="af43b-108">Proppage.dll è incluso nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="af43b-108">Proppage.dll is included in the Windows SDK.</span></span>

 

<span data-ttu-id="af43b-109">L'applicazione deve registrare l'istanza del grafico di filtro nella tabella degli oggetti in esecuzione (ROT).</span><span class="sxs-lookup"><span data-stu-id="af43b-109">The application must register the filter graph instance in the Running Object Table (ROT).</span></span> <span data-ttu-id="af43b-110">Il ROT è una tabella di ricerca accessibile a livello globale che tiene traccia degli oggetti in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="af43b-110">The ROT is a globally accessible look-up table that keeps track of running objects.</span></span> <span data-ttu-id="af43b-111">Gli oggetti vengono registrati nel ROT per moniker.</span><span class="sxs-lookup"><span data-stu-id="af43b-111">Objects are registered in the ROT by moniker.</span></span> <span data-ttu-id="af43b-112">Per connettersi al grafo, GraphEdit Cerca i moniker per i moniker il cui nome visualizzato corrisponde a un formato particolare:</span><span class="sxs-lookup"><span data-stu-id="af43b-112">To connect to the graph, GraphEdit searches the ROT for monikers whose display name matches a particular format:</span></span>


```C++
!FilterGraph X pid Y
```



<span data-ttu-id="af43b-113">dove *X* è l'indirizzo esadecimale del gestore del grafico del filtro e *Y* è l'ID del processo, anche in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="af43b-113">where *X* is the hexadecimal address of the Filter Graph Manager, and *Y* is the process id, also in hexadecimal.</span></span>

<span data-ttu-id="af43b-114">Quando l'applicazione crea il grafico di filtro per la prima volta, chiamare la funzione seguente:</span><span class="sxs-lookup"><span data-stu-id="af43b-114">When your application first creates the filter graph, call the following function:</span></span>


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



<span data-ttu-id="af43b-115">Questa funzione crea un moniker e una nuova voce ROT per il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="af43b-115">This function creates a moniker and a new ROT entry for the filter graph.</span></span> <span data-ttu-id="af43b-116">Il primo parametro è un puntatore al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="af43b-116">The first parameter is a pointer to the filter graph.</span></span> <span data-ttu-id="af43b-117">Il secondo parametro riceve un valore che identifica la nuova voce ROT.</span><span class="sxs-lookup"><span data-stu-id="af43b-117">The second parameter receives a value that identifies the new ROT entry.</span></span> <span data-ttu-id="af43b-118">Prima che l'applicazione rilasci il grafo del filtro, chiamare la funzione seguente per rimuovere la voce ROT.</span><span class="sxs-lookup"><span data-stu-id="af43b-118">Before the application releases the filter graph, call the following function to remove the ROT entry.</span></span> <span data-ttu-id="af43b-119">Il parametro *pdwRegister* è l'identificatore restituito dalla funzione AddToRot.</span><span class="sxs-lookup"><span data-stu-id="af43b-119">The *pdwRegister* parameter is the identifier returned by the AddToRot function.</span></span>


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



<span data-ttu-id="af43b-120">Nell'esempio di codice seguente viene illustrato come chiamare queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="af43b-120">The following code example shows how to call these functions.</span></span> <span data-ttu-id="af43b-121">In questo esempio, il codice che aggiunge e rimuove le voci ROT viene compilato in modo condizionale, in modo che sia incluso solo nelle build di debug.</span><span class="sxs-lookup"><span data-stu-id="af43b-121">In this example, the code that adds and removes ROT entries is conditionally compiled, so that it is included only in debug builds.</span></span>


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



<span data-ttu-id="af43b-122">Per visualizzare il grafico di filtro in GraphEdit, eseguire l'applicazione e GraphEdit allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="af43b-122">To view the filter graph in GraphEdit, run your application and GraphEdit at the same time.</span></span> <span data-ttu-id="af43b-123">Nel menu **file** GraphEdit fare clic su **Connetti a grafo remoto...** Nella finestra di dialogo **Connetti al grafico** selezionare l'ID del processo (PID) dell'applicazione e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="af43b-123">In the GraphEdit **File** menu, click **Connect to Remote Graph...** In the **Connect To Graph** dialog box, select the process id (pid) of your application and click **OK**.</span></span> <span data-ttu-id="af43b-124">GraphEdit carica il grafico del filtro e lo Visualizza.</span><span class="sxs-lookup"><span data-stu-id="af43b-124">GraphEdit loads the filter graph and displays it.</span></span> <span data-ttu-id="af43b-125">Non usare altre funzionalità di GraphEdit in questo grafico. potrebbero verificarsi risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="af43b-125">Don't use any other GraphEdit features on this graph—it might cause unexpected results.</span></span> <span data-ttu-id="af43b-126">Ad esempio, non aggiungere o rimuovere filtri oppure arrestare e avviare il grafo.</span><span class="sxs-lookup"><span data-stu-id="af43b-126">For example, don't add or remove filters, or stop and start the graph.</span></span> <span data-ttu-id="af43b-127">Chiudere GraphEdit prima di uscire dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="af43b-127">Close GraphEdit before exiting your application.</span></span>

> [!Note]  
> <span data-ttu-id="af43b-128">L'applicazione potrebbe raggiungere varie asserzioni quando viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="af43b-128">Your application might hit various asserts when it exits.</span></span> <span data-ttu-id="af43b-129">che possono essere tuttavia ignorati.</span><span class="sxs-lookup"><span data-stu-id="af43b-129">You can ignore these.</span></span>

 

<span data-ttu-id="af43b-130">Nella figura seguente viene illustrata la finestra **di dialogo Connetti al grafico** .</span><span class="sxs-lookup"><span data-stu-id="af43b-130">The following illustration shows the **Connect To Graph** dialog box.</span></span>

![Connetti a grafico](images/gedit-spy.png)

<span data-ttu-id="af43b-132">Quando GraphEdit carica il grafo, viene eseguito nel contesto dell'applicazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af43b-132">When GraphEdit loads the graph, it executes in the context of the target application.</span></span> <span data-ttu-id="af43b-133">Pertanto, GraphEdit potrebbe bloccarsi perché è in attesa del thread.</span><span class="sxs-lookup"><span data-stu-id="af43b-133">Therefore, GraphEdit might block because it is waiting for the thread.</span></span> <span data-ttu-id="af43b-134">Questo può verificarsi, ad esempio, se si esegue il codice istruzione per istruzione nel debugger.</span><span class="sxs-lookup"><span data-stu-id="af43b-134">For example, this can occur if you are stepping through your code in the debugger.</span></span>

<span data-ttu-id="af43b-135">Questa funzionalità deve essere utilizzata solo nelle build di debug dell'applicazione, non nelle compilazioni finali, perché consente ad altre applicazioni di visualizzare o controllare il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="af43b-135">This feature should be used only in debug builds of your application, not retail builds, because it enables other applications to view or control the filter graph.</span></span>

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a><span data-ttu-id="af43b-136">Connessione a un grafo remoto dalla riga di comando</span><span class="sxs-lookup"><span data-stu-id="af43b-136">Connecting to a Remote Graph from the Command Line</span></span>

<span data-ttu-id="af43b-137">GraphEdit supporta un'opzione della riga di comando per caricare automaticamente un grafo remoto all'avvio.</span><span class="sxs-lookup"><span data-stu-id="af43b-137">GraphEdit supports a command-line option to load a remote graph automatically on startup.</span></span> <span data-ttu-id="af43b-138">La sintassi è:</span><span class="sxs-lookup"><span data-stu-id="af43b-138">The syntax is:</span></span>


```C++
GraphEdt -a moniker
```



<span data-ttu-id="af43b-139">dove *moniker* è un moniker creato mediante la funzione AddToRot, descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="af43b-139">where *moniker* is a moniker created using the AddToRot function, described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af43b-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af43b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af43b-141">Simulazione della creazione di grafici con GraphEdit</span><span class="sxs-lookup"><span data-stu-id="af43b-141">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



