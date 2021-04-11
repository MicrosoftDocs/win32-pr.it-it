---
description: Suddivide una matrice di trasformazione 3D generale nei componenti scalari, rotazionali e di conversione.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Funzione D3DXMatrixDecompose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235169"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="4d472-103">Funzione D3DXMatrixDecompose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4d472-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="4d472-104">Suddivide una matrice di trasformazione 3D generale nei componenti scalari, rotazionali e di conversione.</span><span class="sxs-lookup"><span data-stu-id="4d472-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d472-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d472-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4d472-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d472-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d472-107">*pOutScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d472-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d472-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d472-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4d472-109">Puntatore al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) di output che contiene i fattori di scala applicati lungo gli assi x, y e z.</span><span class="sxs-lookup"><span data-stu-id="4d472-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="4d472-110">*pOutRotation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d472-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d472-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d472-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4d472-112">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che descrive la rotazione.</span><span class="sxs-lookup"><span data-stu-id="4d472-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="4d472-113">*pOutTranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d472-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d472-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d472-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4d472-115">Puntatore al vettore D3DXVECTOR3 che descrive la traduzione.</span><span class="sxs-lookup"><span data-stu-id="4d472-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="4d472-116">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d472-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d472-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d472-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4d472-118">Puntatore a una matrice di input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) da scomporre.</span><span class="sxs-lookup"><span data-stu-id="4d472-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d472-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d472-119">Return value</span></span>

<span data-ttu-id="4d472-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4d472-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4d472-121">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4d472-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4d472-122">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4d472-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d472-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d472-123">Requirements</span></span>



| <span data-ttu-id="4d472-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d472-124">Requirement</span></span> | <span data-ttu-id="4d472-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4d472-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d472-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d472-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4d472-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d472-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4d472-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="4d472-128">Library</span></span><br/> | <dl> <span data-ttu-id="4d472-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d472-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d472-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d472-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d472-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4d472-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
