---
title: Metodo ID3DX11EffectShaderResourceVariable SetResourceArray (D3dx11effect. h)
description: Impostare una matrice di risorse dello shader.
ms.assetid: b9597878-01af-42f3-9cc6-2ce1af4f08f6
keywords:
- Metodo SetResourceArray Direct3D 11
- Metodo SetResourceArray Direct3D 11, interfaccia ID3DX11EffectShaderResourceVariable
- Interfaccia ID3DX11EffectShaderResourceVariable Direct3D 11, metodo SetResourceArray
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResourceArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570c461c7bb503b2a11f46a4bb1dca24dfd16201
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356094"
---
# <a name="id3dx11effectshaderresourcevariablesetresourcearray-method"></a><span data-ttu-id="3f051-106">Metodo ID3DX11EffectShaderResourceVariable:: SetResourceArray</span><span class="sxs-lookup"><span data-stu-id="3f051-106">ID3DX11EffectShaderResourceVariable::SetResourceArray method</span></span>

<span data-ttu-id="3f051-107">Impostare una matrice di risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="3f051-107">Set an array of shader resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f051-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f051-108">Syntax</span></span>


```C++
HRESULT SetResourceArray(
   ID3D11ShaderResourceView **ppResources,
   UINT                     Offset,
   UINT                     Count
);
```



## <a name="parameters"></a><span data-ttu-id="3f051-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f051-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f051-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="3f051-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="3f051-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="3f051-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="3f051-112">Indirizzo di una matrice di interfacce shader-Resource-View.</span><span class="sxs-lookup"><span data-stu-id="3f051-112">The address of an array of shader-resource-view interfaces.</span></span> <span data-ttu-id="3f051-113">Vedere [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="3f051-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="3f051-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3f051-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3f051-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f051-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3f051-116">Indice della matrice in base zero per ottenere la prima interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3f051-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="3f051-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="3f051-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3f051-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f051-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3f051-119">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="3f051-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f051-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f051-120">Return value</span></span>

<span data-ttu-id="3f051-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f051-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f051-122">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3f051-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f051-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f051-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3f051-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="3f051-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3f051-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3f051-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3f051-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3f051-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f051-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f051-127">Requirements</span></span>



| <span data-ttu-id="3f051-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f051-128">Requirement</span></span> | <span data-ttu-id="3f051-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3f051-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f051-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f051-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3f051-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f051-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3f051-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f051-132">Library</span></span><br/> | <dl> <span data-ttu-id="3f051-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="3f051-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f051-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f051-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f051-135">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="3f051-135">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

