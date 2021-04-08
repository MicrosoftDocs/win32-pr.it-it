---
title: Interfaccia IADsPathname
description: Analizza e modifica vari elementi di un ADsPath.
ms.assetid: 1f820488-2e75-4257-90c7-9ec67aac4fe4
ms.tgt_platform: multiple
keywords:
- Interfaccia IADsPathname ADSI
- IADsPathname ADSI, utilizzo
- ADSI ADSI, codice di esempio C/C++, uso di IADsPathname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5cbc5901c8f9dcebebde485decc49fc5bcf312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855293"
---
# <a name="iadspathname-interface"></a><span data-ttu-id="8dc53-106">Interfaccia IADsPathname</span><span class="sxs-lookup"><span data-stu-id="8dc53-106">IADsPathname Interface</span></span>

<span data-ttu-id="8dc53-107">L'interfaccia [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) analizza e modifica vari elementi di un ADsPath.</span><span class="sxs-lookup"><span data-stu-id="8dc53-107">The [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface parses and modifies various elements of an ADsPath.</span></span> <span data-ttu-id="8dc53-108">Converte inoltre ADsPaths tra diversi formati di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8dc53-108">It also converts ADsPaths between various display formats.</span></span>

<span data-ttu-id="8dc53-109">Nell'esempio di codice seguente viene estratto e restituito il nome del server da un ADsPath valido per la visualizzazione all'utente in un'utilità di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="8dc53-109">The following code example extracts and returns the server name from a valid ADsPath for display to the user in a maintenance utility.</span></span>


```C++
HRESULT GetServerName(BSTR adsPath, BSTR *adsServer)
{
    HRESULT hr = S_OK;
    IADsPathname *pIADsPathname = NULL;
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
 
    // Set the path.
    hr = pIADsPathname->Set(adsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
        // Extract and return the server name.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_SERVER, adsServer);
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
}
```



<span data-ttu-id="8dc53-110">L'esempio di codice seguente consente di inizializzare un oggetto ADSI appena creato impostando la proprietà del **nome distinto** dell'oggetto dal proprio ADsPath.</span><span class="sxs-lookup"><span data-stu-id="8dc53-110">The following code example helps to initialize a newly created ADSI object by setting the object's **Distinguished Name** property from its own ADsPath.</span></span> <span data-ttu-id="8dc53-111">Tenere presente che la routine chiamante deve eseguire il commit di tutte le modifiche apportate all'archivio directory sottostante richiamando il metodo **seinfo** .</span><span class="sxs-lookup"><span data-stu-id="8dc53-111">Be aware that the calling routine must commit any changes to the underlying directory store by invoking the **SetInfo** method.</span></span>


```C++
HRESULT SetDistinguishedName(IADs *pIADs)
{
    HRESULT hr = S_OK;
    CComBSTR sbstrADsPath;
    IADsPathname *pIADsPathname = NULL;
 
    // Get the ADsPath for this object.
    hr = pIADs->get_ADsPath(&sbstrADsPath);
    if (FAILED(hr))
        return (hr);
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
     // Set the path.
    hr = pIADsPathname->Set(sbstrADsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
    {
        CComBSTR sbstrDNPath;

        // Convert the path to Distinguished Name format.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,
                                     &sbstrDNPath);
 
        if (SUCCEEDED(hr))
        {
            // Set the distinguished name property.
            VARIANT var;
            VariantInit(&var);
            V_BSTR(&var) = sbstrDNPath;
            V_VT(&var) = VT_BSTR;
            hr = pIADs->Put(CComBSTR("distinguishedName"), var);
            VariantClear(&var);
        }
    }
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
 
}
```



 

 




