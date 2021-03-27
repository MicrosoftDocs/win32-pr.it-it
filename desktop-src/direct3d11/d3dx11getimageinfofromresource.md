---
title: Funzione D3DX11GetImageInfoFromResource (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare le funzioni delle risorse, quindi utilizzare la libreria DirectXTex (strumenti), LoadFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Recupera le informazioni su una determinata immagine in una risorsa.
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- Funzione D3DX11GetImageInfoFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982328"
---
# <a name="d3dx11getimageinfofromresource-function"></a><span data-ttu-id="76190-106">D3DX11GetImageInfoFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="76190-106">D3DX11GetImageInfoFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="76190-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="76190-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="76190-108">Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della [risorsa](/windows/desktop/menurc/resources-functions), quindi utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LOADFROMXXXMEMORY** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="76190-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then use [DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="76190-109">Recupera le informazioni su una determinata immagine in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="76190-109">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="76190-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76190-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="76190-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="76190-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76190-112">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76190-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76190-113">Tipo: **[ **hmodule**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76190-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="76190-114">Modulo in cui viene caricata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="76190-114">Module where the resource is loaded.</span></span> <span data-ttu-id="76190-115">Impostare questo parametro su **null** per specificare il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="76190-115">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="76190-116">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76190-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76190-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76190-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="76190-118">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="76190-118">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="76190-119">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="76190-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="76190-120">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="76190-120">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="76190-121">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="76190-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="76190-122">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76190-122">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76190-123">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="76190-123">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="76190-124">Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="76190-124">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="76190-125">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="76190-125">Can be **NULL**.</span></span> <span data-ttu-id="76190-126">Vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="76190-126">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="76190-127">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76190-127">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76190-128">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="76190-128">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="76190-129">Puntatore a una \_ \_ struttura di informazioni sull'immagine D3DX11 per la compilazione con la descrizione dei dati nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="76190-129">Pointer to a D3DX11\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="76190-130">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76190-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76190-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="76190-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="76190-132">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="76190-132">A pointer to the return value.</span></span> <span data-ttu-id="76190-133">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="76190-133">May be **NULL**.</span></span> <span data-ttu-id="76190-134">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="76190-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76190-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76190-135">Return value</span></span>

<span data-ttu-id="76190-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="76190-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="76190-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="76190-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="76190-138">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="76190-138">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="76190-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="76190-139">Remarks</span></span>

<span data-ttu-id="76190-140">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="76190-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="76190-141">Se è definito Unicode, la chiamata di funzione viene risolta in **D3DX11GetImageInfoFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="76190-141">If Unicode is defined, the function call resolves to **D3DX11GetImageInfoFromResourceW**.</span></span> <span data-ttu-id="76190-142">In caso contrario, la chiamata di funzione viene risolta in **D3DX11GetImageInfoFromResourceA** perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="76190-142">Otherwise, the function call resolves to **D3DX11GetImageInfoFromResourceA** because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="76190-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76190-143">Requirements</span></span>



| <span data-ttu-id="76190-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="76190-144">Requirement</span></span> | <span data-ttu-id="76190-145">Valore</span><span class="sxs-lookup"><span data-stu-id="76190-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76190-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76190-146">Header</span></span><br/>  | <dl> <span data-ttu-id="76190-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="76190-147"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="76190-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="76190-148">Library</span></span><br/> | <dl> <span data-ttu-id="76190-149"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76190-149"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="76190-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76190-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76190-151">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="76190-151">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

