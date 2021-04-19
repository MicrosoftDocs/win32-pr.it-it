---
description: Funzione proxy per il metodo CreateFastMetadataEncoderFromFrameDecode.
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: Funzione IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 101bb6aca30f3511a8eb370afa8eb8fd6dda1c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317897"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a><span data-ttu-id="75d8e-103">IWICImagingFactory \_ CreateFastMetadataEncoderFromFrameDecode- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="75d8e-103">IWICImagingFactory\_CreateFastMetadataEncoderFromFrameDecode\_Proxy function</span></span>

<span data-ttu-id="75d8e-104">Funzione proxy per il metodo [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) .</span><span class="sxs-lookup"><span data-stu-id="75d8e-104">Proxy function for the [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d8e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75d8e-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="75d8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75d8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d8e-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75d8e-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d8e-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="75d8e-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="75d8e-109">_pIFrameDecoder \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75d8e-109">_pIFrameDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d8e-110">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="75d8e-110">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="75d8e-111">[_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da cui creare il [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="75d8e-111">The [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) to create the [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="75d8e-112">*ppIFME* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="75d8e-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75d8e-113">Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="75d8e-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="75d8e-114">Puntatore che riceve un puntatore a un nuovo [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="75d8e-114">A pointer that receives a pointer to a new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d8e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75d8e-115">Return value</span></span>

<span data-ttu-id="75d8e-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="75d8e-116">Type: **HRESULT**</span></span>

<span data-ttu-id="75d8e-117">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="75d8e-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75d8e-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75d8e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="75d8e-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="75d8e-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="75d8e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75d8e-120">Requirements</span></span>



| <span data-ttu-id="75d8e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="75d8e-121">Requirement</span></span> | <span data-ttu-id="75d8e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="75d8e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d8e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75d8e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="75d8e-124">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75d8e-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="75d8e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75d8e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="75d8e-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75d8e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="75d8e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="75d8e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d8e-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75d8e-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




