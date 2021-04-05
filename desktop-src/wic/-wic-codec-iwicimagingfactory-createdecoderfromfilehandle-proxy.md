---
description: Funzione proxy per il metodo CreateDecoderFromFileHandle.
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: Funzione IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967696"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a><span data-ttu-id="c8731-103">IWICImagingFactory \_ CreateDecoderFromFileHandle- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="c8731-103">IWICImagingFactory\_CreateDecoderFromFileHandle\_Proxy function</span></span>

<span data-ttu-id="c8731-104">Funzione proxy per il metodo [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) .</span><span class="sxs-lookup"><span data-stu-id="c8731-104">Proxy function for the [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8731-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8731-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="c8731-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8731-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8731-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8731-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8731-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="c8731-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="c8731-109">_hFile \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8731-109">_hFile\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8731-110">Tipo: **ULONG \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="c8731-110">Type: **ULONG\_PTR**</span></span>

<span data-ttu-id="c8731-111">Handle di file da cui creare il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="c8731-111">The file handle to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="c8731-112">*pguidVendor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8731-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8731-113">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="c8731-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="c8731-114">GUID del fornitore per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="c8731-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="c8731-115">_metadataOptions \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8731-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8731-116">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="c8731-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="c8731-117">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) da utilizzare durante la creazione del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="c8731-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="c8731-118">*ppIDecoder* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8731-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8731-119">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="c8731-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="c8731-120">Puntatore che riceve un puntatore a un nuovo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="c8731-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8731-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8731-121">Return value</span></span>

<span data-ttu-id="c8731-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c8731-122">Type: **HRESULT**</span></span>

<span data-ttu-id="c8731-123">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c8731-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8731-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8731-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8731-125">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c8731-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c8731-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8731-126">Requirements</span></span>



| <span data-ttu-id="c8731-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8731-127">Requirement</span></span> | <span data-ttu-id="c8731-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c8731-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8731-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8731-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c8731-130">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8731-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c8731-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8731-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c8731-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c8731-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c8731-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c8731-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8731-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8731-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




