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
# <a name="container-browser"></a><span data-ttu-id="a8860-105">Browser contenitore</span><span class="sxs-lookup"><span data-stu-id="a8860-105">Container Browser</span></span>

<span data-ttu-id="a8860-106">Un'applicazione può utilizzare la funzione [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) per visualizzare una finestra di dialogo che può essere utilizzata per esplorare i contenitori in un servizio dominio di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a8860-106">An application can use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to display a dialog box that can be used to browse through the containers in an Active Directory Domain Service.</span></span> <span data-ttu-id="a8860-107">Nella finestra di dialogo vengono visualizzati i contenitori in un formato struttura ad albero, che consente all'utente di spostarsi nell'albero utilizzando la tastiera e il mouse.</span><span class="sxs-lookup"><span data-stu-id="a8860-107">The dialog box displays the containers in a tree format and enables the user to navigate through the tree using the keyboard and mouse.</span></span> <span data-ttu-id="a8860-108">Quando l'utente seleziona un elemento nella finestra di dialogo, viene specificato il ADsPath del contenitore selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a8860-108">When the user selects an item in the dialog box, the ADsPath of the container selected by the user is provided.</span></span>

<span data-ttu-id="a8860-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) accetta un puntatore a una struttura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) che contiene i dati relativi alla finestra di dialogo e restituisce l'ADsPath dell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="a8860-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) takes a pointer to a [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure that contains data about the dialog box and returns the ADsPath of the selected item.</span></span>

<span data-ttu-id="a8860-110">Il membro **pszRoot** è un puntatore a una stringa Unicode che contiene il contenitore radice dell'albero.</span><span class="sxs-lookup"><span data-stu-id="a8860-110">The **pszRoot** member is a pointer to a Unicode string that contains the root container of the tree.</span></span> <span data-ttu-id="a8860-111">Se **pszRoot** è **null**, l'albero conterrà l'intero albero.</span><span class="sxs-lookup"><span data-stu-id="a8860-111">If **pszRoot** is **NULL**, the tree will contain the entire tree.</span></span>

<span data-ttu-id="a8860-112">Il membro **pszPath** riceve il ADsPath dell'oggetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="a8860-112">The **pszPath** member receives the ADsPath of the selected object.</span></span> <span data-ttu-id="a8860-113">È possibile specificare un particolare contenitore da visualizzare e selezionare quando la finestra di dialogo viene visualizzata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="a8860-113">It is possible to specify a particular container to be visible and selected when the dialog box is first displayed.</span></span> <span data-ttu-id="a8860-114">Questa operazione viene eseguita impostando **pszPath** su ADsPath dell'elemento da selezionare e impostando il flag **DSBI \_ EXPANDONOPEN** in **dwFlags**.</span><span class="sxs-lookup"><span data-stu-id="a8860-114">This is accomplished by setting **pszPath** to the ADsPath of the item to be selected and setting the **DSBI\_EXPANDONOPEN** flag in **dwFlags**.</span></span>

<span data-ttu-id="a8860-115">Il contenuto e il comportamento della finestra di dialogo possono anche essere controllati in fase di esecuzione implementando una funzione [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="a8860-115">The contents and behavior of the dialog box can also be controlled at runtime by implementing a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="a8860-116">La funzione **BFFCallBack** viene implementata dall'applicazione e viene chiamata quando si verificano determinati eventi.</span><span class="sxs-lookup"><span data-stu-id="a8860-116">The **BFFCallBack** function is implemented by the application and is called when certain events occur.</span></span> <span data-ttu-id="a8860-117">Un'applicazione può utilizzare questi eventi per controllare la modalità di visualizzazione degli elementi nella finestra di dialogo e il contenuto effettivo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a8860-117">An application can use these events to control how the items in the dialog box are displayed as well as the actual contents of the dialog box.</span></span> <span data-ttu-id="a8860-118">Un'applicazione, ad esempio, può filtrare gli elementi visualizzati nella finestra di dialogo implementando una funzione **BFFCallBack** in grado di gestire la notifica **DSBM \_ QUERYINSERT** .</span><span class="sxs-lookup"><span data-stu-id="a8860-118">For example, an application can filter the items displayed in the dialog box by implementing a **BFFCallBack** function that can handle the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="a8860-119">Quando viene ricevuta una notifica **DSBM \_ QUERYINSERT** , usare il membro **pszADsPath** della struttura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) per determinare quale elemento sta per essere inserito.</span><span class="sxs-lookup"><span data-stu-id="a8860-119">When a **DSBM\_QUERYINSERT** notification is received, use the **pszADsPath** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure to determine which item is about to be inserted.</span></span> <span data-ttu-id="a8860-120">Se l'applicazione determina che l'elemento non deve essere visualizzato, può nascondere l'elemento attenendosi alla procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="a8860-120">If the application determines that the item should not be displayed, it can hide the item by performing the following steps.</span></span>

1.  <span data-ttu-id="a8860-121">Aggiungere il flag di **\_ stato DSBF** al membro **dwMask** della struttura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="a8860-121">Add the **DSBF\_STATE** flag to the **dwMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
2.  <span data-ttu-id="a8860-122">Aggiungere il flag **DSBS \_ Hidden** al membro **dwStateMask** della struttura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="a8860-122">Add the **DSBS\_HIDDEN** flag to the **dwStateMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
3.  <span data-ttu-id="a8860-123">Aggiungere il flag **DSBS \_ Hidden** al membro **dwState** della struttura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="a8860-123">Add the **DSBS\_HIDDEN** flag to the **dwState** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
4.  <span data-ttu-id="a8860-124">Restituisce un valore diverso da zero dalla funzione [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="a8860-124">Return a nonzero value from the [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span>

<span data-ttu-id="a8860-125">Oltre a nascondere determinati elementi, un'applicazione può modificare il testo e l'icona visualizzati per l'elemento gestendo la notifica **DSBM \_ QUERYINSERT** .</span><span class="sxs-lookup"><span data-stu-id="a8860-125">In addition to hiding certain items, an application can modify the text and icon displayed for the item by handling the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="a8860-126">Per ulteriori informazioni, vedere [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span><span class="sxs-lookup"><span data-stu-id="a8860-126">For more information, see [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span></span>

<span data-ttu-id="a8860-127">La funzione [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) può utilizzare la **notifica \_ inizializzata BFFM** per ottenere l'handle della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a8860-127">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function can use the **BFFM\_INITIALIZED** notification to obtain the handle of the dialog box.</span></span> <span data-ttu-id="a8860-128">L'applicazione può utilizzare questo handle per inviare messaggi, ad esempio **BFFM \_ ENABLEOK**, alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a8860-128">The application can use this handle to send messages, such as **BFFM\_ENABLEOK**, to the dialog box.</span></span> <span data-ttu-id="a8860-129">Per ulteriori informazioni sui messaggi che possono essere inviati alla finestra di dialogo, vedere [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span><span class="sxs-lookup"><span data-stu-id="a8860-129">For more information about the messages that can be sent to the dialog box, see [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span></span>

<span data-ttu-id="a8860-130">L'handle della finestra di dialogo può essere utilizzato anche per accedere direttamente ai controlli nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a8860-130">The dialog box handle can also be used to gain direct access to the controls in the dialog box.</span></span> <span data-ttu-id="a8860-131">**DSBID \_ BANNER** è l'identificatore del controllo testo statico in cui viene visualizzato il membro **pszTitle** della struttura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="a8860-131">**DSBID\_BANNER** is the identifier for the static text control that the **pszTitle** member of the [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure is displayed in.</span></span> <span data-ttu-id="a8860-132">**DSBID \_ CONTAINER** è l'identificatore del controllo di visualizzazione albero utilizzato per visualizzare il contenuto della struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="a8860-132">**DSBID\_CONTAINERLIST** is the identifier of the tree view control used to display the tree contents.</span></span> <span data-ttu-id="a8860-133">L'uso di questi elementi deve essere evitato, se possibile, per evitare futuri problemi di compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a8860-133">Use of these items should be avoided, if possible, to prevent future application compatibility problems.</span></span>

<span data-ttu-id="a8860-134">Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare la funzione [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) per creare la finestra di dialogo browser contenitore e implementare una funzione [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="a8860-134">The following C++ code example shows how to use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to create the container browser dialog box and implement a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="a8860-135">[**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) usa la notifica **DSBM \_ QUERYINSERT** per modificare il nome visualizzato per ogni elemento nel nome distinto dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a8860-135">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) uses the **DSBM\_QUERYINSERT** notification to change the display name for each item to the distinguished name of the item.</span></span>


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



 

 