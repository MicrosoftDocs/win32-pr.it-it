---
description: Funzione proxy per il metodo CreateFastMetadataEncoderFromDecoder.
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: Funzione IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cdeb682139feb03c19cd66e999b6e3b8b7b366d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312981"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a><span data-ttu-id="2f705-103">IWICImagingFactory \_ CreateFastMetadataEncoderFromDecoder- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="2f705-103">IWICImagingFactory\_CreateFastMetadataEncoderFromDecoder\_Proxy function</span></span>

<span data-ttu-id="2f705-104">Funzione proxy per il metodo [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) .</span><span class="sxs-lookup"><span data-stu-id="2f705-104">Proxy function for the [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f705-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f705-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="2f705-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f705-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f705-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f705-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f705-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="2f705-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="2f705-109">_pIDecoder \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f705-109">_pIDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f705-110">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="2f705-110">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="2f705-111">Decodificatore da cui creare il [_ *IWICFastMetadataEncoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="2f705-111">The decoder to create the [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="2f705-112">*ppIFME* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f705-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f705-113">Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="2f705-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="2f705-114">Puntatore che riceve un puntatore al nuovo [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="2f705-114">A pointer that receives a pointer to the new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f705-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f705-115">Return value</span></span>

<span data-ttu-id="2f705-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f705-116">Type: **HRESULT**</span></span>

<span data-ttu-id="2f705-117">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2f705-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f705-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f705-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f705-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="2f705-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2f705-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f705-120">Requirements</span></span>



| <span data-ttu-id="2f705-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f705-121">Requirement</span></span> | <span data-ttu-id="2f705-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2f705-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f705-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f705-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2f705-124">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f705-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2f705-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f705-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2f705-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f705-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2f705-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2f705-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f705-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f705-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




