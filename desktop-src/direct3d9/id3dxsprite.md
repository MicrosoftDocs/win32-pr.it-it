---
description: L'interfaccia ID3DXSprite fornisce un set di metodi che semplificano il processo di creazione di sprite con Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interfaccia ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886295"
---
# <a name="id3dxsprite-interface"></a><span data-ttu-id="ec535-103">Interfaccia ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="ec535-103">ID3DXSprite interface</span></span>

<span data-ttu-id="ec535-104">L'interfaccia ID3DXSprite fornisce un set di metodi che semplificano il processo di creazione di sprite con Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ec535-104">The ID3DXSprite interface provides a set of methods that simplify the process of drawing sprites using Microsoft Direct3D.</span></span>

## <a name="members"></a><span data-ttu-id="ec535-105">Membri</span><span class="sxs-lookup"><span data-stu-id="ec535-105">Members</span></span>

<span data-ttu-id="ec535-106">L'interfaccia **ID3DXSprite** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ec535-106">The **ID3DXSprite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ec535-107">**ID3DXSprite** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ec535-107">**ID3DXSprite** also has these types of members:</span></span>

-   [<span data-ttu-id="ec535-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="ec535-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ec535-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ec535-109">Methods</span></span>

<span data-ttu-id="ec535-110">L'interfaccia **ID3DXSprite** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ec535-110">The **ID3DXSprite** interface has these methods.</span></span>



| <span data-ttu-id="ec535-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="ec535-111">Method</span></span>                                                | <span data-ttu-id="ec535-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec535-112">Description</span></span>                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec535-113">**Inizia**</span><span class="sxs-lookup"><span data-stu-id="ec535-113">**Begin**</span></span>](id3dxsprite--begin.md)                   | <span data-ttu-id="ec535-114">Prepara un dispositivo per il disegno degli sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-114">Prepares a device for drawing sprites.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="ec535-115">**Disegna**</span><span class="sxs-lookup"><span data-stu-id="ec535-115">**Draw**</span></span>](id3dxsprite--draw.md)                     | <span data-ttu-id="ec535-116">Aggiunge uno sprite all'elenco di sprite in batch.</span><span class="sxs-lookup"><span data-stu-id="ec535-116">Adds a sprite to the list of batched sprites.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="ec535-117">**Fine**</span><span class="sxs-lookup"><span data-stu-id="ec535-117">**End**</span></span>](id3dxsprite--end.md)                       | <span data-ttu-id="ec535-118">Chiama [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) e ripristina lo stato del dispositivo in modo che sia stato prima della chiamata a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="ec535-118">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span><br/>                                            |
| [<span data-ttu-id="ec535-119">**Svuotamento**</span><span class="sxs-lookup"><span data-stu-id="ec535-119">**Flush**</span></span>](id3dxsprite--flush.md)                   | <span data-ttu-id="ec535-120">Impone l'invio di tutti gli sprite in batch al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ec535-120">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="ec535-121">Gli Stati del dispositivo rimangono invariati dopo l'ultima chiamata a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="ec535-121">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="ec535-122">L'elenco degli sprite in batch viene quindi cancellato.</span><span class="sxs-lookup"><span data-stu-id="ec535-122">The list of batched sprites is then cleared.</span></span><br/> |
| [<span data-ttu-id="ec535-123">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="ec535-123">**GetDevice**</span></span>](id3dxsprite--getdevice.md)           | <span data-ttu-id="ec535-124">Recupera il dispositivo associato all'oggetto Sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-124">Retrieves the device associated with the sprite object.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="ec535-125">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="ec535-125">**GetTransform**</span></span>](id3dxsprite--gettransform.md)     | <span data-ttu-id="ec535-126">Ottiene la trasformazione sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-126">Gets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="ec535-127">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="ec535-127">**OnLostDevice**</span></span>](id3dxsprite--onlostdevice.md)     | <span data-ttu-id="ec535-128">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="ec535-128">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="ec535-129">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ec535-129">This method should be called whenever a device is lost or before resetting a device.</span></span><br/>                              |
| [<span data-ttu-id="ec535-130">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="ec535-130">**OnResetDevice**</span></span>](id3dxsprite--onresetdevice.md)   | <span data-ttu-id="ec535-131">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="ec535-131">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="ec535-132">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="ec535-132">**SetTransform**</span></span>](id3dxsprite--settransform.md)     | <span data-ttu-id="ec535-133">Imposta la trasformazione sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-133">Sets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="ec535-134">**SetWorldViewLH**</span><span class="sxs-lookup"><span data-stu-id="ec535-134">**SetWorldViewLH**</span></span>](id3dxsprite--setworldviewlh.md) | <span data-ttu-id="ec535-135">Imposta la trasformazione di visualizzazione globale a sinistra per uno sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-135">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="ec535-136">È necessaria una chiamata a questo metodo prima di eseguire il Billboard o l'ordinamento degli sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-136">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                 |
| [<span data-ttu-id="ec535-137">**SetWorldViewRH**</span><span class="sxs-lookup"><span data-stu-id="ec535-137">**SetWorldViewRH**</span></span>](id3dxsprite--setworldviewrh.md) | <span data-ttu-id="ec535-138">Imposta la trasformazione di visualizzazione globale a destra per uno sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-138">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="ec535-139">È necessaria una chiamata a questo metodo prima di eseguire il Billboard o l'ordinamento degli sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-139">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="ec535-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec535-140">Remarks</span></span>

<span data-ttu-id="ec535-141">L'interfaccia **ID3DXSprite** viene ottenuta chiamando la funzione [**D3DXCreateSprite**](d3dxcreatesprite.md) .</span><span class="sxs-lookup"><span data-stu-id="ec535-141">The **ID3DXSprite** interface is obtained by calling the [**D3DXCreateSprite**](d3dxcreatesprite.md) function.</span></span>

<span data-ttu-id="ec535-142">L'applicazione in genere chiama prima [**ID3DXSprite:: Begin**](id3dxsprite--begin.md), che consente di controllare lo stato di rendering del dispositivo, la fusione alfa e la trasformazione e l'ordinamento degli sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-142">The application typically first calls [**ID3DXSprite::Begin**](id3dxsprite--begin.md), which allows control over the device render state, alpha blending, and sprite transformation and sorting.</span></span> <span data-ttu-id="ec535-143">Per ogni sprite da visualizzare, chiamare [**ID3DXSprite::D RAW**](id3dxsprite--draw.md).</span><span class="sxs-lookup"><span data-stu-id="ec535-143">Then for each sprite to be displayed, call [**ID3DXSprite::Draw**](id3dxsprite--draw.md).</span></span> <span data-ttu-id="ec535-144">**ID3DXSprite::D RAW** può essere chiamato ripetutamente per archiviare un numero qualsiasi di sprite.</span><span class="sxs-lookup"><span data-stu-id="ec535-144">**ID3DXSprite::Draw** can be called repeatedly to store any number of sprites.</span></span> <span data-ttu-id="ec535-145">Per visualizzare gli sprite in batch sul dispositivo, chiamare [**ID3DXSprite:: end**](id3dxsprite--end.md) o [**ID3DXSprite:: Flush**](id3dxsprite--flush.md).</span><span class="sxs-lookup"><span data-stu-id="ec535-145">To display the batched sprites to the device, call [**ID3DXSprite::End**](id3dxsprite--end.md) or [**ID3DXSprite::Flush**](id3dxsprite--flush.md).</span></span>

<span data-ttu-id="ec535-146">Il tipo LPD3DXSPRITE è definito come puntatore all'interfaccia **ID3DXSprite** .</span><span class="sxs-lookup"><span data-stu-id="ec535-146">The LPD3DXSPRITE type is defined as a pointer to the **ID3DXSprite** interface.</span></span>


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a><span data-ttu-id="ec535-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec535-147">Requirements</span></span>



| <span data-ttu-id="ec535-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec535-148">Requirement</span></span> | <span data-ttu-id="ec535-149">Valore</span><span class="sxs-lookup"><span data-stu-id="ec535-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec535-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec535-150">Header</span></span><br/>  | <dl> <span data-ttu-id="ec535-151"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec535-151"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ec535-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec535-152">Library</span></span><br/> | <dl> <span data-ttu-id="ec535-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec535-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ec535-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec535-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec535-155">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ec535-155">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
