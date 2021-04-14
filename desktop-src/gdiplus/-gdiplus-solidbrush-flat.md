---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funzioni SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977546"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="f42d3-103">Funzioni SolidBrush</span><span class="sxs-lookup"><span data-stu-id="f42d3-103">SolidBrush Functions</span></span>

<span data-ttu-id="f42d3-104">Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="f42d3-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="f42d3-105">Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++.</span><span class="sxs-lookup"><span data-stu-id="f42d3-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="f42d3-106">Si consiglia di non chiamare direttamente le funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="f42d3-106">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="f42d3-107">Quando si effettuano chiamate a GDI+, è consigliabile chiamare i metodi e le funzioni forniti dai wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="f42d3-107">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="f42d3-108">Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat.</span><span class="sxs-lookup"><span data-stu-id="f42d3-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="f42d3-109">Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="f42d3-109">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="f42d3-110">Le funzioni API Flat seguenti sono incapsulate dalla classe C++ [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) .</span><span class="sxs-lookup"><span data-stu-id="f42d3-110">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="f42d3-111">Funzioni pennello e metodi wrapper corrispondenti</span><span class="sxs-lookup"><span data-stu-id="f42d3-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="f42d3-112">Flat-funzione</span><span class="sxs-lookup"><span data-stu-id="f42d3-112">Flat function</span></span>                                                                               | <span data-ttu-id="f42d3-113">Wrapper (metodo)</span><span class="sxs-lookup"><span data-stu-id="f42d3-113">Wrapper method</span></span>                                                                                       | <span data-ttu-id="f42d3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f42d3-114">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f42d3-115">**GpStatus WINGDIPAPI GdipCreateSolidFill (ARGB color, GpSolidFill \* \* Brush)**</span><span class="sxs-lookup"><span data-stu-id="f42d3-115">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="f42d3-116">[**SolidBrush:: SolidBrush (IN colori const& colore)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="f42d3-116">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="f42d3-117">Crea un oggetto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) in base a un colore</span><span class="sxs-lookup"><span data-stu-id="f42d3-117">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="f42d3-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor ( \* pennello GpSolidFill, colore ARGB)**</span><span class="sxs-lookup"><span data-stu-id="f42d3-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="f42d3-119">**SolidBrush:: ToColor (IN colori const& colore)**</span><span class="sxs-lookup"><span data-stu-id="f42d3-119">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="f42d3-120">Imposta il colore del pennello a tinta unita</span><span class="sxs-lookup"><span data-stu-id="f42d3-120">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="f42d3-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor ( \* pennello GpSolidFill, \* colore ARGB)**</span><span class="sxs-lookup"><span data-stu-id="f42d3-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="f42d3-122">**SolidBrush:: GetColor (colore del colore OUT \* ) const**</span><span class="sxs-lookup"><span data-stu-id="f42d3-122">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="f42d3-123">Ottiene il colore di questo pennello a tinta unita</span><span class="sxs-lookup"><span data-stu-id="f42d3-123">Gets the color of this solid brush</span></span>                                                      |



 

 

 
