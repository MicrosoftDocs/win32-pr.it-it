---
title: Metodo OnSearch
description: Metodo OnSearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Plug-in di Windows Media Player, metodo OnSearch
- plug-in, metodo OnSearch
- plug-in dell'interfaccia utente, metodo OnSearch
- Plug-in dell'interfaccia utente, metodo OnSearch
- Metodo OnSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5c33af434028e6ee72c757c8d71def0d4109fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044823"
---
# <a name="the-onsearch-method"></a><span data-ttu-id="1451b-108">Metodo OnSearch</span><span class="sxs-lookup"><span data-stu-id="1451b-108">The OnSearch Method</span></span>

<span data-ttu-id="1451b-109">Il metodo OnSearch viene chiamato da Windows Media Player quando si fa clic sul pulsante **Cerca** .</span><span class="sxs-lookup"><span data-stu-id="1451b-109">The OnSearch method is called by Windows Media Player when the **Search** button is clicked.</span></span> <span data-ttu-id="1451b-110">Questo metodo recupera l'oggetto **multimediale** corrente e lo passa al metodo launchpage.</span><span class="sxs-lookup"><span data-stu-id="1451b-110">This method retrieves the current **Media** object and passes it to the LaunchPage method.</span></span>

<span data-ttu-id="1451b-111">Il codice seguente viene usato per implementare questo metodo:</span><span class="sxs-lookup"><span data-stu-id="1451b-111">The following code is used to implement this method:</span></span>


```C++
LRESULT OnSearch(WORD wNotifyCode, WORD wID, HWND hwndCtl, BOOL& fHandled)
{
    HRESULT hr;
    CComPtr<IWMPMedia> spMedia;

    if( m_pPlugin && m_pPlugin->m_spCore )
    {
        // Get a pointer to the current media item.
        hr = m_pPlugin->m_spCore->get_currentMedia(&spMedia);
        if (SUCCEEDED(hr) && spMedia)
        {
            LaunchPage(spMedia);
        }
    else
        {
            MessageBox(_T("There is no media loaded."), _T("Warn"), MB_OK | MB_ICONWARNING);
        }
    }
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="1451b-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1451b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1451b-113">**Implementazione di CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="1451b-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




