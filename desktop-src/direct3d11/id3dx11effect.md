---
title: Interfaccia ID3DX11Effect (D3dx11effect. h)
description: Un'interfaccia ID3DX11Effect gestisce un set di oggetti di stato, risorse e shader per l'implementazione di un effetto di rendering.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Interfaccia ID3DX11Effect Direct3D 11
- Interfaccia ID3DX11Effect Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395946ea4276bc57595abdeb18e7d1755ca0ff1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996083"
---
# <a name="id3dx11effect-interface"></a><span data-ttu-id="c9249-105">Interfaccia ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="c9249-105">ID3DX11Effect interface</span></span>

<span data-ttu-id="c9249-106">Un'interfaccia **ID3DX11Effect** gestisce un set di oggetti di stato, risorse e shader per l'implementazione di un effetto di rendering.</span><span class="sxs-lookup"><span data-stu-id="c9249-106">An **ID3DX11Effect** interface manages a set of state objects, resources, and shaders for implementing a rendering effect.</span></span>

## <a name="members"></a><span data-ttu-id="c9249-107">Membri</span><span class="sxs-lookup"><span data-stu-id="c9249-107">Members</span></span>

<span data-ttu-id="c9249-108">L'interfaccia **ID3DX11Effect** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c9249-108">The **ID3DX11Effect** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c9249-109">**ID3DX11Effect** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c9249-109">**ID3DX11Effect** also has these types of members:</span></span>

-   [<span data-ttu-id="c9249-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="c9249-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c9249-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c9249-111">Methods</span></span>

<span data-ttu-id="c9249-112">L'interfaccia **ID3DX11Effect** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c9249-112">The **ID3DX11Effect** interface has these methods.</span></span>



| <span data-ttu-id="c9249-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="c9249-113">Method</span></span>                                                                     | <span data-ttu-id="c9249-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9249-114">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9249-115">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="c9249-115">**CloneEffect**</span></span>](id3dx11effect-cloneeffect.md)                           | <span data-ttu-id="c9249-116">Crea una copia di un'interfaccia effetto.</span><span class="sxs-lookup"><span data-stu-id="c9249-116">Creates a copy of an effect interface.</span></span><br/>                                         |
| [<span data-ttu-id="c9249-117">**GetClassLinkage**</span><span class="sxs-lookup"><span data-stu-id="c9249-117">**GetClassLinkage**</span></span>](id3dx11effect-getclasslinkage.md)                   | <span data-ttu-id="c9249-118">Ottiene un'interfaccia di collegamento di classe.</span><span class="sxs-lookup"><span data-stu-id="c9249-118">Gets a class linkage interface.</span></span><br/>                                                |
| [<span data-ttu-id="c9249-119">**GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="c9249-119">**GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md) | <span data-ttu-id="c9249-120">Ottenere un buffer costante in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="c9249-120">Get a constant buffer by index.</span></span><br/>                                                |
| [<span data-ttu-id="c9249-121">**GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="c9249-121">**GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)   | <span data-ttu-id="c9249-122">Ottenere un buffer costante in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c9249-122">Get a constant buffer by name.</span></span><br/>                                                 |
| [<span data-ttu-id="c9249-123">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="c9249-123">**GetDesc**</span></span>](id3dx11effect-getdesc.md)                                   | <span data-ttu-id="c9249-124">Ottenere una descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="c9249-124">Get an effect description.</span></span><br/>                                                     |
| [<span data-ttu-id="c9249-125">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="c9249-125">**GetDevice**</span></span>](id3dx11effect-getdevice.md)                               | <span data-ttu-id="c9249-126">Ottenere il dispositivo che ha creato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="c9249-126">Get the device that created the effect.</span></span><br/>                                        |
| [<span data-ttu-id="c9249-127">**GetGroupByIndex**</span><span class="sxs-lookup"><span data-stu-id="c9249-127">**GetGroupByIndex**</span></span>](id3dx11effect-getgroupbyindex.md)                   | <span data-ttu-id="c9249-128">Ottiene un effetto Group by index.</span><span class="sxs-lookup"><span data-stu-id="c9249-128">Gets an effect group by index.</span></span><br/>                                                 |
| [<span data-ttu-id="c9249-129">**GetGroupByName**</span><span class="sxs-lookup"><span data-stu-id="c9249-129">**GetGroupByName**</span></span>](id3dx11effect-getgroupbyname.md)                     | <span data-ttu-id="c9249-130">Ottiene un gruppo di effetti per nome.</span><span class="sxs-lookup"><span data-stu-id="c9249-130">Gets an effect group by name.</span></span><br/>                                                  |
| [<span data-ttu-id="c9249-131">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="c9249-131">**GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)           | <span data-ttu-id="c9249-132">Ottenere una tecnica in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="c9249-132">Get a technique by index.</span></span><br/>                                                      |
| [<span data-ttu-id="c9249-133">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="c9249-133">**GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)             | <span data-ttu-id="c9249-134">Ottenere una tecnica in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c9249-134">Get a technique by name.</span></span><br/>                                                       |
| [<span data-ttu-id="c9249-135">**GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="c9249-135">**GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)             | <span data-ttu-id="c9249-136">Ottiene una variabile in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="c9249-136">Get a variable by index.</span></span><br/>                                                       |
| [<span data-ttu-id="c9249-137">**GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="c9249-137">**GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)               | <span data-ttu-id="c9249-138">Ottenere una variabile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c9249-138">Get a variable by name.</span></span><br/>                                                        |
| [<span data-ttu-id="c9249-139">**GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="c9249-139">**GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)       | <span data-ttu-id="c9249-140">Ottenere una variabile in base alla semantica.</span><span class="sxs-lookup"><span data-stu-id="c9249-140">Get a variable by semantic.</span></span><br/>                                                    |
| [<span data-ttu-id="c9249-141">**Ottimizzato**</span><span class="sxs-lookup"><span data-stu-id="c9249-141">**IsOptimized**</span></span>](id3dx11effect-isoptimized.md)                           | <span data-ttu-id="c9249-142">Testare un effetto per verificare se i metadati della reflection sono stati rimossi dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="c9249-142">Test an effect to see if the reflection metadata has been removed from memory.</span></span><br/> |
| [<span data-ttu-id="c9249-143">**isValid**</span><span class="sxs-lookup"><span data-stu-id="c9249-143">**IsValid**</span></span>](id3dx11effect-isvalid.md)                                   | <span data-ttu-id="c9249-144">Testare un effetto per verificare se contiene una sintassi valida.</span><span class="sxs-lookup"><span data-stu-id="c9249-144">Test an effect to see if it contains valid syntax.</span></span><br/>                             |
| [<span data-ttu-id="c9249-145">**Ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="c9249-145">**Optimize**</span></span>](id3dx11effect-optimize.md)                                 | <span data-ttu-id="c9249-146">Ridurre al minimo la quantità di memoria necessaria per un effetto.</span><span class="sxs-lookup"><span data-stu-id="c9249-146">Minimize the amount of memory required for an effect.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="c9249-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9249-147">Remarks</span></span>

<span data-ttu-id="c9249-148">Un effetto viene creato chiamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="c9249-148">An effect is created by calling [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

<span data-ttu-id="c9249-149">Il sistema di effetti raggruppa le informazioni necessarie per il rendering in un effetto che contiene gli oggetti di stato per l'assegnazione delle modifiche di stato nei gruppi, le risorse per fornire i dati di input e l'archiviazione dei dati di output e i programmi che controllano il modo in cui viene eseguito il rendering denominato shader.</span><span class="sxs-lookup"><span data-stu-id="c9249-149">The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders.</span></span>

> [!Note]  
> <span data-ttu-id="c9249-150">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c9249-150">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c9249-151">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c9249-151">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c9249-152">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c9249-152">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

> [!Note]
>
> <span data-ttu-id="c9249-153">Se si chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un oggetto **ID3DX11Effect** per recuperare l'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , **QueryInterface** restituisce E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="c9249-153">If you call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an **ID3DX11Effect** object to retrieve the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, **QueryInterface** returns E\_NOINTERFACE.</span></span> <span data-ttu-id="c9249-154">Per risolvere questo problema, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="c9249-154">To work around this issue, use the following code:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="requirements"></a><span data-ttu-id="c9249-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9249-155">Requirements</span></span>
>
> 
>
<span data-ttu-id="c9249-156">| Requisito | Valore |</span><span class="sxs-lookup"><span data-stu-id="c9249-156">| Requirement | Value |</span></span>
> <span data-ttu-id="c9249-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9249-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Header</span></span><br/>  | <dl> <span data-ttu-id="c9249-158"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9249-158"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    <span data-ttu-id="c9249-159">| | Libreria</span><span class="sxs-lookup"><span data-stu-id="c9249-159">| | Library</span></span><br/> | <dl> <span data-ttu-id="c9249-160"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c9249-160"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |
>
> 
>
> ## <a name="see-also"></a><span data-ttu-id="c9249-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9249-161">See also</span></span>
>
> <dl> <dt>

[<span data-ttu-id="c9249-162">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="c9249-162">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="c9249-163">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="c9249-163">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>
>
>  
>
>  
>
