---
description: L'interfaccia ID3DXFont incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interfaccia ID3DXFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323538"
---
# <a name="id3dxfont-interface"></a><span data-ttu-id="5e7f1-103">Interfaccia ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="5e7f1-103">ID3DXFont interface</span></span>

<span data-ttu-id="5e7f1-104">L'interfaccia ID3DXFont incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-104">The ID3DXFont interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="5e7f1-105">Membri</span><span class="sxs-lookup"><span data-stu-id="5e7f1-105">Members</span></span>

<span data-ttu-id="5e7f1-106">L'interfaccia **ID3DXFont** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5e7f1-106">The **ID3DXFont** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5e7f1-107">**ID3DXFont** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5e7f1-107">**ID3DXFont** also has these types of members:</span></span>

-   [<span data-ttu-id="5e7f1-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="5e7f1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5e7f1-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="5e7f1-109">Methods</span></span>

<span data-ttu-id="5e7f1-110">L'interfaccia **ID3DXFont** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-110">The **ID3DXFont** interface has these methods.</span></span>



| <span data-ttu-id="5e7f1-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="5e7f1-111">Method</span></span>                                                    | <span data-ttu-id="5e7f1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e7f1-112">Description</span></span>                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e7f1-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-113">**DrawText**</span></span>](id3dxfont--drawtext.md)                   | <span data-ttu-id="5e7f1-114">Disegna il testo formattato.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-114">Draws formatted text.</span></span> <span data-ttu-id="5e7f1-115">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="5e7f1-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-116">**GetDC**</span></span>](id3dxfont--getdc.md)                         | <span data-ttu-id="5e7f1-117">Restituisce un handle per un contesto di periferica di visualizzazione (DC) con il set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-117">Returns a handle to a display device context (DC) that has the font set.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="5e7f1-118">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-118">**GetDesc**</span></span>](id3dxfont--getdesc.md)                     | <span data-ttu-id="5e7f1-119">Ottiene una descrizione dell'oggetto del tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-119">Gets a description of the current font object.</span></span> <span data-ttu-id="5e7f1-120">GetDescW e getdesca sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito a una struttura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ Desca** , rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-120">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span><br/> |
| [<span data-ttu-id="5e7f1-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-121">**GetDevice**</span></span>](id3dxfont--getdevice.md)                 | <span data-ttu-id="5e7f1-122">Recupera il dispositivo Direct3D associato all'oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-122">Retrieves the Direct3D device associated with the font object.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="5e7f1-123">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-123">**GetGlyphData**</span></span>](id3dxfont--getglyphdata.md)           | <span data-ttu-id="5e7f1-124">Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-124">Returns information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="5e7f1-125">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-125">**GetTextMetrics**</span></span>](id3dxfont--gettextmetrics.md)       | <span data-ttu-id="5e7f1-126">Recupera le caratteristiche dei tipi di carattere identificate in una struttura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="5e7f1-126">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="5e7f1-127">Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-127">This method supports ANSI and Unicode compiler settings.</span></span><br/>                                                                       |
| [<span data-ttu-id="5e7f1-128">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-128">**OnLostDevice**</span></span>](id3dxfont--onlostdevice.md)           | <span data-ttu-id="5e7f1-129">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-129">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="5e7f1-130">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-130">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/>                                              |
| [<span data-ttu-id="5e7f1-131">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-131">**OnResetDevice**</span></span>](id3dxfont--onresetdevice.md)         | <span data-ttu-id="5e7f1-132">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-132">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="5e7f1-133">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-133">**PreloadCharacters**</span></span>](id3dxfont--preloadcharacters.md) | <span data-ttu-id="5e7f1-134">Carica una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-134">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="5e7f1-135">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-135">**PreloadGlyphs**</span></span>](id3dxfont--preloadglyphs.md)         | <span data-ttu-id="5e7f1-136">Carica una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-136">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="5e7f1-137">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="5e7f1-137">**PreloadText**</span></span>](id3dxfont--preloadtext.md)             | <span data-ttu-id="5e7f1-138">Carica il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-138">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="5e7f1-139">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e7f1-139">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="5e7f1-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e7f1-140">Remarks</span></span>

<span data-ttu-id="5e7f1-141">L'interfaccia **ID3DXFont** viene ottenuta chiamando [**D3DXCreateFont**](d3dxcreatefont.md) o [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="5e7f1-141">The **ID3DXFont** interface is obtained by calling [**D3DXCreateFont**](d3dxcreatefont.md) or [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span></span>

<span data-ttu-id="5e7f1-142">Il tipo LPD3DXFONT è definito come puntatore all'interfaccia **ID3DXFont** .</span><span class="sxs-lookup"><span data-stu-id="5e7f1-142">The LPD3DXFONT type is defined as a pointer to the **ID3DXFont** interface.</span></span>


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a><span data-ttu-id="5e7f1-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e7f1-143">Requirements</span></span>



| <span data-ttu-id="5e7f1-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e7f1-144">Requirement</span></span> | <span data-ttu-id="5e7f1-145">Valore</span><span class="sxs-lookup"><span data-stu-id="5e7f1-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e7f1-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e7f1-146">Header</span></span><br/>  | <dl> <span data-ttu-id="5e7f1-147"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f1-147"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5e7f1-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e7f1-148">Library</span></span><br/> | <dl> <span data-ttu-id="5e7f1-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f1-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e7f1-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e7f1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e7f1-151">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="5e7f1-151">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
