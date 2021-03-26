---
title: Metodo ID3DX11EffectStringVariable GetStringArray (D3dx11effect. h)
description: Ottiene una matrice di stringhe.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- Metodo GetStringArray Direct3D 11
- Metodo GetStringArray Direct3D 11, interfaccia ID3DX11EffectStringVariable
- Interfaccia ID3DX11EffectStringVariable Direct3D 11, Metodo GetStringArray
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982139"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a><span data-ttu-id="24b70-106">Metodo ID3DX11EffectStringVariable:: GetStringArray</span><span class="sxs-lookup"><span data-stu-id="24b70-106">ID3DX11EffectStringVariable::GetStringArray method</span></span>

<span data-ttu-id="24b70-107">Ottiene una matrice di stringhe.</span><span class="sxs-lookup"><span data-stu-id="24b70-107">Get an array of strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b70-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24b70-108">Syntax</span></span>


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a><span data-ttu-id="24b70-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="24b70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b70-110">*ppStrings*</span><span class="sxs-lookup"><span data-stu-id="24b70-110">*ppStrings*</span></span> 
</dt> <dd>

<span data-ttu-id="24b70-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="24b70-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="24b70-112">Puntatore alla prima stringa nella matrice.</span><span class="sxs-lookup"><span data-stu-id="24b70-112">A pointer to the first string in the array.</span></span>

</dd> <dt>

<span data-ttu-id="24b70-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="24b70-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="24b70-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="24b70-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="24b70-115">Offset (in numero di stringhe) tra l'inizio della matrice e la prima stringa da ottenere.</span><span class="sxs-lookup"><span data-stu-id="24b70-115">The offset (in number of strings) between the start of the array and the first string to get.</span></span>

</dd> <dt>

<span data-ttu-id="24b70-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="24b70-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="24b70-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="24b70-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="24b70-118">Numero di stringhe nella matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="24b70-118">The number of strings in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24b70-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24b70-119">Return value</span></span>

<span data-ttu-id="24b70-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24b70-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24b70-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="24b70-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="24b70-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="24b70-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24b70-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="24b70-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="24b70-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="24b70-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="24b70-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="24b70-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24b70-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24b70-126">Requirements</span></span>



| <span data-ttu-id="24b70-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b70-127">Requirement</span></span> | <span data-ttu-id="24b70-128">Valore</span><span class="sxs-lookup"><span data-stu-id="24b70-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b70-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24b70-129">Header</span></span><br/>  | <dl> <span data-ttu-id="24b70-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="24b70-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="24b70-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="24b70-131">Library</span></span><br/> | <dl> <span data-ttu-id="24b70-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="24b70-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b70-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24b70-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b70-134">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="24b70-134">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

