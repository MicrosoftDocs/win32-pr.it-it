---
title: Cancellazione di un CD riscrivibile
description: Cancellazione di un CD riscrivibile
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, cancellazione di CDs riscrivibili
- masterizzazione di CDs, cancellazione di CDs riscrivibili
- cancellazione di CDs riscrivibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046308"
---
# <a name="erasing-a-rewritable-cd"></a><span data-ttu-id="03756-113">Cancellazione di un CD riscrivibile</span><span class="sxs-lookup"><span data-stu-id="03756-113">Erasing a Rewritable CD</span></span>

<span data-ttu-id="03756-114">L'interfaccia [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) fornisce un metodo per cancellare i dischi CD-RW.</span><span class="sxs-lookup"><span data-stu-id="03756-114">The [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface provides a method for erasing CD-RW discs.</span></span> <span data-ttu-id="03756-115">Prima di cancellare un CD, è prima necessario assicurarsi che l'operazione sia supportata.</span><span class="sxs-lookup"><span data-stu-id="03756-115">Before erasing a CD, you must first ensure that the operation is supported.</span></span> <span data-ttu-id="03756-116">Per ulteriori informazioni, vedere [recupero dello stato dell'unità e del disco](retrieving-the-drive-and-disc-status.md).</span><span class="sxs-lookup"><span data-stu-id="03756-116">For more information, see [Retrieving the Drive and Disc Status](retrieving-the-drive-and-disc-status.md).</span></span>

<span data-ttu-id="03756-117">Per iniziare a cancellare il contenuto di un CD riscrivibile, chiamare [IWMPCdromBurn:: erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="03756-117">To begin erasing the contents of a rewritable CD, call [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span>


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a><span data-ttu-id="03756-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03756-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03756-119">**Masterizzazione di un CD**</span><span class="sxs-lookup"><span data-stu-id="03756-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="03756-120">**Recupero dell'interfaccia di masterizzazione CD**</span><span class="sxs-lookup"><span data-stu-id="03756-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="03756-121">**Avvio del processo di masterizzazione**</span><span class="sxs-lookup"><span data-stu-id="03756-121">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="03756-122">**Recupero dello stato dell'unità e del disco**</span><span class="sxs-lookup"><span data-stu-id="03756-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="03756-123">**Recupero dello stato di masterizzazione**</span><span class="sxs-lookup"><span data-stu-id="03756-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




