---
title: Metodo LaunchPage
description: Metodo LaunchPage
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Plug-in di Windows Media Player, metodo LaunchPage
- plug-in, metodo LaunchPage
- plug-in dell'interfaccia utente, metodo LaunchPage
- Plug-in dell'interfaccia utente, metodo LaunchPage
- Metodo LaunchPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f04974eba1ba5c86300de44acd2ba6e2920954f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044925"
---
# <a name="the-launchpage-method"></a><span data-ttu-id="48b58-108">Metodo LaunchPage</span><span class="sxs-lookup"><span data-stu-id="48b58-108">The LaunchPage Method</span></span>

<span data-ttu-id="48b58-109">Il metodo LaunchPage fornisce la funzionalità principale del plug-in, ovvero l'avvio di una pagina di ricerca che contiene informazioni sull'autore dell'elemento multimediale passato al metodo.</span><span class="sxs-lookup"><span data-stu-id="48b58-109">The LaunchPage method provides the primary functionality of the plug-in, which is to launch a search page containing information about the artist of the media item passed to the method.</span></span>

<span data-ttu-id="48b58-110">Questo metodo viene chiamato dal metodo OnSearch utilizzando l'oggetto **multimediale** corrente.</span><span class="sxs-lookup"><span data-stu-id="48b58-110">This method is called by the OnSearch method using the current **Media** object.</span></span>

<span data-ttu-id="48b58-111">Il codice seguente viene usato per implementare questo metodo:</span><span class="sxs-lookup"><span data-stu-id="48b58-111">The following code is used to implement this method:</span></span>


```C++
void LaunchPage(IWMPMedia *pMedia)
{
    USES_CONVERSION;

    HRESULT hr;
    CComBSTR bstrType;
    CComBSTR bstrArtist;

    // Get the name of the artist.
    bstrType = _T("artist");
    hr = pMedia->getItemInfo(bstrType, &bstrArtist);
    if (SUCCEEDED(hr)) 
    {
        // Create the search URL.
        TCHAR szSearch[MAX_PATH];
        _stprintf_s(szSearch, MAX_PATH, _T("https://search.msn.com/results.asp?q=%s"), OLE2T(bstrArtist));
        CComBSTR bstrURL = szSearch;

        // Launch the search page.
        m_pPlugin->m_spCore->launchURL(bstrURL);
    }
    else
    {
        MessageBox(_T("Failed to get artist information from media."), _T("Warn"), MB_OK | MB_ICONWARNING);
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="48b58-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48b58-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48b58-113">**Implementazione di CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="48b58-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




