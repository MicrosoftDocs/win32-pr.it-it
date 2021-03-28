---
description: Questo argomento elenca i costruttori della classe Region. Per un elenco completo delle classi, vedere classe Region.
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Costruttori Region. Region
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98663587fab3722d689c9d34578d60daad922a2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131366"
---
# <a name="regionregion-constructors"></a><span data-ttu-id="bfc71-104">Costruttori Region. Region</span><span class="sxs-lookup"><span data-stu-id="bfc71-104">Region.Region constructors</span></span>

<span data-ttu-id="bfc71-105">Questo argomento elenca i costruttori della classe [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) .</span><span class="sxs-lookup"><span data-stu-id="bfc71-105">This topic lists the constructors of the [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) class.</span></span> <span data-ttu-id="bfc71-106">Per un elenco completo delle classi, vedere **classe Region**.</span><span class="sxs-lookup"><span data-stu-id="bfc71-106">For a complete class listing, see **Region Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bfc71-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="bfc71-107">Overload list</span></span>



| <span data-ttu-id="bfc71-108">Costruttore</span><span class="sxs-lookup"><span data-stu-id="bfc71-108">Constructor</span></span>                                                                 | <span data-ttu-id="bfc71-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfc71-109">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc71-110">[**Region (HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span><span class="sxs-lookup"><span data-stu-id="bfc71-110">[**Region(HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span></span>                  | <span data-ttu-id="bfc71-111">Crea un'area identica all'area specificata da un handle per un'area GDI.</span><span class="sxs-lookup"><span data-stu-id="bfc71-111">Creates a region that is identical to the region that is specified by a handle to a GDI region.</span></span><br/>                                                                                       |
| <span data-ttu-id="bfc71-112">[**Region (Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="bfc71-112">[**Region(Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span></span>            | <span data-ttu-id="bfc71-113">Crea un'area definita da un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="bfc71-113">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="bfc71-114">[**Region (RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="bfc71-114">[**Region(RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span></span>          | <span data-ttu-id="bfc71-115">Crea un'area definita da un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="bfc71-115">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="bfc71-116">[**Region (BYTE \* , int)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span><span class="sxs-lookup"><span data-stu-id="bfc71-116">[**Region(BYTE\*,INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span></span> | <span data-ttu-id="bfc71-117">Crea un'area definita dai dati ottenuti da un'altra area.</span><span class="sxs-lookup"><span data-stu-id="bfc71-117">Creates a region that is defined by data obtained from another region.</span></span> <br/>                                                                                                               |
| <span data-ttu-id="bfc71-118">[**Region (GraphicsPath \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span><span class="sxs-lookup"><span data-stu-id="bfc71-118">[**Region(GraphicsPath\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span></span>        | <span data-ttu-id="bfc71-119">Crea un'area definita da un percorso (un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) ) e dispone di una modalità di riempimento contenuta nell'oggetto **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="bfc71-119">Creates a region that is defined by a path (a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object) and has a fill mode that is contained in the **GraphicsPath** object.</span></span><br/> |
| <span data-ttu-id="bfc71-120">[**Region ()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span><span class="sxs-lookup"><span data-stu-id="bfc71-120">[**Region()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span></span>                           | <span data-ttu-id="bfc71-121">Crea un'area infinita.</span><span class="sxs-lookup"><span data-stu-id="bfc71-121">Creates a region that is infinite.</span></span> <span data-ttu-id="bfc71-122">È il costruttore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bfc71-122">This is the default constructor.</span></span> <br/>                                                                                                                  |



 

 
