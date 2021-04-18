---
description: Funzione proxy per il metodo CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: Funzione IWICImagingFactory_CreateDecoderFromFilename_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319121"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a><span data-ttu-id="70b97-103">IWICImagingFactory \_ CreateDecoderFromFilename- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="70b97-103">IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function</span></span>

<span data-ttu-id="70b97-104">Funzione proxy per il metodo [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="70b97-104">Proxy function for the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70b97-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="70b97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="70b97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70b97-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b97-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b97-108">Tipo: \**IWICImagingFactory \** _</span><span class="sxs-lookup"><span data-stu-id="70b97-108">Type: \**IWICImagingFactory \** _</span></span>

</dd> <dt>

<span data-ttu-id="70b97-109">_wzFilename \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b97-109">_wzFilename\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b97-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="70b97-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="70b97-111">Puntatore a una stringa con terminazione null che specifica il nome di un oggetto da creare o aprire.</span><span class="sxs-lookup"><span data-stu-id="70b97-111">A pointer to a null-terminated string that specifies the name of an object to create or open.</span></span>

</dd> <dt>

<span data-ttu-id="70b97-112">*pguidVendor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b97-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b97-113">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="70b97-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="70b97-114">GUID del fornitore per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="70b97-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="70b97-115">_dwDesiredAccess \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b97-115">_dwDesiredAccess\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b97-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="70b97-116">Type: **DWORD**</span></span>

<span data-ttu-id="70b97-117">Accesso all'oggetto, che può essere letto, scritto o entrambi.</span><span class="sxs-lookup"><span data-stu-id="70b97-117">The access to the object, which can be read, write, or both.</span></span>

<span data-ttu-id="70b97-118">Per ulteriori informazioni, vedere file di [sicurezza e accesso \[ \] ai file](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="70b97-118">For more information, see [File Security and Access Rights \[Files\]](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b97-119">*metadataOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b97-119">*metadataOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b97-120">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="70b97-120">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="70b97-121">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) da utilizzare durante la creazione del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="70b97-121">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="70b97-122">*ppIDecoder* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="70b97-122">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70b97-123">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="70b97-123">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="70b97-124">Puntatore che riceve un puntatore al nuovo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="70b97-124">A pointer that receives a pointer to the new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70b97-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70b97-125">Return value</span></span>

<span data-ttu-id="70b97-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="70b97-126">Type: **HRESULT**</span></span>

<span data-ttu-id="70b97-127">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="70b97-127">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70b97-128">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70b97-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="70b97-129">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="70b97-129">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="70b97-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70b97-130">Requirements</span></span>



| <span data-ttu-id="70b97-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="70b97-131">Requirement</span></span> | <span data-ttu-id="70b97-132">Valore</span><span class="sxs-lookup"><span data-stu-id="70b97-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b97-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70b97-133">Minimum supported client</span></span><br/> | <span data-ttu-id="70b97-134">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70b97-134">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="70b97-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70b97-135">Minimum supported server</span></span><br/> | <span data-ttu-id="70b97-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70b97-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="70b97-137">DLL</span><span class="sxs-lookup"><span data-stu-id="70b97-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b97-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70b97-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

