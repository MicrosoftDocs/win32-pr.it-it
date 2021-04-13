---
description: Recupera le coordinate di trama (u, v) di ogni Texel.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'Metodo ID3DXTextureGutterHelper:: GetTexelMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354999"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a><span data-ttu-id="df7a6-103">Metodo ID3DXTextureGutterHelper:: GetTexelMap</span><span class="sxs-lookup"><span data-stu-id="df7a6-103">ID3DXTextureGutterHelper::GetTexelMap method</span></span>

<span data-ttu-id="df7a6-104">Recupera le coordinate di trama (u, v) di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="df7a6-104">Retrieves the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="df7a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df7a6-105">Syntax</span></span>


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="df7a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df7a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df7a6-107">*pTexelData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="df7a6-107">*pTexelData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df7a6-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="df7a6-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="df7a6-109">Puntatore alla posizione in coordinate di trama in pixel (u, v) in cui si trova ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="df7a6-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df7a6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df7a6-110">Return value</span></span>

<span data-ttu-id="df7a6-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df7a6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df7a6-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="df7a6-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="df7a6-113">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="df7a6-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="df7a6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="df7a6-114">Remarks</span></span>

<span data-ttu-id="df7a6-115">Per la [**classe 2 e 4 Texel**](id3dxtexturegutterhelper.md), le coordinate di trama restituite (u, v) corrispondono al punto più vicino sul triangolo più vicino.</span><span class="sxs-lookup"><span data-stu-id="df7a6-115">For [**class 2 and 4 texels**](id3dxtexturegutterhelper.md), the returned (u, v) texture coordinates correspond to the closest point on the closest triangle.</span></span>

<span data-ttu-id="df7a6-116">L'applicazione deve allocare e gestire pTexelData.</span><span class="sxs-lookup"><span data-stu-id="df7a6-116">The application must allocate and manage pTexelData.</span></span>

## <a name="requirements"></a><span data-ttu-id="df7a6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df7a6-117">Requirements</span></span>



| <span data-ttu-id="df7a6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="df7a6-118">Requirement</span></span> | <span data-ttu-id="df7a6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="df7a6-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df7a6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df7a6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="df7a6-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="df7a6-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="df7a6-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="df7a6-122">Library</span></span><br/> | <dl> <span data-ttu-id="df7a6-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df7a6-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df7a6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df7a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df7a6-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="df7a6-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




