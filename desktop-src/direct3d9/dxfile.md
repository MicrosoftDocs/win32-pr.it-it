---
description: I flag seguenti vengono usati per specificare i canali in una trama su cui operare. Deprecato.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Costanti DXFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42b20ca9934b9a4203e05f477ea8c40853a0a836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997298"
---
# <a name="dxfile-constants"></a><span data-ttu-id="60d19-104">Costanti DXFILE</span><span class="sxs-lookup"><span data-stu-id="60d19-104">DXFILE Constants</span></span>

<span data-ttu-id="60d19-105">I flag seguenti vengono usati per specificare i canali in una trama su cui operare.</span><span class="sxs-lookup"><span data-stu-id="60d19-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="60d19-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="60d19-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="60d19-107">DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="60d19-107">DXFILEFORMAT</span></span>



| <span data-ttu-id="60d19-108">\#Definire</span><span class="sxs-lookup"><span data-stu-id="60d19-108">\#define</span></span>                 | <span data-ttu-id="60d19-109">Valore</span><span class="sxs-lookup"><span data-stu-id="60d19-109">Value</span></span> | <span data-ttu-id="60d19-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d19-110">Description</span></span>      |
|--------------------------|-------|------------------|
| <span data-ttu-id="60d19-111">FILE BINARIO DXFILEFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="60d19-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="60d19-112">0</span><span class="sxs-lookup"><span data-stu-id="60d19-112">0</span></span>     | <span data-ttu-id="60d19-113">File binario.</span><span class="sxs-lookup"><span data-stu-id="60d19-113">Binary file.</span></span>     |
| <span data-ttu-id="60d19-114">TESTO \_ DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="60d19-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="60d19-115">1</span><span class="sxs-lookup"><span data-stu-id="60d19-115">1</span></span>     | <span data-ttu-id="60d19-116">File di testo.</span><span class="sxs-lookup"><span data-stu-id="60d19-116">Text file.</span></span>       |
| <span data-ttu-id="60d19-117">DXFILEFORMAT \_ COMPRESSO</span><span class="sxs-lookup"><span data-stu-id="60d19-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="60d19-118">2</span><span class="sxs-lookup"><span data-stu-id="60d19-118">2</span></span>     | <span data-ttu-id="60d19-119">File compresso.</span><span class="sxs-lookup"><span data-stu-id="60d19-119">Compressed file.</span></span> |



 

<span data-ttu-id="60d19-120">Queste \# definisce sono dichiarate in Dxfile.h.</span><span class="sxs-lookup"><span data-stu-id="60d19-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="60d19-121">DXFILELOADOPTIONS</span><span class="sxs-lookup"><span data-stu-id="60d19-121">DXFILELOADOPTIONS</span></span>



| <span data-ttu-id="60d19-122">\#Definire</span><span class="sxs-lookup"><span data-stu-id="60d19-122">\#define</span></span>                 | <span data-ttu-id="60d19-123">Valore</span><span class="sxs-lookup"><span data-stu-id="60d19-123">Value</span></span> | <span data-ttu-id="60d19-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d19-124">Description</span></span>                  |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="60d19-125">DXFILELOAD \_ FROMFILE</span><span class="sxs-lookup"><span data-stu-id="60d19-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="60d19-126">0x00L</span><span class="sxs-lookup"><span data-stu-id="60d19-126">0x00L</span></span> | <span data-ttu-id="60d19-127">Caricare un file da un file.</span><span class="sxs-lookup"><span data-stu-id="60d19-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="60d19-128">DXFILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="60d19-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="60d19-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="60d19-129">0x01L</span></span> | <span data-ttu-id="60d19-130">Caricare un file da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="60d19-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="60d19-131">DXFILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="60d19-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="60d19-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="60d19-132">0x02L</span></span> | <span data-ttu-id="60d19-133">Caricare un file dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="60d19-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="60d19-134">DXFILELOAD \_ FROMSTREAM</span><span class="sxs-lookup"><span data-stu-id="60d19-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="60d19-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="60d19-135">0x04L</span></span> | <span data-ttu-id="60d19-136">Caricare un file da un flusso.</span><span class="sxs-lookup"><span data-stu-id="60d19-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="60d19-137">DXFILELOAD \_ FROMURL</span><span class="sxs-lookup"><span data-stu-id="60d19-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="60d19-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="60d19-138">0x08L</span></span> | <span data-ttu-id="60d19-139">Caricare un file da un URL.</span><span class="sxs-lookup"><span data-stu-id="60d19-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="60d19-140">Queste \# definisce vengono dichiarate in Dxfile.h.</span><span class="sxs-lookup"><span data-stu-id="60d19-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60d19-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60d19-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60d19-142">Riferimento al file X (legacy)</span><span class="sxs-lookup"><span data-stu-id="60d19-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



