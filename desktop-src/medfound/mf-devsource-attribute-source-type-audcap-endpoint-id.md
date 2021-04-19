---
description: Specifica l'ID endpoint per un dispositivo di acquisizione audio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325960"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a><span data-ttu-id="b0f70-103">Attributo MF \_ DEVSOURCE \_ tipo di \_ origine attributo \_ \_ AUDCAP \_ endpoint \_ ID</span><span class="sxs-lookup"><span data-stu-id="b0f70-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="b0f70-104">Specifica l'ID endpoint per un dispositivo di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="b0f70-104">Specifies the endpoint ID for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="b0f70-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b0f70-105">Data type</span></span>

<span data-ttu-id="b0f70-106">**WCHAR\***</span><span class="sxs-lookup"><span data-stu-id="b0f70-106">**WCHAR\***</span></span>

## <a name="getset"></a><span data-ttu-id="b0f70-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b0f70-107">Get/set</span></span>

<span data-ttu-id="b0f70-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="b0f70-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b0f70-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="b0f70-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f70-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0f70-110">Remarks</span></span>

<span data-ttu-id="b0f70-111">Il valore dell'attributo è un ID endpoint.</span><span class="sxs-lookup"><span data-stu-id="b0f70-111">The value of the attribute is an endpoint ID.</span></span> <span data-ttu-id="b0f70-112">Questo attributo viene usato con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0f70-112">This attribute is used with the following functions:</span></span>

-   <span data-ttu-id="b0f70-113">Può essere usato come input per le funzioni [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="b0f70-113">It can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="b0f70-114">In questo contesto, l'attributo specifica il dispositivo di acquisizione audio per la funzione.</span><span class="sxs-lookup"><span data-stu-id="b0f70-114">In this context, the attribute specifies the audio capture device for the function.</span></span> <span data-ttu-id="b0f70-115">È possibile ottenere l'ID endpoint per un determinato dispositivo chiamando il metodo [**IMMDevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) .</span><span class="sxs-lookup"><span data-stu-id="b0f70-115">You can get the endpoint ID for a given device by calling the [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method.</span></span> <span data-ttu-id="b0f70-116">Per ulteriori informazioni, vedere la documentazione principale sull'API audio.</span><span class="sxs-lookup"><span data-stu-id="b0f70-116">See the Core Audio API documentation for more information.</span></span>
-   <span data-ttu-id="b0f70-117">Quando la funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) enumera i dispositivi audio, gli oggetti attivazione restituiti contengono questo attributo.</span><span class="sxs-lookup"><span data-stu-id="b0f70-117">When the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function enumerates audio devices, the returned activation objects contain this attribute.</span></span> <span data-ttu-id="b0f70-118">L'attributo viene utilizzato internamente dall'oggetto Activation durante la creazione dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="b0f70-118">The attribute is used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="b0f70-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b0f70-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f70-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0f70-120">Requirements</span></span>



| <span data-ttu-id="b0f70-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0f70-121">Requirement</span></span> | <span data-ttu-id="b0f70-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b0f70-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f70-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0f70-123">Header</span></span><br/> | <dl> <span data-ttu-id="b0f70-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f70-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f70-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0f70-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f70-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0f70-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b0f70-127">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="b0f70-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="b0f70-128">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b0f70-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
