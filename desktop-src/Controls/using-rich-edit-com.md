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
# <a name="how-to-use-ole-in-rich-edit-controls"></a>Come utilizzare OLE nei controlli Rich Edit

In questa sezione vengono fornite informazioni sull'utilizzo di Object Linking and Embedding (OLE) in controlli Rich Edit.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-a-rich-edit-interface"></a>Usare un'interfaccia Rich Edit

I controlli Rich Edit espongono alcune funzionalità tramite le interfacce Component Object Model (COM). Ottenendo un'interfaccia da un controllo, si ottiene la possibilità di usare altri oggetti all'interno del controllo. È possibile ottenere questa interfaccia inviando il [**messaggio \_ GETOLEINTERFACE em**](em-getoleinterface.md) . Dall'interfaccia [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) è quindi possibile ottenere le interfacce utilizzate nel modello a [oggetti di testo](text-object-model.md).

Un'altra interfaccia, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), viene implementata dalle applicazioni per definire il comportamento del controllo quando interagisce con gli oggetti.

### <a name="insert-an-object-into-a-rich-edit-control"></a>Inserire un oggetto in un controllo Rich Edit

Nell'esempio di codice seguente viene inserito un oggetto file in un controllo Rich Edit. Se un programma è associato al tipo di file nel computer dell'utente (ad esempio, Microsoft Excel per un file xls), il contenuto del file viene visualizzato nel controllo; in caso contrario, viene visualizzata un'icona.

1.  Ottenere l'interfaccia [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  Creazione di un archivio strutturato.

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  Configurare il formato dei dati.

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  Ottenere un puntatore al sito di visualizzazione.

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  Creare l'oggetto e recuperare la relativa interfaccia **IUnknown** .

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

    

6.  Ottenere l'interfaccia IOleObject per l'oggetto.

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  Per assicurarsi che i riferimenti vengano conteggiati correttamente, inviare una notifica all'oggetto che contiene.

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  Configurare le informazioni sull'oggetto.

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

    

9.  Sposta il punto di inserimento alla fine del testo e aggiunge un ritorno a capo.

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. Inserire l'oggetto.

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. Eseguire la pulizia.

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a>Uso di IRichEditOleCallback

Le applicazioni implementano l'interfaccia [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) per rispondere alle query o azioni correlate a OLE eseguite da un controllo Rich Edit. Associare l'implementazione dell'interfaccia al controllo inviando un messaggio [**\_ SETOLECALLBACK em**](em-setolecallback.md) . Il controllo chiama quindi i metodi sull'implementazione dell'interfaccia nel modo appropriato.

Ad esempio, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) viene chiamato quando l'utente tenta di trascinare o incollare un oggetto nel controllo. Se l'applicazione può accettare i dati, l'implementazione del metodo restituisce S \_ OK. in caso contrario, restituisce un codice di errore. Il metodo può anche eseguire altre azioni, ad esempio l'avviso che indica all'utente che i file di tale tipo non possono essere inseriti nel controllo.

## <a name="complete-insertobject-example-function"></a>Funzione di esempio InsertObject completa

Nell'esempio di codice riportato di seguito vengono illustrati i frammenti di codice precedenti combinati in un'unica funzione completa che include la gestione degli errori.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




