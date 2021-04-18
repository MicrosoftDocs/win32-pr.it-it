---
description: Blocca un intervallo di dati di esempio vertici o Texel e ottiene un puntatore alla posizione nella memoria del buffer.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'Metodo ID3DXPRTBuffer:: LockBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2da8cb5a6a2e036fb7b495a129a5ef29d9ff749
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323039"
---
# <a name="id3dxprtbufferlockbuffer-method"></a><span data-ttu-id="5ccbb-103">Metodo ID3DXPRTBuffer:: LockBuffer</span><span class="sxs-lookup"><span data-stu-id="5ccbb-103">ID3DXPRTBuffer::LockBuffer method</span></span>

<span data-ttu-id="5ccbb-104">Blocca un intervallo di dati di esempio vertici o Texel e ottiene un puntatore alla posizione nella memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="5ccbb-104">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ccbb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ccbb-105">Syntax</span></span>


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="5ccbb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ccbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ccbb-107">*Inizio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccbb-107">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccbb-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ccbb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ccbb-109">Indice del campione di dati vertex o Texel.</span><span class="sxs-lookup"><span data-stu-id="5ccbb-109">Index of the sample of vertex or texel data.</span></span>

</dd> <dt>

<span data-ttu-id="5ccbb-110">*NumSamples valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccbb-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccbb-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ccbb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ccbb-112">Numero di vertici (o Texel) campionati.</span><span class="sxs-lookup"><span data-stu-id="5ccbb-112">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="5ccbb-113">*ppData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ccbb-113">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccbb-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5ccbb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="5ccbb-115">Puntatore alla posizione in memoria in cui inizia l'esempio di avvio.</span><span class="sxs-lookup"><span data-stu-id="5ccbb-115">Pointer to the location in memory where the Start sample begins.</span></span> <span data-ttu-id="5ccbb-116">Il layout della memoria dei dati del buffer è il seguente:</span><span class="sxs-lookup"><span data-stu-id="5ccbb-116">The memory layout of the buffer data is:</span></span>


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ccbb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ccbb-117">Return value</span></span>

<span data-ttu-id="5ccbb-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ccbb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ccbb-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ccbb-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5ccbb-120">Se il metodo ha esito negativo, verrà restituito il valore seguente:</span><span class="sxs-lookup"><span data-stu-id="5ccbb-120">If the method fails, the following value will be returned:</span></span>

## <a name="remarks"></a><span data-ttu-id="5ccbb-121">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="5ccbb-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5ccbb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ccbb-122">Requirements</span></span>



| <span data-ttu-id="5ccbb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ccbb-123">Requirement</span></span> | <span data-ttu-id="5ccbb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5ccbb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ccbb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ccbb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5ccbb-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ccbb-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5ccbb-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ccbb-127">Library</span></span><br/> | <dl> <span data-ttu-id="5ccbb-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ccbb-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ccbb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ccbb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ccbb-130">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="5ccbb-130">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="5ccbb-131">**ID3DXPRTBuffer::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="5ccbb-131">**ID3DXPRTBuffer::GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[<span data-ttu-id="5ccbb-132">**ID3DXPRTBuffer::GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="5ccbb-132">**ID3DXPRTBuffer::GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[<span data-ttu-id="5ccbb-133">**ID3DXPRTBuffer::GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="5ccbb-133">**ID3DXPRTBuffer::GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
