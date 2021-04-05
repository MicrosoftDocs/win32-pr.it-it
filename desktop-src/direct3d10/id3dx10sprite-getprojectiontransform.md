---
description: Ottiene la matrice di proiezione sprite applicata a tutti gli sprite.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'Metodo ID3DX10Sprite:: GetProjectionTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762382"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a><span data-ttu-id="ad6ca-103">Metodo ID3DX10Sprite:: GetProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="ad6ca-103">ID3DX10Sprite::GetProjectionTransform method</span></span>

<span data-ttu-id="ad6ca-104">Ottiene la matrice di proiezione sprite applicata a tutti gli sprite.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-104">Get the sprite projection matrix that is applied to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad6ca-105">Syntax</span></span>


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="ad6ca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad6ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad6ca-107">*pProjectionTransform* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ad6ca-107">*pProjectionTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad6ca-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad6ca-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ad6ca-109">Puntatore a un [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) che verrà impostato sulla matrice di proiezione dello sprite.</span><span class="sxs-lookup"><span data-stu-id="ad6ca-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the sprite's projection matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad6ca-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad6ca-110">Return value</span></span>

<span data-ttu-id="ad6ca-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad6ca-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad6ca-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ad6ca-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad6ca-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad6ca-113">Requirements</span></span>



| <span data-ttu-id="ad6ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad6ca-114">Requirement</span></span> | <span data-ttu-id="ad6ca-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ad6ca-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6ca-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad6ca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ad6ca-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad6ca-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad6ca-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad6ca-118">Library</span></span><br/> | <dl> <span data-ttu-id="ad6ca-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad6ca-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad6ca-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad6ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6ca-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="ad6ca-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="ad6ca-122">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ad6ca-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
