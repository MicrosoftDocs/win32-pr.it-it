---
description: Contiene i flag che definiscono le funzionalità della sessione multimediale in base alla presentazione corrente.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: Attributo MF_EVENT_SESSIONCAPS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309562"
---
# <a name="mf_event_sessioncaps-attribute"></a><span data-ttu-id="a39fb-103">\_Attributo SESSIONCAPS dell'evento MF \_</span><span class="sxs-lookup"><span data-stu-id="a39fb-103">MF\_EVENT\_SESSIONCAPS attribute</span></span>

<span data-ttu-id="a39fb-104">Contiene i flag che definiscono le funzionalità della sessione multimediale in base alla presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="a39fb-104">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="a39fb-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a39fb-105">Data type</span></span>

<span data-ttu-id="a39fb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a39fb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a39fb-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a39fb-107">Remarks</span></span>

<span data-ttu-id="a39fb-108">Questo attributo contiene un operatore OR bit per bit di **zero o più** flag.</span><span class="sxs-lookup"><span data-stu-id="a39fb-108">This attribute contains a bitwise **OR** of zero or more flags.</span></span> <span data-ttu-id="a39fb-109">Per un elenco dei flag possibili, vedere [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="a39fb-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span>

<span data-ttu-id="a39fb-110">Questo attributo viene utilizzato con l'evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a39fb-110">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="a39fb-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a39fb-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a39fb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a39fb-112">Requirements</span></span>



| <span data-ttu-id="a39fb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a39fb-113">Requirement</span></span> | <span data-ttu-id="a39fb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a39fb-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a39fb-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a39fb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a39fb-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a39fb-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a39fb-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a39fb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a39fb-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a39fb-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a39fb-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a39fb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a39fb-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a39fb-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a39fb-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a39fb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39fb-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a39fb-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a39fb-123">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="a39fb-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="a39fb-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="a39fb-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a39fb-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="a39fb-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




