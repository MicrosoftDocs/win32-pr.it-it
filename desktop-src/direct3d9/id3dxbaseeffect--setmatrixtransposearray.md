---
description: Imposta una matrice di matrici trasposte.
ms.assetid: 5dc65424-b0cd-490d-900e-60b9f7536ace
title: 'Metodo ID3DXBaseEffect:: SetMatrixTransposeArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e646761435f75688fe652683281297ca2b8de99e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323083"
---
# <a name="id3dxbaseeffectsetmatrixtransposearray-method"></a><span data-ttu-id="0bc6c-103">Metodo ID3DXBaseEffect:: SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="0bc6c-103">ID3DXBaseEffect::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="0bc6c-104">Imposta una matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="0bc6c-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc6c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bc6c-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="0bc6c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bc6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc6c-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc6c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc6c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0bc6c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0bc6c-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="0bc6c-109">Unique identifier.</span></span> <span data-ttu-id="0bc6c-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0bc6c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bc6c-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc6c-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc6c-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bc6c-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0bc6c-113">Matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="0bc6c-113">Array of transposed matrices.</span></span> <span data-ttu-id="0bc6c-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0bc6c-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bc6c-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0bc6c-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc6c-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bc6c-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bc6c-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="0bc6c-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc6c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0bc6c-118">Return value</span></span>

<span data-ttu-id="0bc6c-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bc6c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bc6c-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bc6c-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0bc6c-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0bc6c-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc6c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bc6c-122">Remarks</span></span>

<span data-ttu-id="0bc6c-123">Una matrice trasposta contiene dati di colonne principali; ovvero ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="0bc6c-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="0bc6c-124">Se le matrici di destinazione sono più piccole delle matrici di origine, i componenti aggiuntivi delle matrici di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="0bc6c-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc6c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bc6c-125">Requirements</span></span>



| <span data-ttu-id="0bc6c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bc6c-126">Requirement</span></span> | <span data-ttu-id="0bc6c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0bc6c-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc6c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0bc6c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0bc6c-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc6c-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0bc6c-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="0bc6c-130">Library</span></span><br/> | <dl> <span data-ttu-id="0bc6c-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bc6c-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0bc6c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bc6c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc6c-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0bc6c-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0bc6c-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="0bc6c-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
