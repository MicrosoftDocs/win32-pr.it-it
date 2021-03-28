---
title: Metodo ID3DX11EffectVectorVariable SetFloatVectorArray (D3dx11effect. h)
description: Impostare una matrice di vettori a quattro componenti che contengono dati a virgola mobile.
ms.assetid: f07edf0f-8a90-41bf-ae03-5a62a19e57e2
keywords:
- Metodo SetFloatVectorArray Direct3D 11
- Metodo SetFloatVectorArray Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11, metodo SetFloatVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f8f731dd90251848095f899bdc141bbc1d6748
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982394"
---
# <a name="id3dx11effectvectorvariablesetfloatvectorarray-method"></a><span data-ttu-id="7775c-106">Metodo ID3DX11EffectVectorVariable:: SetFloatVectorArray</span><span class="sxs-lookup"><span data-stu-id="7775c-106">ID3DX11EffectVectorVariable::SetFloatVectorArray method</span></span>

<span data-ttu-id="7775c-107">Impostare una matrice di vettori a quattro componenti che contengono dati a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="7775c-107">Set an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7775c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7775c-108">Syntax</span></span>


```C++
HRESULT SetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="7775c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7775c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7775c-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="7775c-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="7775c-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="7775c-111">Type: **float\***</span></span>

<span data-ttu-id="7775c-112">Puntatore all'inizio dei dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="7775c-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="7775c-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="7775c-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="7775c-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7775c-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7775c-115">Deve essere impostato su 0; Questa operazione è riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="7775c-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="7775c-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="7775c-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="7775c-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7775c-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7775c-118">Numero di elementi di matrice da impostare.</span><span class="sxs-lookup"><span data-stu-id="7775c-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7775c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7775c-119">Return value</span></span>

<span data-ttu-id="7775c-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7775c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7775c-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7775c-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7775c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="7775c-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7775c-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="7775c-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7775c-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7775c-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7775c-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7775c-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7775c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7775c-126">Requirements</span></span>



| <span data-ttu-id="7775c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7775c-127">Requirement</span></span> | <span data-ttu-id="7775c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="7775c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7775c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7775c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7775c-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7775c-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7775c-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="7775c-131">Library</span></span><br/> | <dl> <span data-ttu-id="7775c-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="7775c-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7775c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7775c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7775c-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="7775c-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

