---
description: Imposta le coordinate di trama (u, v) di ogni Texel.
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: 'Metodo ID3DXTextureGutterHelper:: SetTexelMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee00394e81dadf147d54dffe0dc02199b2274e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323364"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a><span data-ttu-id="8019d-103">Metodo ID3DXTextureGutterHelper:: SetTexelMap</span><span class="sxs-lookup"><span data-stu-id="8019d-103">ID3DXTextureGutterHelper::SetTexelMap method</span></span>

<span data-ttu-id="8019d-104">Imposta le coordinate di trama (u, v) di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="8019d-104">Sets the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="8019d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8019d-105">Syntax</span></span>


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="8019d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8019d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8019d-107">*pTexelData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8019d-107">*pTexelData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8019d-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8019d-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8019d-109">Puntatore alla posizione in coordinate di trama in pixel (u, v) in cui si trova ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="8019d-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8019d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8019d-110">Return value</span></span>

<span data-ttu-id="8019d-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8019d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8019d-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8019d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8019d-113">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="8019d-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="8019d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8019d-114">Requirements</span></span>



| <span data-ttu-id="8019d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8019d-115">Requirement</span></span> | <span data-ttu-id="8019d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8019d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8019d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8019d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8019d-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8019d-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8019d-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="8019d-119">Library</span></span><br/> | <dl> <span data-ttu-id="8019d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8019d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8019d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8019d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8019d-122">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="8019d-122">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




