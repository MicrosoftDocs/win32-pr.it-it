---
description: 'Funzione D3DXMatrixDecompose (D3DX10Math.h): suddivide una matrice di trasformazione 3D generale nei componenti scalari, rotazionali e traslazionali.'
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Funzione D3DXMatrixDecompose (D3DX10Math.h)
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
ms.openlocfilehash: cc87de99d72283c20f25b15ea8d0e5864e2550d9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113209"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="522cf-103">Funzione D3DXMatrixDecompose (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="522cf-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="522cf-104">Suddivide una matrice di trasformazione 3D generale nei relativi componenti scalari, rotazionali e traslazionali.</span><span class="sxs-lookup"><span data-stu-id="522cf-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="522cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="522cf-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="522cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="522cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522cf-107">*pOutScale* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="522cf-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="522cf-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="522cf-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="522cf-109">Puntatore all'oggetto [**D3DXVECTOR3**](d3d10-d3dxvector3.md) di output che contiene i fattori di scala applicati lungo gli assi x, y e z.</span><span class="sxs-lookup"><span data-stu-id="522cf-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="522cf-110">*pOutRotation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="522cf-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="522cf-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="522cf-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="522cf-112">Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che descrive la rotazione.</span><span class="sxs-lookup"><span data-stu-id="522cf-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="522cf-113">*pOutTranslation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="522cf-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="522cf-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="522cf-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="522cf-115">Puntatore al vettore D3DXVECTOR3 che descrive la conversione.</span><span class="sxs-lookup"><span data-stu-id="522cf-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="522cf-116">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="522cf-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="522cf-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="522cf-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="522cf-118">Puntatore a una matrice [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di input da scomporre.</span><span class="sxs-lookup"><span data-stu-id="522cf-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="522cf-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="522cf-119">Return value</span></span>

<span data-ttu-id="522cf-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="522cf-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="522cf-121">Se la funzione ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="522cf-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="522cf-122">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="522cf-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="522cf-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="522cf-123">Requirements</span></span>



| <span data-ttu-id="522cf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="522cf-124">Requirement</span></span> | <span data-ttu-id="522cf-125">Valore</span><span class="sxs-lookup"><span data-stu-id="522cf-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="522cf-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="522cf-126">Header</span></span><br/>  | <dl> <span data-ttu-id="522cf-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="522cf-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="522cf-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="522cf-128">Library</span></span><br/> | <dl> <span data-ttu-id="522cf-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="522cf-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="522cf-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="522cf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522cf-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="522cf-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
