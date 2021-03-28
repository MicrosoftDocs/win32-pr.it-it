---
title: Metodo ID3DX11EffectMatrixVariable SetMatrixTranspose (D3dx11effect. h)
description: Trasponi e imposta una matrice a virgola mobile.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Metodo SetMatrixTranspose Direct3D 11
- Metodo SetMatrixTranspose Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo SetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982259"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a><span data-ttu-id="df40c-106">Metodo ID3DX11EffectMatrixVariable:: SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="df40c-106">ID3DX11EffectMatrixVariable::SetMatrixTranspose method</span></span>

<span data-ttu-id="df40c-107">Trasponi e imposta una matrice a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="df40c-107">Transpose and set a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="df40c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df40c-108">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="df40c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="df40c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df40c-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="df40c-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="df40c-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="df40c-111">Type: **float\***</span></span>

<span data-ttu-id="df40c-112">Puntatore al primo elemento di una matrice.</span><span class="sxs-lookup"><span data-stu-id="df40c-112">A pointer to the first element of a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df40c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df40c-113">Return value</span></span>

<span data-ttu-id="df40c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df40c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df40c-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="df40c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df40c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="df40c-116">Remarks</span></span>

<span data-ttu-id="df40c-117">Se si traspone una matrice, l'ordine dei dati viene riorganizzato dall'ordine delle colonne di riga a quello delle righe di colonna (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="df40c-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="df40c-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="df40c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="df40c-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="df40c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="df40c-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="df40c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df40c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df40c-121">Requirements</span></span>



| <span data-ttu-id="df40c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df40c-122">Requirement</span></span> | <span data-ttu-id="df40c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="df40c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df40c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df40c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="df40c-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="df40c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="df40c-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="df40c-126">Library</span></span><br/> | <dl> <span data-ttu-id="df40c-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="df40c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df40c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df40c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df40c-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="df40c-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





