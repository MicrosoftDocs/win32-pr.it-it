---
title: Metodo ID3DX11EffectVectorVariable GetIntVectorArray (D3dx11effect. h)
description: Ottenere una matrice di vettori a quattro componenti che contengono dati di tipo Integer.
ms.assetid: cabc3bb1-8b65-455a-af84-f96219f7cfb5
keywords:
- Metodo GetIntVectorArray Direct3D 11
- Metodo GetIntVectorArray Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11, metodo GetIntVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetIntVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024db61b559d74c6453c6838795d5785ca7a0eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355474"
---
# <a name="id3dx11effectvectorvariablegetintvectorarray-method"></a><span data-ttu-id="88de5-106">Metodo ID3DX11EffectVectorVariable:: GetIntVectorArray</span><span class="sxs-lookup"><span data-stu-id="88de5-106">ID3DX11EffectVectorVariable::GetIntVectorArray method</span></span>

<span data-ttu-id="88de5-107">Ottenere una matrice di vettori a quattro componenti che contengono dati di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="88de5-107">Get an array of four-component vectors that contain integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="88de5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88de5-108">Syntax</span></span>


```C++
HRESULT GetIntVectorArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="88de5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="88de5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88de5-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="88de5-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="88de5-111">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="88de5-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="88de5-112">Puntatore all'inizio dei dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="88de5-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="88de5-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="88de5-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="88de5-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="88de5-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="88de5-115">Deve essere impostato su 0; Questa operazione è riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="88de5-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="88de5-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="88de5-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="88de5-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="88de5-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="88de5-118">Numero di elementi di matrice da impostare.</span><span class="sxs-lookup"><span data-stu-id="88de5-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88de5-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88de5-119">Return value</span></span>

<span data-ttu-id="88de5-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="88de5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="88de5-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="88de5-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="88de5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="88de5-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="88de5-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="88de5-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="88de5-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="88de5-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="88de5-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="88de5-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88de5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88de5-126">Requirements</span></span>



| <span data-ttu-id="88de5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="88de5-127">Requirement</span></span> | <span data-ttu-id="88de5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="88de5-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88de5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88de5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="88de5-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="88de5-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="88de5-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="88de5-131">Library</span></span><br/> | <dl> <span data-ttu-id="88de5-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="88de5-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88de5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88de5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88de5-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="88de5-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

