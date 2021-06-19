---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe SolidBrush C++.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funzioni SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395556"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="790e0-104">Funzioni SolidBrush</span><span class="sxs-lookup"><span data-stu-id="790e0-104">SolidBrush Functions</span></span>

<span data-ttu-id="790e0-105">Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="790e0-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="790e0-106">Le funzioni nell'API flat GDI+ vengono incapsulate da una raccolta di circa 40 classi C++.</span><span class="sxs-lookup"><span data-stu-id="790e0-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="790e0-107">È consigliabile non chiamare direttamente le funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="790e0-107">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="790e0-108">Ogni volta che si effettuano chiamate a GDI+, è consigliabile eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="790e0-108">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="790e0-109">Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat.</span><span class="sxs-lookup"><span data-stu-id="790e0-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="790e0-110">Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API (API flat GDI+).](-gdiplus-flatapi-flat.md)</span><span class="sxs-lookup"><span data-stu-id="790e0-110">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="790e0-111">Le funzioni API flat seguenti vengono incapsulate dalla [**classe SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++.</span><span class="sxs-lookup"><span data-stu-id="790e0-111">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="790e0-112">Funzioni Brush e metodi wrapper corrispondenti</span><span class="sxs-lookup"><span data-stu-id="790e0-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="790e0-113">Funzione flat</span><span class="sxs-lookup"><span data-stu-id="790e0-113">Flat function</span></span>                                                                               | <span data-ttu-id="790e0-114">Metodo wrapper</span><span class="sxs-lookup"><span data-stu-id="790e0-114">Wrapper method</span></span>                                                                                       | <span data-ttu-id="790e0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="790e0-115">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="790e0-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \* \* brush)**</span><span class="sxs-lookup"><span data-stu-id="790e0-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="790e0-117">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="790e0-117">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="790e0-118">Crea un [**oggetto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basato su un colore</span><span class="sxs-lookup"><span data-stu-id="790e0-118">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="790e0-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \* brush, ARGB color)**</span><span class="sxs-lookup"><span data-stu-id="790e0-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="790e0-120">**SolidBrush::SetColor(IN const Color& colore)**</span><span class="sxs-lookup"><span data-stu-id="790e0-120">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="790e0-121">Imposta il colore di questo pennello a tinta unita</span><span class="sxs-lookup"><span data-stu-id="790e0-121">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="790e0-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \* brush, ARGB \* color)**</span><span class="sxs-lookup"><span data-stu-id="790e0-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="790e0-123">**SolidBrush::GetColor(OUT Color \* color) const**</span><span class="sxs-lookup"><span data-stu-id="790e0-123">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="790e0-124">Ottiene il colore di questo pennello a tinta unita</span><span class="sxs-lookup"><span data-stu-id="790e0-124">Gets the color of this solid brush</span></span>                                                      |



 

 

 
