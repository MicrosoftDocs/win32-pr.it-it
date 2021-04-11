---
description: Avviare il rendering di una mappa dell'ambiente emisferica.
ms.assetid: 1150aad9-dd8c-4943-afaf-90794faaaf70
title: 'Metodo ID3DXRenderToEnvMap:: BeginHemisphere (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginHemisphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96eb4bbf4cfc6cac952368337456b946f64cf711
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234989"
---
# <a name="id3dxrendertoenvmapbeginhemisphere-method"></a><span data-ttu-id="83712-103">Metodo ID3DXRenderToEnvMap:: BeginHemisphere</span><span class="sxs-lookup"><span data-stu-id="83712-103">ID3DXRenderToEnvMap::BeginHemisphere method</span></span>

<span data-ttu-id="83712-104">Avviare il rendering di una mappa dell'ambiente emisferica.</span><span class="sxs-lookup"><span data-stu-id="83712-104">Initiate the rendering of a hemispheric environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="83712-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83712-105">Syntax</span></span>


```C++
HRESULT BeginHemisphere(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="83712-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83712-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83712-107">*pTexZPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83712-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83712-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="83712-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="83712-109">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta l'area di rendering della trama positiva.</span><span class="sxs-lookup"><span data-stu-id="83712-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive texture render surface.</span></span>

</dd> <dt>

<span data-ttu-id="83712-110">*pTexZNeg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83712-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83712-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="83712-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="83712-112">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la superficie di rendering della trama negativa.</span><span class="sxs-lookup"><span data-stu-id="83712-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative texture render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83712-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83712-113">Return value</span></span>

<span data-ttu-id="83712-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83712-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83712-115">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83712-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83712-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL. E \_ non riescono</span><span class="sxs-lookup"><span data-stu-id="83712-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="83712-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="83712-117">Remarks</span></span>

<span data-ttu-id="83712-118">Per creare la faccia, vedere [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="83712-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="83712-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83712-119">Requirements</span></span>



| <span data-ttu-id="83712-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="83712-120">Requirement</span></span> | <span data-ttu-id="83712-121">Valore</span><span class="sxs-lookup"><span data-stu-id="83712-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83712-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83712-122">Header</span></span><br/>  | <dl> <span data-ttu-id="83712-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="83712-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="83712-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="83712-124">Library</span></span><br/> | <dl> <span data-ttu-id="83712-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83712-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83712-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83712-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83712-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="83712-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="83712-128">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="83712-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
