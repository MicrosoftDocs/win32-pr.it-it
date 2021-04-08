---
description: Allocatore di superficie VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Allocatore di superficie VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757676"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="bc80b-103">Allocatore di superficie VBI</span><span class="sxs-lookup"><span data-stu-id="bc80b-103">VBI Surface Allocator</span></span>

<span data-ttu-id="bc80b-104">VBI Surface allocator controlla l'allocazione dei buffer VBI nei grafici della televisione analogica con scenari di acquisizione della porta video hardware.</span><span class="sxs-lookup"><span data-stu-id="bc80b-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="bc80b-105">Con i dispositivi come il decodificatore BT829, il buffer del frame può contenere più buffer di acquisizione VBI a cui si accede tramite un meccanismo proprietario basato su hardware noto in modo generico come porta video.</span><span class="sxs-lookup"><span data-stu-id="bc80b-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="bc80b-106">Il filtro VBI Surface allocator si connette a valle dal filtro di acquisizione e non ha un pin di output.</span><span class="sxs-lookup"><span data-stu-id="bc80b-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="bc80b-107">Il filtro opera a stretto contatto con il [mixer overlay](overlay-mixer-filter.md) (tramite DirectDraw) per eseguire operazioni coordinate sulla porta video hardware, usando la stessa memoria limitata del buffer di frame SVGA.</span><span class="sxs-lookup"><span data-stu-id="bc80b-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bc80b-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="bc80b-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="bc80b-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="bc80b-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="bc80b-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="bc80b-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="bc80b-111">\_Video di MEDIATYPE, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="bc80b-111">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="bc80b-112">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="bc80b-112">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="bc80b-113">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="bc80b-113">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="bc80b-114">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="bc80b-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="bc80b-115">MEDIATYPE \_ null, MEDIASUBTYPE \_ null.</span><span class="sxs-lookup"><span data-stu-id="bc80b-115">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="bc80b-116">(Nessun elemento è mai connesso al pin di output).</span><span class="sxs-lookup"><span data-stu-id="bc80b-116">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="bc80b-117">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="bc80b-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="bc80b-118">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="bc80b-118">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="bc80b-119">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="bc80b-119">Filter CLSID</span></span>                             | <span data-ttu-id="bc80b-120">\_VBISURFACES CLSID</span><span class="sxs-lookup"><span data-stu-id="bc80b-120">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="bc80b-121">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="bc80b-121">Property Page CLSID</span></span>                      | <span data-ttu-id="bc80b-122">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc80b-122">No property page.</span></span>                                                                   |
| <span data-ttu-id="bc80b-123">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="bc80b-123">Executable</span></span>                               | <span data-ttu-id="bc80b-124">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="bc80b-124">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="bc80b-125">Merito</span><span class="sxs-lookup"><span data-stu-id="bc80b-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="bc80b-126">VALORE \_ normale</span><span class="sxs-lookup"><span data-stu-id="bc80b-126">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="bc80b-127">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="bc80b-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="bc80b-128">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="bc80b-128">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="bc80b-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc80b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc80b-130">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="bc80b-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



