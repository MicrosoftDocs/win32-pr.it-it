---
description: Contiene il collegamento simbolico per un driver di acquisizione video.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130722"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a><span data-ttu-id="9b44c-103">Attributo MF \_ DEVSOURCE \_ tipo di \_ origine attributo \_ \_ VidCap \_ collegamento simbolico \_</span><span class="sxs-lookup"><span data-stu-id="9b44c-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute</span></span>

<span data-ttu-id="9b44c-104">Contiene il collegamento simbolico per un driver di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="9b44c-104">Contains the symbolic link for a video capture driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="9b44c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9b44c-105">Data type</span></span>

<span data-ttu-id="9b44c-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9b44c-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="9b44c-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="9b44c-107">Get/set</span></span>

<span data-ttu-id="9b44c-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="9b44c-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="9b44c-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="9b44c-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b44c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b44c-110">Remarks</span></span>

<span data-ttu-id="9b44c-111">Utilizzare questo attributo come input per la funzione [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="9b44c-111">Use this attribute as input to the [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="9b44c-112">Inoltre, questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b44c-112">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="9b44c-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="9b44c-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="9b44c-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="9b44c-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="9b44c-115">Il collegamento simbolico deve essere considerato una stringa opaca.</span><span class="sxs-lookup"><span data-stu-id="9b44c-115">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="9b44c-116">Il nome visualizzato leggibile per un dispositivo è contenuto nell'attributo del [ \_ \_ \_ \_ nome descrittivo dell'attributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) .</span><span class="sxs-lookup"><span data-stu-id="9b44c-116">The human-readable display name for a device is contained in the [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute.</span></span>

<span data-ttu-id="9b44c-117">\_ \_ \_ \_ È possibile passare l'attributo di collegamento simbolico VidCap del tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ come valore dell'argomento DevicePath della funzione [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .</span><span class="sxs-lookup"><span data-stu-id="9b44c-117">The MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute can be passed in as the value of the DevicePath argument of the [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) function.</span></span>

<span data-ttu-id="9b44c-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9b44c-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b44c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b44c-119">Requirements</span></span>



| <span data-ttu-id="9b44c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b44c-120">Requirement</span></span> | <span data-ttu-id="9b44c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9b44c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b44c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b44c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9b44c-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9b44c-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9b44c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b44c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9b44c-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b44c-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9b44c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b44c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b44c-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b44c-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b44c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b44c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b44c-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9b44c-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9b44c-130">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="9b44c-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="9b44c-131">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="9b44c-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
