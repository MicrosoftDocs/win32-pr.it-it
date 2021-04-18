---
description: Creare una visualizzazione risorse shader da una risorsa.
ms.assetid: 207cda5f-5b7e-420a-988f-135cd2a04eb0
title: Funzione D3DX10CreateShaderResourceViewFromResource (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 12de92153b6f812b4f014f53e918e7a97000eda6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322940"
---
# <a name="d3dx10createshaderresourceviewfromresource-function"></a><span data-ttu-id="8f318-103">D3DX10CreateShaderResourceViewFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="8f318-103">D3DX10CreateShaderResourceViewFromResource function</span></span>

<span data-ttu-id="8f318-104">Creare una visualizzazione risorse shader da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="8f318-104">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f318-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f318-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromResource(
  _In_  ID3D10Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="8f318-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f318-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f318-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f318-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f318-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="8f318-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="8f318-109">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8f318-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8f318-110">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f318-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f318-111">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f318-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f318-112">Handle per il modulo della risorsa che contiene la visualizzazione delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="8f318-112">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="8f318-113">HMODULE può essere ottenuto con la [funzione GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="8f318-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="8f318-114">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f318-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f318-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f318-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f318-116">Nome della visualizzazione risorse dello shader in hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="8f318-116">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="8f318-117">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="8f318-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8f318-118">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8f318-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="8f318-119">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f318-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f318-120">Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f318-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="8f318-121">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8f318-121">Optional.</span></span> <span data-ttu-id="8f318-122">Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="8f318-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8f318-123">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f318-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f318-124">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f318-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="8f318-125">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="8f318-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="8f318-126">Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="8f318-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="8f318-127">*ppShaderResourceView* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8f318-127">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f318-128">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="8f318-128">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="8f318-129">Indirizzo di un puntatore alla visualizzazione risorse shader (vedere [**interfaccia ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="8f318-129">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="8f318-130">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8f318-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f318-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="8f318-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="8f318-132">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8f318-132">A pointer to the return value.</span></span> <span data-ttu-id="8f318-133">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8f318-133">May be **NULL**.</span></span> <span data-ttu-id="8f318-134">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="8f318-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f318-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f318-135">Return value</span></span>

<span data-ttu-id="8f318-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8f318-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8f318-137">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8f318-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f318-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f318-138">Requirements</span></span>



| <span data-ttu-id="8f318-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f318-139">Requirement</span></span> | <span data-ttu-id="8f318-140">Valore</span><span class="sxs-lookup"><span data-stu-id="8f318-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f318-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f318-141">Header</span></span><br/>  | <dl> <span data-ttu-id="8f318-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f318-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8f318-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="8f318-143">Library</span></span><br/> | <dl> <span data-ttu-id="8f318-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f318-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8f318-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f318-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f318-146">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="8f318-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="8f318-147">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="8f318-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
