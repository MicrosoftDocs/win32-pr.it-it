---
title: Metodo ID3DX11EffectMatrixVariable GetMatrixTranspose (D3dx11effect. h)
description: Trasporre e ottenere una matrice a virgola mobile.
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- Metodo GetMatrixTranspose Direct3D 11
- Metodo GetMatrixTranspose Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo GetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa5c8eb8e424041a05461636d1eaf7b65c7cd4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058638"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a><span data-ttu-id="25228-106">Metodo ID3DX11EffectMatrixVariable:: GetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="25228-106">ID3DX11EffectMatrixVariable::GetMatrixTranspose method</span></span>

<span data-ttu-id="25228-107">Trasporre e ottenere una matrice a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="25228-107">Transpose and get a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="25228-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25228-108">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="25228-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="25228-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25228-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="25228-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="25228-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="25228-111">Type: **float\***</span></span>

<span data-ttu-id="25228-112">Puntatore al primo elemento di una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="25228-112">A pointer to the first element of a transposed matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25228-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25228-113">Return value</span></span>

<span data-ttu-id="25228-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25228-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25228-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="25228-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25228-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="25228-116">Remarks</span></span>

<span data-ttu-id="25228-117">Se si traspone una matrice, l'ordine dei dati viene riorganizzato dall'ordine delle colonne di riga a quello delle righe di colonna (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="25228-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="25228-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="25228-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="25228-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="25228-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="25228-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="25228-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25228-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25228-121">Requirements</span></span>



| <span data-ttu-id="25228-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="25228-122">Requirement</span></span> | <span data-ttu-id="25228-123">Valore</span><span class="sxs-lookup"><span data-stu-id="25228-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25228-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25228-124">Header</span></span><br/>  | <dl> <span data-ttu-id="25228-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="25228-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="25228-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="25228-126">Library</span></span><br/> | <dl> <span data-ttu-id="25228-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="25228-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25228-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25228-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25228-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="25228-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





