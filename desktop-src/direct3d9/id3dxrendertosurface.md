---
description: L'interfaccia ID3DXRenderToSurface viene utilizzata per generalizzare il processo di rendering nelle superfici.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interfaccia ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355824"
---
# <a name="id3dxrendertosurface-interface"></a><span data-ttu-id="f8ca5-103">Interfaccia ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="f8ca5-103">ID3DXRenderToSurface interface</span></span>

<span data-ttu-id="f8ca5-104">L'interfaccia ID3DXRenderToSurface viene utilizzata per generalizzare il processo di rendering nelle superfici.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-104">The ID3DXRenderToSurface interface is used to generalize the process of rendering to surfaces.</span></span>

## <a name="members"></a><span data-ttu-id="f8ca5-105">Membri</span><span class="sxs-lookup"><span data-stu-id="f8ca5-105">Members</span></span>

<span data-ttu-id="f8ca5-106">L'interfaccia **ID3DXRenderToSurface** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f8ca5-106">The **ID3DXRenderToSurface** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f8ca5-107">**ID3DXRenderToSurface** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8ca5-107">**ID3DXRenderToSurface** also has these types of members:</span></span>

-   [<span data-ttu-id="f8ca5-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="f8ca5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f8ca5-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f8ca5-109">Methods</span></span>

<span data-ttu-id="f8ca5-110">L'interfaccia **ID3DXRenderToSurface** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-110">The **ID3DXRenderToSurface** interface has these methods.</span></span>



| <span data-ttu-id="f8ca5-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="f8ca5-111">Method</span></span>                                                       | <span data-ttu-id="f8ca5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8ca5-112">Description</span></span>                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8ca5-113">**BeginScene**</span><span class="sxs-lookup"><span data-stu-id="f8ca5-113">**BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)       | <span data-ttu-id="f8ca5-114">Inizia una scena.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-114">Begins a scene.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="f8ca5-115">**EndScene**</span><span class="sxs-lookup"><span data-stu-id="f8ca5-115">**EndScene**</span></span>](id3dxrendertosurface--endscene.md)           | <span data-ttu-id="f8ca5-116">Termina una scena.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-116">Ends a scene.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="f8ca5-117">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="f8ca5-117">**GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)             | <span data-ttu-id="f8ca5-118">Recupera i parametri della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-118">Retrieves the parameters of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="f8ca5-119">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="f8ca5-119">**GetDevice**</span></span>](id3dxrendertosurface--getdevice.md)         | <span data-ttu-id="f8ca5-120">Recupera il dispositivo Direct3D associato alla superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-120">Retrieves the Direct3D device associated with the render surface.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="f8ca5-121">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="f8ca5-121">**OnLostDevice**</span></span>](id3dxrendertosurface--onlostdevice.md)   | <span data-ttu-id="f8ca5-122">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-122">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="f8ca5-123">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-123">This method should be called whenever a device is lost or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="f8ca5-124">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="f8ca5-124">**OnResetDevice**</span></span>](id3dxrendertosurface--onresetdevice.md) | <span data-ttu-id="f8ca5-125">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-125">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="f8ca5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8ca5-126">Remarks</span></span>

<span data-ttu-id="f8ca5-127">Le superfici possono essere usate in diversi modi, tra cui le destinazioni di rendering, il rendering fuori schermo o il rendering in trame.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-127">Surfaces can be used in a variety of ways including render targets, off-screen rendering, or rendering to textures.</span></span>

<span data-ttu-id="f8ca5-128">Una superficie può essere configurata usando un viewport separato usando il metodo [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md) per fornire una visualizzazione di rendering personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-128">A surface can be configured using a separate viewport using the [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md) method, to provide a custom render view.</span></span> <span data-ttu-id="f8ca5-129">Se la superficie non è una destinazione di rendering, viene utilizzata una destinazione di rendering compatibile e il risultato viene copiato nell'area alla fine della scena.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-129">If the surface is not a render target, a compatible render target is used, and the result is copied to the surface at the end of the scene.</span></span>

<span data-ttu-id="f8ca5-130">L'interfaccia **ID3DXRenderToSurface** viene ottenuta chiamando la funzione [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ca5-130">The **ID3DXRenderToSurface** interface is obtained by calling the [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) function.</span></span>

<span data-ttu-id="f8ca5-131">Il tipo LPD3DXRENDERTOSURFACE è definito come puntatore all'interfaccia **ID3DXRenderToSurface** .</span><span class="sxs-lookup"><span data-stu-id="f8ca5-131">The LPD3DXRENDERTOSURFACE type is defined as a pointer to the **ID3DXRenderToSurface** interface.</span></span>


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a><span data-ttu-id="f8ca5-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8ca5-132">Requirements</span></span>



| <span data-ttu-id="f8ca5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8ca5-133">Requirement</span></span> | <span data-ttu-id="f8ca5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f8ca5-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ca5-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8ca5-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f8ca5-136"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ca5-136"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f8ca5-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8ca5-137">Library</span></span><br/> | <dl> <span data-ttu-id="f8ca5-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8ca5-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8ca5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8ca5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ca5-140">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="f8ca5-140">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
