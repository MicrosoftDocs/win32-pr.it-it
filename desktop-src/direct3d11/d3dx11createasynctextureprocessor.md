---
title: Funzione D3DX11CreateAsyncTextureProcessor (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un elaboratore di dati da utilizzare con una pompa di thread. | Funzione D3DX11CreateAsyncTextureProcessor (D3DX11tex. h)
ms.assetid: 4f23d265-b326-4449-b7ca-dd0596511b35
keywords:
- Funzione D3DX11CreateAsyncTextureProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612be6da4dce05ccae368edc4effea83a823dcff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996017"
---
# <a name="d3dx11createasynctextureprocessor-function"></a><span data-ttu-id="a0f64-107">D3DX11CreateAsyncTextureProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="a0f64-107">D3DX11CreateAsyncTextureProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="a0f64-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a0f64-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="a0f64-109">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a0f64-109">See Remarks.</span></span>

 

<span data-ttu-id="a0f64-110">Creare un elaboratore di dati da utilizzare con una [**pompa di thread**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="a0f64-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f64-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0f64-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="a0f64-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0f64-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f64-113">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f64-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f64-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="a0f64-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="a0f64-115">Puntatore a Devive (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span><span class="sxs-lookup"><span data-stu-id="a0f64-115">A pointer to the devive (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span></span>

</dd> <dt>

<span data-ttu-id="a0f64-116">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f64-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f64-117">Tipo: **[ **D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0f64-117">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="a0f64-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0f64-118">Optional.</span></span> <span data-ttu-id="a0f64-119">Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="a0f64-119">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a0f64-120">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a0f64-120">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f64-121">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a0f64-121">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="a0f64-122">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="a0f64-122">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f64-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0f64-123">Return value</span></span>

<span data-ttu-id="a0f64-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0f64-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0f64-125">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a0f64-125">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f64-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0f64-126">Remarks</span></span>

<span data-ttu-id="a0f64-127">Questa API crea un'interfaccia del processore dati e carica la trama; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) crea l'interfaccia del processore dati.</span><span class="sxs-lookup"><span data-stu-id="a0f64-127">This API does creates a data-processor interface and loads the texture; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

<span data-ttu-id="a0f64-128">Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="a0f64-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="a0f64-129">Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="a0f64-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="a0f64-130">Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a0f64-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f64-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0f64-131">Requirements</span></span>



| <span data-ttu-id="a0f64-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f64-132">Requirement</span></span> | <span data-ttu-id="a0f64-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a0f64-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f64-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0f64-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a0f64-135"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f64-135"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a0f64-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0f64-136">Library</span></span><br/> | <dl> <span data-ttu-id="a0f64-137"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0f64-137"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a0f64-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0f64-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f64-139">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="a0f64-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

