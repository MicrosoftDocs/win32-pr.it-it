---
title: Metodo ID3DX11EffectMatrixVariable SetMatrixArray (D3dx11effect. h)
description: Impostare una matrice di matrici a virgola mobile.
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- Metodo SetMatrixArray Direct3D 11
- Metodo SetMatrixArray Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo SetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffe0f6a81e0086a9afd6da9e464f09ae577dab2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982370"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a><span data-ttu-id="ef518-106">Metodo ID3DX11EffectMatrixVariable:: SetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="ef518-106">ID3DX11EffectMatrixVariable::SetMatrixArray method</span></span>

<span data-ttu-id="ef518-107">Impostare una matrice di matrici a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="ef518-107">Set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef518-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef518-108">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="ef518-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef518-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef518-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="ef518-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="ef518-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="ef518-111">Type: **float\***</span></span>

<span data-ttu-id="ef518-112">Puntatore alla prima matrice.</span><span class="sxs-lookup"><span data-stu-id="ef518-112">A pointer to the first matrix.</span></span>

</dd> <dt>

<span data-ttu-id="ef518-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="ef518-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="ef518-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ef518-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ef518-115">Numero di elementi della matrice da ignorare dall'inizio della matrice.</span><span class="sxs-lookup"><span data-stu-id="ef518-115">The number of matrix elements to skip from the start of the array.</span></span>

</dd> <dt>

<span data-ttu-id="ef518-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="ef518-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="ef518-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ef518-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ef518-118">Numero di elementi da impostare.</span><span class="sxs-lookup"><span data-stu-id="ef518-118">The number of elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef518-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef518-119">Return value</span></span>

<span data-ttu-id="ef518-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef518-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef518-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ef518-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef518-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef518-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ef518-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="ef518-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ef518-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ef518-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ef518-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ef518-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef518-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef518-126">Requirements</span></span>



| <span data-ttu-id="ef518-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef518-127">Requirement</span></span> | <span data-ttu-id="ef518-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ef518-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef518-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef518-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ef518-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef518-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ef518-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef518-131">Library</span></span><br/> | <dl> <span data-ttu-id="ef518-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="ef518-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef518-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef518-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef518-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="ef518-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

