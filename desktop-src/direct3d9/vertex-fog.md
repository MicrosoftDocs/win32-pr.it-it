---
description: Quando il sistema esegue l'offuscamento dei vertici, applica i calcoli di nebbia a ogni vertice in un poligono, quindi interpola i risultati sulla superficie del poligono durante la rasterizzazione.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Nebbia vertice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123336"
---
# <a name="vertex-fog-direct3d-9"></a><span data-ttu-id="3f125-103">Nebbia vertice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3f125-103">Vertex Fog (Direct3D 9)</span></span>

<span data-ttu-id="3f125-104">Quando il sistema esegue l'offuscamento dei vertici, applica i calcoli di nebbia a ogni vertice in un poligono, quindi interpola i risultati sulla superficie del poligono durante la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="3f125-104">When the system performs vertex fogging, it applies fog calculations at each vertex in a polygon, and then interpolates the results across the face of the polygon during rasterization.</span></span> <span data-ttu-id="3f125-105">Gli effetti della nebbia dei vertici vengono calcolati dal motore di illuminazione e trasformazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3f125-105">Vertex fog effects are computed by the Direct3D lighting and transformation engine.</span></span> <span data-ttu-id="3f125-106">Per altre informazioni, vedere [parametri di nebbia (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3f125-106">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="3f125-107">Se l'applicazione non usa Direct3D per la trasformazione e l'illuminazione, l'applicazione deve eseguire calcoli di nebbia.</span><span class="sxs-lookup"><span data-stu-id="3f125-107">If your application does not use Direct3D for transformation and lighting, the application must perform fog calculations.</span></span> <span data-ttu-id="3f125-108">In questo caso, inserire il fattore di nebbia calcolato nel componente alfa del colore speculare per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="3f125-108">In this case, place the fog factor that is computed in the alpha component of the specular color for each vertex.</span></span> <span data-ttu-id="3f125-109">È possibile utilizzare le formule desiderate, in base all'intervallo, al volume volumetrico o in altro modo.</span><span class="sxs-lookup"><span data-stu-id="3f125-109">You are free to use whatever formulas you want - range-based, volumetric, or otherwise.</span></span> <span data-ttu-id="3f125-110">Direct3D usa il fattore di nebbia fornito per l'interpolazione tra la faccia di ogni poligono.</span><span class="sxs-lookup"><span data-stu-id="3f125-110">Direct3D uses the supplied fog factor to interpolate across the face of each polygon.</span></span> <span data-ttu-id="3f125-111">Anche le applicazioni che eseguono la trasformazione e l'illuminazione devono eseguire i propri calcoli relativi alla nebbia dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3f125-111">Applications that perform their own transformation and lighting must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="3f125-112">Di conseguenza, un'applicazione di questo tipo deve abilitare solo la fusione di nebbia e impostare il colore di nebbia tramite gli Stati di rendering associati, come descritto in [blending di nebbia (Direct3D 9)](fog-blending.md) e [nebbia color (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="3f125-112">As a result, such an application need only enable fog blending and set the fog color through the associated render states, as described in [Fog Blending (Direct3D 9)](fog-blending.md) and [Fog Color (Direct3D 9)](fog-color.md).</span></span>

> [!Note]  
> <span data-ttu-id="3f125-113">Quando si usa un vertex shader, è necessario usare la nebbia del vertice.</span><span class="sxs-lookup"><span data-stu-id="3f125-113">When using a vertex shader, you must use vertex fog.</span></span> <span data-ttu-id="3f125-114">Questa operazione viene eseguita usando vertex shader per scrivere l'intensità di nebbia per vertice nel registro oFog.</span><span class="sxs-lookup"><span data-stu-id="3f125-114">This is accomplished by using the vertex shader to write the per-vertex fog intensity to the oFog register.</span></span> <span data-ttu-id="3f125-115">Al termine dell'pixel shader, i dati oFog vengono usati per eseguire l'interpolazione lineare con il colore di nebbia.</span><span class="sxs-lookup"><span data-stu-id="3f125-115">After the pixel shader completes, the oFog data is used to linearly interpolate with the fog color.</span></span> <span data-ttu-id="3f125-116">Questa intensità non è disponibile in un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="3f125-116">This intensity is not available in a pixel shader.</span></span>

 

## <a name="range-based-fog"></a><span data-ttu-id="3f125-117">Nebbia Range-Based</span><span class="sxs-lookup"><span data-stu-id="3f125-117">Range-Based Fog</span></span>

> [!Note]  
> <span data-ttu-id="3f125-118">Direct3D usa calcoli di nebbia basati su intervallo solo quando si usa la nebbia dei vertici con il motore di trasformazione e illuminazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3f125-118">Direct3D uses range-based fog calculations only when using vertex fog with the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="3f125-119">Questo perché la nebbia dei pixel è implementata nel driver di dispositivo e attualmente non esiste alcun hardware per supportare la nebbia basata sull'intervallo per pixel.</span><span class="sxs-lookup"><span data-stu-id="3f125-119">This is because pixel fog is implemented in the device driver, and no hardware currently exists to support per-pixel range-based fog.</span></span> <span data-ttu-id="3f125-120">Se l'applicazione esegue una trasformazione e un'illuminazione proprie, deve eseguire i propri calcoli di nebbia, basati sull'intervallo o in altro modo.</span><span class="sxs-lookup"><span data-stu-id="3f125-120">If your application performs its own transformation and lighting, it must perform its own fog calculations, range-based or otherwise.</span></span>

 

<span data-ttu-id="3f125-121">In alcuni casi, l'utilizzo di fog può introdurre artefatti grafici che comportano la fusione di oggetti con il colore di nebbia in modi non intuitivi.</span><span class="sxs-lookup"><span data-stu-id="3f125-121">Sometimes, using fog can introduce graphic artifacts that cause objects to be blended with the fog color in nonintuitive ways.</span></span> <span data-ttu-id="3f125-122">Si supponga, ad esempio, una scena in cui sono presenti due oggetti visibili: uno abbastanza distante per essere influenzato dalla nebbia e l'altro sufficientemente vicino a non essere interessato.</span><span class="sxs-lookup"><span data-stu-id="3f125-122">For example, imagine a scene in which there are two visible objects: one distant enough to be affected by fog, and the other near enough to be unaffected.</span></span> <span data-ttu-id="3f125-123">Se l'area di visualizzazione ruota sul posto, gli effetti di nebbia evidenti possono cambiare anche se gli oggetti sono stazionari.</span><span class="sxs-lookup"><span data-stu-id="3f125-123">If the viewing area rotates in place, the apparent fog effects can change, even if the objects are stationary.</span></span> <span data-ttu-id="3f125-124">Il diagramma seguente mostra una visualizzazione dall'alto verso il basso di una situazione di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="3f125-124">The following diagram shows a top-down view of such a situation.</span></span>

![diagramma di due punti di vista e del modo in cui influiscono sulla nebbia per due oggetti](images/artifog.png)

<span data-ttu-id="3f125-126">La nebbia basata sull'intervallo è un altro metodo, più accurato, per determinare gli effetti di nebbia.</span><span class="sxs-lookup"><span data-stu-id="3f125-126">Range-based fog is another, more accurate, way to determine the fog effects.</span></span> <span data-ttu-id="3f125-127">Nella nebbia basata sull'intervallo, Direct3D usa la distanza effettiva dal punto di vista a un vertice per i calcoli di nebbia.</span><span class="sxs-lookup"><span data-stu-id="3f125-127">In range-based fog, Direct3D uses the actual distance from the viewpoint to a vertex for its fog calculations.</span></span> <span data-ttu-id="3f125-128">Direct3D aumenta l'effetto della nebbia Man mano che la distanza tra i due punti aumenta, anziché la profondità del vertice all'interno della scena, evitando così gli artefatti rotazionali.</span><span class="sxs-lookup"><span data-stu-id="3f125-128">Direct3D increases the effect of fog as the distance between the two points increases, rather than the depth of the vertex within in the scene, thereby avoiding rotational artifacts.</span></span>

<span data-ttu-id="3f125-129">Se il dispositivo corrente supporta la nebbia basata sull'intervallo, verrà impostato il \_ valore D3DPRASTERCAPS FOGRANGE nel membro RasterCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando si chiama il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="3f125-129">If the current device supports range-based fog, it will set the D3DPRASTERCAPS\_FOGRANGE value in the RasterCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="3f125-130">Per abilitare la nebbia basata sull'intervallo, impostare lo \_ stato di rendering RANGEFOGENABLE di D3DRS su **true**.</span><span class="sxs-lookup"><span data-stu-id="3f125-130">To enable range-based fog, set the D3DRS\_RANGEFOGENABLE render state to **TRUE**.</span></span>

<span data-ttu-id="3f125-131">La nebbia basata sull'intervallo viene calcolata da Direct3D durante la trasformazione e l'illuminazione.</span><span class="sxs-lookup"><span data-stu-id="3f125-131">Range-based fog is computed by Direct3D during transformation and lighting.</span></span> <span data-ttu-id="3f125-132">Le applicazioni che non usano il motore di trasformazione e di illuminazione Direct3D devono anche eseguire i propri calcoli relativi alla nebbia dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3f125-132">Applications that don't use the Direct3D transformation and lighting engine must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="3f125-133">In questo caso, fornire il fattore di nebbia basato sull'intervallo nel componente alfa del componente speculare per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="3f125-133">In this case, provide the range-based fog factor in the alpha component of the specular component for each vertex.</span></span>

## <a name="using-vertex-fog"></a><span data-ttu-id="3f125-134">Uso della nebbia del vertice</span><span class="sxs-lookup"><span data-stu-id="3f125-134">Using Vertex Fog</span></span>

<span data-ttu-id="3f125-135">Usare la procedura seguente per abilitare la nebbia dei vertici nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f125-135">Use the following steps to enable vertex fog in your application.</span></span>

1.  <span data-ttu-id="3f125-136">Abilitare la fusione di nebbia impostando D3DRS \_ FOGENABLE su **true**.</span><span class="sxs-lookup"><span data-stu-id="3f125-136">Enable fog blending by setting D3DRS\_FOGENABLE to **TRUE**.</span></span>
2.  <span data-ttu-id="3f125-137">Impostare il colore di nebbia nello \_ stato di rendering FogColor di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="3f125-137">Set the fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="3f125-138">Scegliere la formula di nebbia desiderata impostando lo \_ stato di rendering FOGVERTEXMODE di D3DRS su un membro del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="3f125-138">Choose the desired fog formula by setting the D3DRS\_FOGVERTEXMODE render state to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="3f125-139">Impostare i parametri di nebbia come desiderato per la formula di nebbia selezionata negli Stati di rendering.</span><span class="sxs-lookup"><span data-stu-id="3f125-139">Set the fog parameters as desired for the selected fog formula in the render states.</span></span>

<span data-ttu-id="3f125-140">Nell'esempio seguente, scritto in C++, viene illustrato il modo in cui questi passaggi potrebbero essere simili nel codice.</span><span class="sxs-lookup"><span data-stu-id="3f125-140">The following example, written in C++, shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



<span data-ttu-id="3f125-141">Alcuni parametri di nebbia sono necessari come valori a virgola mobile, anche se il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta solo valori DWORD nel secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="3f125-141">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method only accepts DWORD values in the second parameter.</span></span> <span data-ttu-id="3f125-142">Questo esempio fornisce correttamente i valori a virgola mobile a questi metodi senza conversione dei dati eseguendo il cast degli indirizzi delle variabili a virgola mobile come puntatori DWORD, quindi dereferenziarli.</span><span class="sxs-lookup"><span data-stu-id="3f125-142">This example successfully provides the floating-point values to these methods without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f125-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f125-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f125-144">Tipi di nebbia</span><span class="sxs-lookup"><span data-stu-id="3f125-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
