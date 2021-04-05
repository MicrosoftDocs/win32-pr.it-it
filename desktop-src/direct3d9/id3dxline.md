---
description: L'interfaccia ID3DXLine implementa il disegno a linee usando triangoli con trama.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interfaccia ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058698"
---
# <a name="id3dxline-interface"></a><span data-ttu-id="a649d-103">Interfaccia ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="a649d-103">ID3DXLine interface</span></span>

<span data-ttu-id="a649d-104">L'interfaccia ID3DXLine implementa il disegno a linee usando triangoli con trama.</span><span class="sxs-lookup"><span data-stu-id="a649d-104">The ID3DXLine interface implements line drawing using textured triangles.</span></span>

## <a name="members"></a><span data-ttu-id="a649d-105">Membri</span><span class="sxs-lookup"><span data-stu-id="a649d-105">Members</span></span>

<span data-ttu-id="a649d-106">L'interfaccia **ID3DXLine** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a649d-106">The **ID3DXLine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a649d-107">**ID3DXLine** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a649d-107">**ID3DXLine** also has these types of members:</span></span>

-   [<span data-ttu-id="a649d-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="a649d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a649d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="a649d-109">Methods</span></span>

<span data-ttu-id="a649d-110">L'interfaccia **ID3DXLine** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a649d-110">The **ID3DXLine** interface has these methods.</span></span>



| <span data-ttu-id="a649d-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="a649d-111">Method</span></span>                                                | <span data-ttu-id="a649d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a649d-112">Description</span></span>                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a649d-113">**Inizia**</span><span class="sxs-lookup"><span data-stu-id="a649d-113">**Begin**</span></span>](id3dxline--begin.md)                     | <span data-ttu-id="a649d-114">Prepara un dispositivo per il disegno delle linee.</span><span class="sxs-lookup"><span data-stu-id="a649d-114">Prepares a device for drawing lines.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="a649d-115">**Disegna**</span><span class="sxs-lookup"><span data-stu-id="a649d-115">**Draw**</span></span>](id3dxline--draw.md)                       | <span data-ttu-id="a649d-116">Disegna una striscia di linea nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a649d-116">Draws a line strip in screen space.</span></span> <span data-ttu-id="a649d-117">L'input è sotto forma di matrice che definisce i punti (di [**D3DXVECTOR2**](d3dxvector2.md)) nell'elenco di righe.</span><span class="sxs-lookup"><span data-stu-id="a649d-117">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span><br/>                                   |
| [<span data-ttu-id="a649d-118">**DrawTransform**</span><span class="sxs-lookup"><span data-stu-id="a649d-118">**DrawTransform**</span></span>](id3dxline--drawtransform.md)     | <span data-ttu-id="a649d-119">Disegna una striscia di linea nello spazio dello schermo con una matrice di trasformazione input specificata.</span><span class="sxs-lookup"><span data-stu-id="a649d-119">Draws a line strip in screen space with a specified input transformation matrix.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="a649d-120">**Fine**</span><span class="sxs-lookup"><span data-stu-id="a649d-120">**End**</span></span>](id3dxline--end.md)                         | <span data-ttu-id="a649d-121">Ripristina lo stato del dispositivo nel modo in cui si trovava quando è stato chiamato [**ID3DXLine:: Begin**](id3dxline--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="a649d-121">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span><br/>                                                                                 |
| [<span data-ttu-id="a649d-122">**GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="a649d-122">**GetAntialias**</span></span>](id3dxline--getantialias.md)       | <span data-ttu-id="a649d-123">Ottiene lo stato di anti-aliasing della linea.</span><span class="sxs-lookup"><span data-stu-id="a649d-123">Gets the line antialiasing state.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="a649d-124">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="a649d-124">**GetDevice**</span></span>](id3dxline--getdevice.md)             | <span data-ttu-id="a649d-125">Recupera il dispositivo Direct3D associato all'oggetto riga.</span><span class="sxs-lookup"><span data-stu-id="a649d-125">Retrieves the Direct3D device associated with the line object.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="a649d-126">**GetGLLines**</span><span class="sxs-lookup"><span data-stu-id="a649d-126">**GetGLLines**</span></span>](id3dxline--getgllines.md)           | <span data-ttu-id="a649d-127">Ottiene la modalità di disegno di riga in stile OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a649d-127">Gets the OpenGL-style line-drawing mode.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="a649d-128">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="a649d-128">**GetPattern**</span></span>](id3dxline--getpattern.md)           | <span data-ttu-id="a649d-129">Ottiene il pattern stipple di linea.</span><span class="sxs-lookup"><span data-stu-id="a649d-129">Gets the line stipple pattern.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="a649d-130">**GetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="a649d-130">**GetPatternScale**</span></span>](id3dxline--getpatternscale.md) | <span data-ttu-id="a649d-131">Ottiene il valore della scala del pattern stipple.</span><span class="sxs-lookup"><span data-stu-id="a649d-131">Gets the stipple-pattern scale value.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="a649d-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="a649d-132">**GetWidth**</span></span>](id3dxline--getwidth.md)               | <span data-ttu-id="a649d-133">Ottiene lo spessore della linea.</span><span class="sxs-lookup"><span data-stu-id="a649d-133">Gets the thickness of the line.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="a649d-134">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="a649d-134">**OnLostDevice**</span></span>](id3dxline--onlostdevice.md)       | <span data-ttu-id="a649d-135">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="a649d-135">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="a649d-136">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a649d-136">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="a649d-137">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="a649d-137">**OnResetDevice**</span></span>](id3dxline--onresetdevice.md)     | <span data-ttu-id="a649d-138">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="a649d-138">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="a649d-139">**SetAntialias**</span><span class="sxs-lookup"><span data-stu-id="a649d-139">**SetAntialias**</span></span>](id3dxline--setantialias.md)       | <span data-ttu-id="a649d-140">Consente di abilitare l'anti-aliasing della linea.</span><span class="sxs-lookup"><span data-stu-id="a649d-140">Toggles line antialiasing.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="a649d-141">**SetGLLines**</span><span class="sxs-lookup"><span data-stu-id="a649d-141">**SetGLLines**</span></span>](id3dxline--setgllines.md)           | <span data-ttu-id="a649d-142">Consente di impostare la modalità per creare linee di tipo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a649d-142">Toggles the mode to draw OpenGL-style lines.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="a649d-143">**Criteri di ricerca**</span><span class="sxs-lookup"><span data-stu-id="a649d-143">**SetPattern**</span></span>](id3dxline--setpattern.md)           | <span data-ttu-id="a649d-144">Applica un modello stipple alla riga.</span><span class="sxs-lookup"><span data-stu-id="a649d-144">Applies a stipple pattern to the line.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="a649d-145">**SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="a649d-145">**SetPatternScale**</span></span>](id3dxline--setpatternscale.md) | <span data-ttu-id="a649d-146">Estende il pattern stipple lungo la direzione della riga.</span><span class="sxs-lookup"><span data-stu-id="a649d-146">Stretches the stipple pattern along the line direction.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="a649d-147">**SetWidth**</span><span class="sxs-lookup"><span data-stu-id="a649d-147">**SetWidth**</span></span>](id3dxline--setwidth.md)               | <span data-ttu-id="a649d-148">Specifica lo spessore della linea.</span><span class="sxs-lookup"><span data-stu-id="a649d-148">Specifies the thickness of the line.</span></span><br/>                                                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="a649d-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="a649d-149">Remarks</span></span>

<span data-ttu-id="a649d-150">Creare un oggetto disegno a linee con [**D3DXCreateLine**](d3dxcreateline.md).</span><span class="sxs-lookup"><span data-stu-id="a649d-150">Create a line drawing object with [**D3DXCreateLine**](d3dxcreateline.md).</span></span>

<span data-ttu-id="a649d-151">Il tipo LPD3DXLINE è definito come puntatore all'interfaccia **ID3DXLine** .</span><span class="sxs-lookup"><span data-stu-id="a649d-151">The LPD3DXLINE type is defined as a pointer to the **ID3DXLine** interface.</span></span>


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a><span data-ttu-id="a649d-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a649d-152">Requirements</span></span>



| <span data-ttu-id="a649d-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="a649d-153">Requirement</span></span> | <span data-ttu-id="a649d-154">Valore</span><span class="sxs-lookup"><span data-stu-id="a649d-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a649d-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a649d-155">Header</span></span><br/>  | <dl> <span data-ttu-id="a649d-156"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a649d-156"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a649d-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="a649d-157">Library</span></span><br/> | <dl> <span data-ttu-id="a649d-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a649d-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a649d-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a649d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a649d-160">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="a649d-160">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
