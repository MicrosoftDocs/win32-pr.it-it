---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funzioni Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345106"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="a9afc-103">Funzioni Brush (GDI+)</span><span class="sxs-lookup"><span data-stu-id="a9afc-103">Brush Functions (GDI+)</span></span>

<span data-ttu-id="a9afc-104">Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="a9afc-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="a9afc-105">Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++.</span><span class="sxs-lookup"><span data-stu-id="a9afc-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="a9afc-106">Si consiglia di non chiamare direttamente le funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="a9afc-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="a9afc-107">Quando si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="a9afc-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="a9afc-108">Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat.</span><span class="sxs-lookup"><span data-stu-id="a9afc-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="a9afc-109">Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="a9afc-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="a9afc-110">Le funzioni API Flat seguenti sono incapsulate dalla classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.</span><span class="sxs-lookup"><span data-stu-id="a9afc-110">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="a9afc-111">Funzioni pennello e metodi wrapper corrispondenti</span><span class="sxs-lookup"><span data-stu-id="a9afc-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="a9afc-112">Flat-funzione</span><span class="sxs-lookup"><span data-stu-id="a9afc-112">Flat function</span></span>                                                                        | <span data-ttu-id="a9afc-113">Wrapper (metodo)</span><span class="sxs-lookup"><span data-stu-id="a9afc-113">Wrapper method</span></span>                                          | <span data-ttu-id="a9afc-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9afc-114">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9afc-115">GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="a9afc-115">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="a9afc-116">**Brush:: Clone**</span><span class="sxs-lookup"><span data-stu-id="a9afc-116">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="a9afc-117">Il metodo [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crea un nuovo oggetto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basato su questo pennello.</span><span class="sxs-lookup"><span data-stu-id="a9afc-117">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="a9afc-118">GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)</span><span class="sxs-lookup"><span data-stu-id="a9afc-118">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="a9afc-119">Virtual ~ Brush ()</span><span class="sxs-lookup"><span data-stu-id="a9afc-119">virtual ~Brush()</span></span>                                        | <span data-ttu-id="a9afc-120">Pulisce le risorse utilizzate da un oggetto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="a9afc-120">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="a9afc-121">GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* Brush, GpBrushType \* Type)</span><span class="sxs-lookup"><span data-stu-id="a9afc-121">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="a9afc-122">**Brush:: GetType**</span><span class="sxs-lookup"><span data-stu-id="a9afc-122">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="a9afc-123">Il metodo [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) ottiene il tipo di questo pennello.</span><span class="sxs-lookup"><span data-stu-id="a9afc-123">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




