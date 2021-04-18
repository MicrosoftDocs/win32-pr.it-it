---
description: Specifica se un'origine dispositivo hardware utilizza l'ora di sistema per i timestamp.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: Attributo MFT_HW_TIMESTAMP_WITH_QPC_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310220"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a><span data-ttu-id="af280-103">\_Timestamp HW \_ MFT \_ con \_ attributo \_ attributo QPC</span><span class="sxs-lookup"><span data-stu-id="af280-103">MFT\_HW\_TIMESTAMP\_WITH\_QPC\_Attribute attribute</span></span>

<span data-ttu-id="af280-104">Specifica se un'origine dispositivo hardware utilizza l'ora di sistema per i timestamp.</span><span class="sxs-lookup"><span data-stu-id="af280-104">Specifies whether a hardware device source uses the system time for time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="af280-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="af280-105">Data type</span></span>

<span data-ttu-id="af280-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="af280-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="af280-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="af280-107">Get/set</span></span>

<span data-ttu-id="af280-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="af280-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="af280-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="af280-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="af280-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="af280-110">Remarks</span></span>

<span data-ttu-id="af280-111">Se questo attributo è **true**, l'origine del dispositivo usa l'ora di sistema, come restituito da **QueryPerformanceCounter**, per gli indicatori di data e ora.</span><span class="sxs-lookup"><span data-stu-id="af280-111">If this attribute is **TRUE**, the device source uses the system time, as returned by the **QueryPerformanceCounter**, for time stamps.</span></span> <span data-ttu-id="af280-112">In caso contrario, l'origine del dispositivo usa il clock del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af280-112">Otherwise, the device source uses the device's clock.</span></span> <span data-ttu-id="af280-113">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="af280-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="af280-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="af280-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="af280-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af280-115">Requirements</span></span>



| <span data-ttu-id="af280-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af280-116">Requirement</span></span> | <span data-ttu-id="af280-117">Valore</span><span class="sxs-lookup"><span data-stu-id="af280-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af280-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af280-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af280-119">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="af280-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="af280-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af280-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af280-121">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="af280-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="af280-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af280-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af280-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="af280-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af280-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af280-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af280-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af280-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="af280-126">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="af280-126">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




