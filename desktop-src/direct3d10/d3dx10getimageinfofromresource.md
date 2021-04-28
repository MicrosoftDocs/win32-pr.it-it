---
description: 'Funzione D3DX10GetImageInfoFromResource: recupera informazioni su una determinata immagine in una risorsa.'
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: Funzione D3DX10GetImageInfoFromResource (D3DX10Tex.h)
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
ms.openlocfilehash: 650d05f379be634bfdd9dfb0908153260f795b00
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098369"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="716a3-103">Funzione D3DX10GetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="716a3-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="716a3-104">Recupera informazioni su una determinata immagine in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="716a3-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="716a3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="716a3-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="716a3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="716a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="716a3-107">*hSrcModule* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="716a3-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716a3-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="716a3-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="716a3-109">Modulo in cui viene caricata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="716a3-109">Module where the resource is loaded.</span></span> <span data-ttu-id="716a3-110">Impostare questo parametro su **NULL** per specificare il modulo associato all'immagine usata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="716a3-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="716a3-111">*pSrcResource* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="716a3-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716a3-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="716a3-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="716a3-113">Puntatore a una stringa che specifica il nome file.</span><span class="sxs-lookup"><span data-stu-id="716a3-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="716a3-114">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="716a3-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="716a3-115">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="716a3-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="716a3-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="716a3-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="716a3-117">*pPump* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="716a3-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716a3-118">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="716a3-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="716a3-119">Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="716a3-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="716a3-120">Può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="716a3-120">Can be **NULL**.</span></span> <span data-ttu-id="716a3-121">Vedere [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="716a3-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="716a3-122">*pSrcInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="716a3-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716a3-123">Tipo: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="716a3-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="716a3-124">Puntatore a una struttura IMAGE INFO D3DX10 da riempire con la descrizione dei \_ dati nel file di \_ origine.</span><span class="sxs-lookup"><span data-stu-id="716a3-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="716a3-125">*pHResult* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="716a3-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="716a3-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="716a3-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="716a3-127">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="716a3-127">A pointer to the return value.</span></span> <span data-ttu-id="716a3-128">Può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="716a3-128">May be **NULL**.</span></span> <span data-ttu-id="716a3-129">Se *pPump* non è **NULL,** *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="716a3-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="716a3-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="716a3-130">Return value</span></span>

<span data-ttu-id="716a3-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="716a3-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="716a3-132">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="716a3-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="716a3-133">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="716a3-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="716a3-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="716a3-134">Remarks</span></span>

<span data-ttu-id="716a3-135">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="716a3-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="716a3-136">Se unicode è definito, la chiamata di funzione viene risolta in D3DX10GetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="716a3-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="716a3-137">In caso contrario, la chiamata di funzione viene risolta in D3DX10GetImageInfoFromResourceA perché vengono usate stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="716a3-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="716a3-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="716a3-138">Requirements</span></span>



| <span data-ttu-id="716a3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="716a3-139">Requirement</span></span> | <span data-ttu-id="716a3-140">Valore</span><span class="sxs-lookup"><span data-stu-id="716a3-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="716a3-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="716a3-141">Header</span></span><br/>  | <dl> <span data-ttu-id="716a3-142"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="716a3-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="716a3-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="716a3-143">Library</span></span><br/> | <dl> <span data-ttu-id="716a3-144"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="716a3-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="716a3-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="716a3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716a3-146">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="716a3-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
