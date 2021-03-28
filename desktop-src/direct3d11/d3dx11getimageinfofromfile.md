---
title: Funzione D3DX11GetImageInfoFromFile (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, GetMetadataFromXXXFile (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Recupera le informazioni su un file di immagine specificato.
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- Funzione D3DX11GetImageInfoFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058650"
---
# <a name="d3dx11getimageinfofromfile-function"></a><span data-ttu-id="868d4-106">D3DX11GetImageInfoFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="868d4-106">D3DX11GetImageInfoFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="868d4-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="868d4-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="868d4-108">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GETMETADATAFROMXXXFILE** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="868d4-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="868d4-109">Recupera le informazioni su un file di immagine specificato.</span><span class="sxs-lookup"><span data-stu-id="868d4-109">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="868d4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="868d4-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="868d4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="868d4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="868d4-112">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="868d4-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868d4-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868d4-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="868d4-114">Nome file dell'immagine di cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="868d4-114">File name of image to retrieve information about.</span></span> <span data-ttu-id="868d4-115">Se \_ sono definiti Unicode o Unicode, questo tipo di parametro è LPCWSTR; in caso contrario, il tipo è LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="868d4-115">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="868d4-116">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="868d4-116">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868d4-117">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="868d4-117">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="868d4-118">Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="868d4-118">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="868d4-119">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="868d4-119">Can be **NULL**.</span></span> <span data-ttu-id="868d4-120">Vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="868d4-120">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="868d4-121">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="868d4-121">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868d4-122">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="868d4-122">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="868d4-123">Puntatore a un [**oggetto \_ D3DX11 \_ informazioni sull'immagine**](d3dx11-image-info.md) da compilare con la descrizione dei dati nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="868d4-123">Pointer to a [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md) to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="868d4-124">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="868d4-124">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="868d4-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="868d4-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="868d4-126">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="868d4-126">A pointer to the return value.</span></span> <span data-ttu-id="868d4-127">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="868d4-127">May be **NULL**.</span></span> <span data-ttu-id="868d4-128">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="868d4-128">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="868d4-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="868d4-129">Return value</span></span>

<span data-ttu-id="868d4-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="868d4-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="868d4-131">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="868d4-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="868d4-132">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="868d4-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="868d4-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="868d4-133">Remarks</span></span>

<span data-ttu-id="868d4-134">Questa funzione supporta le stringhe Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="868d4-134">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="868d4-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="868d4-135">Requirements</span></span>



| <span data-ttu-id="868d4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="868d4-136">Requirement</span></span> | <span data-ttu-id="868d4-137">Valore</span><span class="sxs-lookup"><span data-stu-id="868d4-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="868d4-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="868d4-138">Header</span></span><br/>  | <dl> <span data-ttu-id="868d4-139"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="868d4-139"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="868d4-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="868d4-140">Library</span></span><br/> | <dl> <span data-ttu-id="868d4-141"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="868d4-141"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="868d4-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="868d4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868d4-143">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="868d4-143">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

