---
description: Recupera le informazioni su una determinata immagine in una risorsa.
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: Funzione D3DXGetImageInfoFromResource (D3dx9tex. h)
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
ms.openlocfilehash: 6875719123fe0b4dca4405570703b2587492975b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762041"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="71793-103">D3DXGetImageInfoFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="71793-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="71793-104">Recupera le informazioni su una determinata immagine in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="71793-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="71793-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71793-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="71793-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="71793-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71793-107">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71793-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71793-108">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71793-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71793-109">Modulo in cui viene caricata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="71793-109">Module where the resource is loaded.</span></span> <span data-ttu-id="71793-110">Impostare questo parametro su **null** per specificare il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="71793-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="71793-111">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71793-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71793-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71793-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71793-113">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="71793-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="71793-114">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="71793-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="71793-115">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="71793-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="71793-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="71793-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="71793-117">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71793-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71793-118">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="71793-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="71793-119">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) che deve essere riempita con la descrizione dei dati nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="71793-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71793-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71793-120">Return value</span></span>

<span data-ttu-id="71793-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71793-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71793-122">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="71793-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="71793-123">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="71793-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="71793-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="71793-124">Remarks</span></span>

<span data-ttu-id="71793-125">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="71793-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="71793-126">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXGetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="71793-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="71793-127">In caso contrario, la chiamata di funzione viene risolta in D3DXGetImageInfoFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="71793-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="71793-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71793-128">Requirements</span></span>



| <span data-ttu-id="71793-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="71793-129">Requirement</span></span> | <span data-ttu-id="71793-130">Valore</span><span class="sxs-lookup"><span data-stu-id="71793-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71793-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71793-131">Header</span></span><br/>  | <dl> <span data-ttu-id="71793-132"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="71793-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="71793-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="71793-133">Library</span></span><br/> | <dl> <span data-ttu-id="71793-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71793-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="71793-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71793-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71793-136">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="71793-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="71793-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="71793-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="71793-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="71793-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
