---
description: Sviluppo di codificatori e decodificatori
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Sviluppo di codificatori e decodificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124554"
---
# <a name="encoder-and-decoder-development"></a><span data-ttu-id="aa510-103">Sviluppo di codificatori e decodificatori</span><span class="sxs-lookup"><span data-stu-id="aa510-103">Encoder and Decoder Development</span></span>

<span data-ttu-id="aa510-104">Questa sezione contiene articoli relativi allo sviluppo di codificatori e decodificatori per DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aa510-104">This section contains articles about encoder and decoder development for DirectShow.</span></span> <span data-ttu-id="aa510-105">Questi argomenti non sono rilevanti per gli sviluppatori di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="aa510-105">These topics are not relevant for application developers.</span></span>

<span data-ttu-id="aa510-106">Un decodificatore software che supporta l'accelerazione video DirectX (VA) deve essere implementato come filtro di trasformazione copia DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aa510-106">A software decoder that supports DirectX Video Acceleration (VA) must be implemented as a DirectShow copy transform filter.</span></span> <span data-ttu-id="aa510-107">Se il decodificatore non supporta DirectX VA, può anche essere implementato come un oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="aa510-107">If the decoder does not support DirectX VA, it can also be implemented as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="aa510-108">Un decodificatore che si connette a un renderer video non deve essere implementato come filtro Trans-on-Place, perché questo comporterà una riduzione significativa delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="aa510-108">A decoder that connects to a video renderer should not be implemented as a trans-in-place filter, because this will result in significant performance degradation.</span></span> <span data-ttu-id="aa510-109">Per informazioni su come scrivere un filtro di trasformazione copia, vedere [scrittura di filtri di trasformazione](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="aa510-109">For information on how to write a copy transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="aa510-110">I codificatori software possono essere implementati come filtri di trasformazione o DMOs.</span><span class="sxs-lookup"><span data-stu-id="aa510-110">Software encoders can be implemented as either transform filters or DMOs.</span></span> <span data-ttu-id="aa510-111">I codificatori non usano DirectX VA, perché DirectX VA attualmente usato solo per la decompressione.</span><span class="sxs-lookup"><span data-stu-id="aa510-111">Encoders do not use DirectX VA, since DirectX VA currently is only used for decompression.</span></span> <span data-ttu-id="aa510-112">La specifica dell'API del codificatore descritta in questa sezione è pertinente per codificatori hardware e software.</span><span class="sxs-lookup"><span data-stu-id="aa510-112">The Encoder API specification described in this section is relevant for both hardware and software encoders.</span></span>

<span data-ttu-id="aa510-113">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="aa510-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="aa510-114">API del codificatore</span><span class="sxs-lookup"><span data-stu-id="aa510-114">Encoder API</span></span>](encoder-api.md)
-   [<span data-ttu-id="aa510-115">Specifiche e interfacce del decodificatore</span><span class="sxs-lookup"><span data-stu-id="aa510-115">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
-   [<span data-ttu-id="aa510-116">Impostazioni del decodificatore per Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="aa510-116">Decoder Settings for Windows Media Center Edition</span></span>](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a><span data-ttu-id="aa510-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa510-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa510-118">Uso di VMR per gli sviluppatori di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa510-118">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



