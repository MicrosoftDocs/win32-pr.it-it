---
title: Metodo ID3DX11EffectMatrixVariable SetMatrixTransposeArray (D3dx11effect. h)
description: Trasponi e imposta una matrice di matrici a virgola mobile.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- Metodo SetMatrixTransposeArray Direct3D 11
- Metodo SetMatrixTransposeArray Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo SetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969466"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a><span data-ttu-id="c6c85-106">Metodo ID3DX11EffectMatrixVariable:: SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="c6c85-106">ID3DX11EffectMatrixVariable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="c6c85-107">Trasponi e imposta una matrice di matrici a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="c6c85-107">Transpose and set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c85-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6c85-108">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="c6c85-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6c85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c85-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="c6c85-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c85-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="c6c85-111">Type: **float\***</span></span>

<span data-ttu-id="c6c85-112">Puntatore a una matrice di matrici.</span><span class="sxs-lookup"><span data-stu-id="c6c85-112">A pointer to an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="c6c85-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="c6c85-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c85-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6c85-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6c85-115">Offset (in numero di matrici) tra l'inizio della matrice e la prima matrice da impostare.</span><span class="sxs-lookup"><span data-stu-id="c6c85-115">The offset (in number of matrices) between the start of the array and the first matrix to set.</span></span>

</dd> <dt>

<span data-ttu-id="c6c85-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="c6c85-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c85-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6c85-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6c85-118">Numero di matrici nella matrice da impostare.</span><span class="sxs-lookup"><span data-stu-id="c6c85-118">The number of matrices in the array to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c85-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6c85-119">Return value</span></span>

<span data-ttu-id="c6c85-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c6c85-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c6c85-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c6c85-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c85-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6c85-122">Remarks</span></span>

<span data-ttu-id="c6c85-123">Se si traspone una matrice, l'ordine dei dati viene riorganizzato dall'ordine delle colonne di riga a quello delle righe di colonna (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="c6c85-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="c6c85-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c6c85-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c6c85-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c6c85-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c6c85-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c6c85-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6c85-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6c85-127">Requirements</span></span>



| <span data-ttu-id="c6c85-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c85-128">Requirement</span></span> | <span data-ttu-id="c6c85-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c6c85-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c85-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6c85-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c6c85-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c85-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c6c85-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6c85-132">Library</span></span><br/> | <dl> <span data-ttu-id="c6c85-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c6c85-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c85-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6c85-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c85-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="c6c85-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

