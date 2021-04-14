---
description: Imposta un valore albedo per ogni Texel, sovrascrivendo i valori albedo precedenti.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'Metodo ID3DXPRTEngine:: SetPerTexelAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401982"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a><span data-ttu-id="c4906-103">Metodo ID3DXPRTEngine:: SetPerTexelAlbedo</span><span class="sxs-lookup"><span data-stu-id="c4906-103">ID3DXPRTEngine::SetPerTexelAlbedo method</span></span>

<span data-ttu-id="c4906-104">Imposta un valore albedo per ogni Texel, sovrascrivendo i valori albedo precedenti.</span><span class="sxs-lookup"><span data-stu-id="c4906-104">Sets an albedo value for each texel, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4906-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4906-105">Syntax</span></span>


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="c4906-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4906-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4906-107">*pAlbedoTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4906-107">*pAlbedoTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4906-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c4906-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c4906-109">Puntatore a un oggetto trama [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) in cui archiviare i valori albedo.</span><span class="sxs-lookup"><span data-stu-id="c4906-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object in which to store albedo values.</span></span>

</dd> <dt>

<span data-ttu-id="c4906-110">*NumChannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4906-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4906-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4906-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4906-112">Numero di canali dei colori da impostare.</span><span class="sxs-lookup"><span data-stu-id="c4906-112">Number of color channels to set.</span></span> <span data-ttu-id="c4906-113">Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.</span><span class="sxs-lookup"><span data-stu-id="c4906-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="c4906-114">*PGH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4906-114">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4906-115">Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="c4906-115">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="c4906-116">Puntatore facoltativo a un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="c4906-116">Optional pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object.</span></span> <span data-ttu-id="c4906-117">Se non viene specificato, viene creato ed eliminato internamente un oggetto helper di rilegatura della trama.</span><span class="sxs-lookup"><span data-stu-id="c4906-117">If not provided, a texture gutter helper object is created and destroyed internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4906-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4906-118">Return value</span></span>

<span data-ttu-id="c4906-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4906-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4906-120">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4906-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c4906-121">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASSTILLDRAWING, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="c4906-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLED3DERR\_OUTOFVIDEOMEMORY, D3DERR\_WASSTILLDRAWING, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4906-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4906-122">Requirements</span></span>



| <span data-ttu-id="c4906-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4906-123">Requirement</span></span> | <span data-ttu-id="c4906-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c4906-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4906-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4906-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c4906-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4906-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c4906-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4906-127">Library</span></span><br/> | <dl> <span data-ttu-id="c4906-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4906-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4906-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4906-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4906-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c4906-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
