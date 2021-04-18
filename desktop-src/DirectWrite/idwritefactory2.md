---
title: Interfaccia IDWriteFactory2
description: Interfaccia Factory radice per tutti gli oggetti DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Scrittura diretta dell'interfaccia IDWriteFactory1
- Scrittura diretta dell'interfaccia IDWriteFactory1, descritta
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301932"
---
# <a name="idwritefactory2-interface"></a><span data-ttu-id="a44b6-105">Interfaccia IDWriteFactory2</span><span class="sxs-lookup"><span data-stu-id="a44b6-105">IDWriteFactory2 interface</span></span>

<span data-ttu-id="a44b6-106">Interfaccia Factory radice per tutti gli oggetti [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a44b6-106">The root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="a44b6-107">Membri</span><span class="sxs-lookup"><span data-stu-id="a44b6-107">Members</span></span>

<span data-ttu-id="a44b6-108">L'interfaccia **IDWriteFactory1** eredita da [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span><span class="sxs-lookup"><span data-stu-id="a44b6-108">The **IDWriteFactory1** interface inherits from [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span></span> <span data-ttu-id="a44b6-109">**IDWriteFactory2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a44b6-109">**IDWriteFactory2** also has these types of members:</span></span>

-   [<span data-ttu-id="a44b6-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a44b6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a44b6-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a44b6-111">Methods</span></span>

<span data-ttu-id="a44b6-112">L'interfaccia **IDWriteFactory1** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a44b6-112">The **IDWriteFactory1** interface has these methods.</span></span>



| <span data-ttu-id="a44b6-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="a44b6-113">Method</span></span>                                                                             | <span data-ttu-id="a44b6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a44b6-114">Description</span></span>                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a44b6-115">**CreateCustomRenderingParams**</span><span class="sxs-lookup"><span data-stu-id="a44b6-115">**CreateCustomRenderingParams**</span></span>](idwritefactory2-createcustomrenderingparams.md) | <span data-ttu-id="a44b6-116">Crea un oggetto parametri di rendering con le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="a44b6-116">Creates a rendering parameters object with the specified properties.</span></span><br/>                            |
| [<span data-ttu-id="a44b6-117">**CreateFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="a44b6-117">**CreateFontFallbackBuilder**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | <span data-ttu-id="a44b6-118">Crea un oggetto generatore di fallback del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="a44b6-118">Creates a font fallback builder object.</span></span><br/>                                                         |
| [<span data-ttu-id="a44b6-119">**CreateGlyphRunAnalysis**</span><span class="sxs-lookup"><span data-stu-id="a44b6-119">**CreateGlyphRunAnalysis**</span></span>](idwritefactory2-createglyphrunanalysis.md)           | <span data-ttu-id="a44b6-120">Crea un oggetto di analisi dell'esecuzione del glifo che incapsula le informazioni utilizzate per il rendering di un'esecuzione del glifo.</span><span class="sxs-lookup"><span data-stu-id="a44b6-120">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span><br/> |
| [<span data-ttu-id="a44b6-121">**GetSystemFontFallback**</span><span class="sxs-lookup"><span data-stu-id="a44b6-121">**GetSystemFontFallback**</span></span>](idwritefactory2-getsystemfontfallback.md)             | <span data-ttu-id="a44b6-122">Crea un oggetto fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="a44b6-122">Creates a font fallback object from the system font fallback list.</span></span><br/>                              |
| [<span data-ttu-id="a44b6-123">**TranslateColorGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="a44b6-123">**TranslateColorGlyphRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | <span data-ttu-id="a44b6-124">Questo metodo viene chiamato su un'esecuzione di glifo per tradurlo in più esecuzioni di glifi a più colori.</span><span class="sxs-lookup"><span data-stu-id="a44b6-124">This method is called on a glyph run to translate it in to multiple color glyph runs.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="a44b6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a44b6-125">Requirements</span></span>



| <span data-ttu-id="a44b6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a44b6-126">Requirement</span></span> | <span data-ttu-id="a44b6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a44b6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a44b6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a44b6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a44b6-129">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a44b6-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="a44b6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a44b6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a44b6-131">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a44b6-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a44b6-132">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a44b6-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a44b6-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="a44b6-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="a44b6-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="a44b6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a44b6-135"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a44b6-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a44b6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a44b6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a44b6-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a44b6-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a44b6-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a44b6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a44b6-139">**IDWriteFactory1**</span><span class="sxs-lookup"><span data-stu-id="a44b6-139">**IDWriteFactory1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[<span data-ttu-id="a44b6-140">**IDWriteFactory archiviata nei**</span><span class="sxs-lookup"><span data-stu-id="a44b6-140">**IDWriteFactory**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

