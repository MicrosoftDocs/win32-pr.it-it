---
title: Funzione D3DX11CreateAsyncResourceLoader (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un caricatore di risorse asincrono.
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- Funzione D3DX11CreateAsyncResourceLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058652"
---
# <a name="d3dx11createasyncresourceloader-function"></a><span data-ttu-id="0c1b3-106">D3DX11CreateAsyncResourceLoader (funzione)</span><span class="sxs-lookup"><span data-stu-id="0c1b3-106">D3DX11CreateAsyncResourceLoader function</span></span>

> [!Note]  
> <span data-ttu-id="0c1b3-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="0c1b3-108">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-108">See Remarks.</span></span>

 

<span data-ttu-id="0c1b3-109">Creare un caricatore di risorse asincrono.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-109">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1b3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c1b3-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="0c1b3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c1b3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c1b3-112">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c1b3-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c1b3-113">Tipo: **[ **hmodule**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0c1b3-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0c1b3-114">Handle per il modulo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-114">Handle to the resource module.</span></span> <span data-ttu-id="0c1b3-115">Usare la [funzione GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per ottenere l'handle.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-115">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="0c1b3-116">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c1b3-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c1b3-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0c1b3-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0c1b3-118">Nome della risorsa in hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-118">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="0c1b3-119">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0c1b3-120">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="0c1b3-121">*ppDataLoader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0c1b3-121">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c1b3-122">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0c1b3-122">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="0c1b3-123">Indirizzo di un puntatore al caricatore di dati asincrono (vedere [**interfaccia ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="0c1b3-123">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c1b3-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c1b3-124">Return value</span></span>

<span data-ttu-id="0c1b3-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c1b3-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c1b3-126">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b3-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c1b3-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c1b3-127">Remarks</span></span>

<span data-ttu-id="0c1b3-128">Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="0c1b3-129">Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="0c1b3-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="0c1b3-130">Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="0c1b3-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1b3-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c1b3-131">Requirements</span></span>



| <span data-ttu-id="0c1b3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c1b3-132">Requirement</span></span> | <span data-ttu-id="0c1b3-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0c1b3-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1b3-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c1b3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0c1b3-135"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c1b3-135"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="0c1b3-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="0c1b3-136">Library</span></span><br/> | <dl> <span data-ttu-id="0c1b3-137"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c1b3-137"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0c1b3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c1b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1b3-139">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="0c1b3-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

