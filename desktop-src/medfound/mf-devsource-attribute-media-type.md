---
description: Specifica il formato di output di un dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: Attributo MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320669"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a><span data-ttu-id="8ac01-103">\_Attributo del \_ \_ tipo di supporto attributo MF DEVSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="8ac01-103">MF\_DEVSOURCE\_ATTRIBUTE\_MEDIA\_TYPE attribute</span></span>

<span data-ttu-id="8ac01-104">Specifica il formato di output di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ac01-104">Specifies the output format of a device.</span></span>

## <a name="data-type"></a><span data-ttu-id="8ac01-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8ac01-105">Data type</span></span>

<span data-ttu-id="8ac01-106">**[**MFT \_ Registra \_ \_ informazioni sul tipo**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** archiviate come **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="8ac01-106">**[**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="8ac01-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="8ac01-107">Get/set</span></span>

<span data-ttu-id="8ac01-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="8ac01-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="8ac01-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="8ac01-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac01-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ac01-110">Remarks</span></span>

<span data-ttu-id="8ac01-111">Questo attributo contiene una coppia di GUID: un tipo principale e un sottotipo.</span><span class="sxs-lookup"><span data-stu-id="8ac01-111">This attribute contains a pair of GUIDs: a major type and a subtype.</span></span> <span data-ttu-id="8ac01-112">Questi GUID descrivono il formato di output predefinito del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ac01-112">These GUIDs describe the default output format of the device.</span></span> <span data-ttu-id="8ac01-113">Il dispositivo potrebbe supportare formati di output aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="8ac01-113">The device might support additional output formats.</span></span>

<span data-ttu-id="8ac01-114">Se, ad esempio, un dispositivo di acquisizione video restituisce un video RGB-32, il valore di questo attributo è `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .</span><span class="sxs-lookup"><span data-stu-id="8ac01-114">For example, if a video capture device outputs RGB-32 video, the value of this attribute is `{ MFMediaType_Video, MFVideoFormat_RGB32 }`.</span></span>

<span data-ttu-id="8ac01-115">Questo attributo è un suggerimento per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8ac01-115">This attribute is a hint to the application.</span></span> <span data-ttu-id="8ac01-116">Per ottenere il formato di output esatto, creare l'origine multimediale per il dispositivo e ottenere il descrittore di presentazione dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="8ac01-116">To get the exact output format, create the media source for the device and get the media source's presentation descriptor.</span></span>

<span data-ttu-id="8ac01-117">Questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ac01-117">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="8ac01-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="8ac01-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="8ac01-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="8ac01-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="8ac01-120">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8ac01-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac01-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ac01-121">Requirements</span></span>



| <span data-ttu-id="8ac01-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ac01-122">Requirement</span></span> | <span data-ttu-id="8ac01-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8ac01-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac01-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ac01-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8ac01-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8ac01-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8ac01-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ac01-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8ac01-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ac01-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8ac01-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ac01-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ac01-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ac01-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac01-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ac01-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac01-131">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8ac01-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8ac01-132">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="8ac01-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="8ac01-133">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ac01-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




