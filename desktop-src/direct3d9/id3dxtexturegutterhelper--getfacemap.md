---
description: Recupera l'indice della faccia mesh a cui appartiene ogni Texel.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'Metodo ID3DXTextureGutterHelper:: GetFaceMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322962"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a><span data-ttu-id="7bbd1-103">Metodo ID3DXTextureGutterHelper:: GetFaceMap</span><span class="sxs-lookup"><span data-stu-id="7bbd1-103">ID3DXTextureGutterHelper::GetFaceMap method</span></span>

<span data-ttu-id="7bbd1-104">Recupera l'indice della faccia mesh a cui appartiene ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-104">Retrieves the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbd1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bbd1-105">Syntax</span></span>


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="7bbd1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bbd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bbd1-107">*pFaceData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bbd1-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbd1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7bbd1-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7bbd1-109">Puntatore all'indice della faccia mesh a cui appartiene ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bbd1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bbd1-110">Return value</span></span>

<span data-ttu-id="7bbd1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7bbd1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7bbd1-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7bbd1-113">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="7bbd1-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="7bbd1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bbd1-114">Remarks</span></span>

<span data-ttu-id="7bbd1-115">I dati della faccia mesh restituiti da questo metodo sono validi solo per Texel validi (non di classe 0).</span><span class="sxs-lookup"><span data-stu-id="7bbd1-115">The mesh face data returned by this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="7bbd1-116">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per Texel validi (non di classe 0).</span><span class="sxs-lookup"><span data-stu-id="7bbd1-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid (non-class 0) texels.</span></span>

<span data-ttu-id="7bbd1-117">Per i [**Texel della classe 2**](id3dxtexturegutterhelper.md), questo metodo recupera la faccia più vicina.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-117">For [**class 2 texels**](id3dxtexturegutterhelper.md), this method retrieves the closest face.</span></span>

<span data-ttu-id="7bbd1-118">L'applicazione deve allocare e gestire pFaceData.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-118">The application must allocate and manage pFaceData.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbd1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bbd1-119">Requirements</span></span>



| <span data-ttu-id="7bbd1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bbd1-120">Requirement</span></span> | <span data-ttu-id="7bbd1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7bbd1-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbd1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bbd1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7bbd1-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bbd1-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7bbd1-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="7bbd1-124">Library</span></span><br/> | <dl> <span data-ttu-id="7bbd1-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bbd1-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7bbd1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bbd1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbd1-127">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="7bbd1-127">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
