---
description: Nell'elenco seguente sono inclusi i metodi pubblici CMSPCallMultiGraph chiamati dal pool di thread.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: Metodi pubblici CMSPCallMultiGraph, chiamati dal pool di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312721"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a><span data-ttu-id="cc634-103">Metodi pubblici CMSPCallMultiGraph, chiamati dal pool di thread</span><span class="sxs-lookup"><span data-stu-id="cc634-103">CMSPCallMultiGraph Public Methods, Called by Thread Pool</span></span>



| <span data-ttu-id="cc634-104">Metodi pubblici CMSPCallMultiGraph</span><span class="sxs-lookup"><span data-stu-id="cc634-104">CMSPCallMultiGraph public methods</span></span>                                   | <span data-ttu-id="cc634-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc634-105">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc634-106">**DispatchGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="cc634-106">**DispatchGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | <span data-ttu-id="cc634-107">Chiamato quando il grafico del filtro segnala un evento.</span><span class="sxs-lookup"><span data-stu-id="cc634-107">Called when the filter graph signals an event.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="cc634-108">**HandleGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="cc634-108">**HandleGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | <span data-ttu-id="cc634-109">Chiamato dal metodo statico [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) .</span><span class="sxs-lookup"><span data-stu-id="cc634-109">Called by the [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) static method.</span></span> <span data-ttu-id="cc634-110">Code [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) nel thread di lavoro msp principale.</span><span class="sxs-lookup"><span data-stu-id="cc634-110">Queues [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) on the main MSP worker thread.</span></span> |
| [<span data-ttu-id="cc634-111">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="cc634-111">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | <span data-ttu-id="cc634-112">Consente all'istanza dell'oggetto chiamata MSP di gestire l'evento Filter Graph.</span><span class="sxs-lookup"><span data-stu-id="cc634-112">Allows the MSP call object instance to handle the filter graph event.</span></span>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="cc634-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc634-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc634-114">**CMSPCallMultiGraph**</span><span class="sxs-lookup"><span data-stu-id="cc634-114">**CMSPCallMultiGraph**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



