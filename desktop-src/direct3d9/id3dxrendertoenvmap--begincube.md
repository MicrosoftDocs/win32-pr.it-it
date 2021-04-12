---
description: Avviare il rendering di una mappa dell'ambiente cubica.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'Metodo ID3DXRenderToEnvMap:: BeginCube (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bff6c8f3bdc49dfe0c1b677c6805cb332c05007d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354574"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a><span data-ttu-id="e9340-103">Metodo ID3DXRenderToEnvMap:: BeginCube</span><span class="sxs-lookup"><span data-stu-id="e9340-103">ID3DXRenderToEnvMap::BeginCube method</span></span>

<span data-ttu-id="e9340-104">Avviare il rendering di una mappa dell'ambiente cubica.</span><span class="sxs-lookup"><span data-stu-id="e9340-104">Initiate the rendering of a cubic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9340-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9340-105">Syntax</span></span>


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a><span data-ttu-id="e9340-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9340-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9340-107">*pCubeTex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9340-107">*pCubeTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9340-108">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="e9340-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="e9340-109">Puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) che rappresenta la trama del cubo a cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="e9340-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface that represents the cube texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9340-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9340-110">Return value</span></span>

<span data-ttu-id="e9340-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9340-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9340-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9340-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9340-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e9340-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9340-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9340-114">Remarks</span></span>

<span data-ttu-id="e9340-115">Per creare ognuno dei 6 visi, vedere [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="e9340-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw each of the 6 faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9340-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9340-116">Requirements</span></span>



| <span data-ttu-id="e9340-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9340-117">Requirement</span></span> | <span data-ttu-id="e9340-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e9340-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9340-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9340-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e9340-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9340-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e9340-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9340-121">Library</span></span><br/> | <dl> <span data-ttu-id="e9340-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9340-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9340-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9340-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9340-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="e9340-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="e9340-125">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="e9340-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
