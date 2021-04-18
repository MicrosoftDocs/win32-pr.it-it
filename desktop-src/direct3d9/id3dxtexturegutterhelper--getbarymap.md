---
description: Recupera le coordinate baricentrica Texel.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'Metodo ID3DXTextureGutterHelper:: GetBaryMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322963"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a><span data-ttu-id="f775a-103">Metodo ID3DXTextureGutterHelper:: GetBaryMap</span><span class="sxs-lookup"><span data-stu-id="f775a-103">ID3DXTextureGutterHelper::GetBaryMap method</span></span>

<span data-ttu-id="f775a-104">Recupera le coordinate baricentrica Texel.</span><span class="sxs-lookup"><span data-stu-id="f775a-104">Retrieves texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="f775a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f775a-105">Syntax</span></span>


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="f775a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f775a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f775a-107">*pBaryData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f775a-107">*pBaryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f775a-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f775a-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f775a-109">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che contiene le prime due coordinate baricentrica di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="f775a-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f775a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f775a-110">Return value</span></span>

<span data-ttu-id="f775a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f775a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f775a-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f775a-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f775a-113">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="f775a-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="f775a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f775a-114">Remarks</span></span>

<span data-ttu-id="f775a-115">La terza coordinata baricentrica viene fornita da:</span><span class="sxs-lookup"><span data-stu-id="f775a-115">The third barycentric coordinate is given by:</span></span>


```
    1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="f775a-116">Le coordinate baricentrica vengono sempre specificate rispetto al triangolo restituito da [**ID3DXTextureGutterHelper:: GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span><span class="sxs-lookup"><span data-stu-id="f775a-116">Barycentric coordinates are always specified with respect to the triangle returned by [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span></span>

<span data-ttu-id="f775a-117">Le coordinate baricentrica restituite da questo metodo sono valide solo per Texel validi (non di classe 0).</span><span class="sxs-lookup"><span data-stu-id="f775a-117">The barycentric coordinates returned by this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="f775a-118">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per i Texel validi.</span><span class="sxs-lookup"><span data-stu-id="f775a-118">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid texels.</span></span>

<span data-ttu-id="f775a-119">Viene eseguito il mapping dei [**Texel della classe 2**](id3dxtexturegutterhelper.md) al punto più vicino sul triangolo nello spazio Texel.</span><span class="sxs-lookup"><span data-stu-id="f775a-119">[**Class 2 texels**](id3dxtexturegutterhelper.md) are mapped to the nearest point on the triangle in texel space.</span></span>

<span data-ttu-id="f775a-120">L'applicazione deve allocare e gestire pBaryData.</span><span class="sxs-lookup"><span data-stu-id="f775a-120">The application must allocate and manage pBaryData.</span></span>

<span data-ttu-id="f775a-121">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="f775a-121">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="f775a-122">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="f775a-122">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="f775a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f775a-123">Requirements</span></span>



| <span data-ttu-id="f775a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f775a-124">Requirement</span></span> | <span data-ttu-id="f775a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f775a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f775a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f775a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f775a-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f775a-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f775a-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="f775a-128">Library</span></span><br/> | <dl> <span data-ttu-id="f775a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f775a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f775a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f775a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f775a-131">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="f775a-131">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




