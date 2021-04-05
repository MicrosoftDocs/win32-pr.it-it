---
title: Selezione di elementi per l'estrazione
description: Selezione di elementi per l'estrazione
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, selezione degli elementi
- copia di CDs, selezione di elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc18ded43b609be6c7ac1f16833b0c8a33505ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955603"
---
# <a name="selecting-items-for-ripping"></a><span data-ttu-id="e8b04-112">Selezione di elementi per l'estrazione</span><span class="sxs-lookup"><span data-stu-id="e8b04-112">Selecting Items for Ripping</span></span>

<span data-ttu-id="e8b04-113">A volte un utente non desidera eseguire il RIP di ogni traccia in un CD.</span><span class="sxs-lookup"><span data-stu-id="e8b04-113">Sometimes a user does not want to rip every track on a CD.</span></span> <span data-ttu-id="e8b04-114">Windows Media Player fornisce un'interfaccia per specificare quali tracce sono selezionate per l'estrazione.</span><span class="sxs-lookup"><span data-stu-id="e8b04-114">Windows Media Player provides an interface for specifying which tracks are selected for ripping.</span></span> <span data-ttu-id="e8b04-115">In genere in un'applicazione di copia di CD è presente un'interfaccia utente che consente all'utente di selezionare le caselle di controllo in un elenco di tracce sul CD.</span><span class="sxs-lookup"><span data-stu-id="e8b04-115">Typically in a CD ripping application there is a user interface that lets the user select check boxes in a list of tracks on the CD.</span></span>

<span data-ttu-id="e8b04-116">Per impostazione predefinita, alcune tracce potrebbero non essere selezionate per la copia.</span><span class="sxs-lookup"><span data-stu-id="e8b04-116">Some tracks might not be selected for ripping by default.</span></span> <span data-ttu-id="e8b04-117">Se una traccia si trova già nella libreria Media Player di Windows, non verrà selezionata automaticamente per la copia.</span><span class="sxs-lookup"><span data-stu-id="e8b04-117">If a track is already in the Windows Media Player library, it will not be automatically selected for ripping.</span></span> <span data-ttu-id="e8b04-118">Il secondo esempio di codice in questa sezione illustra come ignorare il valore predefinito e selezionare manualmente una traccia per la copia, se è già stata ricopiata.</span><span class="sxs-lookup"><span data-stu-id="e8b04-118">The second code example in this section demonstrates how to bypass the default value and manually select a track for ripping if it has already been ripped.</span></span>

<span data-ttu-id="e8b04-119">Nell'esempio di codice riportato di seguito viene illustrato come determinare se una traccia è selezionata per l'estrazione:</span><span class="sxs-lookup"><span data-stu-id="e8b04-119">The following code example demonstrates how to determine whether a track is selected for ripping:</span></span>


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



<span data-ttu-id="e8b04-120">Nell'esempio di codice riportato di seguito viene illustrato come specificare se è selezionata una traccia per l'estrazione.</span><span class="sxs-lookup"><span data-stu-id="e8b04-120">The following code example demonstrates how to specify whether a track is selected for ripping.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e8b04-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8b04-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8b04-122">**Copia di un CD**</span><span class="sxs-lookup"><span data-stu-id="e8b04-122">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="e8b04-123">**Recupero dell'interfaccia di copia da CD**</span><span class="sxs-lookup"><span data-stu-id="e8b04-123">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="e8b04-124">**Avvio del processo RIP**</span><span class="sxs-lookup"><span data-stu-id="e8b04-124">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="e8b04-125">**Recupero dello stato di RIP**</span><span class="sxs-lookup"><span data-stu-id="e8b04-125">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> </dl>

 

 




