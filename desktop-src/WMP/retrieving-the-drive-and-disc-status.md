---
title: Recupero dello stato dell'unità e del disco
description: Recupero dello stato dell'unità e del disco
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, recupero dello stato di unità e dischi
- masterizzazione di CD, recupero dello stato di unità e dischi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858025"
---
# <a name="retrieving-the-drive-and-disc-status"></a><span data-ttu-id="7afa0-112">Recupero dello stato dell'unità e del disco</span><span class="sxs-lookup"><span data-stu-id="7afa0-112">Retrieving the Drive and Disc Status</span></span>

<span data-ttu-id="7afa0-113">Prima di avviare un'operazione di masterizzazione CD, è necessario verificare che l'unità CD-ROM selezionata supporti l'operazione che si desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="7afa0-113">Before starting a CD burning operation, you must ensure that the selected CD-ROM drive supports the operation you want to perform.</span></span> <span data-ttu-id="7afa0-114">È ad esempio necessario verificare che un CD sia in grado di essere cancellato prima di chiamare [IWMPCdromBurn:: erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="7afa0-114">For instance, you must check that a CD is capable of being erased before calling [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span> <span data-ttu-id="7afa0-115">Il codice seguente illustra un esempio dell'uso di [IWMPCdromBurn:: disavailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) per determinare se un'operazione è supportata:</span><span class="sxs-lookup"><span data-stu-id="7afa0-115">The following code shows an example of using [IWMPCdromBurn::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) to determine whether an operation is supported:</span></span>


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="7afa0-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7afa0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7afa0-117">**Masterizzazione di un CD**</span><span class="sxs-lookup"><span data-stu-id="7afa0-117">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="7afa0-118">**Recupero dell'interfaccia di masterizzazione CD**</span><span class="sxs-lookup"><span data-stu-id="7afa0-118">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="7afa0-119">**Avvio del processo di masterizzazione**</span><span class="sxs-lookup"><span data-stu-id="7afa0-119">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="7afa0-120">**Cancellazione di un CD riscrivibile**</span><span class="sxs-lookup"><span data-stu-id="7afa0-120">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="7afa0-121">**Recupero dello stato di masterizzazione**</span><span class="sxs-lookup"><span data-stu-id="7afa0-121">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




