---
description: Recupera le informazioni su una determinata immagine in una risorsa.
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: Funzione D3DX10GetImageInfoFromResource (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e77efb973e20a5db708d28b49f0cee27bee7d4e5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234971"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="37cd4-103">D3DX10GetImageInfoFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="37cd4-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="37cd4-104">Recupera le informazioni su una determinata immagine in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="37cd4-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="37cd4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37cd4-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="37cd4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37cd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37cd4-107">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37cd4-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37cd4-108">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37cd4-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37cd4-109">Modulo in cui viene caricata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="37cd4-109">Module where the resource is loaded.</span></span> <span data-ttu-id="37cd4-110">Impostare questo parametro su **null** per specificare il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="37cd4-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="37cd4-111">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37cd4-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37cd4-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37cd4-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37cd4-113">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="37cd4-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="37cd4-114">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="37cd4-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="37cd4-115">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="37cd4-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="37cd4-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="37cd4-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="37cd4-117">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37cd4-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37cd4-118">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="37cd4-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="37cd4-119">Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="37cd4-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="37cd4-120">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="37cd4-120">Can be **NULL**.</span></span> <span data-ttu-id="37cd4-121">Vedere [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="37cd4-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="37cd4-122">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37cd4-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37cd4-123">Tipo: **[ **d3dx10 \_ Image \_ info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="37cd4-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="37cd4-124">Puntatore a una \_ \_ struttura di informazioni sull'immagine d3dx10 per la compilazione con la descrizione dei dati nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="37cd4-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="37cd4-125">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="37cd4-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37cd4-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="37cd4-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="37cd4-127">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="37cd4-127">A pointer to the return value.</span></span> <span data-ttu-id="37cd4-128">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="37cd4-128">May be **NULL**.</span></span> <span data-ttu-id="37cd4-129">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="37cd4-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37cd4-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37cd4-130">Return value</span></span>

<span data-ttu-id="37cd4-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37cd4-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37cd4-132">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="37cd4-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="37cd4-133">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="37cd4-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="37cd4-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="37cd4-134">Remarks</span></span>

<span data-ttu-id="37cd4-135">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="37cd4-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="37cd4-136">Se è definito Unicode, la chiamata di funzione viene risolta in D3DX10GetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="37cd4-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="37cd4-137">In caso contrario, la chiamata di funzione viene risolta in D3DX10GetImageInfoFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="37cd4-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="37cd4-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37cd4-138">Requirements</span></span>



| <span data-ttu-id="37cd4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="37cd4-139">Requirement</span></span> | <span data-ttu-id="37cd4-140">Valore</span><span class="sxs-lookup"><span data-stu-id="37cd4-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37cd4-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37cd4-141">Header</span></span><br/>  | <dl> <span data-ttu-id="37cd4-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="37cd4-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="37cd4-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="37cd4-143">Library</span></span><br/> | <dl> <span data-ttu-id="37cd4-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37cd4-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="37cd4-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37cd4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37cd4-146">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="37cd4-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
