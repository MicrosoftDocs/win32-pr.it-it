---
description: Imposta una matrice di puntatori a matrici trasposte.
ms.assetid: 11a21077-eeee-4d52-ac16-41444e3eca4f
title: 'Metodo ID3DXBaseEffect:: SetMatrixTransposePointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1152deccdcadebe9f421fac6d7d5ce53c8d3e5f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323279"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a><span data-ttu-id="ea914-103">Metodo ID3DXBaseEffect:: SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="ea914-103">ID3DXBaseEffect::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="ea914-104">Imposta una matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="ea914-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea914-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea914-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ea914-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea914-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea914-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea914-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea914-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ea914-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ea914-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="ea914-109">Unique identifier.</span></span> <span data-ttu-id="ea914-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ea914-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea914-111">*ppMatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea914-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea914-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="ea914-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="ea914-113">Matrice di puntatori alle matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="ea914-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="ea914-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="ea914-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea914-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ea914-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea914-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea914-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea914-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="ea914-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea914-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea914-118">Return value</span></span>

<span data-ttu-id="ea914-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea914-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea914-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea914-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea914-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ea914-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea914-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea914-122">Remarks</span></span>

<span data-ttu-id="ea914-123">Una matrice trasposta contiene dati di colonne principali; ovvero ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="ea914-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="ea914-124">Se le matrici di destinazione sono più piccole delle matrici di origine, i componenti aggiuntivi delle matrici di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="ea914-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea914-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea914-125">Requirements</span></span>



| <span data-ttu-id="ea914-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea914-126">Requirement</span></span> | <span data-ttu-id="ea914-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ea914-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea914-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea914-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ea914-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea914-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ea914-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea914-130">Library</span></span><br/> | <dl> <span data-ttu-id="ea914-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea914-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ea914-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea914-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea914-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ea914-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ea914-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="ea914-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
