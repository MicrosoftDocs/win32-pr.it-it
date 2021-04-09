---
description: Le enumerazioni seguenti vengono utilizzate per specificare le informazioni sulla creazione e l'accesso alle risorse durante il rendering.
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: Enumerazioni di risorse (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ae6e115fe8ae9a731e5778b986940cb17a915d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049290"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a><span data-ttu-id="01779-103">Enumerazioni di risorse (grafica Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="01779-103">Resource Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="01779-104">Le enumerazioni seguenti vengono utilizzate per specificare le informazioni sulla creazione e l'accesso alle risorse durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="01779-104">The following enumerations are used to specify information about how resources are created and accessed during rendering.</span></span>



| <span data-ttu-id="01779-105">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="01779-105">Enumeration</span></span>                                                     | <span data-ttu-id="01779-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01779-106">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01779-107">**\_Flag di binding D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="01779-107">**D3D10\_BIND\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | <span data-ttu-id="01779-108">Consente di identificare la modalità di utilizzo di una risorsa da parte della pipeline e di determinare le fasi della pipeline a cui è possibile associare una risorsa.</span><span class="sxs-lookup"><span data-stu-id="01779-108">Identifies how a resource will be used by the pipeline and determines which pipeline stage(s) a resource can be bound to.</span></span> |
| [<span data-ttu-id="01779-109">**\_Flag di \_ accesso alla CPU D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="01779-109">**D3D10\_CPU\_ACCESS\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | <span data-ttu-id="01779-110">Specifica i tipi di accesso alla CPU consentiti per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="01779-110">Specifies the types of CPU access allowed for a resource.</span></span>                                                                 |
| [<span data-ttu-id="01779-111">**\_Dimensione DSV \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="01779-111">**D3D10\_DSV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | <span data-ttu-id="01779-112">Specifica la modalità di accesso a una risorsa utilizzata in una visualizzazione di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="01779-112">Specifies how to access a resource that is used in a depth-stencil view.</span></span>                                                  |
| [<span data-ttu-id="01779-113">**\_Mappa D3D10**</span><span class="sxs-lookup"><span data-stu-id="01779-113">**D3D10\_MAP**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | <span data-ttu-id="01779-114">Identifica una risorsa di cui eseguire il mapping per la lettura e la scrittura da parte della CPU.</span><span class="sxs-lookup"><span data-stu-id="01779-114">Identifies a resource to be mapped for reading and writing by the CPU.</span></span>                                                    |
| [<span data-ttu-id="01779-115">**\_Flag mappa \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="01779-115">**D3D10\_MAP\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | <span data-ttu-id="01779-116">Specifica il modo in cui la CPU deve rispondere a qualsiasi metodo della mappa quando la GPU non è ancora terminata con la risorsa.</span><span class="sxs-lookup"><span data-stu-id="01779-116">Specifies how the CPU should respond to any Map methods when the GPU is not yet finished with the resource.</span></span>               |
| [<span data-ttu-id="01779-117">**\_Dimensione della risorsa D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="01779-117">**D3D10\_RESOURCE\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | <span data-ttu-id="01779-118">Identifica il tipo di risorsa in uso.</span><span class="sxs-lookup"><span data-stu-id="01779-118">Identifies the type of resource that is in use.</span></span>                                                                           |
| [<span data-ttu-id="01779-119">**\_ \_ Flag varie della risorsa D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="01779-119">**D3D10\_RESOURCE\_MISC\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | <span data-ttu-id="01779-120">Identifica le opzioni di creazione di risorse meno comuni.</span><span class="sxs-lookup"><span data-stu-id="01779-120">Identifies less common resource creation options.</span></span>                                                                         |
| [<span data-ttu-id="01779-121">**\_Dimensione D3D10 RTV \_**</span><span class="sxs-lookup"><span data-stu-id="01779-121">**D3D10\_RTV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | <span data-ttu-id="01779-122">Specifica come accedere a una risorsa utilizzata in una visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="01779-122">Specifies how to access a resource used in a render target view.</span></span>                                                          |
| [<span data-ttu-id="01779-123">**Utilizzo di D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="01779-123">**D3D10\_USAGE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | <span data-ttu-id="01779-124">Identifica il modo in cui una risorsa deve essere letta e scritta dalla CPU e/o dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="01779-124">Identifies how a resource is expected to be read and written by the CPU and/or the GPU.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="01779-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01779-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01779-126">Riferimento alla risorsa</span><span class="sxs-lookup"><span data-stu-id="01779-126">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



