---
title: Interfaccia IDWriteTextAnalyzer2
description: Analizza varie proprietà di testo per l'elaborazione di script complessi.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Scrittura diretta dell'interfaccia IDWriteTextAnalyzer2
- Scrittura diretta dell'interfaccia IDWriteTextAnalyzer2, descritta
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518106"
---
# <a name="idwritetextanalyzer2-interface"></a><span data-ttu-id="c6d67-105">Interfaccia IDWriteTextAnalyzer2</span><span class="sxs-lookup"><span data-stu-id="c6d67-105">IDWriteTextAnalyzer2 interface</span></span>

<span data-ttu-id="c6d67-106">Analizza varie proprietà di testo per l'elaborazione di script complessi.</span><span class="sxs-lookup"><span data-stu-id="c6d67-106">Analyzes various text properties for complex script processing.</span></span>

## <a name="members"></a><span data-ttu-id="c6d67-107">Membri</span><span class="sxs-lookup"><span data-stu-id="c6d67-107">Members</span></span>

<span data-ttu-id="c6d67-108">L'interfaccia **IDWriteTextAnalyzer2** eredita da [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span><span class="sxs-lookup"><span data-stu-id="c6d67-108">The **IDWriteTextAnalyzer2** interface inherits from [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span></span> <span data-ttu-id="c6d67-109">**IDWriteTextAnalyzer2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c6d67-109">**IDWriteTextAnalyzer2** also has these types of members:</span></span>

-   [<span data-ttu-id="c6d67-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="c6d67-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c6d67-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c6d67-111">Methods</span></span>

<span data-ttu-id="c6d67-112">L'interfaccia **IDWriteTextAnalyzer2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c6d67-112">The **IDWriteTextAnalyzer2** interface has these methods.</span></span>



| <span data-ttu-id="c6d67-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="c6d67-113">Method</span></span>                                                                                    | <span data-ttu-id="c6d67-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6d67-114">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6d67-115">**CheckTypographicFeature**</span><span class="sxs-lookup"><span data-stu-id="c6d67-115">**CheckTypographicFeature**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | <span data-ttu-id="c6d67-116">Verifica se è disponibile una funzionalità tipografica per un glifo o un set di glifi.</span><span class="sxs-lookup"><span data-stu-id="c6d67-116">Checks if a typographic feature is available for a glyph or a set of glyphs.</span></span><br/> |
| [<span data-ttu-id="c6d67-117">**GetGlyphOrientationTransform**</span><span class="sxs-lookup"><span data-stu-id="c6d67-117">**GetGlyphOrientationTransform**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | <span data-ttu-id="c6d67-118">Restituisce la matrice di trasformazione 2x3 per l'angolo corrispondente per creare l'esecuzione del glifo.</span><span class="sxs-lookup"><span data-stu-id="c6d67-118">Returns 2x3 transform matrix for the respective angle to draw the glyph run.</span></span><br/> |
| [<span data-ttu-id="c6d67-119">**GetTypographicFeatures**</span><span class="sxs-lookup"><span data-stu-id="c6d67-119">**GetTypographicFeatures**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | <span data-ttu-id="c6d67-120">Restituisce un elenco completo delle funzionalità OpenType disponibili per uno script o un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="c6d67-120">Returns a complete list of OpenType features available for a script or font.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c6d67-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6d67-121">Requirements</span></span>



| <span data-ttu-id="c6d67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6d67-122">Requirement</span></span> | <span data-ttu-id="c6d67-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c6d67-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d67-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6d67-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d67-125">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c6d67-125">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="c6d67-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6d67-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d67-127">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c6d67-127">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c6d67-128">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6d67-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c6d67-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="c6d67-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="c6d67-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6d67-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6d67-131"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6d67-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c6d67-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c6d67-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6d67-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6d67-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c6d67-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6d67-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d67-135">**IDWriteTextAnalyzer1**</span><span class="sxs-lookup"><span data-stu-id="c6d67-135">**IDWriteTextAnalyzer1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

