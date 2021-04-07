---
title: Eseguire il mapping tra le dichiarazioni D3D9 e D3D8
description: Questa tabella esegue il mapping dei membri di una dichiarazione D3DVERTEXELEMENT9 a una dichiarazione Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745551"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a><span data-ttu-id="4fc77-103">Eseguire il mapping tra le dichiarazioni D3D9 e D3D8</span><span class="sxs-lookup"><span data-stu-id="4fc77-103">Map between D3D9 and D3D8 declarations</span></span>

<span data-ttu-id="4fc77-104">Questa tabella esegue il mapping dei membri di una Dichiarazione [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) a una dichiarazione Direct3D 8.</span><span class="sxs-lookup"><span data-stu-id="4fc77-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a Direct3D 8 declaration.</span></span>



| <span data-ttu-id="4fc77-105">Utilizzo di Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="4fc77-105">Direct3D 9 Usage</span></span>           | <span data-ttu-id="4fc77-106">Indice di utilizzo di Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="4fc77-106">Direct3D 9 Usage index</span></span> | <span data-ttu-id="4fc77-107">Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="4fc77-107">Direct3D 8</span></span>            |
|----------------------------|------------------------|-----------------------|
| <span data-ttu-id="4fc77-108">\_Posizione D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc77-108">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="4fc77-109">0</span><span class="sxs-lookup"><span data-stu-id="4fc77-109">0</span></span>                      | <span data-ttu-id="4fc77-110">\_Posizione D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="4fc77-110">D3DVSDE\_POSITION</span></span>     |
| <span data-ttu-id="4fc77-111">\_Posizione D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc77-111">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="4fc77-112">1</span><span class="sxs-lookup"><span data-stu-id="4fc77-112">1</span></span>                      | <span data-ttu-id="4fc77-113">\_POSITION2 D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="4fc77-113">D3DVSDE\_POSITION2</span></span>    |
| <span data-ttu-id="4fc77-114">D3DDECLUSAGE \_ normale</span><span class="sxs-lookup"><span data-stu-id="4fc77-114">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="4fc77-115">0</span><span class="sxs-lookup"><span data-stu-id="4fc77-115">0</span></span>                      | <span data-ttu-id="4fc77-116">D3DVSDE \_ normale</span><span class="sxs-lookup"><span data-stu-id="4fc77-116">D3DVSDE\_NORMAL</span></span>       |
| <span data-ttu-id="4fc77-117">D3DDECLUSAGE \_ normale</span><span class="sxs-lookup"><span data-stu-id="4fc77-117">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="4fc77-118">1</span><span class="sxs-lookup"><span data-stu-id="4fc77-118">1</span></span>                      | <span data-ttu-id="4fc77-119">\_NORMAL2 D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="4fc77-119">D3DVSDE\_NORMAL2</span></span>      |
| <span data-ttu-id="4fc77-120">\_BLENDWEIGHT D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc77-120">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="4fc77-121">0</span><span class="sxs-lookup"><span data-stu-id="4fc77-121">0</span></span>                      | <span data-ttu-id="4fc77-122">\_BLENDWEIGHT D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="4fc77-122">D3DVSDE\_BLENDWEIGHT</span></span>  |
| <span data-ttu-id="4fc77-123">\_BLENDINDICES D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc77-123">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="4fc77-124">0</span><span class="sxs-lookup"><span data-stu-id="4fc77-124">0</span></span>                      | <span data-ttu-id="4fc77-125">\_BLENDINDICES D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="4fc77-125">D3DVSDE\_BLENDINDICES</span></span> |
| <span data-ttu-id="4fc77-126">\_PSIZE D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc77-126">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="4fc77-127">0</span><span class="sxs-lookup"><span data-stu-id="4fc77-127">0</span></span>                      | <span data-ttu-id="4fc77-128">\_PSIZE D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="4fc77-128">D3DVSDE\_PSIZE</span></span>        |
| <span data-ttu-id="4fc77-129">\_Colore D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc77-129">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="4fc77-130">0</span><span class="sxs-lookup"><span data-stu-id="4fc77-130">0</span></span>                      | <span data-ttu-id="4fc77-131">D3DVSDE \_ diffuse</span><span class="sxs-lookup"><span data-stu-id="4fc77-131">D3DVSDE\_DIFFUSE</span></span>      |
| <span data-ttu-id="4fc77-132">\_Colore D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc77-132">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="4fc77-133">1</span><span class="sxs-lookup"><span data-stu-id="4fc77-133">1</span></span>                      | <span data-ttu-id="4fc77-134">D3DVSDE \_ speculare</span><span class="sxs-lookup"><span data-stu-id="4fc77-134">D3DVSDE\_SPECULAR</span></span>     |
| <span data-ttu-id="4fc77-135">\_TEXCOORD D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc77-135">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="4fc77-136">n</span><span class="sxs-lookup"><span data-stu-id="4fc77-136">n</span></span>                      | <span data-ttu-id="4fc77-137">\_TEXCOORDN D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="4fc77-137">D3DVSDE\_TEXCOORDn</span></span>    |



 

<span data-ttu-id="4fc77-138">Quando si usa una dichiarazione con l'elaborazione dei vertici hardware in un driver Direct3D 7, il runtime di Direct3D lo converte in una FVF con le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="4fc77-138">When a declaration is used with hardware vertex processing on a Direct3D 7 driver, the Direct3D runtime converts it to a FVF with the following rules:</span></span>

-   <span data-ttu-id="4fc77-139">È necessario usare solo il flusso 0 (evidente dal limite MaxStreams).</span><span class="sxs-lookup"><span data-stu-id="4fc77-139">Only stream 0 should be used (evident from the MaxStreams cap).</span></span>
-   <span data-ttu-id="4fc77-140">L'ordine degli elementi Vertex deve essere uguale a quello di FVF bit.</span><span class="sxs-lookup"><span data-stu-id="4fc77-140">The order of vertex elements should be the same as order of FVF bits.</span></span>
-   <span data-ttu-id="4fc77-141">Non sono consentiti gap nelle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="4fc77-141">Gaps in texture coordinates are not allowed.</span></span>
-   <span data-ttu-id="4fc77-142">Qualsiasi elemento Vertex non descritto la tabella non può essere convertito in un FVF valido per tutti i driver pre-DirectX 8 e, di conseguenza, non può essere usato in questi driver.</span><span class="sxs-lookup"><span data-stu-id="4fc77-142">Any vertex element not described the table cannot be converted into a valid FVF for all pre-DirectX 8 drivers and, hence, cannot be used on those drivers.</span></span>
-   <span data-ttu-id="4fc77-143">Solo D3DDECLTYPE \_ FLOAT2 è consentito per gli elementi Vertex con D3DDECLUSAGE \_ TEXCOORD se il dispositivo non imposta una delle \_ estremità D3DPTEXTURECAPS previste o \_ D3DPTEXTURECAPS mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="4fc77-143">Only D3DDECLTYPE\_FLOAT2 is allowed for vertex elements with D3DDECLUSAGE\_TEXCOORD if device does not set either of the D3DPTEXTURECAPS\_PROJECTED or D3DPTEXTURECAPS\_CUBEMAP caps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fc77-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4fc77-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fc77-145">Dichiarazione vertici</span><span class="sxs-lookup"><span data-stu-id="4fc77-145">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



