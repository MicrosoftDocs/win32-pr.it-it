---
title: Risorse
description: In questa sezione vengono descritti gli aspetti delle risorse Direct3D 11.
ms.assetid: 5b8b1198-73ed-4058-9fc6-a1c43902d732
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9ed73d81d2521fe97b36e6bfc8d71e387f8c9c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047620"
---
# <a name="resources"></a><span data-ttu-id="320b2-103">Risorse</span><span class="sxs-lookup"><span data-stu-id="320b2-103">Resources</span></span>

<span data-ttu-id="320b2-104">Le risorse forniscono i dati alla pipeline e definiscono gli elementi di cui viene eseguito il rendering durante la scena.</span><span class="sxs-lookup"><span data-stu-id="320b2-104">Resources provide data to the pipeline and define what is rendered during your scene.</span></span> <span data-ttu-id="320b2-105">Le risorse possono essere caricate dal supporto del gioco o create dinamicamente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="320b2-105">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="320b2-106">In genere, le risorse includono i dati di trama, i dati dei vertici e gli shader.</span><span class="sxs-lookup"><span data-stu-id="320b2-106">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="320b2-107">La maggior parte delle applicazioni Direct3D crea ed Elimina in modo estensivo le risorse per tutta la loro durata.</span><span class="sxs-lookup"><span data-stu-id="320b2-107">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span> <span data-ttu-id="320b2-108">In questa sezione vengono descritti gli aspetti delle risorse Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="320b2-108">This section describes aspects of Direct3D 11 resources.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="320b2-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="320b2-109">In this section</span></span>



| <span data-ttu-id="320b2-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="320b2-110">Topic</span></span>                                                                                             | <span data-ttu-id="320b2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="320b2-111">Description</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="320b2-112">Introduzione a una risorsa in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="320b2-112">Introduction to a Resource in Direct3D 11</span></span>](overviews-direct3d-11-resources-intro.md)<br/> | <span data-ttu-id="320b2-113">Questo argomento introduce risorse Direct3D, ad esempio buffer e trame.</span><span class="sxs-lookup"><span data-stu-id="320b2-113">This topic introduces Direct3D resources such as buffers and textures.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="320b2-114">Tipi di risorse</span><span class="sxs-lookup"><span data-stu-id="320b2-114">Types of Resources</span></span>](overviews-direct3d-11-resources-types.md)<br/>                        | <span data-ttu-id="320b2-115">Questo argomento descrive i tipi di risorse di Direct3D 10, nonché i nuovi tipi in Direct3D 11, inclusi i buffer strutturati e le trame scrivibili e i buffer.</span><span class="sxs-lookup"><span data-stu-id="320b2-115">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span><br/>                                                                       |
| [<span data-ttu-id="320b2-116">Limiti delle risorse</span><span class="sxs-lookup"><span data-stu-id="320b2-116">Resource Limits</span></span>](overviews-direct3d-11-resources-limits.md)<br/>                          | <span data-ttu-id="320b2-117">Questo argomento contiene un elenco di risorse supportate da Direct3D 11 (in particolare, il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 11 o 9. x).</span><span class="sxs-lookup"><span data-stu-id="320b2-117">This topic contains a list of resources that Direct3D 11 supports (specifically [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11 or 9.x hardware).</span></span><br/>                                 |
| [<span data-ttu-id="320b2-118">Sottorisorse</span><span class="sxs-lookup"><span data-stu-id="320b2-118">Subresources</span></span>](overviews-direct3d-11-resources-subresources.md)<br/>                       | <span data-ttu-id="320b2-119">Questo argomento descrive le sottorisorse di trama o parti di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="320b2-119">This topic describes texture subresources, or portions of a resource.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="320b2-120">Buffer</span><span class="sxs-lookup"><span data-stu-id="320b2-120">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)<br/>                                 | <span data-ttu-id="320b2-121">I buffer contengono dati usati per descrivere la geometria, indicizzare le informazioni sulla geometria e le costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="320b2-121">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="320b2-122">Questa sezione descrive i buffer usati in Direct3D 11 e i collegamenti alla documentazione basata su attività per gli scenari comuni.</span><span class="sxs-lookup"><span data-stu-id="320b2-122">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/> |
| [<span data-ttu-id="320b2-123">Trame</span><span class="sxs-lookup"><span data-stu-id="320b2-123">Textures</span></span>](overviews-direct3d-11-resources-textures.md)<br/>                               | <span data-ttu-id="320b2-124">Questa sezione descrive le trame usate in Direct3D 11 e i collegamenti alla documentazione basata su attività per gli scenari comuni.</span><span class="sxs-lookup"><span data-stu-id="320b2-124">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="320b2-125">Regole sui formati a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="320b2-125">Floating-point rules</span></span>](floating-point-rules.md)<br/>                                       | <span data-ttu-id="320b2-126">Direct3D 11 supporta diverse rappresentazioni a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="320b2-126">Direct3D 11 supports several floating-point representations.</span></span> <span data-ttu-id="320b2-127">Tutti i calcoli a virgola mobile operano in un subset definito delle regole a virgola mobile a precisione singola IEEE 754 32 bit.</span><span class="sxs-lookup"><span data-stu-id="320b2-127">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point rules.</span></span><br/>                                               |
| [<span data-ttu-id="320b2-128">Risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="320b2-128">Tiled resources</span></span>](tiled-resources.md)<br/>                                                 | <span data-ttu-id="320b2-129">Le risorse affiancate possono essere considerate come risorse logiche di grandi dimensioni che utilizzano piccole quantità di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="320b2-129">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span><br/>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="320b2-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="320b2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="320b2-131">Guida alla programmazione per Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="320b2-131">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





