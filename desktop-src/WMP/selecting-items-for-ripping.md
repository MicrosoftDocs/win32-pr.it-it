---
title: Selezione degli elementi per il ripping
description: Selezione degli elementi per il ripping
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Windows Media Player, ripping CD
- Windows Media Player a oggetti, ripping CD
- modello a oggetti, ripping CD
- Windows Media Player ActiveX controllo, ripping CD
- ActiveX controllo, ripping CD
- Windows Media Player Controllo ActiveX per dispositivi mobili, ripping cd
- Windows Media Player Dispositivi mobili, ripping di CD
- RIPPING CD, selezione di elementi
- ripping di CD, selezione di elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea677028fab6b3c39466e916bd8bb59ea8cee4d370730c096cbb98978f4abc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646651"
---
# <a name="selecting-items-for-ripping"></a>Selezione degli elementi per il ripping

In alcuni casi, un utente non vuole ripertarsi ogni traccia su un CD. Windows Media Player fornisce un'interfaccia per specificare quali tracce vengono selezionate per il ripping. In genere in un'applicazione di ripping di CD è disponibile un'interfaccia utente che consente all'utente di selezionare le caselle di controllo in un elenco di tracce nel CD.

Alcune tracce potrebbero non essere selezionate per lo ripping per impostazione predefinita. Se una traccia è già presente nella libreria Windows Media Player, non verrà selezionata automaticamente per il ripping. Il secondo esempio di codice in questa sezione illustra come ignorare il valore predefinito e selezionare manualmente una traccia da ripping se è già stata decompressa.

Nell'esempio di codice seguente viene illustrato come determinare se una traccia è selezionata per il ripping:


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



Nell'esempio di codice seguente viene illustrato come specificare se una traccia è selezionata per il ripping.


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
    }

    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ripping di un CD**](ripping-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di copia da CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Avvio del processo Rip**](starting-the-rip-process.md)
</dt> <dt>

[**Recupero dello stato rip**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




