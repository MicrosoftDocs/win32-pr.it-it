---
description: 'Metodo ID3DXBaseEffect::SetMatrixTransposePointerArray : imposta una matrice di puntatori alle matrici trasposte.'
ms.assetid: 11a21077-eeee-4d52-ac16-41444e3eca4f
title: Metodo ID3DXBaseEffect::SetMatrixTransposePointerArray (D3DX9Shader.h)
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
ms.openlocfilehash: 3f35afad1120a26a60f670d12410584b2f9db7f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107389"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a><span data-ttu-id="e8105-103">Metodo ID3DXBaseEffect::SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="e8105-103">ID3DXBaseEffect::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="e8105-104">Imposta una matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="e8105-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8105-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8105-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="e8105-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8105-107">*hParameter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e8105-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8105-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e8105-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e8105-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="e8105-109">Unique identifier.</span></span> <span data-ttu-id="e8105-110">Vedere [Handle (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="e8105-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8105-111">*ppMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e8105-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8105-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="e8105-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="e8105-113">Matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="e8105-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="e8105-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e8105-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8105-115">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e8105-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8105-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8105-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8105-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="e8105-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8105-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8105-118">Return value</span></span>

<span data-ttu-id="e8105-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8105-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8105-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8105-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e8105-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e8105-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8105-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8105-122">Remarks</span></span>

<span data-ttu-id="e8105-123">Una matrice trasposta contiene dati principali della colonna. ciò significa che ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="e8105-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="e8105-124">Se le matrici di destinazione sono più piccole delle matrici di origine, i componenti aggiuntivi delle matrici di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="e8105-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8105-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8105-125">Requirements</span></span>



| <span data-ttu-id="e8105-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8105-126">Requirement</span></span> | <span data-ttu-id="e8105-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e8105-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8105-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8105-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e8105-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="e8105-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e8105-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8105-130">Library</span></span><br/> | <dl> <span data-ttu-id="e8105-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8105-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e8105-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8105-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8105-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e8105-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="e8105-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="e8105-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
