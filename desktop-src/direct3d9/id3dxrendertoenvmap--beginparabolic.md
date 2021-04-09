---
description: Avviare il rendering di una mappa dell'ambiente parabolica.
ms.assetid: 80456084-f5f5-4dfe-805a-7eaaf7f7cb2a
title: 'Metodo ID3DXRenderToEnvMap:: BeginParabolic (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginParabolic
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a818abb424fa55bc01eca7ce9f64bc5629a7d50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058596"
---
# <a name="id3dxrendertoenvmapbeginparabolic-method"></a><span data-ttu-id="fb11b-103">Metodo ID3DXRenderToEnvMap:: BeginParabolic</span><span class="sxs-lookup"><span data-stu-id="fb11b-103">ID3DXRenderToEnvMap::BeginParabolic method</span></span>

<span data-ttu-id="fb11b-104">Avviare il rendering di una mappa dell'ambiente parabolica.</span><span class="sxs-lookup"><span data-stu-id="fb11b-104">Initiate the rendering of a parabolic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb11b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb11b-105">Syntax</span></span>


```C++
HRESULT BeginParabolic(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="fb11b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb11b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb11b-107">*pTexZPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb11b-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb11b-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="fb11b-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="fb11b-109">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama di rendering positiva.</span><span class="sxs-lookup"><span data-stu-id="fb11b-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive render texture.</span></span>

</dd> <dt>

<span data-ttu-id="fb11b-110">*pTexZNeg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb11b-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb11b-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="fb11b-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="fb11b-112">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama di rendering negativa.</span><span class="sxs-lookup"><span data-stu-id="fb11b-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative render texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb11b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb11b-113">Return value</span></span>

<span data-ttu-id="fb11b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb11b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb11b-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb11b-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb11b-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL. E \_ non riescono</span><span class="sxs-lookup"><span data-stu-id="fb11b-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="fb11b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb11b-117">Remarks</span></span>

<span data-ttu-id="fb11b-118">Per creare le facce, vedere [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="fb11b-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb11b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb11b-119">Requirements</span></span>



| <span data-ttu-id="fb11b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb11b-120">Requirement</span></span> | <span data-ttu-id="fb11b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fb11b-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb11b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb11b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="fb11b-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb11b-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fb11b-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="fb11b-124">Library</span></span><br/> | <dl> <span data-ttu-id="fb11b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb11b-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb11b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb11b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb11b-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="fb11b-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="fb11b-128">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="fb11b-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
