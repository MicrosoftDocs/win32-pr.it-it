---
description: Trasforma le animazioni in un set di animazioni in un formato compresso e restituisce un puntatore al buffer che archivia i dati compressi.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'Metodo ID3DXKeyframedAnimationSet:: Compress (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323530"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a><span data-ttu-id="d9944-103">Metodo ID3DXKeyframedAnimationSet:: Compress</span><span class="sxs-lookup"><span data-stu-id="d9944-103">ID3DXKeyframedAnimationSet::Compress method</span></span>

<span data-ttu-id="d9944-104">Trasforma le animazioni in un set di animazioni in un formato compresso e restituisce un puntatore al buffer che archivia i dati compressi.</span><span class="sxs-lookup"><span data-stu-id="d9944-104">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9944-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9944-105">Syntax</span></span>


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="d9944-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9944-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9944-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9944-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9944-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9944-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9944-109">Uno dei valori [**di \_ flag D3DXCOMPRESSION**](./d3dxcompression-flags.md) che definiscono la modalità di compressione utilizzata per l'archiviazione dei dati del set di animazioni compressi.</span><span class="sxs-lookup"><span data-stu-id="d9944-109">One of the [**D3DXCOMPRESSION\_FLAGS**](./d3dxcompression-flags.md) values that define the compression mode used for storing compressed animation set data.</span></span> <span data-ttu-id="d9944-110">\_Il valore predefinito di D3DXCOMPRESS è l'unico valore attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="d9944-110">D3DXCOMPRESS\_DEFAULT is the only value currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="d9944-111">*Lossiness* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9944-111">*Lossiness* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9944-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9944-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9944-113">Percentuale di perdita di compressione desiderata nell'intervallo compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="d9944-113">Desired compression loss ratio, in the range from 0 to 1.</span></span>

</dd> <dt>

<span data-ttu-id="d9944-114">*pHierarchy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9944-114">*pHierarchy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9944-115">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="d9944-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="d9944-116">Puntatore a una gerarchia del frame di trasformazione [**D3DXFRAME**](d3dxframe.md) .</span><span class="sxs-lookup"><span data-stu-id="d9944-116">Pointer to a [**D3DXFRAME**](d3dxframe.md) transformation frame hierarchy.</span></span> <span data-ttu-id="d9944-117">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d9944-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d9944-118">*ppCompressedData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d9944-118">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9944-119">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9944-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d9944-120">Indirizzo di un puntatore al set di animazioni compresso [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d9944-120">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) compressed animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9944-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9944-121">Return value</span></span>

<span data-ttu-id="d9944-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9944-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9944-123">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9944-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d9944-124">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="d9944-124">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9944-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9944-125">Requirements</span></span>



| <span data-ttu-id="d9944-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9944-126">Requirement</span></span> | <span data-ttu-id="d9944-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d9944-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9944-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9944-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d9944-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9944-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d9944-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="d9944-130">Library</span></span><br/> | <dl> <span data-ttu-id="d9944-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9944-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9944-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9944-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9944-133">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d9944-133">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
