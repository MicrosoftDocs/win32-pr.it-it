---
title: Metodo OnSearch
description: Metodo OnSearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Windows Media Player plug-in, metodo OnSearch
- plug-in, metodo OnSearch
- plug-in dell'interfaccia utente,metodo OnSearch
- Plug-in dell'interfaccia utente, metodo OnSearch
- Metodo OnSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ab5cb4b26d291a940ed329e2422240e6fc36e5ba980431af169d58f1398fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118001"
---
# <a name="the-onsearch-method"></a>Metodo OnSearch

Il metodo OnSearch viene chiamato da Windows Media Player **quando** si fa clic sul pulsante Cerca. Questo metodo recupera l'oggetto **Media** corrente e lo passa al metodo LaunchPage.

Per implementare questo metodo viene usato il codice seguente:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




