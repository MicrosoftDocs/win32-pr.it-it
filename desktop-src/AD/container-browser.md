---
title: Browser contenitore
description: Un'applicazione può utilizzare la funzione DsBrowseForContainer per visualizzare una finestra di dialogo che può essere utilizzata per esplorare i contenitori in un servizio Dominio di Active Directory.
ms.assetid: aa88d565-ff25-4082-964a-9a230d2607f2
ms.tgt_platform: multiple
keywords:
- ANNUNCIO del browser contenitore
- Active Directory contenitori, browser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964c67873cc7936a75e2b9c1cdf331d0fa1fdae1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046544"
---
# <a name="container-browser"></a>Browser contenitore

Un'applicazione può utilizzare la funzione [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) per visualizzare una finestra di dialogo che può essere utilizzata per esplorare i contenitori in un servizio dominio di Active Directory. Nella finestra di dialogo vengono visualizzati i contenitori in un formato struttura ad albero, che consente all'utente di spostarsi nell'albero utilizzando la tastiera e il mouse. Quando l'utente seleziona un elemento nella finestra di dialogo, viene specificato il ADsPath del contenitore selezionato dall'utente.

[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) accetta un puntatore a una struttura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) che contiene i dati relativi alla finestra di dialogo e restituisce l'ADsPath dell'elemento selezionato.

Il membro **pszRoot** è un puntatore a una stringa Unicode che contiene il contenitore radice dell'albero. Se **pszRoot** è **null**, l'albero conterrà l'intero albero.

Il membro **pszPath** riceve il ADsPath dell'oggetto selezionato. È possibile specificare un particolare contenitore da visualizzare e selezionare quando la finestra di dialogo viene visualizzata per la prima volta. Questa operazione viene eseguita impostando **pszPath** su ADsPath dell'elemento da selezionare e impostando il flag **DSBI \_ EXPANDONOPEN** in **dwFlags**.

Il contenuto e il comportamento della finestra di dialogo possono anche essere controllati in fase di esecuzione implementando una funzione [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . La funzione **BFFCallBack** viene implementata dall'applicazione e viene chiamata quando si verificano determinati eventi. Un'applicazione può utilizzare questi eventi per controllare la modalità di visualizzazione degli elementi nella finestra di dialogo e il contenuto effettivo della finestra di dialogo. Un'applicazione, ad esempio, può filtrare gli elementi visualizzati nella finestra di dialogo implementando una funzione **BFFCallBack** in grado di gestire la notifica **DSBM \_ QUERYINSERT** . Quando viene ricevuta una notifica **DSBM \_ QUERYINSERT** , usare il membro **pszADsPath** della struttura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) per determinare quale elemento sta per essere inserito. Se l'applicazione determina che l'elemento non deve essere visualizzato, può nascondere l'elemento attenendosi alla procedura seguente.

1.  Aggiungere il flag di **\_ stato DSBF** al membro **dwMask** della struttura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
2.  Aggiungere il flag **DSBS \_ Hidden** al membro **dwStateMask** della struttura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
3.  Aggiungere il flag **DSBS \_ Hidden** al membro **dwState** della struttura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
4.  Restituisce un valore diverso da zero dalla funzione [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .

Oltre a nascondere determinati elementi, un'applicazione può modificare il testo e l'icona visualizzati per l'elemento gestendo la notifica **DSBM \_ QUERYINSERT** . Per ulteriori informazioni, vedere [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).

La funzione [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) può utilizzare la **notifica \_ inizializzata BFFM** per ottenere l'handle della finestra di dialogo. L'applicazione può utilizzare questo handle per inviare messaggi, ad esempio **BFFM \_ ENABLEOK**, alla finestra di dialogo. Per ulteriori informazioni sui messaggi che possono essere inviati alla finestra di dialogo, vedere [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).

L'handle della finestra di dialogo può essere utilizzato anche per accedere direttamente ai controlli nella finestra di dialogo. **DSBID \_ BANNER** è l'identificatore del controllo testo statico in cui viene visualizzato il membro **pszTitle** della struttura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) . **DSBID \_ CONTAINER** è l'identificatore del controllo di visualizzazione albero utilizzato per visualizzare il contenuto della struttura ad albero. L'uso di questi elementi deve essere evitato, se possibile, per evitare futuri problemi di compatibilità delle applicazioni.

Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare la funzione [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) per creare la finestra di dialogo browser contenitore e implementare una funzione [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) usa la notifica **DSBM \_ QUERYINSERT** per modificare il nome visualizzato per ogni elemento nel nome distinto dell'elemento.


```C++
#include <shlobj.h>
#include <dsclient.h>
#include <atlbase.h>

/**********

    WideCharToLocal()
   
***********/

int WideCharToLocal(LPTSTR pLocal, LPWSTR pWide, DWORD dwChars)
{
    *pLocal = NULL;
    size_t nWideLength = 0;
    wchar_t *pwszSubstring;

    nWideLength = wcslen(pWide);

#ifdef UNICODE
    if(nWideLength < dwChars)
    {
        wcsncpy_s(pLocal, pWide, dwChars);
    }
    else
    {
        wcsncpy_s(pLocal, pWide, dwChars-1);
        pLocal[dwChars-1] = NULL;
    }
#else
    if(nWideLength < dwChars)
    {
        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pWide, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);
    }
    else
    {
        pwszSubstring = new WCHAR[dwChars];
        wcsncpy_s(pwszSubstring,pWide,dwChars-1);
        pwszSubstring[dwChars-1] = NULL;

        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pwszSubstring, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);

    delete [] pwszSubstring;
    }
#endif

    return lstrlen(pLocal);
}

/**********

    BrowseCallback()

***********/

int CALLBACK BrowseCallback(HWND hWnd, 
                            UINT uMsg, 
                            LPARAM lParam, 
                            LPARAM lpData)
{
    switch(uMsg)
    {
    case DSBM_QUERYINSERT:
        {
            BOOL fReturn = FALSE;
            DSBITEM *pItem = (DSBITEM*)lParam;

            /*
            If this is to the root item, get the distinguished name 
            for the object and set the display name to the 
            distinguished name.
            */
            if(!(pItem->dwState & DSBS_ROOT))
            {
                HRESULT hr;
                IADs    *pads;

                hr = ADsGetObject(pItem->pszADsPath , 
                    IID_IADs, (LPVOID*)&pads);
                if(SUCCEEDED(hr))
                {
                    VARIANT var;

                    VariantInit(&var);
                    hr = pads->Get(CComBSTR("distinguishedName"), 
                        &var);
                    if(SUCCEEDED(hr))
                    {
                        if(VT_BSTR == var.vt)
                        {
                            WideCharToLocal(pItem->szDisplayName, 
                                var.bstrVal, 
                                DSB_MAX_DISPLAYNAME_CHARS);
                            pItem->dwMask |= DSBF_DISPLAYNAME;
                            fReturn = TRUE;
                        }
                        
                        VariantClear(&var);
                    }
                    
                    pads->Release();
                }
            }

            return fReturn;
        }

        break;
    }
    
    return FALSE;
}

/***********

    BrowseForContainer()

************/

HRESULT BrowseForContainer(HWND hwndParent, 
    LPOLESTR *ppContainerADsPath)
{
    HRESULT hr = E_FAIL;
    DSBROWSEINFO dsbi;
    OLECHAR wszPath[MAX_PATH * 2];
    DWORD result;
 
    if(!ppContainerADsPath)
    {
        return E_INVALIDARG;
    }
 
    ZeroMemory(&dsbi, sizeof(dsbi));
    dsbi.hwndOwner = hwndParent;
    dsbi.cbStruct = sizeof (DSBROWSEINFO);
    dsbi.pszCaption = TEXT("Browse for a Container");
    dsbi.pszTitle = TEXT("Select an Active Directory container.");
    dsbi.pszRoot = NULL;
    dsbi.pszPath = wszPath;
    dsbi.cchPath = sizeof(wszPath)/sizeof(OLECHAR);
    dsbi.dwFlags = DSBI_INCLUDEHIDDEN |
                    DSBI_IGNORETREATASLEAF|
                    DSBI_RETURN_FORMAT;
    dsbi.pfnCallback = BrowseCallback;
    dsbi.lParam = 0;
    dsbi.dwReturnFormat = ADS_FORMAT_X500;
 
    // Display the browse dialog box.
    // Returns -1, 0, IDOK, or IDCANCEL.
    result = DsBrowseForContainer(&dsbi); 
    if(IDOK == result)
    {
        // Allocate memory for the string.
        *ppContainerADsPath = (OLECHAR*)CoTaskMemAlloc(
            sizeof(OLECHAR)*(wcslen(wszPath) + 1));
        if(*ppContainerADsPath)
        {
            wcscpy_s(*ppContainerADsPath, wszPath);
            // Caller must free using CoTaskMemFree. 
            hr = S_OK;
        }
        else
        {
            hr = E_FAIL;
        }
    }
    else
    {
        hr = E_FAIL;
    }
 
    return hr;
}
```



 

 