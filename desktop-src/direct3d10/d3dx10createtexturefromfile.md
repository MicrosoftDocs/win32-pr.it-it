---
description: Creare una risorsa di trama da un file.
ms.assetid: 23edad1f-89bb-4b62-8c48-3be1cd0690d2
title: Funzione D3DX10CreateTextureFromFile (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27db799bfd521133a2c137556fdd7408be974854
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322938"
---
# <a name="d3dx10createtexturefromfile-function"></a><span data-ttu-id="c59e7-103">D3DX10CreateTextureFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="c59e7-103">D3DX10CreateTextureFromFile function</span></span>

<span data-ttu-id="c59e7-104">Creare una risorsa di trama da un file.</span><span class="sxs-lookup"><span data-stu-id="c59e7-104">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c59e7-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromFile(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="c59e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c59e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c59e7-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c59e7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c59e7-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="c59e7-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="c59e7-109">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c59e7-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="c59e7-110">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c59e7-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c59e7-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c59e7-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c59e7-112">Nome del file che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c59e7-112">The name of the file containing the resource.</span></span> <span data-ttu-id="c59e7-113">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c59e7-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c59e7-114">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c59e7-114">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="c59e7-115">Per un elenco dei formati di file di immagine supportati, vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="c59e7-115">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md) enumeration for a list of the supported image file formats.</span></span>

</dd> <dt>

<span data-ttu-id="c59e7-116">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c59e7-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c59e7-117">Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c59e7-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="c59e7-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c59e7-118">Optional.</span></span> <span data-ttu-id="c59e7-119">Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="c59e7-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c59e7-120">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c59e7-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c59e7-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c59e7-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="c59e7-122">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="c59e7-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="c59e7-123">Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="c59e7-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="c59e7-124">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c59e7-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c59e7-125">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="c59e7-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="c59e7-126">Indirizzo di un puntatore alla risorsa di trama (vedere [**interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="c59e7-126">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="c59e7-127">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c59e7-127">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c59e7-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c59e7-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c59e7-129">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c59e7-129">A pointer to the return value.</span></span> <span data-ttu-id="c59e7-130">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c59e7-130">May be **NULL**.</span></span> <span data-ttu-id="c59e7-131">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="c59e7-131">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c59e7-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c59e7-132">Return value</span></span>

<span data-ttu-id="c59e7-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c59e7-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c59e7-134">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c59e7-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c59e7-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="c59e7-135">Remarks</span></span>

<span data-ttu-id="c59e7-136">Per un elenco dei formati di immagine supportati, vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="c59e7-136">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c59e7-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c59e7-137">Requirements</span></span>



| <span data-ttu-id="c59e7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c59e7-138">Requirement</span></span> | <span data-ttu-id="c59e7-139">Valore</span><span class="sxs-lookup"><span data-stu-id="c59e7-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c59e7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c59e7-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c59e7-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c59e7-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c59e7-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="c59e7-142">Library</span></span><br/> | <dl> <span data-ttu-id="c59e7-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c59e7-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59e7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c59e7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59e7-145">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="c59e7-145">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="c59e7-146">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="c59e7-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
