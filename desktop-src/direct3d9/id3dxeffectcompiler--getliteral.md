---
description: Ottiene uno stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'Metodo ID3DXEffectCompiler:: GetLiteral (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322348"
---
# <a name="id3dxeffectcompilergetliteral-method"></a><span data-ttu-id="dee1d-104">Metodo ID3DXEffectCompiler:: GetLiteral</span><span class="sxs-lookup"><span data-stu-id="dee1d-104">ID3DXEffectCompiler::GetLiteral method</span></span>

<span data-ttu-id="dee1d-105">Ottiene uno stato letterale di un parametro.</span><span class="sxs-lookup"><span data-stu-id="dee1d-105">Gets a literal status of a parameter.</span></span> <span data-ttu-id="dee1d-106">Un parametro letterale ha un valore che non cambia durante la durata di un effetto.</span><span class="sxs-lookup"><span data-stu-id="dee1d-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee1d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dee1d-107">Syntax</span></span>


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="dee1d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dee1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dee1d-109">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dee1d-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee1d-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dee1d-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dee1d-111">Identificatore univoco per un parametro.</span><span class="sxs-lookup"><span data-stu-id="dee1d-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="dee1d-112">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dee1d-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee1d-113">*pLiteral* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dee1d-113">*pLiteral* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dee1d-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dee1d-114">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dee1d-115">Restituisce true se il parametro è un valore letterale e false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dee1d-115">Returns True if the parameter is a literal, and False otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dee1d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dee1d-116">Return value</span></span>

<span data-ttu-id="dee1d-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dee1d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dee1d-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dee1d-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dee1d-119">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="dee1d-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dee1d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="dee1d-120">Remarks</span></span>

<span data-ttu-id="dee1d-121">Questo metodo cambia solo se il parametro è un valore letterale o meno.</span><span class="sxs-lookup"><span data-stu-id="dee1d-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="dee1d-122">Per modificare il valore di un parametro, usare un metodo come [**ID3DXBaseEffect::**](id3dxbaseeffect--setbool.md) SetValue o [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="dee1d-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dee1d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dee1d-123">Requirements</span></span>



| <span data-ttu-id="dee1d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee1d-124">Requirement</span></span> | <span data-ttu-id="dee1d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="dee1d-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee1d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dee1d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="dee1d-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="dee1d-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="dee1d-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="dee1d-128">Library</span></span><br/> | <dl> <span data-ttu-id="dee1d-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dee1d-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dee1d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dee1d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee1d-131">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="dee1d-131">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="dee1d-132">Utilizzi e valori letterali (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dee1d-132">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="dee1d-133">**ID3DXEffectCompiler:: seliteral**</span><span class="sxs-lookup"><span data-stu-id="dee1d-133">**ID3DXEffectCompiler::SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
