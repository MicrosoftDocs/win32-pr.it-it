---
description: L'interfaccia ID3DX10Font incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interfaccia ID3DX10Font (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235038"
---
# <a name="id3dx10font-interface"></a><span data-ttu-id="ef620-103">Interfaccia ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="ef620-103">ID3DX10Font interface</span></span>

<span data-ttu-id="ef620-104">L'interfaccia ID3DX10Font incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="ef620-104">The ID3DX10Font interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="ef620-105">Membri</span><span class="sxs-lookup"><span data-stu-id="ef620-105">Members</span></span>

<span data-ttu-id="ef620-106">L'interfaccia **ID3DX10Font** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ef620-106">The **ID3DX10Font** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ef620-107">**ID3DX10Font** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ef620-107">**ID3DX10Font** also has these types of members:</span></span>

-   [<span data-ttu-id="ef620-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="ef620-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef620-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ef620-109">Methods</span></span>

<span data-ttu-id="ef620-110">L'interfaccia **ID3DX10Font** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ef620-110">The **ID3DX10Font** interface has these methods.</span></span>



| <span data-ttu-id="ef620-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="ef620-111">Method</span></span>                                                     | <span data-ttu-id="ef620-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef620-112">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef620-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="ef620-113">**DrawText**</span></span>](id3dx10font-drawtext.md)                   | <span data-ttu-id="ef620-114">Creare testo formattato.</span><span class="sxs-lookup"><span data-stu-id="ef620-114">Draw formatted text.</span></span> <span data-ttu-id="ef620-115">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef620-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                        |
| [<span data-ttu-id="ef620-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="ef620-116">**GetDC**</span></span>](id3dx10font-getdc.md)                         | <span data-ttu-id="ef620-117">Restituisce un handle a un contesto di periferica di visualizzazione (DC) sul quale è impostato il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="ef620-117">Return a handle to a display device context (DC) that has the font set onto it.</span></span><br/>                                                            |
| [<span data-ttu-id="ef620-118">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="ef620-118">**GetDesc**</span></span>](id3dx10font-getdesc.md)                     | <span data-ttu-id="ef620-119">Ottiene una descrizione dell'oggetto del tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="ef620-119">Get a description of the current font object.</span></span><br/>                                                                                              |
| [<span data-ttu-id="ef620-120">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="ef620-120">**GetDevice**</span></span>](id3dx10font-getdevice.md)                 | <span data-ttu-id="ef620-121">Recuperare il dispositivo Direct3D associato all'oggetto tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="ef620-121">Retrieve the Direct3D device associated with the font object.</span></span><br/>                                                                              |
| [<span data-ttu-id="ef620-122">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="ef620-122">**GetGlyphData**</span></span>](id3dx10font-getglyphdata.md)           | <span data-ttu-id="ef620-123">Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.</span><span class="sxs-lookup"><span data-stu-id="ef620-123">Return information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                     |
| [<span data-ttu-id="ef620-124">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="ef620-124">**GetTextMetrics**</span></span>](id3dx10font-gettextmetrics.md)       | <span data-ttu-id="ef620-125">Recuperare le caratteristiche dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="ef620-125">Retrieve font characteristics.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="ef620-126">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="ef620-126">**PreloadCharacters**</span></span>](id3dx10font-preloadcharacters.md) | <span data-ttu-id="ef620-127">Caricare una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef620-127">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                        |
| [<span data-ttu-id="ef620-128">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="ef620-128">**PreloadGlyphs**</span></span>](id3dx10font-preloadglyphs.md)         | <span data-ttu-id="ef620-129">Caricare una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef620-129">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                            |
| [<span data-ttu-id="ef620-130">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="ef620-130">**PreloadText**</span></span>](id3dx10font-preloadtext.md)             | <span data-ttu-id="ef620-131">Caricare il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef620-131">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="ef620-132">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef620-132">This method supports ANSI and Unicode strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef620-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef620-133">Remarks</span></span>

<span data-ttu-id="ef620-134">L'interfaccia ID3DX10Font viene ottenuta chiamando [**D3DX10CreateFont**](d3dx10createfont.md) o [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="ef620-134">The ID3DX10Font interface is obtained by calling [**D3DX10CreateFont**](d3dx10createfont.md) or [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span></span>

<span data-ttu-id="ef620-135">Il tipo LPD3DX10FONT è definito come puntatore all'interfaccia ID3DX10Font.</span><span class="sxs-lookup"><span data-stu-id="ef620-135">The LPD3DX10FONT type is defined as a pointer to the ID3DX10Font interface.</span></span>


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a><span data-ttu-id="ef620-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef620-136">Requirements</span></span>



| <span data-ttu-id="ef620-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef620-137">Requirement</span></span> | <span data-ttu-id="ef620-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ef620-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef620-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef620-139">Header</span></span><br/>  | <dl> <span data-ttu-id="ef620-140"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef620-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef620-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef620-141">Library</span></span><br/> | <dl> <span data-ttu-id="ef620-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef620-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef620-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef620-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef620-144">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ef620-144">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
