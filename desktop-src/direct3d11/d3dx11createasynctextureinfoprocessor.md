---
title: Funzione D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un elaboratore di dati da utilizzare con una pompa di thread. | Funzione D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- Funzione D3DX11CreateAsyncTextureInfoProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aac60b1d496e0f1d4ecb604b18a8ef71cac8b5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996029"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a><span data-ttu-id="9b9a3-107">D3DX11CreateAsyncTextureInfoProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="9b9a3-107">D3DX11CreateAsyncTextureInfoProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="9b9a3-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9b9a3-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9b9a3-109">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9b9a3-109">See Remarks.</span></span>

 

<span data-ttu-id="9b9a3-110">Creare un elaboratore di dati da utilizzare con una [**pompa di thread**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a3-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9a3-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b9a3-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="9b9a3-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b9a3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b9a3-113">*pImageInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b9a3-113">*pImageInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9a3-114">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b9a3-114">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="9b9a3-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9b9a3-115">Optional.</span></span> <span data-ttu-id="9b9a3-116">Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ Image \_ info**](d3dx11-image-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="9b9a3-116">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a3-117">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9b9a3-117">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9a3-118">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9b9a3-118">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="9b9a3-119">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="9b9a3-119">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b9a3-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b9a3-120">Return value</span></span>

<span data-ttu-id="9b9a3-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b9a3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b9a3-122">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a3-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b9a3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b9a3-123">Remarks</span></span>

<span data-ttu-id="9b9a3-124">Questa API crea un'interfaccia di elaborazione dati. [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) crea l'interfaccia del processore dati e carica la trama.</span><span class="sxs-lookup"><span data-stu-id="9b9a3-124">This API does creates a data-processor interface; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

<span data-ttu-id="9b9a3-125">Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="9b9a3-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="9b9a3-126">Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="9b9a3-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="9b9a3-127">Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="9b9a3-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b9a3-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b9a3-128">Requirements</span></span>



| <span data-ttu-id="9b9a3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b9a3-129">Requirement</span></span> | <span data-ttu-id="9b9a3-130">Valore</span><span class="sxs-lookup"><span data-stu-id="9b9a3-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9a3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b9a3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9b9a3-132"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b9a3-132"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9b9a3-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="9b9a3-133">Library</span></span><br/> | <dl> <span data-ttu-id="9b9a3-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b9a3-134"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9b9a3-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b9a3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b9a3-136">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="9b9a3-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

