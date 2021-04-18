---
description: Crea una superficie di rendering.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: Funzione D3DXCreateRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322729"
---
# <a name="d3dxcreaterendertosurface-function"></a><span data-ttu-id="f83e0-103">D3DXCreateRenderToSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="f83e0-103">D3DXCreateRenderToSurface function</span></span>

<span data-ttu-id="f83e0-104">Crea una superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="f83e0-104">Creates a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f83e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f83e0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a><span data-ttu-id="f83e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f83e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f83e0-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f83e0-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83e0-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f83e0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f83e0-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , il dispositivo da associare alla superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="f83e0-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="f83e0-110">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f83e0-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83e0-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f83e0-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f83e0-112">Larghezza della superficie di rendering, in pixel.</span><span class="sxs-lookup"><span data-stu-id="f83e0-112">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f83e0-113">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f83e0-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83e0-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f83e0-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f83e0-115">Altezza della superficie di rendering, in pixel.</span><span class="sxs-lookup"><span data-stu-id="f83e0-115">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f83e0-116">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f83e0-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83e0-117">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f83e0-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="f83e0-118">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="f83e0-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="f83e0-119">*DepthStencil* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f83e0-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83e0-120">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f83e0-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f83e0-121">Se **true**, l'area di rendering supporta una superficie di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="f83e0-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="f83e0-122">In caso contrario, questo membro è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="f83e0-122">Otherwise, this member is set to **FALSE**.</span></span> <span data-ttu-id="f83e0-123">Questa funzione creerà un nuovo buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="f83e0-123">This function will create a new depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f83e0-124">*DepthStencilFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f83e0-124">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83e0-125">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f83e0-125">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="f83e0-126">Se *DepthStencil* è impostato su **true**, questo parametro è un membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di stencil depth della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="f83e0-126">If *DepthStencil* is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="f83e0-127">*ppRenderToSurface* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f83e0-127">*ppRenderToSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f83e0-128">Tipo: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span><span class="sxs-lookup"><span data-stu-id="f83e0-128">Type: **[**LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span></span>

<span data-ttu-id="f83e0-129">Indirizzo di un puntatore a un'interfaccia [**ID3DXRenderToSurface**](id3dxrendertosurface.md) , che rappresenta la superficie di rendering creata.</span><span class="sxs-lookup"><span data-stu-id="f83e0-129">Address of a pointer to an [**ID3DXRenderToSurface**](id3dxrendertosurface.md) interface, representing the created render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f83e0-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f83e0-130">Return value</span></span>

<span data-ttu-id="f83e0-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f83e0-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f83e0-132">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f83e0-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f83e0-133">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="f83e0-133">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f83e0-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f83e0-134">Requirements</span></span>



| <span data-ttu-id="f83e0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f83e0-135">Requirement</span></span> | <span data-ttu-id="f83e0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f83e0-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f83e0-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f83e0-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f83e0-138"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f83e0-138"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f83e0-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="f83e0-139">Library</span></span><br/> | <dl> <span data-ttu-id="f83e0-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f83e0-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f83e0-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f83e0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f83e0-142">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="f83e0-142">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
