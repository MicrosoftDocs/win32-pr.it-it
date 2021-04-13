---
description: Consente di abilitare o disabilitare lo stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'Metodo ID3DXEffectCompiler:: seliteral (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354354"
---
# <a name="id3dxeffectcompilersetliteral-method"></a><span data-ttu-id="837b9-104">Metodo ID3DXEffectCompiler:: seliteral</span><span class="sxs-lookup"><span data-stu-id="837b9-104">ID3DXEffectCompiler::SetLiteral method</span></span>

<span data-ttu-id="837b9-105">Consente di abilitare o disabilitare lo stato letterale di un parametro.</span><span class="sxs-lookup"><span data-stu-id="837b9-105">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="837b9-106">Un parametro letterale ha un valore che non cambia durante la durata di un effetto.</span><span class="sxs-lookup"><span data-stu-id="837b9-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="837b9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="837b9-107">Syntax</span></span>


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a><span data-ttu-id="837b9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="837b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="837b9-109">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="837b9-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="837b9-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="837b9-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="837b9-111">Identificatore univoco per un parametro.</span><span class="sxs-lookup"><span data-stu-id="837b9-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="837b9-112">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="837b9-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="837b9-113">*Valore letterale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="837b9-113">*Literal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="837b9-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="837b9-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="837b9-115">Impostare su **true** per fare in modo che il parametro sia un valore letterale e **false** se il parametro può modificare il valore durante la durata dello shader.</span><span class="sxs-lookup"><span data-stu-id="837b9-115">Set to **TRUE** to make the parameter a literal, and **FALSE** if the parameter can change value during the shader lifetime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="837b9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="837b9-116">Return value</span></span>

<span data-ttu-id="837b9-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="837b9-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="837b9-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="837b9-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="837b9-119">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="837b9-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="837b9-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="837b9-120">Remarks</span></span>

<span data-ttu-id="837b9-121">Questo metodo cambia solo se il parametro è un valore letterale o meno.</span><span class="sxs-lookup"><span data-stu-id="837b9-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="837b9-122">Per modificare il valore di un parametro, usare un metodo come [**ID3DXBaseEffect::**](id3dxbaseeffect--setbool.md) SetValue o [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="837b9-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

<span data-ttu-id="837b9-123">Questa funzione deve essere chiamata prima che l'effetto venga compilato.</span><span class="sxs-lookup"><span data-stu-id="837b9-123">This function must be called before the effect is compiled.</span></span> <span data-ttu-id="837b9-124">Di seguito è riportato un esempio di come è possibile usare questa funzione:</span><span class="sxs-lookup"><span data-stu-id="837b9-124">Here is an example of how one might use this function:</span></span>


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a><span data-ttu-id="837b9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="837b9-125">Requirements</span></span>



| <span data-ttu-id="837b9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="837b9-126">Requirement</span></span> | <span data-ttu-id="837b9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="837b9-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="837b9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="837b9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="837b9-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="837b9-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="837b9-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="837b9-130">Library</span></span><br/> | <dl> <span data-ttu-id="837b9-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="837b9-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="837b9-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="837b9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837b9-133">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="837b9-133">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="837b9-134">Utilizzi e valori letterali (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="837b9-134">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="837b9-135">**ID3DXEffectCompiler:: GetLiteral**</span><span class="sxs-lookup"><span data-stu-id="837b9-135">**ID3DXEffectCompiler::GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
