---
description: Imposta una matrice di valori a virgola mobile.
ms.assetid: 4b9c27b4-0255-4bbf-9168-491936d64fb9
title: 'Metodo ID3DXBaseEffect:: SetFloatArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9927f3cd79d7950a94e62881089fb06c67395bac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234935"
---
# <a name="id3dxbaseeffectsetfloatarray-method"></a><span data-ttu-id="fca8d-103">Metodo ID3DXBaseEffect:: SetFloatArray</span><span class="sxs-lookup"><span data-stu-id="fca8d-103">ID3DXBaseEffect::SetFloatArray method</span></span>

<span data-ttu-id="fca8d-104">Imposta una matrice di valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="fca8d-104">Sets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca8d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fca8d-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hParameter,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="fca8d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fca8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fca8d-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fca8d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fca8d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fca8d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fca8d-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="fca8d-109">Unique identifier.</span></span> <span data-ttu-id="fca8d-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fca8d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fca8d-111">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fca8d-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fca8d-112">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fca8d-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fca8d-113">Matrice di valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="fca8d-113">Array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="fca8d-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fca8d-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fca8d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fca8d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fca8d-116">Numero di valori a virgola mobile nella matrice.</span><span class="sxs-lookup"><span data-stu-id="fca8d-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fca8d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fca8d-117">Return value</span></span>

<span data-ttu-id="fca8d-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fca8d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fca8d-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fca8d-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fca8d-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fca8d-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fca8d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fca8d-121">Requirements</span></span>



| <span data-ttu-id="fca8d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fca8d-122">Requirement</span></span> | <span data-ttu-id="fca8d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fca8d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fca8d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fca8d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fca8d-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca8d-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fca8d-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="fca8d-126">Library</span></span><br/> | <dl> <span data-ttu-id="fca8d-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fca8d-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fca8d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fca8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca8d-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fca8d-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fca8d-130">**GetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="fca8d-130">**GetFloatArray**</span></span>](id3dxbaseeffect--getfloatarray.md)
</dt> </dl>

 

 
