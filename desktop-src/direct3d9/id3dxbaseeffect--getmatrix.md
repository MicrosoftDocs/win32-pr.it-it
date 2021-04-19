---
description: Ottiene una matrice nontransposed.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'Metodo ID3DXBaseEffect:: getMatrix (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323600"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a><span data-ttu-id="87d26-103">Metodo ID3DXBaseEffect:: getMatrix</span><span class="sxs-lookup"><span data-stu-id="87d26-103">ID3DXBaseEffect::GetMatrix method</span></span>

<span data-ttu-id="87d26-104">Ottiene una matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="87d26-104">Gets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d26-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87d26-105">Syntax</span></span>


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="87d26-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87d26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d26-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87d26-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87d26-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="87d26-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="87d26-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="87d26-109">Unique identifier.</span></span> <span data-ttu-id="87d26-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="87d26-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="87d26-111">*pmatrix* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="87d26-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87d26-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87d26-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87d26-113">Restituisce una matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="87d26-113">Returns a nontransposed matrix.</span></span> <span data-ttu-id="87d26-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="87d26-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d26-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87d26-115">Return value</span></span>

<span data-ttu-id="87d26-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87d26-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87d26-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="87d26-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="87d26-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="87d26-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d26-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="87d26-119">Remarks</span></span>

<span data-ttu-id="87d26-120">Una matrice nontransposed contiene dati principali della riga; ovvero ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="87d26-120">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="87d26-121">Se la matrice di destinazione è più grande della matrice di origine, verranno riempiti solo i componenti in alto a sinistra della matrice di destinazione e i componenti rimanenti verranno impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="87d26-121">If the destination matrix is larger than the source matrix, only the upper-left components of the destination matrix will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d26-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87d26-122">Requirements</span></span>



| <span data-ttu-id="87d26-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="87d26-123">Requirement</span></span> | <span data-ttu-id="87d26-124">Valore</span><span class="sxs-lookup"><span data-stu-id="87d26-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d26-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87d26-125">Header</span></span><br/>  | <dl> <span data-ttu-id="87d26-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="87d26-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="87d26-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="87d26-127">Library</span></span><br/> | <dl> <span data-ttu-id="87d26-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87d26-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="87d26-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87d26-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d26-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="87d26-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="87d26-131">**Sematrix**</span><span class="sxs-lookup"><span data-stu-id="87d26-131">**SetMatrix**</span></span>](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




