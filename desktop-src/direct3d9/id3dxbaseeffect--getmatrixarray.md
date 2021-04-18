---
description: Ottiene una matrice di matrici nontransposed.
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: 'Metodo ID3DXBaseEffect:: GetMatrixArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 242b3c42976f9bfe4ad8ecad4d965c473839ffdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323599"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a><span data-ttu-id="15872-103">Metodo ID3DXBaseEffect:: GetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="15872-103">ID3DXBaseEffect::GetMatrixArray method</span></span>

<span data-ttu-id="15872-104">Ottiene una matrice di matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="15872-104">Gets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="15872-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15872-105">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="15872-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15872-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15872-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15872-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="15872-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="15872-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="15872-109">Unique identifier.</span></span> <span data-ttu-id="15872-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="15872-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="15872-111">*pmatrix* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="15872-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15872-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="15872-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="15872-113">Restituisce una matrice di matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="15872-113">Returns an array of nontransposed matrices.</span></span> <span data-ttu-id="15872-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="15872-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="15872-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="15872-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15872-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15872-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15872-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="15872-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15872-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15872-118">Return value</span></span>

<span data-ttu-id="15872-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15872-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15872-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15872-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="15872-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="15872-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="15872-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="15872-122">Remarks</span></span>

<span data-ttu-id="15872-123">Una matrice nontransposed contiene dati principali della riga; ovvero ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="15872-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="15872-124">Se le matrici di destinazione sono più grandi delle matrici di origine, verranno riempiti solo i componenti in alto a sinistra di ogni matrice di destinazione e i componenti della matrice di destinazione rimanenti verranno impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="15872-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="15872-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15872-125">Requirements</span></span>



| <span data-ttu-id="15872-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="15872-126">Requirement</span></span> | <span data-ttu-id="15872-127">Valore</span><span class="sxs-lookup"><span data-stu-id="15872-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15872-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15872-128">Header</span></span><br/>  | <dl> <span data-ttu-id="15872-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="15872-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="15872-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="15872-130">Library</span></span><br/> | <dl> <span data-ttu-id="15872-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15872-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="15872-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15872-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15872-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="15872-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="15872-134">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="15872-134">**SetMatrixArray**</span></span>](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
