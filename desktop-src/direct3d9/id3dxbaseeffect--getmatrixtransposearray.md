---
description: Ottiene una matrice di matrici trasposte.
ms.assetid: fbfcb2e4-82ca-4f79-923e-35749c5b9586
title: 'Metodo ID3DXBaseEffect:: GetMatrixTransposeArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c5f3709a31067b82e9752a9e97db6f3a2a323a19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762358"
---
# <a name="id3dxbaseeffectgetmatrixtransposearray-method"></a><span data-ttu-id="16716-103">Metodo ID3DXBaseEffect:: GetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="16716-103">ID3DXBaseEffect::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="16716-104">Ottiene una matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="16716-104">Gets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="16716-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16716-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="16716-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16716-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16716-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16716-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16716-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="16716-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="16716-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="16716-109">Unique identifier.</span></span> <span data-ttu-id="16716-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="16716-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="16716-111">*pmatrix* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="16716-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16716-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="16716-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16716-113">Restituisce una matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="16716-113">Returns an array of transposed matrices.</span></span> <span data-ttu-id="16716-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="16716-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="16716-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="16716-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16716-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16716-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16716-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="16716-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16716-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16716-118">Return value</span></span>

<span data-ttu-id="16716-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16716-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16716-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="16716-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="16716-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="16716-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="16716-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="16716-122">Remarks</span></span>

<span data-ttu-id="16716-123">Una matrice trasposta contiene dati di colonne principali; ovvero ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="16716-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="16716-124">Se le matrici di destinazione sono più grandi delle matrici di origine, verranno riempiti solo i componenti in alto a sinistra di ogni matrice di destinazione e i componenti della matrice di destinazione rimanenti verranno impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="16716-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="16716-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16716-125">Requirements</span></span>



| <span data-ttu-id="16716-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="16716-126">Requirement</span></span> | <span data-ttu-id="16716-127">Valore</span><span class="sxs-lookup"><span data-stu-id="16716-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16716-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16716-128">Header</span></span><br/>  | <dl> <span data-ttu-id="16716-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="16716-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="16716-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="16716-130">Library</span></span><br/> | <dl> <span data-ttu-id="16716-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16716-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="16716-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16716-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16716-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="16716-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="16716-134">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="16716-134">**SetMatrixTransposeArray**</span></span>](id3dxbaseeffect--setmatrixtransposearray.md)
</dt> </dl>

 

 
