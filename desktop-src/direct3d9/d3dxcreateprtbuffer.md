---
description: Crea un buffer PRT (pre-Computed Radiance Transfer) che può essere compresso o riempito da un simulatore. Questa funzione deve essere usata per creare buffer per vertice o volume.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: Funzione D3DXCreatePRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322734"
---
# <a name="d3dxcreateprtbuffer-function"></a><span data-ttu-id="ed725-104">D3DXCreatePRTBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="ed725-104">D3DXCreatePRTBuffer function</span></span>

<span data-ttu-id="ed725-105">Crea un buffer PRT (pre-Computed Radiance Transfer) che può essere compresso o riempito da un simulatore.</span><span class="sxs-lookup"><span data-stu-id="ed725-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="ed725-106">Questa funzione deve essere usata per creare buffer per vertice o volume.</span><span class="sxs-lookup"><span data-stu-id="ed725-106">This function should be used to create per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed725-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed725-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ed725-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed725-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed725-109">*NumSamples valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed725-109">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed725-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed725-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed725-111">Numero di vertici (o Texel) campionati.</span><span class="sxs-lookup"><span data-stu-id="ed725-111">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="ed725-112">*NumCoeffs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed725-112">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed725-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed725-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed725-114">Numero di coefficienti per percorso di esempio.</span><span class="sxs-lookup"><span data-stu-id="ed725-114">Number of coefficients per sample location.</span></span> <span data-ttu-id="ed725-115">Quando si usa il PRT sferica (SH), il numero di coefficienti deve essere Order ², dove Order è l'ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="ed725-115">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="ed725-116">L'ordine deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="ed725-116">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="ed725-117">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="ed725-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="ed725-118">*NumChannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed725-118">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed725-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed725-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed725-120">Numero di canali dei colori da impostare nella rete.</span><span class="sxs-lookup"><span data-stu-id="ed725-120">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="ed725-121">Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.</span><span class="sxs-lookup"><span data-stu-id="ed725-121">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="ed725-122">*ppBuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ed725-122">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed725-123">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed725-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="ed725-124">Indirizzo di un puntatore all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) creato.</span><span class="sxs-lookup"><span data-stu-id="ed725-124">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed725-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed725-125">Return value</span></span>

<span data-ttu-id="ed725-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed725-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed725-127">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed725-127">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ed725-128">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ed725-128">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed725-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed725-129">Remarks</span></span>

<span data-ttu-id="ed725-130">Quando viene creato il buffer, tutti i valori vengono inizializzati su zero.</span><span class="sxs-lookup"><span data-stu-id="ed725-130">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed725-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed725-131">Requirements</span></span>



| <span data-ttu-id="ed725-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed725-132">Requirement</span></span> | <span data-ttu-id="ed725-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ed725-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed725-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed725-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ed725-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed725-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ed725-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed725-136">Library</span></span><br/> | <dl> <span data-ttu-id="ed725-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed725-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed725-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed725-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed725-139">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="ed725-139">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="ed725-140">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="ed725-140">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
