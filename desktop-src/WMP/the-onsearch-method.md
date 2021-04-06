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
# <a name="the-onsearch-method"></a>Metodo OnSearch

Il metodo OnSearch viene chiamato da Windows Media Player quando si fa clic sul pulsante **Cerca** . Questo metodo recupera l'oggetto **multimediale** corrente e lo passa al metodo launchpage.

Il codice seguente viene usato per implementare questo metodo:


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

 

 




