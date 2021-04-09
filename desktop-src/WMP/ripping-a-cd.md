---
title: Copia di un CD
description: Copia di un CD
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping di CD, informazioni
- ripping di CDs, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856573"
---
# <a name="ripping-a-cd"></a><span data-ttu-id="dfb96-112">Copia di un CD</span><span class="sxs-lookup"><span data-stu-id="dfb96-112">Ripping a CD</span></span>

<span data-ttu-id="dfb96-113">È possibile copiare un CD usando il controllo Media Player di Windows in due modi.</span><span class="sxs-lookup"><span data-stu-id="dfb96-113">There are two ways to rip a CD by using the Windows Media Player control.</span></span> <span data-ttu-id="dfb96-114">Windows Media Player 9 è in grado di rippare CDs usando **IWMPPlayerServices:: setTaskPane**.</span><span class="sxs-lookup"><span data-stu-id="dfb96-114">Windows Media Player 9 can rip CDs by using **IWMPPlayerServices::setTaskPane**.</span></span> <span data-ttu-id="dfb96-115">Windows Media Player 11 introduce l'interfaccia **IWMPCdromRip** per rippare CDS.</span><span class="sxs-lookup"><span data-stu-id="dfb96-115">Windows Media Player 11 introduces the **IWMPCdromRip** interface for ripping CDs.</span></span> <span data-ttu-id="dfb96-116">Questa interfaccia offre più funzionalità di **IWMPPlayerServices:: setTaskPane** ed è consigliabile usare **IWMPCdromRip** se disponibile.</span><span class="sxs-lookup"><span data-stu-id="dfb96-116">This interface provides more functionality than **IWMPPlayerServices::setTaskPane**, and it is recommended that you use **IWMPCdromRip** if it is available.</span></span>

<span data-ttu-id="dfb96-117">Le sezioni seguenti descrivono come rippare un CD usando Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="dfb96-117">The following sections describe how to rip a CD by using Windows Media Player.</span></span>

-   [<span data-ttu-id="dfb96-118">Ripping mediante l'interfaccia IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="dfb96-118">Ripping by Using the IWMPCdromRip Interface</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [<span data-ttu-id="dfb96-119">Estrazione tramite IWMPPlayerServices:: setTaskPane</span><span class="sxs-lookup"><span data-stu-id="dfb96-119">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a><span data-ttu-id="dfb96-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dfb96-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfb96-121">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="dfb96-121">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




