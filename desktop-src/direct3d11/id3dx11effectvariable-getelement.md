---
title: Metodo GetElement ID3DX11EffectVariable (D3dx11effect. h)
description: Ottiene un elemento di matrice.
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- Metodo GetElement Direct3D 11
- Metodo GetElement Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, Metodo GetElement
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b887bb9e4c1d40f4d3eb0d36b9a7b4d2698b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982136"
---
# <a name="id3dx11effectvariablegetelement-method"></a><span data-ttu-id="b2175-106">Metodo ID3DX11EffectVariable:: GetElement</span><span class="sxs-lookup"><span data-stu-id="b2175-106">ID3DX11EffectVariable::GetElement method</span></span>

<span data-ttu-id="b2175-107">Ottiene un elemento di matrice.</span><span class="sxs-lookup"><span data-stu-id="b2175-107">Get an array element.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2175-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2175-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="b2175-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2175-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2175-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="b2175-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="b2175-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2175-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b2175-112">Indice in base zero; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="b2175-112">A zero-based index; otherwise 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2175-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2175-113">Return value</span></span>

<span data-ttu-id="b2175-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2175-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="b2175-115">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="b2175-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2175-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2175-116">Remarks</span></span>

<span data-ttu-id="b2175-117">Se la variabile Effect è una matrice, usare questo metodo per restituire uno degli elementi.</span><span class="sxs-lookup"><span data-stu-id="b2175-117">If the effect variable is an array, use this method to return one of the elements.</span></span>

> [!Note]  
> <span data-ttu-id="b2175-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="b2175-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b2175-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="b2175-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b2175-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b2175-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2175-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2175-121">Requirements</span></span>



| <span data-ttu-id="b2175-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2175-122">Requirement</span></span> | <span data-ttu-id="b2175-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b2175-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2175-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2175-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b2175-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2175-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b2175-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2175-126">Library</span></span><br/> | <dl> <span data-ttu-id="b2175-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="b2175-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2175-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2175-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2175-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="b2175-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

