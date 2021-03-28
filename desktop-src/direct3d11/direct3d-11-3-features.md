---
title: Funzionalità di Direct3D 11,3
description: Le sezioni seguenti descrivono che la funzionalità è stata aggiunta in Direct3D 11,3. Queste funzionalità sono disponibili anche in Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399969"
---
# <a name="direct3d-113-features"></a><span data-ttu-id="8978c-104">Funzionalità di Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="8978c-104">Direct3D 11.3 Features</span></span>

<span data-ttu-id="8978c-105">Le sezioni seguenti descrivono che la funzionalità è stata aggiunta in Direct3D 11,3.</span><span class="sxs-lookup"><span data-stu-id="8978c-105">The following sections describe the functionality has been added in Direct3D 11.3.</span></span> <span data-ttu-id="8978c-106">Queste funzionalità sono disponibili anche in Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="8978c-106">These features are also available in Direct3D 12.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="8978c-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8978c-107">In this section</span></span>



| <span data-ttu-id="8978c-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="8978c-108">Topic</span></span>                                                                                               | <span data-ttu-id="8978c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8978c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8978c-110">Rasterizzazione conservativa</span><span class="sxs-lookup"><span data-stu-id="8978c-110">Conservative Rasterization</span></span>](conservative-rasterization.md)<br/>                             | <span data-ttu-id="8978c-111">La rasterizzazione conservativa aggiunge una certa certezza al rendering in pixel, che risulta utile in particolare per gli algoritmi di rilevamento dei conflitti.</span><span class="sxs-lookup"><span data-stu-id="8978c-111">Conservative rasterization adds some certainty to pixel rendering, which is helpful in particular to collision detection algorithms.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="8978c-112">Mapping trama predefinito</span><span class="sxs-lookup"><span data-stu-id="8978c-112">Default Texture Mapping</span></span>](default-texture-mapping.md)<br/>                                   | <span data-ttu-id="8978c-113">L'uso del mapping di trama predefinito riduce la copia e l'utilizzo della memoria e condivide i dati di immagine tra la GPU e la CPU.</span><span class="sxs-lookup"><span data-stu-id="8978c-113">The use of default texture mapping reduces copying and memory usage while sharing image data between the GPU and the CPU.</span></span> <span data-ttu-id="8978c-114">Tuttavia, deve essere usato solo in situazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="8978c-114">However, it should only be used in specific situations.</span></span> <span data-ttu-id="8978c-115">Il layout swizzle standard evita di copiare o swizzling i dati in più layout.</span><span class="sxs-lookup"><span data-stu-id="8978c-115">The standard swizzle layout avoids copying or swizzling data in multiple layouts.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="8978c-116">Visualizzazioni degli ordini di rasterizzatore</span><span class="sxs-lookup"><span data-stu-id="8978c-116">Rasterizer Order Views</span></span>](rasterizer-order-views.md)<br/>                                     | <span data-ttu-id="8978c-117">Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.</span><span class="sxs-lookup"><span data-stu-id="8978c-117">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="8978c-118">In questo modo è possibile utilizzare gli algoritmi OIT (Order Independent Transparency), che forniscono risultati di rendering migliori quando più oggetti trasparenti sono in linea tra loro in una vista.</span><span class="sxs-lookup"><span data-stu-id="8978c-118">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span> <br/> |
| [<span data-ttu-id="8978c-119">Valore di riferimento dello stencil specificato dello shader</span><span class="sxs-lookup"><span data-stu-id="8978c-119">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)<br/> | <span data-ttu-id="8978c-120">L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.</span><span class="sxs-lookup"><span data-stu-id="8978c-120">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="8978c-121">Caricamenti Unordered Access View tipizzati</span><span class="sxs-lookup"><span data-stu-id="8978c-121">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)<br/>               | <span data-ttu-id="8978c-122">Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un formato DXGI specifico \_ .</span><span class="sxs-lookup"><span data-stu-id="8978c-122">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="8978c-123">Architettura di memoria unificata</span><span class="sxs-lookup"><span data-stu-id="8978c-123">Unified Memory Architecture</span></span>](unified-memory-architecture.md)<br/>                           | <span data-ttu-id="8978c-124">L'esecuzione di query per determinare se l'architettura di memoria unificata (UMA) è supportata può contribuire a determinare come gestire alcune risorse.</span><span class="sxs-lookup"><span data-stu-id="8978c-124">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="8978c-125">Risorse affiancate al volume</span><span class="sxs-lookup"><span data-stu-id="8978c-125">Volume Tiled Resources</span></span>](volume-tiled-resources.md)<br/>                                     | <span data-ttu-id="8978c-126">Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.</span><span class="sxs-lookup"><span data-stu-id="8978c-126">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="8978c-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8978c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8978c-128">Novità di Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="8978c-128">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





