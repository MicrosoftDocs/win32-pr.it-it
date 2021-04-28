---
description: 'Metodo ID3DXBaseEffect::SetMatrixTranspose: imposta una matrice trasposta.'
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: Metodo ID3DXBaseEffect::SetMatrixTranspose (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 384d4a7ed5e1b769218b9290ed6cc0f7f060bd66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107399"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="37858-103">Metodo ID3DXBaseEffect::SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="37858-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="37858-104">Imposta una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="37858-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="37858-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37858-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="37858-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37858-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37858-107">*hParameter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="37858-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37858-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="37858-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="37858-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="37858-109">Unique identifier.</span></span> <span data-ttu-id="37858-110">Vedere [Handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="37858-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="37858-111">*pMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="37858-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37858-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="37858-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="37858-113">Puntatore a una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="37858-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="37858-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="37858-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37858-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37858-115">Return value</span></span>

<span data-ttu-id="37858-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37858-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37858-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="37858-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="37858-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="37858-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="37858-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="37858-119">Remarks</span></span>

<span data-ttu-id="37858-120">Una matrice trasposta contiene dati principali della colonna. in altri, ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="37858-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="37858-121">Se la matrice di destinazione è più piccola della matrice di origine, i componenti aggiuntivi della matrice di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="37858-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="37858-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37858-122">Requirements</span></span>



| <span data-ttu-id="37858-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="37858-123">Requirement</span></span> | <span data-ttu-id="37858-124">Valore</span><span class="sxs-lookup"><span data-stu-id="37858-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="37858-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37858-125">Header</span></span><br/>  | <dl> <span data-ttu-id="37858-126"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="37858-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="37858-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="37858-127">Library</span></span><br/> | <dl> <span data-ttu-id="37858-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="37858-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="37858-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37858-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37858-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="37858-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="37858-131">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="37858-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




