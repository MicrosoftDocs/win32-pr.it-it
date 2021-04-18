---
title: Attributi delle risorse comuni
description: Le istruzioni per la definizione delle risorse supportate in Windows a 16 bit includono un'opzione Load-MEM che specifica le caratteristiche di caricamento e memoria della risorsa.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298459"
---
# <a name="common-resource-attributes"></a><span data-ttu-id="0bfe8-103">Attributi delle risorse comuni</span><span class="sxs-lookup"><span data-stu-id="0bfe8-103">Common Resource Attributes</span></span>

<span data-ttu-id="0bfe8-104">Le istruzioni per la definizione delle risorse supportate in Windows a 16 bit includono un'opzione *Load-MEM* che specifica le caratteristiche di caricamento e memoria della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-104">The resource-definition statements supported on 16-bit Windows include a *load-mem* option that specifies the loading and memory characteristics of the resource.</span></span> <span data-ttu-id="0bfe8-105">Questi attributi sono consentiti negli script di risorse per la compatibilità con le versioni precedenti, ma vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-105">These attributes are permitted in resource scripts for backward compatibility, but they are ignored.</span></span> <span data-ttu-id="0bfe8-106">Le risorse di Windows vengono caricate quando viene caricato il modulo corrispondente e vengono liberate quando il modulo viene scaricato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-106">Windows resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

## <a name="load-attributes"></a><span data-ttu-id="0bfe8-107">Carica attributi</span><span class="sxs-lookup"><span data-stu-id="0bfe8-107">Load Attributes</span></span>

<span data-ttu-id="0bfe8-108">Gli attributi Load specificano quando deve essere caricata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-108">The load attributes specify when the resource is to be loaded.</span></span> <span data-ttu-id="0bfe8-109">Il parametro Load deve essere uno degli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-109">The load parameter must be one of the following attributes.</span></span>



| <span data-ttu-id="0bfe8-110">Attributo</span><span class="sxs-lookup"><span data-stu-id="0bfe8-110">Attribute</span></span>      | <span data-ttu-id="0bfe8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bfe8-111">Description</span></span>                                                                  |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0bfe8-112">**PRECARICARE**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-112">**PRELOAD**</span></span>    | <span data-ttu-id="0bfe8-113">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-113">Ignored.</span></span> <span data-ttu-id="0bfe8-114">In Windows a 16 bit la risorsa viene caricata con il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-114">In 16-bit Windows, the resource is loaded with the executable file.</span></span> |
| <span data-ttu-id="0bfe8-115">**LOADONCALL**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-115">**LOADONCALL**</span></span> | <span data-ttu-id="0bfe8-116">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-116">Ignored.</span></span> <span data-ttu-id="0bfe8-117">Nelle finestre a 16 bit la risorsa viene caricata quando viene chiamata.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-117">In 16-bit Windows, the resource is loaded when called.</span></span>              |



 

## <a name="memory-attributes"></a><span data-ttu-id="0bfe8-118">Attributi di memoria</span><span class="sxs-lookup"><span data-stu-id="0bfe8-118">Memory Attributes</span></span>

<span data-ttu-id="0bfe8-119">Gli attributi di memoria specificano se la risorsa è fissa o spostata, se è annullabile e se è pura.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-119">The memory attributes specify whether the resource is fixed or movable, whether it is discardable, and whether it is pure.</span></span> <span data-ttu-id="0bfe8-120">Il parametro Memory può essere costituito da uno o più degli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-120">The memory parameter can be one or more of the following attributes.</span></span>



| <span data-ttu-id="0bfe8-121">Attributo</span><span class="sxs-lookup"><span data-stu-id="0bfe8-121">Attribute</span></span>       | <span data-ttu-id="0bfe8-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bfe8-122">Description</span></span>                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bfe8-123">**FIXED**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-123">**FIXED**</span></span>       | <span data-ttu-id="0bfe8-124">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-124">Ignored.</span></span> <span data-ttu-id="0bfe8-125">Nelle finestre a 16 bit la risorsa rimane in una posizione di memoria fissa.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-125">In 16-bit Windows, the resource remains at a fixed memory location.</span></span>                                                              |
| <span data-ttu-id="0bfe8-126">**SPOSTABILE**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-126">**MOVEABLE**</span></span>    | <span data-ttu-id="0bfe8-127">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-127">Ignored.</span></span> <span data-ttu-id="0bfe8-128">Nelle finestre a 16 bit è possibile spostare la risorsa se necessario per compattare la memoria.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-128">In 16-bit Windows, the resource can be moved if necessary to compact memory.</span></span>                                                     |
| <span data-ttu-id="0bfe8-129">**ANNULLABILE**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-129">**DISCARDABLE**</span></span> | <span data-ttu-id="0bfe8-130">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-130">Ignored.</span></span> <span data-ttu-id="0bfe8-131">Nelle finestre a 16 bit la risorsa può essere eliminata se non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-131">In 16-bit Windows, the resource can be discarded if no longer needed.</span></span>                                                            |
| <span data-ttu-id="0bfe8-132">**PURO**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-132">**PURE**</span></span>        | <span data-ttu-id="0bfe8-133">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-133">Ignored.</span></span> <span data-ttu-id="0bfe8-134">Accettato per la compatibilità con gli script di risorse esistenti.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-134">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="0bfe8-135">**IMPURO**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-135">**IMPURE**</span></span>      | <span data-ttu-id="0bfe8-136">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-136">Ignored.</span></span> <span data-ttu-id="0bfe8-137">Accettato per la compatibilità con gli script di risorse esistenti.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-137">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="0bfe8-138">**CONDIVISO**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-138">**SHARED**</span></span>      | <span data-ttu-id="0bfe8-139">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-139">Ignored.</span></span> <span data-ttu-id="0bfe8-140">In Windows a 16 bit, SHARED viene ignorato per i moduli normali.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-140">In 16-bit Windows, SHARED is ignored for regular modules.</span></span> <span data-ttu-id="0bfe8-141">Per una risorsa da un modulo Windows ROM, la memoria è condivisa.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-141">For a resource from a ROM Windows module, the memory is shared.</span></span>        |
| <span data-ttu-id="0bfe8-142">**NONSHARED**</span><span class="sxs-lookup"><span data-stu-id="0bfe8-142">**NONSHARED**</span></span>   | <span data-ttu-id="0bfe8-143">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-143">Ignored.</span></span> <span data-ttu-id="0bfe8-144">In Windows a 16 bit, non condiviso viene ignorato per i moduli normali.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-144">In 16-bit Windows, NONSHARED is ignored for regular modules.</span></span> <span data-ttu-id="0bfe8-145">Per una risorsa da un modulo Windows ROM, la memoria non è condivisa.</span><span class="sxs-lookup"><span data-stu-id="0bfe8-145">For a resource from a ROM Windows module, the memory is not shared.</span></span> |



 

 

 




