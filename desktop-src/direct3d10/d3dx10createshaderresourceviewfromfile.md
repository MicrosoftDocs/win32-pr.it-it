---
description: Creare una visualizzazione risorse shader da un file.
ms.assetid: 97aa848b-e24c-4ebd-8819-b9741ea12b60
title: Funzione D3DX10CreateShaderResourceViewFromFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb787bed64d16f7593fba1f97c96ceeaa217b4e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401979"
---
# <a name="d3dx10createshaderresourceviewfromfile-function"></a><span data-ttu-id="abbe1-103">D3DX10CreateShaderResourceViewFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="abbe1-103">D3DX10CreateShaderResourceViewFromFile function</span></span>

<span data-ttu-id="abbe1-104">Creare una visualizzazione risorse shader da un file.</span><span class="sxs-lookup"><span data-stu-id="abbe1-104">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="abbe1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abbe1-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromFile(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="abbe1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="abbe1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abbe1-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abbe1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbe1-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="abbe1-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="abbe1-109">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="abbe1-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="abbe1-110">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abbe1-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbe1-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abbe1-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abbe1-112">Nome del file che contiene la visualizzazione delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="abbe1-112">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="abbe1-113">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="abbe1-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="abbe1-114">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="abbe1-114">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="abbe1-115">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abbe1-115">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbe1-116">Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="abbe1-116">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="abbe1-117">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="abbe1-117">Optional.</span></span> <span data-ttu-id="abbe1-118">Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="abbe1-118">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="abbe1-119">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abbe1-119">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbe1-120">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="abbe1-120">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="abbe1-121">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="abbe1-121">Pointer to a thread-pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="abbe1-122">Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="abbe1-122">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="abbe1-123">*ppShaderResourceView* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="abbe1-123">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abbe1-124">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="abbe1-124">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="abbe1-125">Indirizzo di un puntatore alla visualizzazione risorse shader (vedere [**interfaccia ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="abbe1-125">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="abbe1-126">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="abbe1-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abbe1-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="abbe1-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="abbe1-128">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="abbe1-128">A pointer to the return value.</span></span> <span data-ttu-id="abbe1-129">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="abbe1-129">May be **NULL**.</span></span> <span data-ttu-id="abbe1-130">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="abbe1-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abbe1-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abbe1-131">Return value</span></span>

<span data-ttu-id="abbe1-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abbe1-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abbe1-133">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="abbe1-133">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abbe1-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="abbe1-134">Remarks</span></span>

<span data-ttu-id="abbe1-135">Per un elenco dei formati di immagine supportati, vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="abbe1-135">For a list of supported image formats, see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abbe1-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abbe1-136">Requirements</span></span>



| <span data-ttu-id="abbe1-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="abbe1-137">Requirement</span></span> | <span data-ttu-id="abbe1-138">Valore</span><span class="sxs-lookup"><span data-stu-id="abbe1-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abbe1-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abbe1-139">Header</span></span><br/>  | <dl> <span data-ttu-id="abbe1-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="abbe1-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="abbe1-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="abbe1-141">Library</span></span><br/> | <dl> <span data-ttu-id="abbe1-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abbe1-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="abbe1-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abbe1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abbe1-144">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="abbe1-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="abbe1-145">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="abbe1-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
