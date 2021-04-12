---
description: Imposta le proprietà del materiale mesh nella scena 3D. Utilizzare questo metodo per specificare i parametri di dispersione della sottosuperficie.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'Metodo ID3DXPRTEngine:: SetMeshMaterials (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355684"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a><span data-ttu-id="64aaf-104">Metodo ID3DXPRTEngine:: SetMeshMaterials</span><span class="sxs-lookup"><span data-stu-id="64aaf-104">ID3DXPRTEngine::SetMeshMaterials method</span></span>

<span data-ttu-id="64aaf-105">Imposta le proprietà del materiale mesh nella scena 3D.</span><span class="sxs-lookup"><span data-stu-id="64aaf-105">Sets mesh material properties in the 3D scene.</span></span> <span data-ttu-id="64aaf-106">Utilizzare questo metodo per specificare i parametri di dispersione della sottosuperficie.</span><span class="sxs-lookup"><span data-stu-id="64aaf-106">Use this method to specify subsurface scattering parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="64aaf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64aaf-107">Syntax</span></span>


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a><span data-ttu-id="64aaf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="64aaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64aaf-109">*ppMaterials* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64aaf-109">*ppMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64aaf-110">Tipo: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="64aaf-110">Type: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md)\*\***</span></span>

<span data-ttu-id="64aaf-111">Indirizzo di un puntatore alle proprietà del materiale mesh desiderato.</span><span class="sxs-lookup"><span data-stu-id="64aaf-111">Address of a pointer to desired mesh material properties.</span></span> <span data-ttu-id="64aaf-112">Vedere [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="64aaf-112">See [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="64aaf-113">*NumMeshes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64aaf-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64aaf-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64aaf-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64aaf-115">Indice della mesh in cui impostare le proprietà del materiale.</span><span class="sxs-lookup"><span data-stu-id="64aaf-115">Index of the mesh on which to set material properties.</span></span>

</dd> <dt>

<span data-ttu-id="64aaf-116">*NumChannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64aaf-116">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64aaf-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64aaf-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64aaf-118">Numero di canali dei colori da impostare nella rete.</span><span class="sxs-lookup"><span data-stu-id="64aaf-118">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="64aaf-119">Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.</span><span class="sxs-lookup"><span data-stu-id="64aaf-119">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span> <span data-ttu-id="64aaf-120">Se si intende modificare questo parametro, impostare prima di tutto l'albedo usando un altro metodo, ad esempio [**ID3DXPRTEngine:: SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) o [**ID3DXPRTEngine:: SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span><span class="sxs-lookup"><span data-stu-id="64aaf-120">If you intend to change this parameter, first set the albedo using another method such as [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) or [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span></span>

</dd> <dt>

<span data-ttu-id="64aaf-121">*bSetAlbedo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64aaf-121">*bSetAlbedo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64aaf-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64aaf-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64aaf-123">Se **true**, imposta l'albedo della mesh su ppMaterials, sovrascrivendo tutti i valori dell'albedo di Texel e vertex esistenti.</span><span class="sxs-lookup"><span data-stu-id="64aaf-123">If **TRUE**, sets the albedo of the mesh to ppMaterials, overwriting all existing texel and vertex albedo values.</span></span> <span data-ttu-id="64aaf-124">Se **false**, conserva tutti i valori dell'albedo di Texel e vertex esistenti impostati da altri metodi; NumChannels deve corrispondere al parametro NumChannels usato per creare il buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span><span class="sxs-lookup"><span data-stu-id="64aaf-124">If **FALSE**, preserves all existing texel and vertex albedo values set by other methods; NumChannels must match the NumChannels parameter used to create the buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span></span>

</dd> <dt>

<span data-ttu-id="64aaf-125">*fLengthScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64aaf-125">*fLengthScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64aaf-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64aaf-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64aaf-127">Scala della scena 3D rispetto a un cubo da 1 mm.</span><span class="sxs-lookup"><span data-stu-id="64aaf-127">Scale of the 3D scene relative to a 1-mm cube.</span></span> <span data-ttu-id="64aaf-128">Utilizzato per i calcoli di dispersione della sottosuperficie.</span><span class="sxs-lookup"><span data-stu-id="64aaf-128">Used for subsurface scattering computations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64aaf-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64aaf-129">Return value</span></span>

<span data-ttu-id="64aaf-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64aaf-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64aaf-131">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64aaf-131">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="64aaf-132">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="64aaf-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="64aaf-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64aaf-133">Requirements</span></span>



| <span data-ttu-id="64aaf-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="64aaf-134">Requirement</span></span> | <span data-ttu-id="64aaf-135">Valore</span><span class="sxs-lookup"><span data-stu-id="64aaf-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64aaf-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64aaf-136">Header</span></span><br/>  | <dl> <span data-ttu-id="64aaf-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="64aaf-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="64aaf-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="64aaf-138">Library</span></span><br/> | <dl> <span data-ttu-id="64aaf-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64aaf-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64aaf-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64aaf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64aaf-141">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="64aaf-141">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
