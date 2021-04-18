---
description: Imposta una matrice di matrici non transposte.
ms.assetid: 27f230bd-9aee-4673-aa70-5ecda541b1be
title: 'Metodo ID3DXTextureShader:: SetMatrixArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b0545d48e16698f44cc48ad467f9454ac94db030
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322783"
---
# <a name="id3dxtextureshadersetmatrixarray-method"></a><span data-ttu-id="2b15b-103">Metodo ID3DXTextureShader:: SetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="2b15b-103">ID3DXTextureShader::SetMatrixArray method</span></span>

<span data-ttu-id="2b15b-104">Imposta una matrice di matrici non transposte.</span><span class="sxs-lookup"><span data-stu-id="2b15b-104">Sets an array of non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b15b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b15b-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2b15b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b15b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b15b-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b15b-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b15b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2b15b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2b15b-109">Identificatore univoco della matrice di matrici costanti.</span><span class="sxs-lookup"><span data-stu-id="2b15b-109">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="2b15b-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="2b15b-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b15b-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b15b-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b15b-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b15b-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2b15b-113">Matrice di matrici non transposte.</span><span class="sxs-lookup"><span data-stu-id="2b15b-113">Array of non-transposed matrices.</span></span> <span data-ttu-id="2b15b-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2b15b-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b15b-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2b15b-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b15b-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b15b-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b15b-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2b15b-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b15b-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b15b-118">Return value</span></span>

<span data-ttu-id="2b15b-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b15b-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b15b-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b15b-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b15b-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2b15b-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b15b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b15b-122">Remarks</span></span>

<span data-ttu-id="2b15b-123">Una matrice non trasposta contiene dati di riga: principali; ovvero ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="2b15b-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b15b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b15b-124">Requirements</span></span>



| <span data-ttu-id="2b15b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b15b-125">Requirement</span></span> | <span data-ttu-id="2b15b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2b15b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b15b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b15b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2b15b-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b15b-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2b15b-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="2b15b-129">Library</span></span><br/> | <dl> <span data-ttu-id="2b15b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b15b-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2b15b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b15b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b15b-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2b15b-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
