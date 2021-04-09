---
description: Funzione proxy per il metodo CreateDecoderFromStream.
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: Funzione IWICImagingFactory_CreateDecoderFromStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1f6f84c9c29d10243f1b3bcb2cad43967547eeae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760190"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a><span data-ttu-id="aa4df-103">IWICImagingFactory \_ CreateDecoderFromStream- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="aa4df-103">IWICImagingFactory\_CreateDecoderFromStream\_Proxy function</span></span>

<span data-ttu-id="aa4df-104">Funzione proxy per il metodo [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="aa4df-104">Proxy function for the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa4df-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="aa4df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa4df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa4df-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa4df-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4df-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="aa4df-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="aa4df-109">_pIStream \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa4df-109">_pIStream\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4df-110">Tipo: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="aa4df-110">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="aa4df-111">Flusso da cui creare il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="aa4df-111">The stream to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="aa4df-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa4df-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4df-113">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="aa4df-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="aa4df-114">GUID del fornitore per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="aa4df-114">The vendor GUID for the decoder .</span></span>

</dd> <dt>

<span data-ttu-id="aa4df-115">_metadataOptions \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa4df-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4df-116">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="aa4df-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="aa4df-117">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) da utilizzare durante la creazione del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="aa4df-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="aa4df-118">*ppIDecoder* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aa4df-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4df-119">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="aa4df-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="aa4df-120">Puntatore che riceve un puntatore a un nuovo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="aa4df-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa4df-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa4df-121">Return value</span></span>

<span data-ttu-id="aa4df-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aa4df-122">Type: **HRESULT**</span></span>

<span data-ttu-id="aa4df-123">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aa4df-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aa4df-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa4df-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa4df-125">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="aa4df-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="aa4df-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa4df-126">Requirements</span></span>



| <span data-ttu-id="aa4df-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4df-127">Requirement</span></span> | <span data-ttu-id="aa4df-128">Valore</span><span class="sxs-lookup"><span data-stu-id="aa4df-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4df-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa4df-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aa4df-130">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa4df-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="aa4df-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa4df-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aa4df-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa4df-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="aa4df-133">DLL</span><span class="sxs-lookup"><span data-stu-id="aa4df-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa4df-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa4df-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

