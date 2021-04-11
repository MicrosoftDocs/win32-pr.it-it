---
title: Come utilizzare OLE nei controlli Rich Edit
description: In questa sezione vengono fornite informazioni sull'utilizzo di Object Linking and Embedding (OLE) in controlli Rich Edit.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104117490"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a><span data-ttu-id="9b813-103">Come utilizzare OLE nei controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9b813-103">How to Use OLE in Rich Edit Controls</span></span>

<span data-ttu-id="9b813-104">In questa sezione vengono fornite informazioni sull'utilizzo di Object Linking and Embedding (OLE) in controlli Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9b813-104">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9b813-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="9b813-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9b813-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="9b813-106">Technologies</span></span>

-   [<span data-ttu-id="9b813-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="9b813-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9b813-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9b813-108">Prerequisites</span></span>

-   <span data-ttu-id="9b813-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="9b813-109">C/C++</span></span>
-   <span data-ttu-id="9b813-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="9b813-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9b813-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="9b813-111">Instructions</span></span>

### <a name="use-a-rich-edit-interface"></a><span data-ttu-id="9b813-112">Usare un'interfaccia Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9b813-112">Use a Rich Edit Interface</span></span>

<span data-ttu-id="9b813-113">I controlli Rich Edit espongono alcune funzionalità tramite le interfacce Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="9b813-113">Rich edit controls expose some of their functionality through Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="9b813-114">Ottenendo un'interfaccia da un controllo, si ottiene la possibilità di usare altri oggetti all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="9b813-114">By obtaining an interface from a control, you gain the ability to work with other objects within the control.</span></span> <span data-ttu-id="9b813-115">È possibile ottenere questa interfaccia inviando il [**messaggio \_ GETOLEINTERFACE em**](em-getoleinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="9b813-115">You can obtain this interface by sending the [**EM\_GETOLEINTERFACE**](em-getoleinterface.md) message.</span></span> <span data-ttu-id="9b813-116">Dall'interfaccia [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) è quindi possibile ottenere le interfacce utilizzate nel modello a [oggetti di testo](text-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="9b813-116">From the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface, you can then obtain interfaces used in the [Text Object Model](text-object-model.md).</span></span>

<span data-ttu-id="9b813-117">Un'altra interfaccia, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), viene implementata dalle applicazioni per definire il comportamento del controllo quando interagisce con gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="9b813-117">Another interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), is implemented by applications to define the behavior of the control when it interacts with objects.</span></span>

### <a name="insert-an-object-into-a-rich-edit-control"></a><span data-ttu-id="9b813-118">Inserire un oggetto in un controllo Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9b813-118">Insert an Object into a Rich Edit Control</span></span>

<span data-ttu-id="9b813-119">Nell'esempio di codice seguente viene inserito un oggetto file in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9b813-119">The following code example inserts a file object into a rich edit control.</span></span> <span data-ttu-id="9b813-120">Se un programma è associato al tipo di file nel computer dell'utente (ad esempio, Microsoft Excel per un file xls), il contenuto del file viene visualizzato nel controllo; in caso contrario, viene visualizzata un'icona.</span><span class="sxs-lookup"><span data-stu-id="9b813-120">If a program is associated with the file type on the user's machine (for example, Microsoft Excel for an .xls file), the contents of the file display in the control; otherwise, an icon appears.</span></span>

1.  <span data-ttu-id="9b813-121">Ottenere l'interfaccia [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="9b813-121">Get the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface.</span></span>

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  <span data-ttu-id="9b813-122">Creazione di un archivio strutturato.</span><span class="sxs-lookup"><span data-stu-id="9b813-122">Create structured storage.</span></span>

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  <span data-ttu-id="9b813-123">Configurare il formato dei dati.</span><span class="sxs-lookup"><span data-stu-id="9b813-123">Set up the data format.</span></span>

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  <span data-ttu-id="9b813-124">Ottenere un puntatore al sito di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9b813-124">Get a pointer to the display site.</span></span>

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  <span data-ttu-id="9b813-125">Creare l'oggetto e recuperare la relativa interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9b813-125">Create the object and retrieve its **IUnknown** interface.</span></span>

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  <span data-ttu-id="9b813-126">Ottenere l'interfaccia IOleObject per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b813-126">Get the IOleObject interface to the object.</span></span>

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  <span data-ttu-id="9b813-127">Per assicurarsi che i riferimenti vengano conteggiati correttamente, inviare una notifica all'oggetto che contiene.</span><span class="sxs-lookup"><span data-stu-id="9b813-127">To ensure that references are counted correctly, notify the object that it is contained.</span></span>

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  <span data-ttu-id="9b813-128">Configurare le informazioni sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b813-128">Set up object info.</span></span>

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  <span data-ttu-id="9b813-129">Sposta il punto di inserimento alla fine del testo e aggiunge un ritorno a capo.</span><span class="sxs-lookup"><span data-stu-id="9b813-129">Move the caret to the end of the text and add a carriage return.</span></span>

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. <span data-ttu-id="9b813-130">Inserire l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b813-130">Insert the object.</span></span>

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. <span data-ttu-id="9b813-131">Eseguire la pulizia.</span><span class="sxs-lookup"><span data-stu-id="9b813-131">Clean up.</span></span>

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a><span data-ttu-id="9b813-132">Uso di IRichEditOleCallback</span><span class="sxs-lookup"><span data-stu-id="9b813-132">Using IRichEditOleCallback</span></span>

<span data-ttu-id="9b813-133">Le applicazioni implementano l'interfaccia [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) per rispondere alle query o azioni correlate a OLE eseguite da un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9b813-133">Applications implement the [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) interface to respond to OLE-related queries or actions that are performed by a rich edit control.</span></span> <span data-ttu-id="9b813-134">Associare l'implementazione dell'interfaccia al controllo inviando un messaggio [**\_ SETOLECALLBACK em**](em-setolecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="9b813-134">You associate your implementation of the interface with the control by sending an [**EM\_SETOLECALLBACK**](em-setolecallback.md) message.</span></span> <span data-ttu-id="9b813-135">Il controllo chiama quindi i metodi sull'implementazione dell'interfaccia nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="9b813-135">The control then calls methods on your implementation of the interface as appropriate.</span></span>

<span data-ttu-id="9b813-136">Ad esempio, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) viene chiamato quando l'utente tenta di trascinare o incollare un oggetto nel controllo.</span><span class="sxs-lookup"><span data-stu-id="9b813-136">For example, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) is called when the user attempts to drag or paste an object into the control.</span></span> <span data-ttu-id="9b813-137">Se l'applicazione può accettare i dati, l'implementazione del metodo restituisce S \_ OK. in caso contrario, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="9b813-137">If your application can accept the data, your implementation of the method returns S\_OK; otherwise, it returns an error code.</span></span> <span data-ttu-id="9b813-138">Il metodo può anche eseguire altre azioni, ad esempio l'avviso che indica all'utente che i file di tale tipo non possono essere inseriti nel controllo.</span><span class="sxs-lookup"><span data-stu-id="9b813-138">The method might also take some other action, such as warning the user that files of that type cannot be placed in the control.</span></span>

## <a name="complete-insertobject-example-function"></a><span data-ttu-id="9b813-139">Funzione di esempio InsertObject completa</span><span class="sxs-lookup"><span data-stu-id="9b813-139">Complete InsertObject Example Function</span></span>

<span data-ttu-id="9b813-140">Nell'esempio di codice riportato di seguito vengono illustrati i frammenti di codice precedenti combinati in un'unica funzione completa che include la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="9b813-140">The following code example demonstrates the previous code snippets combined into one complete function that includes error handling.</span></span>


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="9b813-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b813-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b813-142">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9b813-142">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="9b813-143">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9b813-143">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




