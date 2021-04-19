---
description: Suddivide una matrice di trasformazione 3D generale nei componenti scalari, rotazionali e di conversione.
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Funzione D3DXMatrixDecompose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323246"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="6597b-103">Funzione D3DXMatrixDecompose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6597b-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="6597b-104">Suddivide una matrice di trasformazione 3D generale nei componenti scalari, rotazionali e di conversione.</span><span class="sxs-lookup"><span data-stu-id="6597b-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="6597b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6597b-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="6597b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6597b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6597b-107">*pOutScale* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6597b-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6597b-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6597b-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6597b-109">Puntatore al [**D3DXVECTOR3**](d3dxvector3.md) di output che contiene i fattori di scala applicati lungo gli assi x, y e z.</span><span class="sxs-lookup"><span data-stu-id="6597b-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="6597b-110">*pOutRotation* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6597b-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6597b-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6597b-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6597b-112">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che descrive la rotazione.</span><span class="sxs-lookup"><span data-stu-id="6597b-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="6597b-113">*pOutTranslation* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6597b-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6597b-114">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6597b-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6597b-115">Puntatore al vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la traduzione.</span><span class="sxs-lookup"><span data-stu-id="6597b-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="6597b-116">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6597b-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6597b-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6597b-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6597b-118">Puntatore a una matrice di input [**D3DXMATRIX**](d3dxmatrix.md) da scomporre.</span><span class="sxs-lookup"><span data-stu-id="6597b-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6597b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6597b-119">Return value</span></span>

<span data-ttu-id="6597b-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6597b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6597b-121">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6597b-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6597b-122">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6597b-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6597b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6597b-123">Requirements</span></span>



| <span data-ttu-id="6597b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6597b-124">Requirement</span></span> | <span data-ttu-id="6597b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6597b-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6597b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6597b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6597b-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6597b-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6597b-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="6597b-128">Library</span></span><br/> | <dl> <span data-ttu-id="6597b-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6597b-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6597b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6597b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6597b-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6597b-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




