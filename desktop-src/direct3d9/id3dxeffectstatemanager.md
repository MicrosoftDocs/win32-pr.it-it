---
description: Si tratta di un'interfaccia implementata dall'utente che consente a un utente di impostare lo stato del dispositivo da un effetto.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Interfaccia ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355229"
---
# <a name="id3dxeffectstatemanager-interface"></a><span data-ttu-id="333b4-103">Interfaccia ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="333b4-103">ID3DXEffectStateManager interface</span></span>

<span data-ttu-id="333b4-104">Si tratta di un'interfaccia implementata dall'utente che consente a un utente di impostare lo stato del dispositivo da un effetto.</span><span class="sxs-lookup"><span data-stu-id="333b4-104">This is a user-implemented interface that allows a user to set the device state from an effect.</span></span> <span data-ttu-id="333b4-105">Ognuno dei metodi in questa interfaccia deve essere implementato dall'utente e sarà quindi utilizzato come callback all'applicazione quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="333b4-105">Each of the methods in this interface must be implemented by the user and will then be used as callbacks to the application when either of the following occur:</span></span>

-   <span data-ttu-id="333b4-106">Un effetto chiama [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="333b4-106">An effect calls [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="333b4-107">Lo stato dell'effetto viene aggiornato dinamicamente chiamando l'API di modifica dello stato appropriato.</span><span class="sxs-lookup"><span data-stu-id="333b4-107">Effect state is dynamically updated by calling the appropriate state change API.</span></span> <span data-ttu-id="333b4-108">Per informazioni dettagliate, vedere singole pagine dei metodi.</span><span class="sxs-lookup"><span data-stu-id="333b4-108">See individual method pages for details.</span></span>

<span data-ttu-id="333b4-109">Quando un'applicazione usa il gestore degli Stati per implementare callback personalizzati, un effetto non salva più automaticamente e ripristina lo stato quando si chiamano [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="333b4-109">When an application uses the state manager to implement custom callbacks, an effect no longer automatically saves and restores state when calling [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="333b4-110">Poiché l'applicazione ha implementato un comportamento di salvataggio e ripristino personalizzato nei callback, questo comportamento automatico viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="333b4-110">Because the application has implemented a custom save and restore behavior in the callbacks, this automatic behavior is bypassed.</span></span>

## <a name="members"></a><span data-ttu-id="333b4-111">Membri</span><span class="sxs-lookup"><span data-stu-id="333b4-111">Members</span></span>

<span data-ttu-id="333b4-112">L'interfaccia **ID3DXEffectStateManager** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="333b4-112">The **ID3DXEffectStateManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="333b4-113">**ID3DXEffectStateManager** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="333b4-113">**ID3DXEffectStateManager** also has these types of members:</span></span>

-   [<span data-ttu-id="333b4-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="333b4-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="333b4-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="333b4-115">Methods</span></span>

<span data-ttu-id="333b4-116">L'interfaccia **ID3DXEffectStateManager** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="333b4-116">The **ID3DXEffectStateManager** interface has these methods.</span></span>



| <span data-ttu-id="333b4-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="333b4-117">Method</span></span>                                                                                | <span data-ttu-id="333b4-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="333b4-118">Description</span></span>                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="333b4-119">**Alleggeribile**</span><span class="sxs-lookup"><span data-stu-id="333b4-119">**LightEnable**</span></span>](id3dxeffectstatemanager--lightenable.md)                           | <span data-ttu-id="333b4-120">Funzione di callback che deve essere implementata da un utente per abilitare o disabilitare una luce.</span><span class="sxs-lookup"><span data-stu-id="333b4-120">A callback function that must be implemented by a user to enable/disable a light.</span></span><br/>                                 |
| [<span data-ttu-id="333b4-121">**SetFVF**</span><span class="sxs-lookup"><span data-stu-id="333b4-121">**SetFVF**</span></span>](id3dxeffectstatemanager--setfvf.md)                                     | <span data-ttu-id="333b4-122">Funzione di callback che deve essere implementata da un utente per impostare un codice FVF.</span><span class="sxs-lookup"><span data-stu-id="333b4-122">A callback function that must be implemented by a user to set a FVF code.</span></span><br/>                                         |
| [<span data-ttu-id="333b4-123">**Chiaro**</span><span class="sxs-lookup"><span data-stu-id="333b4-123">**SetLight**</span></span>](id3dxeffectstatemanager--setlight.md)                                 | <span data-ttu-id="333b4-124">Funzione di callback che deve essere implementata da un utente per impostare una luce.</span><span class="sxs-lookup"><span data-stu-id="333b4-124">A callback function that must be implemented by a user to set a light.</span></span><br/>                                            |
| [<span data-ttu-id="333b4-125">**Materiali**</span><span class="sxs-lookup"><span data-stu-id="333b4-125">**SetMaterial**</span></span>](id3dxeffectstatemanager--setmaterial.md)                           | <span data-ttu-id="333b4-126">Funzione di callback che deve essere implementata da un utente per impostare lo stato del materiale.</span><span class="sxs-lookup"><span data-stu-id="333b4-126">A callback function that must be implemented by a user to set material state.</span></span><br/>                                     |
| [<span data-ttu-id="333b4-127">**SetNPatchMode**</span><span class="sxs-lookup"><span data-stu-id="333b4-127">**SetNPatchMode**</span></span>](id3dxeffectstatemanager--setnpatchmode.md)                       | <span data-ttu-id="333b4-128">Funzione di callback che deve essere implementata da un utente per impostare il numero di segmenti di suddivisione per N-patch.</span><span class="sxs-lookup"><span data-stu-id="333b4-128">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span><br/>   |
| [<span data-ttu-id="333b4-129">**SetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="333b4-129">**SetPixelShader**</span></span>](id3dxeffectstatemanager--setpixelshader.md)                     | <span data-ttu-id="333b4-130">Funzione di callback che deve essere implementata da un utente per impostare un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="333b4-130">A callback function that must be implemented by a user to set a pixel shader.</span></span><br/>                                     |
| [<span data-ttu-id="333b4-131">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="333b4-131">**SetPixelShaderConstantB**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | <span data-ttu-id="333b4-132">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="333b4-132">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="333b4-133">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="333b4-133">**SetPixelShaderConstantF**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | <span data-ttu-id="333b4-134">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="333b4-134">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="333b4-135">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="333b4-135">**SetPixelShaderConstantI**</span></span>](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | <span data-ttu-id="333b4-136">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="333b4-136">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |
| [<span data-ttu-id="333b4-137">**SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="333b4-137">**SetRenderState**</span></span>](id3dxeffectstatemanager--setrenderstate.md)                     | <span data-ttu-id="333b4-138">Funzione di callback che deve essere implementata da un utente per impostare lo stato di rendering.</span><span class="sxs-lookup"><span data-stu-id="333b4-138">A callback function that must be implemented by a user to set render state.</span></span><br/>                                       |
| [<span data-ttu-id="333b4-139">**SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="333b4-139">**SetSamplerState**</span></span>](id3dxeffectstatemanager--setsamplerstate.md)                   | <span data-ttu-id="333b4-140">Funzione di callback che deve essere implementata da un utente per impostare un campionatore.</span><span class="sxs-lookup"><span data-stu-id="333b4-140">A callback function that must be implemented by a user to set a sampler.</span></span><br/>                                          |
| [<span data-ttu-id="333b4-141">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="333b4-141">**SetTexture**</span></span>](id3dxeffectstatemanager--settexture.md)                             | <span data-ttu-id="333b4-142">Funzione di callback che deve essere implementata da un utente per impostare una trama.</span><span class="sxs-lookup"><span data-stu-id="333b4-142">A callback function that must be implemented by a user to set a texture.</span></span><br/>                                          |
| [<span data-ttu-id="333b4-143">**SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="333b4-143">**SetTextureStageState**</span></span>](id3dxeffectstatemanager--settexturestagestate.md)         | <span data-ttu-id="333b4-144">Funzione di callback che deve essere implementata da un utente per impostare lo stato della fase della trama.</span><span class="sxs-lookup"><span data-stu-id="333b4-144">A callback function that must be implemented by a user to set the texture stage state.</span></span><br/>                            |
| [<span data-ttu-id="333b4-145">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="333b4-145">**SetTransform**</span></span>](id3dxeffectstatemanager--settransform.md)                         | <span data-ttu-id="333b4-146">Funzione di callback che deve essere implementata da un utente per impostare una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="333b4-146">A callback function that must be implemented by a user to set a transform.</span></span><br/>                                        |
| [<span data-ttu-id="333b4-147">**SetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="333b4-147">**SetVertexShader**</span></span>](id3dxeffectstatemanager--setvertexshader.md)                   | <span data-ttu-id="333b4-148">Funzione di callback che deve essere implementata da un utente per impostare un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="333b4-148">A callback function that must be implemented by a user to set a vertex shader.</span></span><br/>                                    |
| [<span data-ttu-id="333b4-149">**SetVertexShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="333b4-149">**SetVertexShaderConstantB**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantb.md) | <span data-ttu-id="333b4-150">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="333b4-150">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="333b4-151">**SetVertexShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="333b4-151">**SetVertexShaderConstantF**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantf.md) | <span data-ttu-id="333b4-152">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="333b4-152">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="333b4-153">**SetVertexShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="333b4-153">**SetVertexShaderConstantI**</span></span>](id3dxeffectstatemanager--setvertexshaderconstanti.md) | <span data-ttu-id="333b4-154">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="333b4-154">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="333b4-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="333b4-155">Remarks</span></span>

<span data-ttu-id="333b4-156">Un utente crea un'interfaccia ID3DXEffectStateManager implementando una classe che deriva da questa interfaccia e implementando tutti i metodi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="333b4-156">A user creates an ID3DXEffectStateManager interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span> <span data-ttu-id="333b4-157">Una volta creata l'interfaccia, è possibile ottenere o impostare il gestore di stato all'interno di un effetto usando [**ID3DXEffect:: GetStateManager**](id3dxeffect--getstatemanager.md) e [**ID3DXEffect:: SetStateManager**](id3dxeffect--setstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="333b4-157">Once the interface is created, you can get or set the state manager within an effect using [**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md) and [**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md).</span></span>

<span data-ttu-id="333b4-158">Il tipo LPD3DXEFFECTSTATEMANAGER è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="333b4-158">The LPD3DXEFFECTSTATEMANAGER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a><span data-ttu-id="333b4-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="333b4-159">Requirements</span></span>



| <span data-ttu-id="333b4-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="333b4-160">Requirement</span></span> | <span data-ttu-id="333b4-161">Valore</span><span class="sxs-lookup"><span data-stu-id="333b4-161">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="333b4-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="333b4-162">Header</span></span><br/>  | <dl> <span data-ttu-id="333b4-163"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="333b4-163"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="333b4-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="333b4-164">Library</span></span><br/> | <dl> <span data-ttu-id="333b4-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="333b4-165"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="333b4-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="333b4-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="333b4-167">Interfacce degli effetti</span><span class="sxs-lookup"><span data-stu-id="333b4-167">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
