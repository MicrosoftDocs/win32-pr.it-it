---
description: 'Metodo ID3DXBaseEffect::SetMatrix: imposta una matrice non trasposta.'
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: Metodo ID3DXBaseEffect::SetMatrix (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7af7dc0daa3dcd29e7b15c4fe435b9626ea41746
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097499"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="0cf69-103">Metodo ID3DXBaseEffect::SetMatrix</span><span class="sxs-lookup"><span data-stu-id="0cf69-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="0cf69-104">Imposta una matrice non trasposta.</span><span class="sxs-lookup"><span data-stu-id="0cf69-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cf69-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="0cf69-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cf69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf69-107">*hParameter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf69-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0cf69-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="0cf69-109">Unique identifier.</span></span> <span data-ttu-id="0cf69-110">Vedere [Handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0cf69-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cf69-111">*pMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0cf69-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf69-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0cf69-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0cf69-113">Puntatore a una matrice non trasposta.</span><span class="sxs-lookup"><span data-stu-id="0cf69-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="0cf69-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0cf69-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf69-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cf69-115">Return value</span></span>

<span data-ttu-id="0cf69-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cf69-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cf69-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cf69-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0cf69-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0cf69-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cf69-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cf69-119">Remarks</span></span>

<span data-ttu-id="0cf69-120">Una matrice non trasposta contiene dati principali di riga.</span><span class="sxs-lookup"><span data-stu-id="0cf69-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="0cf69-121">In altre parole, ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="0cf69-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="0cf69-122">Se la matrice di destinazione è più piccola della matrice di origine, i componenti aggiuntivi della matrice di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="0cf69-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf69-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cf69-123">Requirements</span></span>



| <span data-ttu-id="0cf69-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cf69-124">Requirement</span></span> | <span data-ttu-id="0cf69-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0cf69-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf69-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cf69-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0cf69-127"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="0cf69-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0cf69-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="0cf69-128">Library</span></span><br/> | <dl> <span data-ttu-id="0cf69-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cf69-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0cf69-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cf69-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf69-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0cf69-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0cf69-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="0cf69-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




