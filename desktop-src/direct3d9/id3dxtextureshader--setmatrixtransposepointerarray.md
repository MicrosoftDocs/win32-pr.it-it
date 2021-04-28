---
description: 'Metodo ID3DXTextureShader::SetMatrixTransposePointerArray: imposta una matrice di puntatori alle matrici trasposte.'
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: Metodo ID3DXTextureShader::SetMatrixTransposePointerArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 46e04c8c86bd0cdf7acea44872d00ad19f620ee6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090149"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="c5f55-103">Metodo ID3DXTextureShader::SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="c5f55-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="c5f55-104">Imposta una matrice di puntatori alle matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="c5f55-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5f55-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c5f55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5f55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5f55-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c5f55-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f55-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c5f55-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c5f55-109">Identificatore univoco della matrice di costanti di matrice.</span><span class="sxs-lookup"><span data-stu-id="c5f55-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="c5f55-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c5f55-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5f55-111">*ppMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c5f55-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f55-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="c5f55-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="c5f55-113">Matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="c5f55-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="c5f55-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c5f55-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5f55-115">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c5f55-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f55-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5f55-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5f55-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="c5f55-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5f55-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5f55-118">Return value</span></span>

<span data-ttu-id="c5f55-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5f55-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5f55-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5f55-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c5f55-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c5f55-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5f55-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5f55-122">Remarks</span></span>

<span data-ttu-id="c5f55-123">Una matrice trasposta contiene dati principali della colonna. in altri, ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="c5f55-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f55-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5f55-124">Requirements</span></span>



| <span data-ttu-id="c5f55-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f55-125">Requirement</span></span> | <span data-ttu-id="c5f55-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c5f55-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f55-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5f55-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c5f55-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f55-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c5f55-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5f55-129">Library</span></span><br/> | <dl> <span data-ttu-id="c5f55-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5f55-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c5f55-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5f55-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f55-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c5f55-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
