---
title: Metodo ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessViewArray (D3dx11effect. h)
description: Impostare una matrice di viste con accesso non ordinato.
ms.assetid: 12d0da06-990a-42b2-9566-cc5136f48781
keywords:
- Metodo SetUnorderedAccessViewArray Direct3D 11
- Metodo SetUnorderedAccessViewArray Direct3D 11, interfaccia ID3DX11EffectUnorderedAccessViewVariable
- Interfaccia ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, metodo SetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053856f294906cf56acf1f38ca90663ebcc34051
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995828"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessviewarray-method"></a><span data-ttu-id="fcb20-106">Metodo ID3DX11EffectUnorderedAccessViewVariable:: SetUnorderedAccessViewArray</span><span class="sxs-lookup"><span data-stu-id="fcb20-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="fcb20-107">Impostare una matrice di viste con accesso non ordinato.</span><span class="sxs-lookup"><span data-stu-id="fcb20-107">Set an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb20-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fcb20-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="fcb20-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fcb20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcb20-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="fcb20-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb20-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="fcb20-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="fcb20-112">Matrice di puntatori [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) .</span><span class="sxs-lookup"><span data-stu-id="fcb20-112">An array of [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="fcb20-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="fcb20-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb20-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fcb20-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fcb20-115">Indice della prima vista di accesso non ordinata.</span><span class="sxs-lookup"><span data-stu-id="fcb20-115">Index of the first unordered-access-view.</span></span>

</dd> <dt>

<span data-ttu-id="fcb20-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="fcb20-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb20-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fcb20-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fcb20-118">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="fcb20-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcb20-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fcb20-119">Return value</span></span>

<span data-ttu-id="fcb20-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcb20-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcb20-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fcb20-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb20-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcb20-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fcb20-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="fcb20-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fcb20-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="fcb20-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fcb20-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fcb20-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fcb20-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcb20-126">Requirements</span></span>



| <span data-ttu-id="fcb20-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcb20-127">Requirement</span></span> | <span data-ttu-id="fcb20-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fcb20-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb20-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fcb20-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fcb20-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcb20-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fcb20-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="fcb20-131">Library</span></span><br/> | <dl> <span data-ttu-id="fcb20-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="fcb20-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcb20-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcb20-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb20-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="fcb20-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

