---
title: Metodo ID3DX11EffectMatrixVariable GetMatrixArray (D3dx11effect. h)
description: Ottenere una matrice di matrici.
ms.assetid: a7598687-a11c-41ad-9fb6-2c16d12f5edc
keywords:
- Metodo GetMatrixArray Direct3D 11
- Metodo GetMatrixArray Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo GetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a339bf6918868473966b6d79bcbe6b6aa3eaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969418"
---
# <a name="id3dx11effectmatrixvariablegetmatrixarray-method"></a><span data-ttu-id="02441-106">Metodo ID3DX11EffectMatrixVariable:: GetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="02441-106">ID3DX11EffectMatrixVariable::GetMatrixArray method</span></span>

<span data-ttu-id="02441-107">Ottenere una matrice di matrici.</span><span class="sxs-lookup"><span data-stu-id="02441-107">Get an array of matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="02441-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02441-108">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="02441-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="02441-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02441-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="02441-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="02441-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="02441-111">Type: **float\***</span></span>

<span data-ttu-id="02441-112">Puntatore al primo elemento della prima matrice in una matrice di matrici.</span><span class="sxs-lookup"><span data-stu-id="02441-112">A pointer to the first element of the first matrix in an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="02441-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="02441-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="02441-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="02441-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="02441-115">Offset (in numero di matrici) tra l'inizio della matrice e la prima matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="02441-115">The offset (in number of matrices) between the start of the array and the first matrix returned.</span></span>

</dd> <dt>

<span data-ttu-id="02441-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="02441-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="02441-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="02441-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="02441-118">Numero di matrici nella matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="02441-118">The number of matrices in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02441-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02441-119">Return value</span></span>

<span data-ttu-id="02441-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02441-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02441-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="02441-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02441-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="02441-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02441-123">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="02441-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="02441-124">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="02441-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="02441-125">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="02441-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02441-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02441-126">Requirements</span></span>



| <span data-ttu-id="02441-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="02441-127">Requirement</span></span> | <span data-ttu-id="02441-128">Valore</span><span class="sxs-lookup"><span data-stu-id="02441-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02441-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02441-129">Header</span></span><br/>  | <dl> <span data-ttu-id="02441-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="02441-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="02441-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="02441-131">Library</span></span><br/> | <dl> <span data-ttu-id="02441-132"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="02441-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02441-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02441-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02441-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="02441-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

