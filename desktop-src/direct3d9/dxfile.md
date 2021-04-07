---
description: I flag seguenti vengono utilizzati per specificare i canali in una trama su cui operare. Deprecato.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Costanti DXFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f1651d17f5acb2ef24ff9dae2ef547c3df7c0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048991"
---
# <a name="dxfile-constants"></a><span data-ttu-id="58f2a-104">Costanti DXFILE</span><span class="sxs-lookup"><span data-stu-id="58f2a-104">DXFILE Constants</span></span>

<span data-ttu-id="58f2a-105">I flag seguenti vengono utilizzati per specificare i canali in una trama su cui operare.</span><span class="sxs-lookup"><span data-stu-id="58f2a-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="58f2a-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="58f2a-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="58f2a-107">DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="58f2a-107">DXFILEFORMAT</span></span>



|                          |       |                  |
|--------------------------|-------|------------------|
| <span data-ttu-id="58f2a-108">\#definire</span><span class="sxs-lookup"><span data-stu-id="58f2a-108">\#define</span></span>                 | <span data-ttu-id="58f2a-109">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2a-109">Value</span></span> | <span data-ttu-id="58f2a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58f2a-110">Description</span></span>      |
| <span data-ttu-id="58f2a-111">\_binario DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="58f2a-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="58f2a-112">0</span><span class="sxs-lookup"><span data-stu-id="58f2a-112">0</span></span>     | <span data-ttu-id="58f2a-113">File binario.</span><span class="sxs-lookup"><span data-stu-id="58f2a-113">Binary file.</span></span>     |
| <span data-ttu-id="58f2a-114">\_testo DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="58f2a-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="58f2a-115">1</span><span class="sxs-lookup"><span data-stu-id="58f2a-115">1</span></span>     | <span data-ttu-id="58f2a-116">File di testo.</span><span class="sxs-lookup"><span data-stu-id="58f2a-116">Text file.</span></span>       |
| <span data-ttu-id="58f2a-117">DXFILEFORMAT \_ compressi</span><span class="sxs-lookup"><span data-stu-id="58f2a-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="58f2a-118">2</span><span class="sxs-lookup"><span data-stu-id="58f2a-118">2</span></span>     | <span data-ttu-id="58f2a-119">File compresso.</span><span class="sxs-lookup"><span data-stu-id="58f2a-119">Compressed file.</span></span> |



 

<span data-ttu-id="58f2a-120">Queste \# definizioni sono dichiarate in dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="58f2a-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="58f2a-121">DXFILELOADOPTIONS</span><span class="sxs-lookup"><span data-stu-id="58f2a-121">DXFILELOADOPTIONS</span></span>



|                          |       |                              |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="58f2a-122">\#definire</span><span class="sxs-lookup"><span data-stu-id="58f2a-122">\#define</span></span>                 | <span data-ttu-id="58f2a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2a-123">Value</span></span> | <span data-ttu-id="58f2a-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58f2a-124">Description</span></span>                  |
| <span data-ttu-id="58f2a-125">\_FROMFILE DXFILELOAD</span><span class="sxs-lookup"><span data-stu-id="58f2a-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="58f2a-126">0x00L</span><span class="sxs-lookup"><span data-stu-id="58f2a-126">0x00L</span></span> | <span data-ttu-id="58f2a-127">Caricare un file da un file.</span><span class="sxs-lookup"><span data-stu-id="58f2a-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="58f2a-128">\_FROMRESOURCE DXFILELOAD</span><span class="sxs-lookup"><span data-stu-id="58f2a-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="58f2a-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="58f2a-129">0x01L</span></span> | <span data-ttu-id="58f2a-130">Caricare un file da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="58f2a-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="58f2a-131">\_FROMMEMORY DXFILELOAD</span><span class="sxs-lookup"><span data-stu-id="58f2a-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="58f2a-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="58f2a-132">0x02L</span></span> | <span data-ttu-id="58f2a-133">Caricare un file dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="58f2a-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="58f2a-134">\_FROMSTREAM DXFILELOAD</span><span class="sxs-lookup"><span data-stu-id="58f2a-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="58f2a-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="58f2a-135">0x04L</span></span> | <span data-ttu-id="58f2a-136">Caricare un file da un flusso.</span><span class="sxs-lookup"><span data-stu-id="58f2a-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="58f2a-137">\_FROMURL DXFILELOAD</span><span class="sxs-lookup"><span data-stu-id="58f2a-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="58f2a-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="58f2a-138">0x08L</span></span> | <span data-ttu-id="58f2a-139">Caricare un file da un URL.</span><span class="sxs-lookup"><span data-stu-id="58f2a-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="58f2a-140">Queste \# definizioni sono dichiarate in dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="58f2a-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58f2a-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58f2a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58f2a-142">Riferimento file X (legacy)</span><span class="sxs-lookup"><span data-stu-id="58f2a-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



