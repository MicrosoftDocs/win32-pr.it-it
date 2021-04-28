---
description: 'Metodo ID3DXBaseEffect::SetMatrixPointerArray: imposta una matrice di puntatori a matrici non trasposte.'
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: Metodo ID3DXBaseEffect::SetMatrixPointerArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cfe30e0132cfa237ddbccc24758b35e102a62b0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093769"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="20edf-103">Metodo ID3DXBaseEffect::SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="20edf-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="20edf-104">Imposta una matrice di puntatori a matrici non trasposte.</span><span class="sxs-lookup"><span data-stu-id="20edf-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="20edf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20edf-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="20edf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20edf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20edf-107">*hParameter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="20edf-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20edf-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="20edf-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="20edf-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="20edf-109">Unique identifier.</span></span> <span data-ttu-id="20edf-110">Vedere [Handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="20edf-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="20edf-111">*ppMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="20edf-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20edf-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="20edf-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="20edf-113">Matrice di puntatori a matrici non trasposte.</span><span class="sxs-lookup"><span data-stu-id="20edf-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="20edf-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="20edf-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="20edf-115">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="20edf-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20edf-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20edf-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20edf-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="20edf-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20edf-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20edf-118">Return value</span></span>

<span data-ttu-id="20edf-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20edf-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20edf-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20edf-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="20edf-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="20edf-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="20edf-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="20edf-122">Remarks</span></span>

<span data-ttu-id="20edf-123">Una matrice non trasposta contiene dati principali di riga. in altri, ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="20edf-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="20edf-124">Se le matrici di destinazione sono più piccole delle matrici di origine, i componenti aggiuntivi delle matrici di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="20edf-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="20edf-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20edf-125">Requirements</span></span>



| <span data-ttu-id="20edf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="20edf-126">Requirement</span></span> | <span data-ttu-id="20edf-127">Valore</span><span class="sxs-lookup"><span data-stu-id="20edf-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20edf-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20edf-128">Header</span></span><br/>  | <dl> <span data-ttu-id="20edf-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="20edf-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="20edf-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="20edf-130">Library</span></span><br/> | <dl> <span data-ttu-id="20edf-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="20edf-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="20edf-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20edf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20edf-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="20edf-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="20edf-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="20edf-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
