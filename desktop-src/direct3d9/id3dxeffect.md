---
description: Utilizzato per impostare ed eseguire query sugli effetti e per scegliere tecniche. Un oggetto Effect può contenere più tecniche per il rendering dello stesso effetto.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interfaccia ID3DXEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322350"
---
# <a name="id3dxeffect-interface"></a><span data-ttu-id="83264-104">Interfaccia ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="83264-104">ID3DXEffect interface</span></span>

<span data-ttu-id="83264-105">Utilizzato per impostare ed eseguire query sugli effetti e per scegliere tecniche.</span><span class="sxs-lookup"><span data-stu-id="83264-105">Used to set and query effects, and to choose techniques.</span></span> <span data-ttu-id="83264-106">Un oggetto Effect può contenere più tecniche per il rendering dello stesso effetto.</span><span class="sxs-lookup"><span data-stu-id="83264-106">An effect object can contain multiple techniques to render the same effect.</span></span>

## <a name="members"></a><span data-ttu-id="83264-107">Membri</span><span class="sxs-lookup"><span data-stu-id="83264-107">Members</span></span>

<span data-ttu-id="83264-108">L'interfaccia **ID3DXEffect** eredita da [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="83264-108">The **ID3DXEffect** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="83264-109">**ID3DXEffect** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="83264-109">**ID3DXEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="83264-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="83264-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="83264-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="83264-111">Methods</span></span>

<span data-ttu-id="83264-112">L'interfaccia **ID3DXEffect** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="83264-112">The **ID3DXEffect** interface has these methods.</span></span>



| <span data-ttu-id="83264-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="83264-113">Method</span></span>                                                                | <span data-ttu-id="83264-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83264-114">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83264-115">**ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="83264-115">**ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)       | <span data-ttu-id="83264-116">Applicare i valori in un blocco di stato allo stato del sistema con effetto corrente.</span><span class="sxs-lookup"><span data-stu-id="83264-116">Apply the values in a state block to the current effect system state.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="83264-117">**Inizia**</span><span class="sxs-lookup"><span data-stu-id="83264-117">**Begin**</span></span>](id3dxeffect--begin.md)                                   | <span data-ttu-id="83264-118">Avvia una tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="83264-118">Starts an active technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="83264-119">**BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="83264-119">**BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)       | <span data-ttu-id="83264-120">Avviare l'acquisizione delle modifiche di stato in un blocco di parametri.</span><span class="sxs-lookup"><span data-stu-id="83264-120">Start capturing state changes in a parameter block.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="83264-121">**BeginPass**</span><span class="sxs-lookup"><span data-stu-id="83264-121">**BeginPass**</span></span>](id3dxeffect--beginpass.md)                           | <span data-ttu-id="83264-122">Inizia un passaggio, all'interno della tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="83264-122">Begins a pass, within the active technique.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="83264-123">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="83264-123">**CloneEffect**</span></span>](id3dxeffect--cloneeffect.md)                       | <span data-ttu-id="83264-124">Crea una copia di un effetto.</span><span class="sxs-lookup"><span data-stu-id="83264-124">Creates a copy of an effect.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="83264-125">**CommitChanges**</span><span class="sxs-lookup"><span data-stu-id="83264-125">**CommitChanges**</span></span>](id3dxeffect--commitchanges.md)                   | <span data-ttu-id="83264-126">Propagare le modifiche di stato che si verificano all'interno di un passaggio attivo al dispositivo prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="83264-126">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span><br/>                                                                                           |
| [<span data-ttu-id="83264-127">**DeleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="83264-127">**DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)     | <span data-ttu-id="83264-128">Elimina un blocco di parametri.</span><span class="sxs-lookup"><span data-stu-id="83264-128">Delete a parameter block.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="83264-129">**Fine**</span><span class="sxs-lookup"><span data-stu-id="83264-129">**End**</span></span>](id3dxeffect--end.md)                                       | <span data-ttu-id="83264-130">Termina una tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="83264-130">Ends an active technique.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="83264-131">**EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="83264-131">**EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)           | <span data-ttu-id="83264-132">Arresta l'acquisizione delle modifiche allo stato del parametro dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="83264-132">Stop capturing effect parameter state changes.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="83264-133">**EndPass**</span><span class="sxs-lookup"><span data-stu-id="83264-133">**EndPass**</span></span>](id3dxeffect--endpass.md)                               | <span data-ttu-id="83264-134">Termina un passaggio attivo.</span><span class="sxs-lookup"><span data-stu-id="83264-134">End an active pass.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="83264-135">**FindNextValidTechnique**</span><span class="sxs-lookup"><span data-stu-id="83264-135">**FindNextValidTechnique**</span></span>](id3dxeffect--findnextvalidtechnique.md) | <span data-ttu-id="83264-136">Cerca la tecnica valida successiva, iniziando dalla tecnica dopo la tecnica specificata.</span><span class="sxs-lookup"><span data-stu-id="83264-136">Searches for the next valid technique, starting at the technique after the specified technique.</span></span><br/>                                                                                       |
| [<span data-ttu-id="83264-137">**GetCurrentTechnique**</span><span class="sxs-lookup"><span data-stu-id="83264-137">**GetCurrentTechnique**</span></span>](id3dxeffect--getcurrenttechnique.md)       | <span data-ttu-id="83264-138">Ottiene la tecnica corrente.</span><span class="sxs-lookup"><span data-stu-id="83264-138">Gets the current technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="83264-139">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="83264-139">**GetDevice**</span></span>](id3dxeffect--getdevice.md)                           | <span data-ttu-id="83264-140">Recupera il dispositivo associato all'effetto.</span><span class="sxs-lookup"><span data-stu-id="83264-140">Retrieves the device associated with the effect.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="83264-141">**GetPool**</span><span class="sxs-lookup"><span data-stu-id="83264-141">**GetPool**</span></span>](id3dxeffect--getpool.md)                               | <span data-ttu-id="83264-142">Ottiene un puntatore al pool di parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="83264-142">Gets a pointer to the pool of shared parameters.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="83264-143">**GetStateManager**</span><span class="sxs-lookup"><span data-stu-id="83264-143">**GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)               | <span data-ttu-id="83264-144">Ottenere il gestore degli Stati dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="83264-144">Get the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="83264-145">**IsParameterUsed**</span><span class="sxs-lookup"><span data-stu-id="83264-145">**IsParameterUsed**</span></span>](id3dxeffect--isparameterused.md)               | <span data-ttu-id="83264-146">Determina se un parametro viene utilizzato dalla tecnica.</span><span class="sxs-lookup"><span data-stu-id="83264-146">Determines if a parameter is used by the technique.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="83264-147">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="83264-147">**OnLostDevice**</span></span>](id3dxeffect--onlostdevice.md)                     | <span data-ttu-id="83264-148">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="83264-148">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="83264-149">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83264-149">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="83264-150">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="83264-150">**OnResetDevice**</span></span>](id3dxeffect--onresetdevice.md)                   | <span data-ttu-id="83264-151">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="83264-151">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="83264-152">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="83264-152">**SetRawValue**</span></span>](id3dxeffect--setrawvalue.md)                       | <span data-ttu-id="83264-153">Impostare un intervallo contiguo di costanti dello shader con una copia di memoria.</span><span class="sxs-lookup"><span data-stu-id="83264-153">Set a contiguous range of shader constants with a memory copy.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="83264-154">**SetStateManager**</span><span class="sxs-lookup"><span data-stu-id="83264-154">**SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)               | <span data-ttu-id="83264-155">Impostare il gestore degli Stati dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="83264-155">Set the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="83264-156">**Setechnique**</span><span class="sxs-lookup"><span data-stu-id="83264-156">**SetTechnique**</span></span>](id3dxeffect--settechnique.md)                     | <span data-ttu-id="83264-157">Imposta la tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="83264-157">Sets the active technique.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="83264-158">**ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="83264-158">**ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)           | <span data-ttu-id="83264-159">Convalidare una tecnica.</span><span class="sxs-lookup"><span data-stu-id="83264-159">Validate a technique.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="83264-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="83264-160">Remarks</span></span>

<span data-ttu-id="83264-161">L'interfaccia ID3DXEffect viene ottenuta chiamando [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)o [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="83264-161">The ID3DXEffect interface is obtained by calling [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md), or [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span></span>

<span data-ttu-id="83264-162">Il tipo LPD3DXEFFECT è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="83264-162">The LPD3DXEFFECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a><span data-ttu-id="83264-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83264-163">Requirements</span></span>



| <span data-ttu-id="83264-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="83264-164">Requirement</span></span> | <span data-ttu-id="83264-165">Valore</span><span class="sxs-lookup"><span data-stu-id="83264-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83264-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83264-166">Header</span></span><br/>  | <dl> <span data-ttu-id="83264-167"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="83264-167"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="83264-168">Libreria</span><span class="sxs-lookup"><span data-stu-id="83264-168">Library</span></span><br/> | <dl> <span data-ttu-id="83264-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83264-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="83264-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83264-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83264-171">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="83264-171">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="83264-172">Interfacce degli effetti</span><span class="sxs-lookup"><span data-stu-id="83264-172">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="83264-173">**D3DXCreateEffect**</span><span class="sxs-lookup"><span data-stu-id="83264-173">**D3DXCreateEffect**</span></span>](d3dxcreateeffect.md)
</dt> <dt>

[<span data-ttu-id="83264-174">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="83264-174">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> <dt>

[<span data-ttu-id="83264-175">**D3DXCreateEffectFromResource**</span><span class="sxs-lookup"><span data-stu-id="83264-175">**D3DXCreateEffectFromResource**</span></span>](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




