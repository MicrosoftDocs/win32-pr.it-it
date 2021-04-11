---
description: Crea un buffer di trasferimento di luminosità pre-calcolato (PRT) compresso da un oggetto ID3DXPRTBuffer non compresso. Questa funzione deve essere usata con i buffer per vertice o per i volumi.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Funzione D3DXCreatePRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354919"
---
# <a name="d3dxcreateprtcompbuffer-function"></a><span data-ttu-id="06008-104">D3DXCreatePRTCompBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="06008-104">D3DXCreatePRTCompBuffer function</span></span>

<span data-ttu-id="06008-105">Crea un buffer di trasferimento di luminosità pre-calcolato (PRT) compresso da un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) non compresso.</span><span class="sxs-lookup"><span data-stu-id="06008-105">Creates a compressed precomputed radiance transfer (PRT) buffer from an uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="06008-106">Questa funzione deve essere usata con i buffer per vertice o per i volumi.</span><span class="sxs-lookup"><span data-stu-id="06008-106">This function should be used with per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="06008-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06008-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="06008-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06008-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06008-109">*Qualità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06008-109">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06008-110">Tipo: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span><span class="sxs-lookup"><span data-stu-id="06008-110">Type: **[**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span></span>

<span data-ttu-id="06008-111">Qualità della compressione armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="06008-111">Quality of spherical harmonic (SH) compression.</span></span> <span data-ttu-id="06008-112">Vedere [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span><span class="sxs-lookup"><span data-stu-id="06008-112">See [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span></span>

</dd> <dt>

<span data-ttu-id="06008-113">*NumClusters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06008-113">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06008-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06008-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06008-115">Numero di cluster da utilizzare per la compressione.</span><span class="sxs-lookup"><span data-stu-id="06008-115">Number of clusters to use for compression.</span></span>

</dd> <dt>

<span data-ttu-id="06008-116">*NumPCA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06008-116">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06008-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06008-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06008-118">Numero di vettori di base dell'analisi dei componenti principali (PCA) da usare in ogni cluster.</span><span class="sxs-lookup"><span data-stu-id="06008-118">Number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span>

</dd> <dt>

<span data-ttu-id="06008-119">*pCB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06008-119">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06008-120">Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="06008-120">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="06008-121">Puntatore facoltativo alla funzione di callback [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) usata per calcolare la percentuale di calcoli di compressione PRT completati.</span><span class="sxs-lookup"><span data-stu-id="06008-121">Optional pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that is used to compute the percentage of PRT compression computations completed.</span></span> <span data-ttu-id="06008-122">La funzione di callback deve essere implementata per restituire S \_ OK per tenere in esecuzione la routine di compressione.</span><span class="sxs-lookup"><span data-stu-id="06008-122">The callback function must be implemented to return S\_OK to keep running the compression routine.</span></span> <span data-ttu-id="06008-123">Qualsiasi altro valore arresterà la compressione.</span><span class="sxs-lookup"><span data-stu-id="06008-123">Any other value will halt compression.</span></span> <span data-ttu-id="06008-124">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="06008-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="06008-125">*lpUserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06008-125">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06008-126">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06008-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06008-127">Puntatore facoltativo a un valore definito dall'utente passato alla funzione di callback [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) .</span><span class="sxs-lookup"><span data-stu-id="06008-127">Optional pointer to a user-defined value passed to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function.</span></span> <span data-ttu-id="06008-128">Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="06008-128">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span> <span data-ttu-id="06008-129">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="06008-129">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="06008-130">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06008-130">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06008-131">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="06008-131">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="06008-132">Indirizzo di un puntatore all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) non compresso che verrà compresso.</span><span class="sxs-lookup"><span data-stu-id="06008-132">Address of a pointer to the uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="06008-133">*ppBuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="06008-133">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06008-134">Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="06008-134">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="06008-135">Indirizzo di un puntatore all'oggetto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) di output.</span><span class="sxs-lookup"><span data-stu-id="06008-135">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06008-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06008-136">Return value</span></span>

<span data-ttu-id="06008-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06008-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06008-138">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06008-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06008-139">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="06008-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="06008-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06008-140">Requirements</span></span>



| <span data-ttu-id="06008-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="06008-141">Requirement</span></span> | <span data-ttu-id="06008-142">Valore</span><span class="sxs-lookup"><span data-stu-id="06008-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06008-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06008-143">Header</span></span><br/>  | <dl> <span data-ttu-id="06008-144"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="06008-144"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="06008-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="06008-145">Library</span></span><br/> | <dl> <span data-ttu-id="06008-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06008-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06008-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06008-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06008-148">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="06008-148">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="06008-149">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="06008-149">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="06008-150">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="06008-150">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
