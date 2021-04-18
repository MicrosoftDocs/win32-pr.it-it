---
title: Avvio del processo RIP
description: Avvio del processo RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, avvio del processo RIP
- copia di CDs, avvio del processo RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299393"
---
# <a name="starting-the-rip-process"></a><span data-ttu-id="c7b07-112">Avvio del processo RIP</span><span class="sxs-lookup"><span data-stu-id="c7b07-112">Starting the Rip Process</span></span>

<span data-ttu-id="c7b07-113">Dopo aver recuperato l'interfaccia di strappo come illustrato nella sezione precedente, avviare il processo di ripping chiamando [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span><span class="sxs-lookup"><span data-stu-id="c7b07-113">After you have retrieved the ripping interface as explained in the previous section, start the ripping process by calling [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span>


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



<span data-ttu-id="c7b07-114">È possibile arrestare l'operazione di strappo chiamando [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span><span class="sxs-lookup"><span data-stu-id="c7b07-114">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a><span data-ttu-id="c7b07-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7b07-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7b07-116">**Copia di un CD**</span><span class="sxs-lookup"><span data-stu-id="c7b07-116">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="c7b07-117">**Recupero dell'interfaccia di copia da CD**</span><span class="sxs-lookup"><span data-stu-id="c7b07-117">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="c7b07-118">**Recupero dello stato di RIP**</span><span class="sxs-lookup"><span data-stu-id="c7b07-118">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="c7b07-119">**Selezione di elementi per l'estrazione**</span><span class="sxs-lookup"><span data-stu-id="c7b07-119">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




