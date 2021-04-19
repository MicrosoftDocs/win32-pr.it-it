---
description: Ottiene una matrice di valori BOOL.
ms.assetid: 4a5e2f48-fa82-47dc-a388-02a8679585d2
title: 'Metodo ID3DXBaseEffect:: GetBoolArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f714dfa91baba14524f12b6c3b2cb85211484cf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323611"
---
# <a name="id3dxbaseeffectgetboolarray-method"></a><span data-ttu-id="3e7ac-103">Metodo ID3DXBaseEffect:: GetBoolArray</span><span class="sxs-lookup"><span data-stu-id="3e7ac-103">ID3DXBaseEffect::GetBoolArray method</span></span>

<span data-ttu-id="3e7ac-104">Ottiene una matrice di valori BOOL.</span><span class="sxs-lookup"><span data-stu-id="3e7ac-104">Gets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e7ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e7ac-105">Syntax</span></span>


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="3e7ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e7ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e7ac-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e7ac-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e7ac-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3e7ac-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3e7ac-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="3e7ac-109">Unique identifier.</span></span> <span data-ttu-id="3e7ac-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3e7ac-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e7ac-111">*PB* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3e7ac-111">*pB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e7ac-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e7ac-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3e7ac-113">Restituisce una matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="3e7ac-113">Returns an array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="3e7ac-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3e7ac-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e7ac-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e7ac-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e7ac-116">Numero di valori booleani nella matrice.</span><span class="sxs-lookup"><span data-stu-id="3e7ac-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e7ac-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e7ac-117">Return value</span></span>

<span data-ttu-id="3e7ac-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e7ac-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e7ac-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3e7ac-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3e7ac-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3e7ac-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e7ac-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e7ac-121">Requirements</span></span>



| <span data-ttu-id="3e7ac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e7ac-122">Requirement</span></span> | <span data-ttu-id="3e7ac-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3e7ac-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7ac-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e7ac-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3e7ac-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e7ac-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3e7ac-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e7ac-126">Library</span></span><br/> | <dl> <span data-ttu-id="3e7ac-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e7ac-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3e7ac-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e7ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e7ac-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3e7ac-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="3e7ac-130">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="3e7ac-130">**SetBoolArray**</span></span>](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 
