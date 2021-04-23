---
description: Allocatore di superficie VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Allocatore di superficie VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909009"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="c4a23-103">Allocatore di superficie VBI</span><span class="sxs-lookup"><span data-stu-id="c4a23-103">VBI Surface Allocator</span></span>

<span data-ttu-id="c4a23-104">L'allocatore di superficie VBI controlla l'allocazione dei buffer VBI nei grafici della tv analogica con scenari di acquisizione di porte video hardware.</span><span class="sxs-lookup"><span data-stu-id="c4a23-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="c4a23-105">Con dispositivi come il decodificatore Bt829, il buffer frame può contenere più buffer di acquisizione VBI a cui si accede tramite un meccanismo proprietario basato su hardware noto genericamente come porta video.</span><span class="sxs-lookup"><span data-stu-id="c4a23-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="c4a23-106">Il filtro VBI Surface Allocator si connette a valle dal filtro di acquisizione e non dispone di un pin di output.</span><span class="sxs-lookup"><span data-stu-id="c4a23-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="c4a23-107">Il filtro funziona a stretto contatto con [il mixer](overlay-mixer-filter.md) di sovrapposizione (tramite DirectDraw) per eseguire operazioni coordinate sulla porta video hardware, utilizzando la stessa memoria buffer frame SVGA limitata.</span><span class="sxs-lookup"><span data-stu-id="c4a23-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



| <span data-ttu-id="c4a23-108">Label</span><span class="sxs-lookup"><span data-stu-id="c4a23-108">Label</span></span> | <span data-ttu-id="c4a23-109">Valore</span><span class="sxs-lookup"><span data-stu-id="c4a23-109">Value</span></span> |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a23-110">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="c4a23-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="c4a23-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="c4a23-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="c4a23-112">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="c4a23-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="c4a23-113">VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="c4a23-113">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="c4a23-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="c4a23-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="c4a23-115">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="c4a23-115">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="c4a23-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="c4a23-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="c4a23-117">MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="c4a23-117">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="c4a23-118">Al pin di output non è mai connesso nulla.</span><span class="sxs-lookup"><span data-stu-id="c4a23-118">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="c4a23-119">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="c4a23-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="c4a23-120">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="c4a23-120">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="c4a23-121">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="c4a23-121">Filter CLSID</span></span>                             | <span data-ttu-id="c4a23-122">CLSID \_ VBISurfaces</span><span class="sxs-lookup"><span data-stu-id="c4a23-122">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="c4a23-123">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c4a23-123">Property Page CLSID</span></span>                      | <span data-ttu-id="c4a23-124">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4a23-124">No property page.</span></span>                                                                   |
| <span data-ttu-id="c4a23-125">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="c4a23-125">Executable</span></span>                               | <span data-ttu-id="c4a23-126">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="c4a23-126">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="c4a23-127">Merito</span><span class="sxs-lookup"><span data-stu-id="c4a23-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="c4a23-128">MERIT \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="c4a23-128">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="c4a23-129">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="c4a23-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c4a23-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c4a23-130">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="c4a23-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4a23-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4a23-132">DirectShow Filters</span><span class="sxs-lookup"><span data-stu-id="c4a23-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



