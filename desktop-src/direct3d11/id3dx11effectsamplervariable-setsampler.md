---
title: Metodo sesampler ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Impostare lo stato del campionatore.
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- Metodo sesampler Direct3D 11
- Metodo sesampler Direct3D 11, interfaccia ID3DX11EffectSamplerVariable
- Interfaccia ID3DX11EffectSamplerVariable Direct3D 11, metodo sesampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a68adef00ac980b532e2fcd877e71eb63dc470
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355199"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a><span data-ttu-id="3d8f7-106">Metodo ID3DX11EffectSamplerVariable:: sesampler</span><span class="sxs-lookup"><span data-stu-id="3d8f7-106">ID3DX11EffectSamplerVariable::SetSampler method</span></span>

<span data-ttu-id="3d8f7-107">Impostare lo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="3d8f7-107">Set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8f7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d8f7-108">Syntax</span></span>


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a><span data-ttu-id="3d8f7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d8f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d8f7-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="3d8f7-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="3d8f7-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3d8f7-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3d8f7-112">Indicizzare in una matrice di interfacce del campionatore.</span><span class="sxs-lookup"><span data-stu-id="3d8f7-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="3d8f7-113">Se è presente una sola interfaccia del campionatore, usare 0.</span><span class="sxs-lookup"><span data-stu-id="3d8f7-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="3d8f7-114">*pSampler*</span><span class="sxs-lookup"><span data-stu-id="3d8f7-114">*pSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="3d8f7-115">Tipo: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span><span class="sxs-lookup"><span data-stu-id="3d8f7-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span></span>

<span data-ttu-id="3d8f7-116">Puntatore a un'interfaccia [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) contenente lo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="3d8f7-116">Pointer to an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) interface containing the sampler state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d8f7-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d8f7-117">Return value</span></span>

<span data-ttu-id="3d8f7-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d8f7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d8f7-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3d8f7-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8f7-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d8f7-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3d8f7-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="3d8f7-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3d8f7-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3d8f7-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3d8f7-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3d8f7-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3d8f7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d8f7-124">Requirements</span></span>



| <span data-ttu-id="3d8f7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d8f7-125">Requirement</span></span> | <span data-ttu-id="3d8f7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3d8f7-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8f7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d8f7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3d8f7-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d8f7-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3d8f7-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d8f7-129">Library</span></span><br/> | <dl> <span data-ttu-id="3d8f7-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="3d8f7-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d8f7-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d8f7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8f7-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="3d8f7-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

