---
description: Crea una mappa dell'ambiente di rendering.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: Funzione D3DXCreateRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058608"
---
# <a name="d3dxcreaterendertoenvmap-function"></a><span data-ttu-id="96111-103">D3DXCreateRenderToEnvMap (funzione)</span><span class="sxs-lookup"><span data-stu-id="96111-103">D3DXCreateRenderToEnvMap function</span></span>

<span data-ttu-id="96111-104">Crea una mappa dell'ambiente di rendering.</span><span class="sxs-lookup"><span data-stu-id="96111-104">Creates a render environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="96111-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96111-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a><span data-ttu-id="96111-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96111-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96111-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96111-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96111-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="96111-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="96111-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che è il dispositivo da associare alla superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="96111-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, which is the device to associate with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="96111-110">*Dimensioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96111-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96111-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96111-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96111-112">Dimensione della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="96111-112">Size of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="96111-113">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96111-113">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96111-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96111-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96111-115">Il numero di livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="96111-115">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="96111-116">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96111-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96111-117">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="96111-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="96111-118">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) che descrive il formato pixel della mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="96111-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the pixel format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="96111-119">*DepthStencil* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96111-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96111-120">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96111-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96111-121">Se **true**, l'area di rendering supporta una superficie di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="96111-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="96111-122">In caso contrario, questo membro è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="96111-122">Otherwise, this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="96111-123">*DepthStencilFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96111-123">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96111-124">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="96111-124">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="96111-125">Se DepthStencil è impostato su **true**, questo parametro è un membro del tipo enumerato [D3DFORMAT](d3dformat.md) che descrive il formato di stencil depth della mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="96111-125">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the depth-stencil format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="96111-126">*ppRenderToEnvMap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96111-126">*ppRenderToEnvMap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96111-127">Tipo: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span><span class="sxs-lookup"><span data-stu-id="96111-127">Type: **[**LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span></span>

<span data-ttu-id="96111-128">Indirizzo di un puntatore a un'interfaccia [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) che rappresenta la mappa dell'ambiente di rendering creata.</span><span class="sxs-lookup"><span data-stu-id="96111-128">Address of a pointer to an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) interface that represents the created render environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96111-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96111-129">Return value</span></span>

<span data-ttu-id="96111-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96111-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96111-131">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96111-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="96111-132">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="96111-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="96111-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96111-133">Requirements</span></span>



| <span data-ttu-id="96111-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="96111-134">Requirement</span></span> | <span data-ttu-id="96111-135">Valore</span><span class="sxs-lookup"><span data-stu-id="96111-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96111-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96111-136">Header</span></span><br/>  | <dl> <span data-ttu-id="96111-137"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="96111-137"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="96111-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="96111-138">Library</span></span><br/> | <dl> <span data-ttu-id="96111-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96111-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96111-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96111-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96111-141">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="96111-141">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
