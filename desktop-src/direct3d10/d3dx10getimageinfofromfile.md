---
description: 'Funzione D3DX10GetImageInfoFromFile: recupera informazioni su un determinato file di immagine.'
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: Funzione D3DX10GetImageInfoFromFile (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3e11c4cb52176b0a144e164501f8c70d1e3678c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098334"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="e1673-103">Funzione D3DX10GetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="e1673-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="e1673-104">Recupera informazioni su un file di immagine specificato.</span><span class="sxs-lookup"><span data-stu-id="e1673-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1673-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1673-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e1673-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1673-107">*pSrcFile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e1673-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1673-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1673-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1673-109">Nome file dell'immagine su cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="e1673-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="e1673-110">Se sono definiti unicode o UNICODE, questo tipo \_ di parametro è LPCWSTR; in caso contrario, il tipo è LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e1673-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="e1673-111">*pPump* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e1673-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1673-112">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1673-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="e1673-113">Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e1673-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="e1673-114">Può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e1673-114">Can be **NULL**.</span></span> <span data-ttu-id="e1673-115">Vedere [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="e1673-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1673-116">*pSrcInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e1673-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1673-117">Tipo: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1673-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="e1673-118">Puntatore a una struttura D3DX10 IMAGE INFO da riempire con la descrizione dei \_ dati nel file di \_ origine.</span><span class="sxs-lookup"><span data-stu-id="e1673-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="e1673-119">*pHResult* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="e1673-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1673-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e1673-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e1673-121">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e1673-121">A pointer to the return value.</span></span> <span data-ttu-id="e1673-122">Può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e1673-122">May be **NULL**.</span></span> <span data-ttu-id="e1673-123">Se *pPump* non è **NULL,** *pHResult* deve essere un percorso di memoria valido fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="e1673-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1673-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1673-124">Return value</span></span>

<span data-ttu-id="e1673-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1673-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1673-126">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1673-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e1673-127">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="e1673-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="e1673-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1673-128">Remarks</span></span>

<span data-ttu-id="e1673-129">Questa funzione supporta entrambe le stringhe Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="e1673-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1673-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1673-130">Requirements</span></span>



| <span data-ttu-id="e1673-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1673-131">Requirement</span></span> | <span data-ttu-id="e1673-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e1673-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1673-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1673-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e1673-134"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="e1673-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e1673-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="e1673-135">Library</span></span><br/> | <dl> <span data-ttu-id="e1673-136"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1673-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e1673-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1673-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1673-138">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="e1673-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
