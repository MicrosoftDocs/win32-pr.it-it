---
title: Recupero dell'interfaccia di copia da CD
description: Recupero dell'interfaccia di copia da CD
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, interfaccia IWMPCdromRip
- ripping di CDs, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103858077"
---
# <a name="retrieving-the-ripping-interface"></a><span data-ttu-id="5d7fb-113">Recupero dell'interfaccia di copia da CD</span><span class="sxs-lookup"><span data-stu-id="5d7fb-113">Retrieving the Ripping Interface</span></span>

<span data-ttu-id="5d7fb-114">Per enumerare le unità CD nel computer dell'utente, usare l'interfaccia **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="5d7fb-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="5d7fb-115">Recuperare un puntatore a questa interfaccia chiamando [IWMPCore:: Get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="5d7fb-115">Retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="5d7fb-116">Usando i metodi [get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) e [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) , è possibile eseguire l'iterazione della raccolta per recuperare un'interfaccia [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) per ogni unità CD nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5d7fb-116">By using the [get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) and [item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface for each CD drive on the user's computer.</span></span>

<span data-ttu-id="5d7fb-117">L'interfaccia **IWMPCdrom** rappresenta una singola unità CD.</span><span class="sxs-lookup"><span data-stu-id="5d7fb-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="5d7fb-118">Prima di iniziare a rippare un CD, è prima necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare l'interfaccia [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .</span><span class="sxs-lookup"><span data-stu-id="5d7fb-118">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface.</span></span>

<span data-ttu-id="5d7fb-119">Nell'esempio di codice seguente viene illustrato come recuperare un'interfaccia per estrarre un CD da un'unità specifica:</span><span class="sxs-lookup"><span data-stu-id="5d7fb-119">The following code example demonstrates how to retrieve an interface for ripping a CD from a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="5d7fb-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d7fb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d7fb-121">**Copia di un CD**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-121">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="5d7fb-122">**Avvio del processo RIP**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-122">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="5d7fb-123">**Recupero dello stato di RIP**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-123">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="5d7fb-124">**Selezione di elementi per l'estrazione**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-124">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> <dt>

[<span data-ttu-id="5d7fb-125">**Interfaccia IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-125">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




