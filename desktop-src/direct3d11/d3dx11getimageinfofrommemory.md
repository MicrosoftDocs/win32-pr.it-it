---
title: Funzione D3DX11GetImageInfoFromMemory (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, GetMetadataFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Ottenere informazioni su un'immagine già caricata in memoria.
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- Funzione D3DX11GetImageInfoFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5f1f04c9540614541b9f63b7833967d6ce959
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982325"
---
# <a name="d3dx11getimageinfofrommemory-function"></a><span data-ttu-id="6c988-106">D3DX11GetImageInfoFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="6c988-106">D3DX11GetImageInfoFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="6c988-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6c988-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="6c988-108">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GETMETADATAFROMXXXMEMORY** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="6c988-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="6c988-109">Ottenere informazioni su un'immagine già caricata in memoria.</span><span class="sxs-lookup"><span data-stu-id="6c988-109">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c988-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c988-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="6c988-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c988-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c988-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c988-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c988-113">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6c988-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6c988-114">Puntatore all'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="6c988-114">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="6c988-115">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c988-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c988-116">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6c988-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6c988-117">Dimensione dell'immagine in memoria, in byte.</span><span class="sxs-lookup"><span data-stu-id="6c988-117">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6c988-118">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c988-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c988-119">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c988-119">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="6c988-120">Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="6c988-120">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="6c988-121">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6c988-121">Can be **NULL**.</span></span> <span data-ttu-id="6c988-122">Vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="6c988-122">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c988-123">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c988-123">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c988-124">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c988-124">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="6c988-125">Informazioni sull'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="6c988-125">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="6c988-126">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c988-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c988-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="6c988-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="6c988-128">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6c988-128">A pointer to the return value.</span></span> <span data-ttu-id="6c988-129">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6c988-129">May be **NULL**.</span></span> <span data-ttu-id="6c988-130">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="6c988-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c988-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c988-131">Return value</span></span>

<span data-ttu-id="6c988-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c988-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c988-133">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6c988-133">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c988-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c988-134">Requirements</span></span>



| <span data-ttu-id="6c988-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c988-135">Requirement</span></span> | <span data-ttu-id="6c988-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6c988-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c988-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c988-137">Header</span></span><br/>  | <dl> <span data-ttu-id="6c988-138"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c988-138"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6c988-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c988-139">Library</span></span><br/> | <dl> <span data-ttu-id="6c988-140"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c988-140"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6c988-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c988-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c988-142">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="6c988-142">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

