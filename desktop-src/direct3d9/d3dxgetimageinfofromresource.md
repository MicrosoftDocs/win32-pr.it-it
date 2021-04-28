---
description: 'Funzione D3DXGetImageInfoFromResource: recupera informazioni su una determinata immagine in una risorsa.'
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: Funzione D3DXGetImageInfoFromResource (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea324ef94ab765bad25f7d07eef07972ab94cff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114449"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="c456e-103">Funzione D3DXGetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="c456e-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="c456e-104">Recupera informazioni su una determinata immagine in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c456e-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c456e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c456e-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c456e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c456e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c456e-107">*hSrcModule* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c456e-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c456e-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c456e-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c456e-109">Modulo in cui viene caricata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c456e-109">Module where the resource is loaded.</span></span> <span data-ttu-id="c456e-110">Impostare questo parametro su **NULL** per specificare il modulo associato all'immagine usata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="c456e-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="c456e-111">*pSrcFile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c456e-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c456e-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c456e-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c456e-113">Puntatore a una stringa che specifica il nome file.</span><span class="sxs-lookup"><span data-stu-id="c456e-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="c456e-114">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c456e-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c456e-115">In caso contrario, il tipo di dati stringa viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c456e-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="c456e-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="c456e-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c456e-117">*pSrcInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c456e-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c456e-118">Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c456e-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="c456e-119">Puntatore a [**una struttura D3DXIMAGE \_ INFO**](d3dximage-info.md) da riempire con la descrizione dei dati nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="c456e-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c456e-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c456e-120">Return value</span></span>

<span data-ttu-id="c456e-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c456e-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c456e-122">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c456e-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c456e-123">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="c456e-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="c456e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c456e-124">Remarks</span></span>

<span data-ttu-id="c456e-125">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="c456e-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c456e-126">Se unicode è definito, la chiamata di funzione viene risolta in D3DXGetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="c456e-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="c456e-127">In caso contrario, la chiamata di funzione viene risolta in D3DXGetImageInfoFromResourceA perché vengono usate stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="c456e-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c456e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c456e-128">Requirements</span></span>



| <span data-ttu-id="c456e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c456e-129">Requirement</span></span> | <span data-ttu-id="c456e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c456e-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c456e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c456e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c456e-132"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="c456e-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c456e-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="c456e-133">Library</span></span><br/> | <dl> <span data-ttu-id="c456e-134"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c456e-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c456e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c456e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c456e-136">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c456e-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="c456e-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="c456e-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="c456e-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="c456e-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
