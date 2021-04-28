---
description: 'Metodo ID3DXBaseEffect::SetBoolArray: imposta una matrice di valori booleani.'
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: Metodo ID3DXBaseEffect::SetBoolArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cad6846914d348dd49d6362d70271c5af078e35d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093829"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="6d1b3-103">Metodo ID3DXBaseEffect::SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="6d1b3-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="6d1b3-104">Imposta una matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="6d1b3-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d1b3-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="6d1b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d1b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d1b3-107">*hParameter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6d1b3-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1b3-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6d1b3-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6d1b3-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="6d1b3-109">Unique identifier.</span></span> <span data-ttu-id="6d1b3-110">Vedere [Handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6d1b3-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d1b3-111">*pB* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6d1b3-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1b3-112">Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d1b3-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6d1b3-113">Matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="6d1b3-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="6d1b3-114">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6d1b3-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d1b3-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d1b3-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d1b3-116">Numero di valori booleani nella matrice.</span><span class="sxs-lookup"><span data-stu-id="6d1b3-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d1b3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d1b3-117">Return value</span></span>

<span data-ttu-id="6d1b3-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d1b3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d1b3-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d1b3-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6d1b3-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6d1b3-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d1b3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d1b3-121">Requirements</span></span>



| <span data-ttu-id="6d1b3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d1b3-122">Requirement</span></span> | <span data-ttu-id="6d1b3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6d1b3-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1b3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d1b3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6d1b3-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="6d1b3-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6d1b3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d1b3-126">Library</span></span><br/> | <dl> <span data-ttu-id="6d1b3-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d1b3-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6d1b3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d1b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1b3-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6d1b3-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="6d1b3-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="6d1b3-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
