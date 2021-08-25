---
title: Metodo LaunchPage
description: Metodo LaunchPage
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Windows Media Player plug-in, metodo LaunchPage
- plug-in, metodo LaunchPage
- plug-in dell'interfaccia utente, metodo LaunchPage
- Plug-in dell'interfaccia utente, metodo LaunchPage
- Metodo LaunchPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a22e1f4b136711a6f4336fbe54d6d90e4bb18b24a88645587311a0b4046f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762721"
---
# <a name="the-launchpage-method"></a>Metodo LaunchPage

Il metodo LaunchPage fornisce la funzionalità principale del plug-in, ovvero l'avvio di una pagina di ricerca contenente informazioni sull'artista dell'elemento multimediale passato al metodo .

Questo metodo viene chiamato dal metodo OnSearch usando l'oggetto **Media** corrente.

Per implementare questo metodo viene usato il codice seguente:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




