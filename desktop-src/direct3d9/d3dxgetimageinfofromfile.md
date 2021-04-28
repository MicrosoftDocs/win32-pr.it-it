---
description: 'Funzione D3DXGetImageInfoFromFile: recupera informazioni su un determinato file di immagine.'
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: Funzione D3DXGetImageInfoFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb03b6482d140a3b78e43d8b99c60499ae6c8b16
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114495"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="a93be-103">Funzione D3DXGetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="a93be-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="a93be-104">Recupera informazioni su un determinato file di immagine.</span><span class="sxs-lookup"><span data-stu-id="a93be-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93be-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a93be-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a93be-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a93be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a93be-107">*pSrcFile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a93be-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a93be-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a93be-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a93be-109">Nome file dell'immagine su cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="a93be-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="a93be-110">Se sono definiti \_ unicode o UNICODE, questo tipo di parametro è LPCWSTR. In caso contrario, il tipo è LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a93be-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="a93be-111">*pSrcInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a93be-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a93be-112">Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a93be-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="a93be-113">Puntatore a [**una struttura D3DXIMAGE \_ INFO**](d3dximage-info.md) da riempire con la descrizione dei dati nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="a93be-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a93be-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a93be-114">Return value</span></span>

<span data-ttu-id="a93be-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a93be-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a93be-116">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a93be-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a93be-117">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="a93be-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="a93be-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a93be-118">Remarks</span></span>

<span data-ttu-id="a93be-119">Questa funzione supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="a93be-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="a93be-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a93be-120">Requirements</span></span>



| <span data-ttu-id="a93be-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a93be-121">Requirement</span></span> | <span data-ttu-id="a93be-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a93be-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a93be-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a93be-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a93be-124"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="a93be-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a93be-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a93be-125">Library</span></span><br/> | <dl> <span data-ttu-id="a93be-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a93be-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a93be-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a93be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93be-128">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a93be-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="a93be-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="a93be-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="a93be-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="a93be-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
