---
description: Specifica il ruolo del dispositivo per un dispositivo di acquisizione audio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049716"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a><span data-ttu-id="73aed-103">\_Attributo del \_ \_ \_ \_ ruolo AUDCAP del tipo di origine dell'attributo \_ MF DEVSOURCE</span><span class="sxs-lookup"><span data-stu-id="73aed-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ROLE attribute</span></span>

<span data-ttu-id="73aed-104">Specifica il ruolo del dispositivo per un dispositivo di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="73aed-104">Specifies the device role for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="73aed-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="73aed-105">Data type</span></span>

<span data-ttu-id="73aed-106">**ERole** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73aed-106">**ERole** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="73aed-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="73aed-107">Get/set</span></span>

<span data-ttu-id="73aed-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="73aed-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="73aed-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="73aed-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="73aed-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="73aed-110">Remarks</span></span>

<span data-ttu-id="73aed-111">Il tipo di enumerazione **eRole** è documentato nella documentazione dell'API audio principale.</span><span class="sxs-lookup"><span data-stu-id="73aed-111">The **eRole** enumeration type is documented in the Core Audio API documentation.</span></span>

<span data-ttu-id="73aed-112">Il valore dell'attributo specifica un ruolo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73aed-112">The value of the attribute specifies a device role.</span></span> <span data-ttu-id="73aed-113">Questo attributo viene utilizzato con le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="73aed-113">This attribute is used with the following functions.</span></span>

<span data-ttu-id="73aed-114">Questo attributo può essere usato come input per le funzioni [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="73aed-114">This attribute can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="73aed-115">Se viene specificato l'attributo, la funzione crea un'origine multimediale che usa il dispositivo di acquisizione audio predefinito per il ruolo del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="73aed-115">If the attribute is specified, the function creates a media source that uses the default audio capture device for the specified device role.</span></span>

<span data-ttu-id="73aed-116">Questo attributo può essere usato anche come input per la funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="73aed-116">This attribute can also be used as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="73aed-117">Se viene specificato l'attributo, l'enumerazione è limitata al ruolo del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="73aed-117">If the attribute is specified, the enumeration is restricted to the specified device role.</span></span> <span data-ttu-id="73aed-118">Inoltre, ogni oggetto attivazione restituito dalla funzione **MFEnumDeviceSources** contiene questo attributo.</span><span class="sxs-lookup"><span data-stu-id="73aed-118">In addition, each activation object returned by the **MFEnumDeviceSources** function contains this attribute.</span></span> <span data-ttu-id="73aed-119">L'attributo viene quindi usato internamente dall'oggetto attivazione quando crea l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="73aed-119">The attribute is then used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="73aed-120">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="73aed-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="73aed-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73aed-121">Requirements</span></span>



| <span data-ttu-id="73aed-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="73aed-122">Requirement</span></span> | <span data-ttu-id="73aed-123">Valore</span><span class="sxs-lookup"><span data-stu-id="73aed-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73aed-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73aed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="73aed-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="73aed-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="73aed-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73aed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="73aed-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="73aed-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="73aed-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73aed-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="73aed-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73aed-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73aed-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73aed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73aed-131">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73aed-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73aed-132">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="73aed-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="73aed-133">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="73aed-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




