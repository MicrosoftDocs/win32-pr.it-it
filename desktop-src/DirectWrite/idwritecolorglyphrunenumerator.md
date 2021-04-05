---
title: Interfaccia IDWriteColorGlyphRunEnumerator
description: Questa interfaccia consente all'applicazione di enumerare le esecuzioni del glifo dei colori.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Scrittura diretta dell'interfaccia IDWriteColorGlyphRunEnumerator
- Scrittura diretta dell'interfaccia IDWriteColorGlyphRunEnumerator, descritta
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742239"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a><span data-ttu-id="86e6d-105">Interfaccia IDWriteColorGlyphRunEnumerator</span><span class="sxs-lookup"><span data-stu-id="86e6d-105">IDWriteColorGlyphRunEnumerator interface</span></span>

<span data-ttu-id="86e6d-106">Questa interfaccia consente all'applicazione di enumerare le esecuzioni del glifo dei colori.</span><span class="sxs-lookup"><span data-stu-id="86e6d-106">This interface allows the application to enumerate through the color glyph runs.</span></span> <span data-ttu-id="86e6d-107">L'enumeratore enumera i livelli in un ordine di ritorno all'inizio per i livelli appropriati.</span><span class="sxs-lookup"><span data-stu-id="86e6d-107">The enumerator enumerates the layers in a back to front order for appropriate layering.</span></span>

## <a name="members"></a><span data-ttu-id="86e6d-108">Membri</span><span class="sxs-lookup"><span data-stu-id="86e6d-108">Members</span></span>

<span data-ttu-id="86e6d-109">L'interfaccia **IDWriteColorGlyphRunEnumerator** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="86e6d-109">The **IDWriteColorGlyphRunEnumerator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86e6d-110">**IDWriteColorGlyphRunEnumerator** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="86e6d-110">**IDWriteColorGlyphRunEnumerator** also has these types of members:</span></span>

-   [<span data-ttu-id="86e6d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="86e6d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="86e6d-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="86e6d-112">Methods</span></span>

<span data-ttu-id="86e6d-113">L'interfaccia **IDWriteColorGlyphRunEnumerator** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="86e6d-113">The **IDWriteColorGlyphRunEnumerator** interface has these methods.</span></span>



| <span data-ttu-id="86e6d-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="86e6d-114">Method</span></span>                                                                | <span data-ttu-id="86e6d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86e6d-115">Description</span></span>                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="86e6d-116">**GetCurrentRun**</span><span class="sxs-lookup"><span data-stu-id="86e6d-116">**GetCurrentRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | <span data-ttu-id="86e6d-117">Restituisce l'esecuzione del glifo corrente dell'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="86e6d-117">Returns the current glyph run of the enumerator.</span></span><br/> |
| [<span data-ttu-id="86e6d-118">**MoveNext**</span><span class="sxs-lookup"><span data-stu-id="86e6d-118">**MoveNext**</span></span>](idwritecolorglyphrunenumerator-movenext.md)           | <span data-ttu-id="86e6d-119">Passare al glifo successivo eseguito nell'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="86e6d-119">Move to the next glyph run in the enumerator.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="86e6d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86e6d-120">Requirements</span></span>



| <span data-ttu-id="86e6d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="86e6d-121">Requirement</span></span> | <span data-ttu-id="86e6d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="86e6d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86e6d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86e6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="86e6d-124">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="86e6d-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="86e6d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86e6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="86e6d-126">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="86e6d-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="86e6d-127">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86e6d-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="86e6d-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="86e6d-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="86e6d-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="86e6d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="86e6d-130"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86e6d-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86e6d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="86e6d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e6d-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e6d-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

