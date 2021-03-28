---
title: Metodo ID3DX11EffectShaderResourceVariable GetResourceArray (D3dx11effect. h)
description: Ottenere una matrice di risorse dello shader.
ms.assetid: 7540183d-dabb-46c2-8df1-6d4734b77f25
keywords:
- Metodo GetResourceArray Direct3D 11
- Metodo GetResourceArray Direct3D 11, interfaccia ID3DX11EffectShaderResourceVariable
- Interfaccia ID3DX11EffectShaderResourceVariable Direct3D 11, metodo GetResourceArray
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResourceArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0091d81b7e157aecb8315e1def380800c8155c60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969524"
---
# <a name="id3dx11effectshaderresourcevariablegetresourcearray-method"></a><span data-ttu-id="7453c-106">Metodo ID3DX11EffectShaderResourceVariable:: GetResourceArray</span><span class="sxs-lookup"><span data-stu-id="7453c-106">ID3DX11EffectShaderResourceVariable::GetResourceArray method</span></span>

<span data-ttu-id="7453c-107">Ottenere una matrice di risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="7453c-107">Get an array of shader resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="7453c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7453c-108">Syntax</span></span>


```C++
HRESULT GetResourceArray(
   ID3D11ShaderResourceView **ppResources,
   UINT                     Offset,
   UINT                     Count
);
```



## <a name="parameters"></a><span data-ttu-id="7453c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7453c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7453c-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="7453c-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="7453c-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="7453c-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="7453c-112">Indirizzo di una matrice di interfacce shader-Resource-View.</span><span class="sxs-lookup"><span data-stu-id="7453c-112">The address of an array of shader-resource-view interfaces.</span></span> <span data-ttu-id="7453c-113">Vedere [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="7453c-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="7453c-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="7453c-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="7453c-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7453c-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7453c-116">Indice della matrice in base zero per ottenere la prima interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7453c-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="7453c-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="7453c-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="7453c-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7453c-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7453c-119">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="7453c-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7453c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7453c-120">Return value</span></span>

<span data-ttu-id="7453c-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7453c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7453c-122">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7453c-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7453c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7453c-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7453c-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="7453c-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7453c-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7453c-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7453c-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7453c-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7453c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7453c-127">Requirements</span></span>



| <span data-ttu-id="7453c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7453c-128">Requirement</span></span> | <span data-ttu-id="7453c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7453c-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7453c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7453c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7453c-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7453c-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7453c-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="7453c-132">Library</span></span><br/> | <dl> <span data-ttu-id="7453c-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="7453c-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7453c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7453c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7453c-135">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="7453c-135">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

