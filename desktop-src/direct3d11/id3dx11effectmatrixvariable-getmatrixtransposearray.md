---
title: Metodo ID3DX11EffectMatrixVariable GetMatrixTransposeArray (D3dx11effect. h)
description: Trasporre e ottenere una matrice di matrici a virgola mobile.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- Metodo GetMatrixTransposeArray Direct3D 11
- Metodo GetMatrixTransposeArray Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo GetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d0a43e69ccf88c15d8296c024535dec42b3f31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982262"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a><span data-ttu-id="78901-106">Metodo ID3DX11EffectMatrixVariable:: GetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="78901-106">ID3DX11EffectMatrixVariable::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="78901-107">Trasporre e ottenere una matrice di matrici a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="78901-107">Transpose and get an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="78901-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78901-108">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="78901-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="78901-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78901-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="78901-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="78901-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="78901-111">Type: **float\***</span></span>

<span data-ttu-id="78901-112">Puntatore al primo elemento di una matrice di matrici tranposed.</span><span class="sxs-lookup"><span data-stu-id="78901-112">A pointer to the first element of an array of tranposed matrices.</span></span>

</dd> <dt>

<span data-ttu-id="78901-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="78901-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="78901-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="78901-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="78901-115">Offset (in numero di matrici) tra l'inizio della matrice e la prima matrice da ottenere.</span><span class="sxs-lookup"><span data-stu-id="78901-115">The offset (in number of matrices) between the start of the array and the first matrix to get.</span></span>

</dd> <dt>

<span data-ttu-id="78901-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="78901-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="78901-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="78901-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="78901-118">Numero di matrici nella matrice da ottenere.</span><span class="sxs-lookup"><span data-stu-id="78901-118">The number of matrices in the array to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78901-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78901-119">Return value</span></span>

<span data-ttu-id="78901-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78901-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78901-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="78901-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78901-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="78901-122">Remarks</span></span>

<span data-ttu-id="78901-123">Se si traspone una matrice, l'ordine dei dati viene riorganizzato dall'ordine delle colonne di riga a quello delle righe di colonna (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="78901-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="78901-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="78901-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="78901-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="78901-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="78901-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="78901-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78901-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78901-127">Requirements</span></span>



| <span data-ttu-id="78901-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="78901-128">Requirement</span></span> | <span data-ttu-id="78901-129">Valore</span><span class="sxs-lookup"><span data-stu-id="78901-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78901-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78901-130">Header</span></span><br/>  | <dl> <span data-ttu-id="78901-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="78901-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="78901-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="78901-132">Library</span></span><br/> | <dl> <span data-ttu-id="78901-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="78901-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78901-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78901-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78901-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="78901-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

