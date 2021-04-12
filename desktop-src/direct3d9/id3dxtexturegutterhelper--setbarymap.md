---
description: Imposta le coordinate del baricentrica Texel.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'Metodo ID3DXTextureGutterHelper:: SetBaryMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235162"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a><span data-ttu-id="1d4c4-103">Metodo ID3DXTextureGutterHelper:: SetBaryMap</span><span class="sxs-lookup"><span data-stu-id="1d4c4-103">ID3DXTextureGutterHelper::SetBaryMap method</span></span>

<span data-ttu-id="1d4c4-104">Imposta le coordinate del baricentrica Texel.</span><span class="sxs-lookup"><span data-stu-id="1d4c4-104">Sets texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d4c4-105">Syntax</span></span>


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="1d4c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d4c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d4c4-107">*pBaryData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d4c4-107">*pBaryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4c4-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d4c4-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="1d4c4-109">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che contiene le prime due coordinate baricentrica di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="1d4c4-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d4c4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d4c4-110">Return value</span></span>

<span data-ttu-id="1d4c4-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d4c4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d4c4-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1d4c4-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1d4c4-113">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="1d4c4-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="1d4c4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d4c4-114">Remarks</span></span>

<span data-ttu-id="1d4c4-115">La terza coordinata baricentrica viene fornita da:</span><span class="sxs-lookup"><span data-stu-id="1d4c4-115">The third barycentric coordinate is given by:</span></span>


```
1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="1d4c4-116">Il baricentrica coordina l'input per questo metodo è valido solo per Texel validi (non di classe 0).</span><span class="sxs-lookup"><span data-stu-id="1d4c4-116">The barycentric coordinates input to this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="1d4c4-117">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per i Texel validi.</span><span class="sxs-lookup"><span data-stu-id="1d4c4-117">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

<span data-ttu-id="1d4c4-118">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="1d4c4-118">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="1d4c4-119">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="1d4c4-119">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4c4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d4c4-120">Requirements</span></span>



| <span data-ttu-id="1d4c4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d4c4-121">Requirement</span></span> | <span data-ttu-id="1d4c4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1d4c4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4c4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d4c4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1d4c4-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4c4-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1d4c4-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="1d4c4-125">Library</span></span><br/> | <dl> <span data-ttu-id="1d4c4-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d4c4-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d4c4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d4c4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4c4-128">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="1d4c4-128">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




