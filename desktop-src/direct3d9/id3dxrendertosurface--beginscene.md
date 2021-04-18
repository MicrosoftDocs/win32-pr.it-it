---
description: Inizia una scena.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'Metodo ID3DXRenderToSurface:: BeginScene (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323527"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a><span data-ttu-id="83b7d-103">Metodo ID3DXRenderToSurface:: BeginScene</span><span class="sxs-lookup"><span data-stu-id="83b7d-103">ID3DXRenderToSurface::BeginScene method</span></span>

<span data-ttu-id="83b7d-104">Inizia una scena.</span><span class="sxs-lookup"><span data-stu-id="83b7d-104">Begins a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b7d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83b7d-105">Syntax</span></span>


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a><span data-ttu-id="83b7d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83b7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b7d-107">*pSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83b7d-107">*pSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b7d-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="83b7d-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="83b7d-109">Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , che rappresenta la superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="83b7d-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="83b7d-110">*pViewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83b7d-110">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b7d-111">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="83b7d-111">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="83b7d-112">Puntatore a una struttura [**D3DVIEWPORT9**](d3dviewport9.md) che descrive il viewport per la scena.</span><span class="sxs-lookup"><span data-stu-id="83b7d-112">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, describing the viewport for the scene.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83b7d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83b7d-113">Return value</span></span>

<span data-ttu-id="83b7d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83b7d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83b7d-115">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83b7d-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83b7d-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL. D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ INVALIDDATA E \_ OutOfMemory</span><span class="sxs-lookup"><span data-stu-id="83b7d-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.D3DERR\_OUTOFVIDEOMEMORY D3DXERR\_INVALIDDATA E\_OUTOFMEMORY</span></span>

## <a name="requirements"></a><span data-ttu-id="83b7d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83b7d-117">Requirements</span></span>



| <span data-ttu-id="83b7d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b7d-118">Requirement</span></span> | <span data-ttu-id="83b7d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="83b7d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83b7d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83b7d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="83b7d-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="83b7d-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="83b7d-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="83b7d-122">Library</span></span><br/> | <dl> <span data-ttu-id="83b7d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83b7d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83b7d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83b7d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b7d-125">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="83b7d-125">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="83b7d-126">**ID3DXRenderToSurface:: EndScene**</span><span class="sxs-lookup"><span data-stu-id="83b7d-126">**ID3DXRenderToSurface::EndScene**</span></span>](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
