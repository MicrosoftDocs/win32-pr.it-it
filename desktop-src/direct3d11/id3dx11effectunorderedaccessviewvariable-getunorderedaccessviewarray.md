---
title: Metodo ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessViewArray (D3dx11effect. h)
description: Ottenere una matrice di viste con accesso non ordinato.
ms.assetid: 38f838bb-cdcb-43c2-8b98-a188f479e93d
keywords:
- Metodo GetUnorderedAccessViewArray Direct3D 11
- Metodo GetUnorderedAccessViewArray Direct3D 11, interfaccia ID3DX11EffectUnorderedAccessViewVariable
- Interfaccia ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, metodo GetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c264b5652287676d0792027f4f0ea8921bdb92f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235093"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessviewarray-method"></a><span data-ttu-id="e70ac-106">Metodo ID3DX11EffectUnorderedAccessViewVariable:: GetUnorderedAccessViewArray</span><span class="sxs-lookup"><span data-stu-id="e70ac-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="e70ac-107">Ottenere una matrice di viste con accesso non ordinato.</span><span class="sxs-lookup"><span data-stu-id="e70ac-107">Get an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70ac-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e70ac-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="e70ac-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e70ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70ac-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="e70ac-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="e70ac-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="e70ac-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="e70ac-112">Puntatore a un puntatore [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) che verrà impostato sulla matrice UAV al ritorno.</span><span class="sxs-lookup"><span data-stu-id="e70ac-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set to the UAV array on return.</span></span>

</dd> <dt>

<span data-ttu-id="e70ac-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="e70ac-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="e70ac-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e70ac-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e70ac-115">Indice della prima interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e70ac-115">Index of the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="e70ac-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="e70ac-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="e70ac-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e70ac-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e70ac-118">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="e70ac-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e70ac-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e70ac-119">Return value</span></span>

<span data-ttu-id="e70ac-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e70ac-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e70ac-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e70ac-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e70ac-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e70ac-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e70ac-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e70ac-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e70ac-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e70ac-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e70ac-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e70ac-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e70ac-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e70ac-126">Requirements</span></span>



| <span data-ttu-id="e70ac-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70ac-127">Requirement</span></span> | <span data-ttu-id="e70ac-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e70ac-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70ac-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e70ac-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e70ac-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e70ac-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e70ac-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e70ac-131">Library</span></span><br/> | <dl> <span data-ttu-id="e70ac-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e70ac-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e70ac-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e70ac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70ac-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="e70ac-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

