---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funzioni di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978986"
---
# <a name="memory-functions"></a><span data-ttu-id="4fa73-103">Funzioni di memoria</span><span class="sxs-lookup"><span data-stu-id="4fa73-103">Memory Functions</span></span>

<span data-ttu-id="4fa73-104">Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="4fa73-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="4fa73-105">Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++.</span><span class="sxs-lookup"><span data-stu-id="4fa73-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="4fa73-106">Si consiglia di non chiamare direttamente le funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="4fa73-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="4fa73-107">Quando si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="4fa73-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="4fa73-108">Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat.</span><span class="sxs-lookup"><span data-stu-id="4fa73-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="4fa73-109">Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="4fa73-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="4fa73-110">Le funzioni API Flat seguenti sono incapsulate dalla classe C++ [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) .</span><span class="sxs-lookup"><span data-stu-id="4fa73-110">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="4fa73-111">Funzioni di memoria e metodi wrapper corrispondenti</span><span class="sxs-lookup"><span data-stu-id="4fa73-111">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="4fa73-112">Flat-funzione</span><span class="sxs-lookup"><span data-stu-id="4fa73-112">Flat function</span></span>                                          | <span data-ttu-id="4fa73-113">Wrapper (metodo)</span><span class="sxs-lookup"><span data-stu-id="4fa73-113">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="4fa73-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fa73-114">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa73-115">GpStatus WINGDIPAPI GdipAlloc (size \_ t size)</span><span class="sxs-lookup"><span data-stu-id="4fa73-115">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="4fa73-116">**GpStatus WINGDIPAPI GdiplusBase void \* (operator new) (size \_ t size \_ )**</span><span class="sxs-lookup"><span data-stu-id="4fa73-116">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="4fa73-117">Alloca memoria per un oggetto GDI+ di Windows.</span><span class="sxs-lookup"><span data-stu-id="4fa73-117">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="4fa73-118">GdipAlloc viene dichiarata in GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="4fa73-118">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="4fa73-119">GpStatus WINGDIPAPI GdipFree (void \* ptr);</span><span class="sxs-lookup"><span data-stu-id="4fa73-119">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="4fa73-120">**GpStatus WINGDIPAPI GdiplusBase void (operator delete) (void \* in \_ PVOID)**</span><span class="sxs-lookup"><span data-stu-id="4fa73-120">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="4fa73-121">Dealloca la memoria per un oggetto GDI+ di Windows.</span><span class="sxs-lookup"><span data-stu-id="4fa73-121">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="4fa73-122">GdipFree viene dichiarata in GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="4fa73-122">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
