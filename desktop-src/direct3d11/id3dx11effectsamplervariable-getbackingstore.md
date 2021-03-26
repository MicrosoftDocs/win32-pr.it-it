---
title: Metodo ID3DX11EffectSamplerVariable GetBackingStore (D3dx11effect. h)
description: Ottiene un puntatore a una variabile che contiene lo stato del campionatore.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Direct3D 11, interfaccia ID3DX11EffectSamplerVariable
- Interfaccia ID3DX11EffectSamplerVariable Direct3D 11, metodo GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355364"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a><span data-ttu-id="fc078-106">Metodo ID3DX11EffectSamplerVariable:: GetBackingStore</span><span class="sxs-lookup"><span data-stu-id="fc078-106">ID3DX11EffectSamplerVariable::GetBackingStore method</span></span>

<span data-ttu-id="fc078-107">Ottiene un puntatore a una variabile che contiene lo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="fc078-107">Get a pointer to a variable that contains sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc078-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc078-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="fc078-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc078-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc078-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="fc078-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="fc078-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc078-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc078-112">Indicizzare in una matrice di descrizioni del campionatore.</span><span class="sxs-lookup"><span data-stu-id="fc078-112">Index into an array of sampler descriptions.</span></span> <span data-ttu-id="fc078-113">Se è presente una sola variabile del campionatore nell'effetto, usare 0.</span><span class="sxs-lookup"><span data-stu-id="fc078-113">If there is only one sampler variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="fc078-114">*pSamplerDesc*</span><span class="sxs-lookup"><span data-stu-id="fc078-114">*pSamplerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="fc078-115">Tipo: **[ **d3d11 \_ Sampler \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span><span class="sxs-lookup"><span data-stu-id="fc078-115">Type: **[**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span></span>

<span data-ttu-id="fc078-116">Puntatore a una descrizione del campionatore (vedere [**d3d11 \_ Sampler \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span><span class="sxs-lookup"><span data-stu-id="fc078-116">A pointer to a sampler description (see [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc078-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc078-117">Return value</span></span>

<span data-ttu-id="fc078-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc078-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc078-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fc078-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc078-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc078-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fc078-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="fc078-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fc078-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="fc078-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fc078-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fc078-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fc078-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc078-124">Requirements</span></span>



| <span data-ttu-id="fc078-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc078-125">Requirement</span></span> | <span data-ttu-id="fc078-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fc078-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc078-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc078-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fc078-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc078-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fc078-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc078-129">Library</span></span><br/> | <dl> <span data-ttu-id="fc078-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="fc078-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc078-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc078-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc078-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="fc078-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

