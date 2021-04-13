---
description: Avviare il rendering di una mappa dell'ambiente sferica.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'Metodo ID3DXRenderToEnvMap:: BeginSphere (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354569"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a><span data-ttu-id="a51ee-103">Metodo ID3DXRenderToEnvMap:: BeginSphere</span><span class="sxs-lookup"><span data-stu-id="a51ee-103">ID3DXRenderToEnvMap::BeginSphere method</span></span>

<span data-ttu-id="a51ee-104">Avviare il rendering di una mappa dell'ambiente sferica.</span><span class="sxs-lookup"><span data-stu-id="a51ee-104">Initiate the rendering of a spherical environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="a51ee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a51ee-105">Syntax</span></span>


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a><span data-ttu-id="a51ee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a51ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a51ee-107">*pTex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a51ee-107">*pTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a51ee-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="a51ee-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="a51ee-109">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama a cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="a51ee-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a51ee-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a51ee-110">Return value</span></span>

<span data-ttu-id="a51ee-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a51ee-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a51ee-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a51ee-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a51ee-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL. E \_ non riescono</span><span class="sxs-lookup"><span data-stu-id="a51ee-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="a51ee-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a51ee-114">Remarks</span></span>

<span data-ttu-id="a51ee-115">Per creare la faccia, vedere [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="a51ee-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="a51ee-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a51ee-116">Requirements</span></span>



| <span data-ttu-id="a51ee-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a51ee-117">Requirement</span></span> | <span data-ttu-id="a51ee-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a51ee-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a51ee-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a51ee-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a51ee-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a51ee-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a51ee-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="a51ee-121">Library</span></span><br/> | <dl> <span data-ttu-id="a51ee-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a51ee-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a51ee-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a51ee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a51ee-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a51ee-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="a51ee-125">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="a51ee-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
