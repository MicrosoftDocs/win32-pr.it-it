---
description: Imposta una matrice non trasposta.
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'Metodo ID3DXBaseEffect:: sematrix (D3DX9Shader. h)'
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
ms.openlocfilehash: 39a5aed1d6321cf0599d212222fd967ee512e20e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530847"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="cac1b-103">Metodo ID3DXBaseEffect:: sematrix</span><span class="sxs-lookup"><span data-stu-id="cac1b-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="cac1b-104">Imposta una matrice non trasposta.</span><span class="sxs-lookup"><span data-stu-id="cac1b-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac1b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cac1b-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="cac1b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cac1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac1b-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cac1b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac1b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cac1b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cac1b-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="cac1b-109">Unique identifier.</span></span> <span data-ttu-id="cac1b-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="cac1b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="cac1b-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cac1b-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac1b-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cac1b-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cac1b-113">Puntatore a una matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="cac1b-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="cac1b-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="cac1b-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac1b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cac1b-115">Return value</span></span>

<span data-ttu-id="cac1b-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cac1b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cac1b-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cac1b-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cac1b-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cac1b-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cac1b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cac1b-119">Remarks</span></span>

<span data-ttu-id="cac1b-120">Una matrice non trasposta contiene dati di riga principali.</span><span class="sxs-lookup"><span data-stu-id="cac1b-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="cac1b-121">In altre parole, ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="cac1b-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="cac1b-122">Se la matrice di destinazione è minore della matrice di origine, i componenti aggiuntivi della matrice di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="cac1b-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac1b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cac1b-123">Requirements</span></span>



| <span data-ttu-id="cac1b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac1b-124">Requirement</span></span> | <span data-ttu-id="cac1b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cac1b-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac1b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cac1b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cac1b-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac1b-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cac1b-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="cac1b-128">Library</span></span><br/> | <dl> <span data-ttu-id="cac1b-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cac1b-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cac1b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cac1b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac1b-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="cac1b-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="cac1b-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="cac1b-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




