---
description: Ricampiona un buffer ID3DXPRTBuffer di input e lo salva in un buffer di output. Questo metodo può essere utilizzato per convertire un buffer di vertice in un buffer di trama e viceversa. Può essere usato anche per convertire i buffer a canale singolo in buffer a 3 canali e viceversa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'Metodo ID3DXPRTEngine:: ResampleBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762292"
---
# <a name="id3dxprtengineresamplebuffer-method"></a><span data-ttu-id="e9dcc-105">Metodo ID3DXPRTEngine:: ResampleBuffer</span><span class="sxs-lookup"><span data-stu-id="e9dcc-105">ID3DXPRTEngine::ResampleBuffer method</span></span>

<span data-ttu-id="e9dcc-106">Ricampiona un buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input e lo salva in un buffer di output.</span><span class="sxs-lookup"><span data-stu-id="e9dcc-106">Resamples an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer and saves it to an output buffer.</span></span> <span data-ttu-id="e9dcc-107">Questo metodo può essere utilizzato per convertire un buffer di vertice in un buffer di trama e viceversa.</span><span class="sxs-lookup"><span data-stu-id="e9dcc-107">This method can be used to convert a vertex buffer to a texture buffer and vice-versa.</span></span> <span data-ttu-id="e9dcc-108">Può essere usato anche per convertire i buffer a canale singolo in buffer a 3 canali e viceversa.</span><span class="sxs-lookup"><span data-stu-id="e9dcc-108">It can also be used to convert single-channel buffers to 3-channel buffers and vice-versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9dcc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9dcc-109">Syntax</span></span>


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a><span data-ttu-id="e9dcc-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9dcc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9dcc-111">*pBufferIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9dcc-111">*pBufferIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9dcc-112">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e9dcc-112">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e9dcc-113">Puntatore al buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input.</span><span class="sxs-lookup"><span data-stu-id="e9dcc-113">Pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e9dcc-114">*pBufferOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e9dcc-114">*pBufferOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9dcc-115">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e9dcc-115">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e9dcc-116">Puntatore al buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output.</span><span class="sxs-lookup"><span data-stu-id="e9dcc-116">Pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9dcc-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9dcc-117">Return value</span></span>

<span data-ttu-id="e9dcc-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9dcc-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9dcc-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9dcc-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e9dcc-120">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e9dcc-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9dcc-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9dcc-121">Requirements</span></span>



| <span data-ttu-id="e9dcc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9dcc-122">Requirement</span></span> | <span data-ttu-id="e9dcc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e9dcc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9dcc-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9dcc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e9dcc-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9dcc-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e9dcc-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9dcc-126">Library</span></span><br/> | <dl> <span data-ttu-id="e9dcc-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9dcc-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9dcc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9dcc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9dcc-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e9dcc-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 




