---
description: 'Metodo ID3DXTextureShader::SetMatrixTransposeArray : imposta una matrice di matrici trasposte.'
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: Metodo ID3DXTextureShader::SetMatrixTransposeArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663f49f600c000ff37974c8ecd4da56ba59630d1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090209"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="eaef8-103">Metodo ID3DXTextureShader::SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="eaef8-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="eaef8-104">Imposta una matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="eaef8-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaef8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eaef8-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="eaef8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eaef8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaef8-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eaef8-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaef8-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="eaef8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="eaef8-109">Identificatore univoco della matrice di costanti di matrice.</span><span class="sxs-lookup"><span data-stu-id="eaef8-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="eaef8-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="eaef8-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaef8-111">*pMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eaef8-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaef8-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="eaef8-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eaef8-113">Matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="eaef8-113">Array of transposed matrices.</span></span> <span data-ttu-id="eaef8-114">Vedere [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="eaef8-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaef8-115">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eaef8-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaef8-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eaef8-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eaef8-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="eaef8-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaef8-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eaef8-118">Return value</span></span>

<span data-ttu-id="eaef8-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eaef8-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eaef8-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eaef8-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eaef8-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="eaef8-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaef8-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="eaef8-122">Remarks</span></span>

<span data-ttu-id="eaef8-123">Una matrice trasposta contiene dati principali della colonna. ciò significa che ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="eaef8-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaef8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaef8-124">Requirements</span></span>



| <span data-ttu-id="eaef8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaef8-125">Requirement</span></span> | <span data-ttu-id="eaef8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="eaef8-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaef8-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eaef8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="eaef8-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="eaef8-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="eaef8-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="eaef8-129">Library</span></span><br/> | <dl> <span data-ttu-id="eaef8-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="eaef8-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="eaef8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eaef8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaef8-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="eaef8-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
