---
title: Metodi DrawText ID2D1RenderTarget
description: Disegna il testo specificato utilizzando le informazioni sul formato fornite da un oggetto IDWriteTextFormat.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Metodi DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326069"
---
# <a name="id2d1rendertargetdrawtext-methods"></a><span data-ttu-id="4bf71-104">ID2D1RenderTarget::D Metodi rawText</span><span class="sxs-lookup"><span data-stu-id="4bf71-104">ID2D1RenderTarget::DrawText methods</span></span>

<span data-ttu-id="4bf71-105">Disegna il testo specificato utilizzando le informazioni sul formato fornite da un oggetto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="4bf71-105">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4bf71-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="4bf71-106">Overload list</span></span>



| <span data-ttu-id="4bf71-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="4bf71-107">Method</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="4bf71-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bf71-108">Description</span></span>                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf71-109">[**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ Rect \_ F&, ID2D1Brush \* , d2d1 \_ , \_ \_ Opzioni di testo di, \_ metodo di misurazione del testo DWrite \_ \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="4bf71-109">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F&,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>  | <span data-ttu-id="4bf71-110">Disegna il testo specificato utilizzando le informazioni sul formato fornite da un oggetto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="4bf71-110">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span><br/>  |
| <span data-ttu-id="4bf71-111">[**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ Rect \_ F \* , ID2D1Brush \* , d2d1 \_ , \_ \_ Opzioni di testo di testo, DWrite \_ testo di \_ misurazione \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="4bf71-111">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F\*,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> | <span data-ttu-id="4bf71-112">Disegna il testo specificato utilizzando le informazioni sul formato fornite da un oggetto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="4bf71-112">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="4bf71-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bf71-113">Remarks</span></span>

<span data-ttu-id="4bf71-114">Per creare testo con Direct2D, usare il metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) per il testo con un formato singolo oppure il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) quando sono necessari più formati, funzionalità OpenType avanzate o hit testing.</span><span class="sxs-lookup"><span data-stu-id="4bf71-114">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format, or the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method when you need multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="4bf71-115">Questi metodi usano l'API DirectWrite per fornire una visualizzazione di testo di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="4bf71-115">These methods use the DirectWrite API to provide high-quality text display.</span></span>

<span data-ttu-id="4bf71-116">Questo metodo non restituisce un codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4bf71-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="4bf71-117">Per determinare se un'operazione di disegno (ad esempio **DrawText**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="4bf71-117">To determine whether a drawing operation (such as **DrawText**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="4bf71-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="4bf71-118">Examples</span></span>

<span data-ttu-id="4bf71-119">Per un esempio, vedere [come creare testo](how-to--draw-text.md).</span><span class="sxs-lookup"><span data-stu-id="4bf71-119">For an example, see [How to Draw Text](how-to--draw-text.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf71-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bf71-120">Requirements</span></span>



| <span data-ttu-id="4bf71-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bf71-121">Requirement</span></span> | <span data-ttu-id="4bf71-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4bf71-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf71-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="4bf71-123">Library</span></span><br/> | <dl> <span data-ttu-id="4bf71-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bf71-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="4bf71-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4bf71-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4bf71-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bf71-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bf71-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bf71-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf71-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="4bf71-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="4bf71-129">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="4bf71-129">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="4bf71-130">Come creare testo</span><span class="sxs-lookup"><span data-stu-id="4bf71-130">How to Draw Text</span></span>](how-to--draw-text.md)
</dt> <dt>

[<span data-ttu-id="4bf71-131">Cenni preliminari sulla formattazione e sul layout del testo</span><span class="sxs-lookup"><span data-stu-id="4bf71-131">Text Formatting and Layout Overview</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

