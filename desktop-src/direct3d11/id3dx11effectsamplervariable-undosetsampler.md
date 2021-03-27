---
title: Metodo ID3DX11EffectSamplerVariable UndoSetSampler (D3dx11effect. h)
description: Ripristinare uno stato del campionatore impostato in precedenza.
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- Metodo UndoSetSampler Direct3D 11
- Metodo UndoSetSampler Direct3D 11, interfaccia ID3DX11EffectSamplerVariable
- Interfaccia ID3DX11EffectSamplerVariable Direct3D 11, metodo UndoSetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e89d72130e92a477b3824f8e5f8fc935e99bd5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355759"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a><span data-ttu-id="5a911-106">Metodo ID3DX11EffectSamplerVariable:: UndoSetSampler</span><span class="sxs-lookup"><span data-stu-id="5a911-106">ID3DX11EffectSamplerVariable::UndoSetSampler method</span></span>

<span data-ttu-id="5a911-107">Ripristinare uno stato del campionatore impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5a911-107">Revert a previously set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a911-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a911-108">Syntax</span></span>


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="5a911-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a911-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a911-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="5a911-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="5a911-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5a911-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5a911-112">Indicizzare in una matrice di interfacce del campionatore.</span><span class="sxs-lookup"><span data-stu-id="5a911-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="5a911-113">Se è presente una sola interfaccia del campionatore, usare 0.</span><span class="sxs-lookup"><span data-stu-id="5a911-113">If there is only one sampler interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a911-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a911-114">Return value</span></span>

<span data-ttu-id="5a911-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a911-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a911-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5a911-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a911-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a911-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5a911-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="5a911-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5a911-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5a911-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5a911-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5a911-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a911-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a911-121">Requirements</span></span>



| <span data-ttu-id="5a911-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a911-122">Requirement</span></span> | <span data-ttu-id="5a911-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5a911-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a911-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a911-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5a911-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a911-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5a911-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a911-126">Library</span></span><br/> | <dl> <span data-ttu-id="5a911-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="5a911-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a911-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a911-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a911-129">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="5a911-129">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

