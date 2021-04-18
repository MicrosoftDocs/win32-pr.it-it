---
description: Una dichiarazione vertici definisce il layout del buffer dei vertici e programma il motore a mosaico.
ms.assetid: 09dae498-3b33-4c33-bc7e-47f2bf784e4c
title: Dichiarazione vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c769aa6fb80de1fd83067ebb9f32b591baa8e883
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303842"
---
# <a name="vertex-declaration-direct3d-9"></a><span data-ttu-id="9742d-103">Dichiarazione vertici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9742d-103">Vertex Declaration (Direct3D 9)</span></span>

<span data-ttu-id="9742d-104">Una dichiarazione vertici definisce il layout del buffer dei vertici e programma il motore a mosaico.</span><span class="sxs-lookup"><span data-stu-id="9742d-104">A vertex declaration defines the vertex buffer layout and programs the tessellation engine.</span></span> <span data-ttu-id="9742d-105">A partire da Direct3D 9, i flussi dei vertici vengono espressi come una matrice di strutture [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , invece di usare codici FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="9742d-105">Starting with Direct3D 9, vertex streams are expressed as an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures (instead of using flexible vertex format (FVF) codes).</span></span> <span data-ttu-id="9742d-106">Ogni elemento della matrice descrive ogni tipo di dati per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="9742d-106">Each array element describes each per-vertex data type.</span></span> <span data-ttu-id="9742d-107">La conversione di FVF> codici nel nuovo formato viene illustrata negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="9742d-107">Converting FVF> codes into the new format is covered in the following topics:</span></span>

-   [<span data-ttu-id="9742d-108">Mapping di codici FVF a una dichiarazione Direct3D 9 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9742d-108">Mapping FVF Codes to a Direct3D 9 Declaration (Direct3D 9)</span></span>](mapping-fvf-codes-to-a-directx-9-declaration.md)
-   [<span data-ttu-id="9742d-109">Codici FVF della funzione fissa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9742d-109">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
-   [<span data-ttu-id="9742d-110">Mapping tra una dichiarazione Direct3D e i codici FVF (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9742d-110">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
-   [<span data-ttu-id="9742d-111">Mapping tra una dichiarazione Direct3D 9 e una dichiarazione Direct3D 8 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9742d-111">Mapping between a Direct3D 9 Declaration and a Direct3D 8 Declaration (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-directx-8.md)
-   [<span data-ttu-id="9742d-112">Programmazione di uno o più flussi (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9742d-112">Programming One or More Streams (Direct3D 9)</span></span>](programming-one-or-more-streams.md)

## <a name="related-topics"></a><span data-ttu-id="9742d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9742d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9742d-114">Buffer vertici</span><span class="sxs-lookup"><span data-stu-id="9742d-114">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 



