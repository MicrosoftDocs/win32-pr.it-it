---
title: Funzione D3DX11CreateAsyncShaderResourceViewProcessor (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- Funzione D3DX11CreateAsyncShaderResourceViewProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3164aac5ddaec3d61108a2cf129b76991b8f76a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996023"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="8ede4-104">D3DX11CreateAsyncShaderResourceViewProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="8ede4-104">D3DX11CreateAsyncShaderResourceViewProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="8ede4-105">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="8ede4-105">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="8ede4-106">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="8ede4-106">See Remarks.</span></span>

 

<span data-ttu-id="8ede4-107">Creare un elaboratore di dati che caricherà una risorsa e quindi crei una visualizzazione delle risorse shader.</span><span class="sxs-lookup"><span data-stu-id="8ede4-107">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="8ede4-108">I processori di dati sono un componente della funzionalità asincrona di caricamento dei dati in D3DX11 che usa le [**pompe di thread**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="8ede4-108">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses [**thread pumps**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ede4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ede4-109">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="8ede4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ede4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ede4-111">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ede4-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ede4-112">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="8ede4-112">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="8ede4-113">Puntatore al dispositivo Direct3D (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) che verrà usato per creare una risorsa e una visualizzazione delle risorse dello shader per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ede4-113">Pointer to the Direct3D device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="8ede4-114">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ede4-114">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ede4-115">Tipo: **[ **D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ede4-115">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="8ede4-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8ede4-116">Optional.</span></span> <span data-ttu-id="8ede4-117">Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="8ede4-117">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8ede4-118">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ede4-118">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ede4-119">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8ede4-119">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="8ede4-120">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="8ede4-120">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ede4-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ede4-121">Return value</span></span>

<span data-ttu-id="8ede4-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ede4-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ede4-123">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8ede4-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ede4-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ede4-124">Remarks</span></span>

<span data-ttu-id="8ede4-125">Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="8ede4-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="8ede4-126">Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="8ede4-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="8ede4-127">Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="8ede4-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ede4-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ede4-128">Requirements</span></span>



| <span data-ttu-id="8ede4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ede4-129">Requirement</span></span> | <span data-ttu-id="8ede4-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8ede4-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ede4-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ede4-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8ede4-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ede4-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="8ede4-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="8ede4-133">Library</span></span><br/> | <dl> <span data-ttu-id="8ede4-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ede4-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8ede4-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ede4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ede4-136">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="8ede4-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

