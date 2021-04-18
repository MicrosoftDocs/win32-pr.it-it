---
title: Interfaccia IDWriteTextFormat1
description: Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali. | Interfaccia IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Scrittura diretta dell'interfaccia IDWriteTextFormat1
- Scrittura diretta dell'interfaccia IDWriteTextFormat1, descritta
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321247"
---
# <a name="idwritetextformat1-interface"></a><span data-ttu-id="5a394-106">Interfaccia IDWriteTextFormat1</span><span class="sxs-lookup"><span data-stu-id="5a394-106">IDWriteTextFormat1 interface</span></span>

<span data-ttu-id="5a394-107">Descrive le proprietà dei tipi di carattere e paragrafi usati per formattare il testo e descrive le informazioni sulle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="5a394-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span> <span data-ttu-id="5a394-108">Questa interfaccia ha tutti gli stessi metodi di [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e aggiunge la possibilità di applicare un orientamento esplicito.</span><span class="sxs-lookup"><span data-stu-id="5a394-108">This interface has all the same methods as [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and adds the ability for you to apply an explicit orientation.</span></span>

## <a name="members"></a><span data-ttu-id="5a394-109">Membri</span><span class="sxs-lookup"><span data-stu-id="5a394-109">Members</span></span>

<span data-ttu-id="5a394-110">L'interfaccia **IDWriteTextFormat1** eredita da [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="5a394-110">The **IDWriteTextFormat1** interface inherits from [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span> <span data-ttu-id="5a394-111">**IDWriteTextFormat1** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5a394-111">**IDWriteTextFormat1** also has these types of members:</span></span>

-   [<span data-ttu-id="5a394-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="5a394-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a394-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="5a394-113">Methods</span></span>

<span data-ttu-id="5a394-114">L'interfaccia **IDWriteTextFormat1** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5a394-114">The **IDWriteTextFormat1** interface has these methods.</span></span>



| <span data-ttu-id="5a394-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="5a394-115">Method</span></span>                                                                                | <span data-ttu-id="5a394-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a394-116">Description</span></span>                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a394-117">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="5a394-117">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | <span data-ttu-id="5a394-118">Ottiene il fallback corrente.</span><span class="sxs-lookup"><span data-stu-id="5a394-118">Gets the current fallback.</span></span> <span data-ttu-id="5a394-119">Se non è stato impostato alcun valore dopo la creazione del layout, sarà nullptr.</span><span class="sxs-lookup"><span data-stu-id="5a394-119">If none was ever set since creating the layout, it will be nullptr.</span></span><br/>               |
| [<span data-ttu-id="5a394-120">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="5a394-120">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | <span data-ttu-id="5a394-121">Ottiene la modalità di wrapping dell'ultima riga.</span><span class="sxs-lookup"><span data-stu-id="5a394-121">Gets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="5a394-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="5a394-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | <span data-ttu-id="5a394-123">Ottiene l'allineamento del margine ottico per il formato di testo.</span><span class="sxs-lookup"><span data-stu-id="5a394-123">Gets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="5a394-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="5a394-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | <span data-ttu-id="5a394-125">Ottiene l'orientamento preferito dei glifi quando si usa una direzione di lettura verticale.</span><span class="sxs-lookup"><span data-stu-id="5a394-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/>                             |
| [<span data-ttu-id="5a394-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="5a394-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | <span data-ttu-id="5a394-127">Applica il fallback del tipo di carattere personalizzato nel layout.</span><span class="sxs-lookup"><span data-stu-id="5a394-127">Applies the custom font fallback onto the layout.</span></span> <span data-ttu-id="5a394-128">Se non è impostato alcun oggetto, viene utilizzato l'elenco di fallback di sistema predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a394-128">If none is set, it uses the default system fallback list.</span></span> <br/> |
| [<span data-ttu-id="5a394-129">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="5a394-129">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | <span data-ttu-id="5a394-130">Imposta la modalità di wrapping dell'ultima riga.</span><span class="sxs-lookup"><span data-stu-id="5a394-130">Sets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="5a394-131">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="5a394-131">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | <span data-ttu-id="5a394-132">Imposta l'allineamento del margine ottico per il formato di testo.</span><span class="sxs-lookup"><span data-stu-id="5a394-132">Sets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="5a394-133">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="5a394-133">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | <span data-ttu-id="5a394-134">Imposta l'orientamento di un formato di testo.</span><span class="sxs-lookup"><span data-stu-id="5a394-134">Sets the orientation of a text format.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="5a394-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a394-135">Requirements</span></span>



| <span data-ttu-id="5a394-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a394-136">Requirement</span></span> | <span data-ttu-id="5a394-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5a394-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a394-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a394-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5a394-139">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a394-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="5a394-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a394-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5a394-141">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a394-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="5a394-142">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a394-142">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5a394-143">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="5a394-143">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="5a394-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a394-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a394-145"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a394-145"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5a394-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5a394-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a394-147"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a394-147"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a394-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a394-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a394-149">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="5a394-149">**IDWriteTextFormat**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

