---
title: Metodo ID3DX11EffectVectorVariable GetFloatVectorArray (D3dx11effect. h)
description: Ottenere una matrice di vettori a quattro componenti che contengono dati a virgola mobile.
ms.assetid: 30ecbd97-c16d-4ea9-b7d9-364887f42a04
keywords:
- Metodo GetFloatVectorArray Direct3D 11
- Metodo GetFloatVectorArray Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11, metodo GetFloatVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a4c53b884c623ca3d11fb4a9a44660ce21d8a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982400"
---
# <a name="id3dx11effectvectorvariablegetfloatvectorarray-method"></a><span data-ttu-id="a1fdd-106">Metodo ID3DX11EffectVectorVariable:: GetFloatVectorArray</span><span class="sxs-lookup"><span data-stu-id="a1fdd-106">ID3DX11EffectVectorVariable::GetFloatVectorArray method</span></span>

<span data-ttu-id="a1fdd-107">Ottenere una matrice di vettori a quattro componenti che contengono dati a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="a1fdd-107">Get an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1fdd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1fdd-108">Syntax</span></span>


```C++
HRESULT GetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="a1fdd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1fdd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1fdd-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="a1fdd-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fdd-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="a1fdd-111">Type: **float\***</span></span>

<span data-ttu-id="a1fdd-112">Puntatore all'inizio dei dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="a1fdd-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="a1fdd-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="a1fdd-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fdd-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1fdd-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a1fdd-115">Deve essere impostato su 0; Questa operazione è riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="a1fdd-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a1fdd-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="a1fdd-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fdd-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1fdd-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a1fdd-118">Numero di elementi di matrice da impostare.</span><span class="sxs-lookup"><span data-stu-id="a1fdd-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1fdd-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1fdd-119">Return value</span></span>

<span data-ttu-id="a1fdd-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1fdd-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1fdd-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a1fdd-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1fdd-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1fdd-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1fdd-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="a1fdd-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a1fdd-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a1fdd-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a1fdd-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a1fdd-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1fdd-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1fdd-126">Requirements</span></span>



| <span data-ttu-id="a1fdd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1fdd-127">Requirement</span></span> | <span data-ttu-id="a1fdd-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a1fdd-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1fdd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1fdd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a1fdd-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1fdd-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a1fdd-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1fdd-131">Library</span></span><br/> | <dl> <span data-ttu-id="a1fdd-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="a1fdd-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1fdd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1fdd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1fdd-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="a1fdd-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

