---
title: Interfaccia IDWriteTextLayout2
description: Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato. | Interfaccia IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Scrittura diretta dell'interfaccia IDWriteTextLayout2
- Scrittura diretta dell'interfaccia IDWriteTextLayout2, descritta
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353281"
---
# <a name="idwritetextlayout2-interface"></a><span data-ttu-id="0fa2c-106">Interfaccia IDWriteTextLayout2</span><span class="sxs-lookup"><span data-stu-id="0fa2c-106">IDWriteTextLayout2 interface</span></span>

<span data-ttu-id="0fa2c-107">Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="0fa2c-108">Membri</span><span class="sxs-lookup"><span data-stu-id="0fa2c-108">Members</span></span>

<span data-ttu-id="0fa2c-109">L'interfaccia **IDWriteTextLayout2** eredita da [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span><span class="sxs-lookup"><span data-stu-id="0fa2c-109">The **IDWriteTextLayout2** interface inherits from [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span></span> <span data-ttu-id="0fa2c-110">**IDWriteTextLayout2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0fa2c-110">**IDWriteTextLayout2** also has these types of members:</span></span>

-   [<span data-ttu-id="0fa2c-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0fa2c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0fa2c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0fa2c-112">Methods</span></span>

<span data-ttu-id="0fa2c-113">L'interfaccia **IDWriteTextLayout2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-113">The **IDWriteTextLayout2** interface has these methods.</span></span>



| <span data-ttu-id="0fa2c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="0fa2c-114">Method</span></span>                                                                                | <span data-ttu-id="0fa2c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fa2c-115">Description</span></span>                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fa2c-116">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-116">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | <span data-ttu-id="0fa2c-117">Ottiene l'oggetto fallback del tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-117">Get the current font fallback object.</span></span> <br/>                                           |
| [<span data-ttu-id="0fa2c-118">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-118">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | <span data-ttu-id="0fa2c-119">Ottiene un valore che indica se l'ultima parola sull'ultima riga viene incapsulata.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-119">Get whether or not the last word on the last line is wrapped.</span></span><br/>                    |
| [<span data-ttu-id="0fa2c-120">**GetMetrics**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-120">**GetMetrics**</span></span>](idwritetextlayout2-getmetrics.md)                                   | <span data-ttu-id="0fa2c-121">Recupera la metrica complessiva per la stringa formattata.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-121">Retrieves overall metrics for the formatted string.</span></span> <br/>                             |
| [<span data-ttu-id="0fa2c-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | <span data-ttu-id="0fa2c-123">Ottenere il modo in cui i glifi si allineano ai bordi del margine.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-123">Get how the glyphs align to the edges the margin.</span></span> <br/>                               |
| [<span data-ttu-id="0fa2c-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | <span data-ttu-id="0fa2c-125">Ottiene l'orientamento preferito dei glifi quando si usa una direzione di lettura verticale.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |
| [<span data-ttu-id="0fa2c-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | <span data-ttu-id="0fa2c-127">Applicare un fallback del tipo di carattere personalizzato al layout.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-127">Apply a custom font fallback onto layout.</span></span><br/>                                        |
| [<span data-ttu-id="0fa2c-128">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-128">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | <span data-ttu-id="0fa2c-129">Indica se l'ultima parola sull'ultima riga viene sottoposta a incapsulamento.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-129">Set whether or not the last word on the last line is wrapped.</span></span> <br/>                   |
| [<span data-ttu-id="0fa2c-130">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-130">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | <span data-ttu-id="0fa2c-131">Imposta il modo in cui i glifi si allineano ai bordi del margine.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-131">Set how the glyphs align to the edges the margin.</span></span><br/>                                |
| [<span data-ttu-id="0fa2c-132">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-132">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | <span data-ttu-id="0fa2c-133">Imposta l'orientamento preferito dei glifi quando si usa una direzione di lettura verticale.</span><span class="sxs-lookup"><span data-stu-id="0fa2c-133">Set the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0fa2c-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fa2c-134">Requirements</span></span>



| <span data-ttu-id="0fa2c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fa2c-135">Requirement</span></span> | <span data-ttu-id="0fa2c-136">Valore</span><span class="sxs-lookup"><span data-stu-id="0fa2c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa2c-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fa2c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0fa2c-138">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0fa2c-138">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="0fa2c-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fa2c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0fa2c-140">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0fa2c-140">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="0fa2c-141">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fa2c-141">Minimum supported phone</span></span><br/>  | <span data-ttu-id="0fa2c-142">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="0fa2c-142">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="0fa2c-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="0fa2c-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="0fa2c-144"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fa2c-144"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0fa2c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0fa2c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fa2c-146"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fa2c-146"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0fa2c-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fa2c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fa2c-148">**IDWriteTextLayout1**</span><span class="sxs-lookup"><span data-stu-id="0fa2c-148">**IDWriteTextLayout1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

