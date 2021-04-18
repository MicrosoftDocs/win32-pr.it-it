---
description: Ottenere informazioni su un'immagine già caricata in memoria.
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: Funzione D3DX10GetImageInfoFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322773"
---
# <a name="d3dx10getimageinfofrommemory-function"></a><span data-ttu-id="0583b-103">D3DX10GetImageInfoFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="0583b-103">D3DX10GetImageInfoFromMemory function</span></span>

<span data-ttu-id="0583b-104">Ottenere informazioni su un'immagine già caricata in memoria.</span><span class="sxs-lookup"><span data-stu-id="0583b-104">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0583b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0583b-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="0583b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0583b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0583b-107">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0583b-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0583b-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0583b-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0583b-109">Puntatore all'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="0583b-109">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="0583b-110">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0583b-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0583b-111">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0583b-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0583b-112">Dimensione dell'immagine in memoria, in byte.</span><span class="sxs-lookup"><span data-stu-id="0583b-112">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0583b-113">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0583b-113">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0583b-114">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="0583b-114">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="0583b-115">Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="0583b-115">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="0583b-116">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0583b-116">Can be **NULL**.</span></span> <span data-ttu-id="0583b-117">Vedere [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="0583b-117">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="0583b-118">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0583b-118">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0583b-119">Tipo: **[ **d3dx10 \_ Image \_ info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0583b-119">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="0583b-120">Informazioni sull'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="0583b-120">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="0583b-121">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0583b-121">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0583b-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="0583b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="0583b-123">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="0583b-123">A pointer to the return value.</span></span> <span data-ttu-id="0583b-124">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0583b-124">May be **NULL**.</span></span> <span data-ttu-id="0583b-125">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="0583b-125">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0583b-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0583b-126">Return value</span></span>

<span data-ttu-id="0583b-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0583b-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0583b-128">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0583b-128">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0583b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0583b-129">Requirements</span></span>



| <span data-ttu-id="0583b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0583b-130">Requirement</span></span> | <span data-ttu-id="0583b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="0583b-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0583b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0583b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0583b-133"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0583b-133"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0583b-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="0583b-134">Library</span></span><br/> | <dl> <span data-ttu-id="0583b-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0583b-135"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0583b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0583b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0583b-137">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="0583b-137">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
