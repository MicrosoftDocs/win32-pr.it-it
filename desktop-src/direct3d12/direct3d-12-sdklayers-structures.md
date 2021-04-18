---
title: Strutture del livello di debug
description: Le strutture seguenti sono dichiarate in d3d12sdklayers. h.
ms.assetid: FE8796A7-98D1-4333-8755-2A47567560B3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573d49d34c4432796ebac68ce004f265259b9eb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298859"
---
# <a name="debug-layer-structures"></a><span data-ttu-id="eddf7-103">Strutture del livello di debug</span><span class="sxs-lookup"><span data-stu-id="eddf7-103">Debug Layer Structures</span></span>

<span data-ttu-id="eddf7-104">Le strutture seguenti sono dichiarate in d3d12sdklayers. h.</span><span class="sxs-lookup"><span data-stu-id="eddf7-104">The following structures are declared in d3d12sdklayers.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eddf7-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="eddf7-105">In this section</span></span>



| <span data-ttu-id="eddf7-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="eddf7-106">Topic</span></span>                                                                                                                                      | <span data-ttu-id="eddf7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eddf7-107">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eddf7-108">**\_Impostazioni di \_ \_ \_ \_ convalida basate su GPU \_ per l'elenco dei \_ comandi di debug D3D12**</span><span class="sxs-lookup"><span data-stu-id="eddf7-108">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)<br/> | <span data-ttu-id="eddf7-109">Descrive le impostazioni dell'elenco di comandi usate dalla convalida GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="eddf7-109">Describes per-command-list settings used by GPU-Based Validation.</span></span> <br/>                                                        |
| [<span data-ttu-id="eddf7-110">**\_Impostazioni di \_ \_ \_ convalida basate su \_ GPU \_ del dispositivo debug D3D12**</span><span class="sxs-lookup"><span data-stu-id="eddf7-110">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)<br/>              | <span data-ttu-id="eddf7-111">Descrive le impostazioni utilizzate dalla convalida GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="eddf7-111">Describes settings used by GPU-Based Validation.</span></span> <br/>                                                                         |
| [<span data-ttu-id="eddf7-112">**\_Fattore di \_ \_ prestazioni del \_ rallentamento GPU \_ del dispositivo \_ di debug D3D12**</span><span class="sxs-lookup"><span data-stu-id="eddf7-112">**D3D12\_DEBUG\_DEVICE\_GPU\_SLOWDOWN\_PERFORMANCE\_FACTOR**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor)<br/>          | <span data-ttu-id="eddf7-113">Descrive la quantità di rallentamento artificiale inserito dal dispositivo di debug per simulare schede grafiche con prestazioni inferiori.</span><span class="sxs-lookup"><span data-stu-id="eddf7-113">Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.</span></span><br/> |
| [<span data-ttu-id="eddf7-114">**\_ \_ Filtro coda informazioni \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="eddf7-114">**D3D12\_INFO\_QUEUE\_FILTER**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)<br/>                                                                   | <span data-ttu-id="eddf7-115">Filtro messaggi di debug; contiene un elenco di tipi di messaggi da concedere o negare.</span><span class="sxs-lookup"><span data-stu-id="eddf7-115">Debug message filter; contains a lists of message types to allow or deny.</span></span><br/>                                                 |
| [<span data-ttu-id="eddf7-116">**\_ \_ \_ Descrizione filtro coda informazioni \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="eddf7-116">**D3D12\_INFO\_QUEUE\_FILTER\_DESC**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter_desc)<br/>                                                        | <span data-ttu-id="eddf7-117">Consentire o negare a determinati tipi di messaggi di passare attraverso un filtro.</span><span class="sxs-lookup"><span data-stu-id="eddf7-117">Allow or deny certain types of messages to pass through a filter.</span></span><br/>                                                         |
| [<span data-ttu-id="eddf7-118">**\_Messaggio D3D12**</span><span class="sxs-lookup"><span data-stu-id="eddf7-118">**D3D12\_MESSAGE**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message)<br/>                                                                                         | <span data-ttu-id="eddf7-119">Messaggio di debug nella coda delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="eddf7-119">A debug message in the Information Queue.</span></span><br/>                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="eddf7-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eddf7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eddf7-121">Configurazione dell'ambiente di programmazione Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eddf7-121">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="eddf7-122">Riferimento al livello di debug</span><span class="sxs-lookup"><span data-stu-id="eddf7-122">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="eddf7-123">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eddf7-123">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





