---
description: 'Metodo ID3DXBaseEffect::SetIntArray : imposta una matrice di numeri interi.'
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: Metodo ID3DXBaseEffect::SetIntArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a14e837a0903290c3197bbb17ec4b2da3f68b419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093759"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="8efc6-103">Metodo ID3DXBaseEffect::SetIntArray</span><span class="sxs-lookup"><span data-stu-id="8efc6-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="8efc6-104">Imposta una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="8efc6-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8efc6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8efc6-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="8efc6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8efc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8efc6-107">*hParameter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8efc6-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efc6-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8efc6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8efc6-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="8efc6-109">Unique identifier.</span></span> <span data-ttu-id="8efc6-110">Vedere [Handle (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="8efc6-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8efc6-111">*pn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8efc6-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efc6-112">Tipo: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8efc6-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8efc6-113">Matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="8efc6-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="8efc6-114">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8efc6-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efc6-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8efc6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8efc6-116">Numero di numeri interi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="8efc6-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8efc6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8efc6-117">Return value</span></span>

<span data-ttu-id="8efc6-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8efc6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8efc6-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8efc6-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8efc6-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8efc6-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8efc6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8efc6-121">Requirements</span></span>



| <span data-ttu-id="8efc6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8efc6-122">Requirement</span></span> | <span data-ttu-id="8efc6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8efc6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8efc6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8efc6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8efc6-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="8efc6-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8efc6-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="8efc6-126">Library</span></span><br/> | <dl> <span data-ttu-id="8efc6-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8efc6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8efc6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8efc6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8efc6-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8efc6-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8efc6-130">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="8efc6-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
