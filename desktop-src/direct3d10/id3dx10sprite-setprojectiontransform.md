---
description: Imposta la matrice di proiezione per tutti gli sprite.
ms.assetid: cb4c5546-1a31-40d9-a943-af4fbddcee01
title: 'Metodo ID3DX10Sprite:: SetProjectionTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c49fb570f87c8c86313e1f4adcf1560fee909433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531087"
---
# <a name="id3dx10spritesetprojectiontransform-method"></a><span data-ttu-id="ce667-103">Metodo ID3DX10Sprite:: SetProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="ce667-103">ID3DX10Sprite::SetProjectionTransform method</span></span>

<span data-ttu-id="ce667-104">Imposta la matrice di proiezione per tutti gli sprite.</span><span class="sxs-lookup"><span data-stu-id="ce667-104">Set the projection matrix for all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce667-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce667-105">Syntax</span></span>


```C++
HRESULT SetProjectionTransform(
  [in] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="ce667-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce667-107">*pProjectionTransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce667-107">*pProjectionTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce667-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce667-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ce667-109">Matrice di proiezione da utilizzare in tutti gli sprite.</span><span class="sxs-lookup"><span data-stu-id="ce667-109">The projection matrix to be used on all sprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce667-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce667-110">Return value</span></span>

<span data-ttu-id="ce667-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce667-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce667-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ce667-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce667-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce667-113">Requirements</span></span>



| <span data-ttu-id="ce667-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce667-114">Requirement</span></span> | <span data-ttu-id="ce667-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ce667-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce667-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce667-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ce667-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce667-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce667-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce667-118">Library</span></span><br/> | <dl> <span data-ttu-id="ce667-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce667-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce667-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce667-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce667-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="ce667-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="ce667-122">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ce667-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
