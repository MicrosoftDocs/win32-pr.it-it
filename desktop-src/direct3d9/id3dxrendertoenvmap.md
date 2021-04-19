---
description: L'interfaccia ID3DXRenderToEnvMap viene utilizzata per generalizzare il processo di rendering nelle mappe dell'ambiente.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Interfaccia ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323528"
---
# <a name="id3dxrendertoenvmap-interface"></a><span data-ttu-id="91db4-103">Interfaccia ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="91db4-103">ID3DXRenderToEnvMap interface</span></span>

<span data-ttu-id="91db4-104">L'interfaccia ID3DXRenderToEnvMap viene utilizzata per generalizzare il processo di rendering nelle mappe dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="91db4-104">The ID3DXRenderToEnvMap interface is used to generalize the process of rendering to environment maps.</span></span>

## <a name="members"></a><span data-ttu-id="91db4-105">Membri</span><span class="sxs-lookup"><span data-stu-id="91db4-105">Members</span></span>

<span data-ttu-id="91db4-106">L'interfaccia **ID3DXRenderToEnvMap** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="91db4-106">The **ID3DXRenderToEnvMap** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="91db4-107">**ID3DXRenderToEnvMap** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="91db4-107">**ID3DXRenderToEnvMap** also has these types of members:</span></span>

-   [<span data-ttu-id="91db4-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="91db4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="91db4-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="91db4-109">Methods</span></span>

<span data-ttu-id="91db4-110">L'interfaccia **ID3DXRenderToEnvMap** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="91db4-110">The **ID3DXRenderToEnvMap** interface has these methods.</span></span>



| <span data-ttu-id="91db4-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="91db4-111">Method</span></span>                                                          | <span data-ttu-id="91db4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91db4-112">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91db4-113">**BeginCube**</span><span class="sxs-lookup"><span data-stu-id="91db4-113">**BeginCube**</span></span>](id3dxrendertoenvmap--begincube.md)             | <span data-ttu-id="91db4-114">Avviare il rendering di una mappa dell'ambiente cubica.</span><span class="sxs-lookup"><span data-stu-id="91db4-114">Initiate the rendering of a cubic environment map.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="91db4-115">**BeginHemisphere**</span><span class="sxs-lookup"><span data-stu-id="91db4-115">**BeginHemisphere**</span></span>](id3dxrendertoenvmap--beginhemisphere.md) | <span data-ttu-id="91db4-116">Avviare il rendering di una mappa dell'ambiente emisferica.</span><span class="sxs-lookup"><span data-stu-id="91db4-116">Initiate the rendering of a hemispheric environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="91db4-117">**BeginParabolic**</span><span class="sxs-lookup"><span data-stu-id="91db4-117">**BeginParabolic**</span></span>](id3dxrendertoenvmap--beginparabolic.md)   | <span data-ttu-id="91db4-118">Avviare il rendering di una mappa dell'ambiente parabolica.</span><span class="sxs-lookup"><span data-stu-id="91db4-118">Initiate the rendering of a parabolic environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="91db4-119">**BeginSphere**</span><span class="sxs-lookup"><span data-stu-id="91db4-119">**BeginSphere**</span></span>](id3dxrendertoenvmap--beginsphere.md)         | <span data-ttu-id="91db4-120">Avviare il rendering di una mappa dell'ambiente sferica.</span><span class="sxs-lookup"><span data-stu-id="91db4-120">Initiate the rendering of a spherical environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="91db4-121">**Fine**</span><span class="sxs-lookup"><span data-stu-id="91db4-121">**End**</span></span>](id3dxrendertoenvmap--end.md)                         | <span data-ttu-id="91db4-122">Ripristinare tutte le destinazioni di rendering e, se necessario, comporre tutti i visi sottoposti a rendering nella superficie della mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="91db4-122">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span><br/>                                                                           |
| [<span data-ttu-id="91db4-123">**Viso**</span><span class="sxs-lookup"><span data-stu-id="91db4-123">**Face**</span></span>](id3dxrendertoenvmap--face.md)                       | <span data-ttu-id="91db4-124">Avviare il disegno di ogni faccia di una mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="91db4-124">Initiate the drawing of each face of an environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="91db4-125">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="91db4-125">**GetDesc**</span></span>](id3dxrendertoenvmap--getdesc.md)                 | <span data-ttu-id="91db4-126">Recupera la descrizione della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="91db4-126">Retrieves the description of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="91db4-127">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="91db4-127">**GetDevice**</span></span>](id3dxrendertoenvmap--getdevice.md)             | <span data-ttu-id="91db4-128">Recupera il dispositivo Direct3D associato alla mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="91db4-128">Retrieves the Direct3D device associated with the environment map.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="91db4-129">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="91db4-129">**OnLostDevice**</span></span>](id3dxrendertoenvmap--onlostdevice.md)       | <span data-ttu-id="91db4-130">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="91db4-130">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="91db4-131">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91db4-131">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="91db4-132">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="91db4-132">**OnResetDevice**</span></span>](id3dxrendertoenvmap--onresetdevice.md)     | <span data-ttu-id="91db4-133">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="91db4-133">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="91db4-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="91db4-134">Remarks</span></span>

<span data-ttu-id="91db4-135">Una mappa dell'ambiente viene utilizzata per la geometria della scena della mappa di trama per offrire una scena più sofisticata senza utilizzare la geometria complessa.</span><span class="sxs-lookup"><span data-stu-id="91db4-135">An environment map is used to texture-map scene geometry to provide a more sophisticated scene without using complex geometry.</span></span> <span data-ttu-id="91db4-136">Questa interfaccia supporta la creazione di superfici per i tipi di geometria seguenti: Cube, Half Sphere o emisferal, parabolica o Sphere.</span><span class="sxs-lookup"><span data-stu-id="91db4-136">This interface supports creating surfaces for the following kinds of geometry: cube, half sphere or hemispheric, parabolic, or sphere.</span></span>

<span data-ttu-id="91db4-137">L'interfaccia **ID3DXRenderToEnvMap** viene ottenuta chiamando la funzione [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="91db4-137">The **ID3DXRenderToEnvMap** interface is obtained by calling the [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) function.</span></span>

<span data-ttu-id="91db4-138">Il tipo LPD3DXRenderToEnvMap è definito come puntatore all'interfaccia **ID3DXRenderToEnvMap** .</span><span class="sxs-lookup"><span data-stu-id="91db4-138">The LPD3DXRenderToEnvMap type is defined as a pointer to the **ID3DXRenderToEnvMap** interface.</span></span>


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a><span data-ttu-id="91db4-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91db4-139">Requirements</span></span>



| <span data-ttu-id="91db4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="91db4-140">Requirement</span></span> | <span data-ttu-id="91db4-141">Valore</span><span class="sxs-lookup"><span data-stu-id="91db4-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91db4-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91db4-142">Header</span></span><br/>  | <dl> <span data-ttu-id="91db4-143"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="91db4-143"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="91db4-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="91db4-144">Library</span></span><br/> | <dl> <span data-ttu-id="91db4-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91db4-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91db4-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91db4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91db4-147">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="91db4-147">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
