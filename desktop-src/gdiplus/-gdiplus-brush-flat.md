---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe Brush C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funzioni Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395086"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="456b7-104">Funzioni Brush (GDI+)</span><span class="sxs-lookup"><span data-stu-id="456b7-104">Brush Functions (GDI+)</span></span>

<span data-ttu-id="456b7-105">Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="456b7-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="456b7-106">Le funzioni nell'API flat GDI+ vengono incapsulate da una raccolta di circa 40 classi C++.</span><span class="sxs-lookup"><span data-stu-id="456b7-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="456b7-107">È consigliabile non chiamare direttamente le funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="456b7-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="456b7-108">Ogni volta che si effettuano chiamate a GDI+, è necessario eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="456b7-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="456b7-109">Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat.</span><span class="sxs-lookup"><span data-stu-id="456b7-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="456b7-110">Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API (API flat GDI+).](-gdiplus-flatapi-flat.md)</span><span class="sxs-lookup"><span data-stu-id="456b7-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="456b7-111">Le funzioni API flat seguenti vengono incapsulate dalla [**classe Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.</span><span class="sxs-lookup"><span data-stu-id="456b7-111">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="456b7-112">Funzioni Brush e metodi wrapper corrispondenti</span><span class="sxs-lookup"><span data-stu-id="456b7-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="456b7-113">Funzione flat</span><span class="sxs-lookup"><span data-stu-id="456b7-113">Flat function</span></span>                                                                        | <span data-ttu-id="456b7-114">Metodo wrapper</span><span class="sxs-lookup"><span data-stu-id="456b7-114">Wrapper method</span></span>                                          | <span data-ttu-id="456b7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="456b7-115">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="456b7-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \* brush, GpBrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="456b7-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="456b7-117">**Brush::Clone**</span><span class="sxs-lookup"><span data-stu-id="456b7-117">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="456b7-118">Il [**metodo Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crea un nuovo [**oggetto Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basato su questo pennello.</span><span class="sxs-lookup"><span data-stu-id="456b7-118">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="456b7-119">GpStatus WINGDIPAPI GdipDeleteBrush(Pennello \* GpBrush)</span><span class="sxs-lookup"><span data-stu-id="456b7-119">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="456b7-120">virtual ~Brush()</span><span class="sxs-lookup"><span data-stu-id="456b7-120">virtual ~Brush()</span></span>                                        | <span data-ttu-id="456b7-121">Pulisce le risorse usate da un [**oggetto Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)</span><span class="sxs-lookup"><span data-stu-id="456b7-121">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="456b7-122">GpStatus WINGDIPAPI GdipGetBrushType(Pennello \* GpBrush, tipo \* GpBrushType)</span><span class="sxs-lookup"><span data-stu-id="456b7-122">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="456b7-123">**Brush::GetType**</span><span class="sxs-lookup"><span data-stu-id="456b7-123">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="456b7-124">Il [**metodo Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) ottiene il tipo di questo pennello.</span><span class="sxs-lookup"><span data-stu-id="456b7-124">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




