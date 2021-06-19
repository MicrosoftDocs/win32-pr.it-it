---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe C++ GdiplusBase.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funzioni di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395826"
---
# <a name="memory-functions"></a><span data-ttu-id="fb726-104">Funzioni di memoria</span><span class="sxs-lookup"><span data-stu-id="fb726-104">Memory Functions</span></span>

<span data-ttu-id="fb726-105">Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="fb726-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="fb726-106">Le funzioni nell'API flat GDI+ vengono incapsulate da una raccolta di circa 40 classi C++.</span><span class="sxs-lookup"><span data-stu-id="fb726-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="fb726-107">È consigliabile non chiamare direttamente le funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="fb726-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="fb726-108">Ogni volta che si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="fb726-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="fb726-109">Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat.</span><span class="sxs-lookup"><span data-stu-id="fb726-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="fb726-110">Per altre informazioni sull'uso di questi metodi wrapper, vedere [API flat GDI+.](-gdiplus-flatapi-flat.md)</span><span class="sxs-lookup"><span data-stu-id="fb726-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="fb726-111">Le funzioni API flat seguenti vengono incapsulate dalla [**classe C++ GdiplusBase.**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase)</span><span class="sxs-lookup"><span data-stu-id="fb726-111">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="fb726-112">Funzioni di memoria e metodi wrapper corrispondenti</span><span class="sxs-lookup"><span data-stu-id="fb726-112">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="fb726-113">Funzione flat</span><span class="sxs-lookup"><span data-stu-id="fb726-113">Flat function</span></span>                                          | <span data-ttu-id="fb726-114">Metodo wrapper</span><span class="sxs-lookup"><span data-stu-id="fb726-114">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="fb726-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb726-115">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb726-116">GpStatus WINGDIPAPI GdipAlloc(size \_ t size)</span><span class="sxs-lookup"><span data-stu-id="fb726-116">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="fb726-117">**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)(size \_ t in \_ size)**</span><span class="sxs-lookup"><span data-stu-id="fb726-117">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="fb726-118">Alloca memoria per un oggetto GDI+ di Windows.</span><span class="sxs-lookup"><span data-stu-id="fb726-118">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="fb726-119">GdipAlloc viene dichiarato in GdiplusMem.h.</span><span class="sxs-lookup"><span data-stu-id="fb726-119">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="fb726-120">GpStatus WINGDIPAPI GdipFree(void \* ptr);</span><span class="sxs-lookup"><span data-stu-id="fb726-120">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="fb726-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void \* in \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="fb726-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="fb726-122">Dealloca la memoria per un oggetto GDI+ di Windows.</span><span class="sxs-lookup"><span data-stu-id="fb726-122">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="fb726-123">GdipFree è dichiarato in GdiplusMem.h.</span><span class="sxs-lookup"><span data-stu-id="fb726-123">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
