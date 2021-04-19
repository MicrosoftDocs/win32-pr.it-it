---
description: Specifica il nome visualizzato per un dispositivo.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: Attributo MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307972"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a><span data-ttu-id="5c705-103">\_Attributo del \_ \_ nome descrittivo dell'attributo MF DEVSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="5c705-103">MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME attribute</span></span>

<span data-ttu-id="5c705-104">Specifica il nome visualizzato per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c705-104">Specifies the display name for a device.</span></span> <span data-ttu-id="5c705-105">Il *nome visualizzato* è una stringa leggibile, adatta per la visualizzazione in un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5c705-105">The *display name* is a human-readable string, suitable for display in a user interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c705-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5c705-106">Data type</span></span>

<span data-ttu-id="5c705-107">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="5c705-107">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="5c705-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="5c705-108">Get/set</span></span>

<span data-ttu-id="5c705-109">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="5c705-109">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="5c705-110">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="5c705-110">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c705-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c705-111">Remarks</span></span>

<span data-ttu-id="5c705-112">Questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c705-112">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="5c705-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="5c705-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="5c705-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="5c705-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="5c705-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5c705-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c705-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c705-116">Requirements</span></span>



| <span data-ttu-id="5c705-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c705-117">Requirement</span></span> | <span data-ttu-id="5c705-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5c705-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c705-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c705-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c705-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5c705-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c705-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c705-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c705-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c705-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5c705-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c705-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c705-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c705-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c705-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c705-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c705-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c705-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c705-127">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="5c705-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="5c705-128">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5c705-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




