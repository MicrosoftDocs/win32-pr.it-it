---
title: Avvio del processo di masterizzazione
description: Avvio del processo di masterizzazione
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, avvio del processo di masterizzazione
- masterizzazione di CDs, avvio del processo di masterizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956202"
---
# <a name="starting-the-burn-process"></a><span data-ttu-id="fd73f-112">Avvio del processo di masterizzazione</span><span class="sxs-lookup"><span data-stu-id="fd73f-112">Starting the Burn Process</span></span>

<span data-ttu-id="fd73f-113">Prima che la masterizzazione possa iniziare, è necessario assegnare una playlist da masterizzare.</span><span class="sxs-lookup"><span data-stu-id="fd73f-113">Before burning can begin, you must assign a playlist to be burned.</span></span> <span data-ttu-id="fd73f-114">Usare [IWMPCdromBurn::p UT \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) per specificare una playlist per la masterizzazione.</span><span class="sxs-lookup"><span data-stu-id="fd73f-114">Use [IWMPCdromBurn::put\_burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) to specify a playlist for burning.</span></span>


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



<span data-ttu-id="fd73f-115">Per informazioni sull'uso delle playlist, vedere [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span><span class="sxs-lookup"><span data-stu-id="fd73f-115">For information about using playlists, see [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span></span>

<span data-ttu-id="fd73f-116">Per avviare l'operazione di masterizzazione, chiamare [IWMPCdromBurn:: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span><span class="sxs-lookup"><span data-stu-id="fd73f-116">To start the burning operation, call [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span></span>


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



<span data-ttu-id="fd73f-117">È possibile arrestare l'operazione di masterizzazione chiamando [IWMPCdromBurn:: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span><span class="sxs-lookup"><span data-stu-id="fd73f-117">You can stop the burning operation by calling [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span></span>


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a><span data-ttu-id="fd73f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd73f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd73f-119">**Masterizzazione di un CD**</span><span class="sxs-lookup"><span data-stu-id="fd73f-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="fd73f-120">**Recupero dell'interfaccia di masterizzazione CD**</span><span class="sxs-lookup"><span data-stu-id="fd73f-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="fd73f-121">**Cancellazione di un CD riscrivibile**</span><span class="sxs-lookup"><span data-stu-id="fd73f-121">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="fd73f-122">**Recupero dello stato dell'unità e del disco**</span><span class="sxs-lookup"><span data-stu-id="fd73f-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="fd73f-123">**Recupero dello stato di masterizzazione**</span><span class="sxs-lookup"><span data-stu-id="fd73f-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




