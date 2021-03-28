---
title: Metodo ID3DX11EffectPass GetDomainShaderDesc (D3dx11effect. h)
description: Ottenere una descrizione dello shader di dominio.
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- Metodo GetDomainShaderDesc Direct3D 11
- Metodo GetDomainShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo GetDomainShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2157134d97332fc9c76267f5e0db49d2c40e96a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982433"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a><span data-ttu-id="496a6-106">Metodo ID3DX11EffectPass:: GetDomainShaderDesc</span><span class="sxs-lookup"><span data-stu-id="496a6-106">ID3DX11EffectPass::GetDomainShaderDesc method</span></span>

<span data-ttu-id="496a6-107">Ottenere una descrizione dello shader di dominio.</span><span class="sxs-lookup"><span data-stu-id="496a6-107">Get a domain-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="496a6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="496a6-108">Syntax</span></span>


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="496a6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="496a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="496a6-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="496a6-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="496a6-111">Tipo: **[ **D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="496a6-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="496a6-112">Puntatore a una descrizione di Domain shader (vedere [**D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="496a6-112">A pointer to a domain-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="496a6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="496a6-113">Return value</span></span>

<span data-ttu-id="496a6-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="496a6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="496a6-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="496a6-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="496a6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="496a6-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="496a6-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="496a6-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="496a6-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="496a6-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="496a6-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="496a6-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="496a6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="496a6-120">Requirements</span></span>



| <span data-ttu-id="496a6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="496a6-121">Requirement</span></span> | <span data-ttu-id="496a6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="496a6-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="496a6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="496a6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="496a6-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="496a6-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="496a6-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="496a6-125">Library</span></span><br/> | <dl> <span data-ttu-id="496a6-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="496a6-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="496a6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="496a6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496a6-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="496a6-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





