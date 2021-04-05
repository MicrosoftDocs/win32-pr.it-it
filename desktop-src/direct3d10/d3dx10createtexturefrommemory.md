---
description: Creare una risorsa di trama da un file che risiede nella memoria di sistema.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: Funzione D3DX10CreateTextureFromMemory (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 885f734cd9caeaccbab27b2fcdb258c032c5d7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969330"
---
# <a name="d3dx10createtexturefrommemory-function"></a><span data-ttu-id="e38cc-103">D3DX10CreateTextureFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="e38cc-103">D3DX10CreateTextureFromMemory function</span></span>

<span data-ttu-id="e38cc-104">Creare una risorsa di trama da un file che risiede nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="e38cc-104">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e38cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e38cc-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e38cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e38cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e38cc-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e38cc-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e38cc-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="e38cc-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="e38cc-109">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e38cc-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e38cc-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e38cc-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e38cc-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e38cc-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e38cc-112">Puntatore alla risorsa nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="e38cc-112">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="e38cc-113">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e38cc-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e38cc-114">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e38cc-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e38cc-115">Dimensioni della risorsa nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="e38cc-115">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="e38cc-116">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e38cc-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e38cc-117">Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e38cc-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="e38cc-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e38cc-118">Optional.</span></span> <span data-ttu-id="e38cc-119">Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="e38cc-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e38cc-120">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e38cc-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e38cc-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e38cc-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="e38cc-122">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="e38cc-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="e38cc-123">Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="e38cc-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="e38cc-124">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e38cc-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e38cc-125">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="e38cc-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="e38cc-126">Indirizzo di un puntatore alla risorsa creata.</span><span class="sxs-lookup"><span data-stu-id="e38cc-126">Address of a pointer to the created resource.</span></span> <span data-ttu-id="e38cc-127">Vedere [**interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="e38cc-127">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="e38cc-128">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e38cc-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e38cc-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e38cc-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e38cc-130">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e38cc-130">A pointer to the return value.</span></span> <span data-ttu-id="e38cc-131">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e38cc-131">May be **NULL**.</span></span> <span data-ttu-id="e38cc-132">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="e38cc-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e38cc-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e38cc-133">Return value</span></span>

<span data-ttu-id="e38cc-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e38cc-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e38cc-135">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e38cc-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e38cc-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="e38cc-136">Remarks</span></span>

<span data-ttu-id="e38cc-137">Per un elenco dei formati di immagine supportati, vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="e38cc-137">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e38cc-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e38cc-138">Requirements</span></span>



| <span data-ttu-id="e38cc-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e38cc-139">Requirement</span></span> | <span data-ttu-id="e38cc-140">Valore</span><span class="sxs-lookup"><span data-stu-id="e38cc-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e38cc-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e38cc-141">Header</span></span><br/>  | <dl> <span data-ttu-id="e38cc-142"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e38cc-142"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e38cc-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="e38cc-143">Library</span></span><br/> | <dl> <span data-ttu-id="e38cc-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e38cc-144"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e38cc-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e38cc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e38cc-146">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="e38cc-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="e38cc-147">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="e38cc-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
