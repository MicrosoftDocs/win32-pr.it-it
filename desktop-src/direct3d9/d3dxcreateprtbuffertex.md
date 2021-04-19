---
description: Crea un buffer PRT (pre-Computed Radiance Transfer) che può essere compresso o riempito da un simulatore. Questa funzione deve essere usata per creare buffer per pixel.
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: Funzione D3DXCreatePRTBufferTex (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3e88073f85d281e164c002ba5180493f6217e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322733"
---
# <a name="d3dxcreateprtbuffertex-function"></a><span data-ttu-id="5fb41-104">D3DXCreatePRTBufferTex (funzione)</span><span class="sxs-lookup"><span data-stu-id="5fb41-104">D3DXCreatePRTBufferTex function</span></span>

<span data-ttu-id="5fb41-105">Crea un buffer PRT (pre-Computed Radiance Transfer) che può essere compresso o riempito da un simulatore.</span><span class="sxs-lookup"><span data-stu-id="5fb41-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="5fb41-106">Questa funzione deve essere usata per creare buffer per pixel.</span><span class="sxs-lookup"><span data-stu-id="5fb41-106">This function should be used to create per-pixel buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fb41-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="5fb41-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fb41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb41-109">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fb41-109">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb41-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fb41-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fb41-111">Larghezza, in pixel, della trama.</span><span class="sxs-lookup"><span data-stu-id="5fb41-111">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5fb41-112">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fb41-112">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb41-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fb41-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fb41-114">Altezza, in pixel, della trama.</span><span class="sxs-lookup"><span data-stu-id="5fb41-114">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5fb41-115">*NumCoeffs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fb41-115">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb41-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fb41-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fb41-117">Numero di coefficienti per percorso di esempio.</span><span class="sxs-lookup"><span data-stu-id="5fb41-117">Number of coefficients per sample location.</span></span> <span data-ttu-id="5fb41-118">Quando si usa il PRT sferica (SH), il numero di coefficienti deve essere Order ², dove Order è l'ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="5fb41-118">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="5fb41-119">L'ordine deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="5fb41-119">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5fb41-120">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="5fb41-120">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5fb41-121">*NumChannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fb41-121">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb41-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fb41-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fb41-123">Numero di canali dei colori da impostare nella rete.</span><span class="sxs-lookup"><span data-stu-id="5fb41-123">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="5fb41-124">Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.</span><span class="sxs-lookup"><span data-stu-id="5fb41-124">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="5fb41-125">*ppBuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5fb41-125">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb41-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5fb41-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="5fb41-127">Indirizzo di un puntatore all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) creato.</span><span class="sxs-lookup"><span data-stu-id="5fb41-127">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb41-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fb41-128">Return value</span></span>

<span data-ttu-id="5fb41-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5fb41-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5fb41-130">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5fb41-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5fb41-131">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5fb41-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fb41-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fb41-132">Remarks</span></span>

<span data-ttu-id="5fb41-133">Quando viene creato il buffer, tutti i valori vengono inizializzati su zero.</span><span class="sxs-lookup"><span data-stu-id="5fb41-133">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fb41-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fb41-134">Requirements</span></span>



| <span data-ttu-id="5fb41-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fb41-135">Requirement</span></span> | <span data-ttu-id="5fb41-136">Valore</span><span class="sxs-lookup"><span data-stu-id="5fb41-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb41-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fb41-137">Header</span></span><br/>  | <dl> <span data-ttu-id="5fb41-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fb41-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5fb41-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="5fb41-139">Library</span></span><br/> | <dl> <span data-ttu-id="5fb41-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fb41-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5fb41-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fb41-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb41-142">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="5fb41-142">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="5fb41-143">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="5fb41-143">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
