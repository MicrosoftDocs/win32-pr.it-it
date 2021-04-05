---
title: Recupero dell'interfaccia di masterizzazione CD
description: Recupero dell'interfaccia di masterizzazione CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, recupero dell'interfaccia IWMPCdromCollection
- masterizzazione di CDs, recupero dell'interfaccia IWMPCdromCollection
- Interfaccia IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046425"
---
# <a name="retrieving-the-cd-burning-interface"></a><span data-ttu-id="686e0-113">Recupero dell'interfaccia di masterizzazione CD</span><span class="sxs-lookup"><span data-stu-id="686e0-113">Retrieving the CD Burning Interface</span></span>

<span data-ttu-id="686e0-114">Per enumerare le unità CD nel computer dell'utente, usare l'interfaccia **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="686e0-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="686e0-115">Per recuperare un puntatore a questa interfaccia, chiamare [IWMPCore:: Get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="686e0-115">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="686e0-116">Usando i metodi **get \_ count** e **Item** , è possibile eseguire l'iterazione della raccolta per recuperare un puntatore di interfaccia [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) per ogni unità CD nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="686e0-116">By using the **get\_count** and **item** methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface pointer for each CD drive on the user's computer.</span></span>

<span data-ttu-id="686e0-117">L'interfaccia **IWMPCdrom** rappresenta una singola unità CD.</span><span class="sxs-lookup"><span data-stu-id="686e0-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="686e0-118">Prima di iniziare a masterizzare un CD, è prima necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare un puntatore all'interfaccia [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .</span><span class="sxs-lookup"><span data-stu-id="686e0-118">Before you begin burning a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface.</span></span>

<span data-ttu-id="686e0-119">Nell'esempio di codice seguente viene illustrato come recuperare un'interfaccia per la masterizzazione di un CD in un'unità specifica:</span><span class="sxs-lookup"><span data-stu-id="686e0-119">The following code example demonstrates how to retrieve an interface for burning a CD to a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="686e0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="686e0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="686e0-121">**Masterizzazione di un CD**</span><span class="sxs-lookup"><span data-stu-id="686e0-121">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="686e0-122">**Avvio del processo di masterizzazione**</span><span class="sxs-lookup"><span data-stu-id="686e0-122">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="686e0-123">**Cancellazione di un CD riscrivibile**</span><span class="sxs-lookup"><span data-stu-id="686e0-123">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="686e0-124">**Recupero dello stato dell'unità e del disco**</span><span class="sxs-lookup"><span data-stu-id="686e0-124">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="686e0-125">**Recupero dello stato di masterizzazione**</span><span class="sxs-lookup"><span data-stu-id="686e0-125">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> <dt>

[<span data-ttu-id="686e0-126">**Interfaccia IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="686e0-126">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




