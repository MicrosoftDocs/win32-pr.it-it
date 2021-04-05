---
description: Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica se i pacchetti di trasporto contengono intestazioni dei pacchetti di contenuto.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: Attributo MF_MT_MPEG2_CONTENT_PACKET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883217"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a><span data-ttu-id="02c69-103">\_ \_ \_ Attributo pacchetto di contenuto \_ MPEG2 MF mt</span><span class="sxs-lookup"><span data-stu-id="02c69-103">MF\_MT\_MPEG2\_CONTENT\_PACKET attribute</span></span>

<span data-ttu-id="02c69-104">Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica se i pacchetti di trasporto contengono intestazioni dei pacchetti di contenuto.</span><span class="sxs-lookup"><span data-stu-id="02c69-104">For a media type that describes an MPEG-2 transport stream (TS), specifies whether the transport packets contain Content Packet headers.</span></span>

## <a name="data-type"></a><span data-ttu-id="02c69-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="02c69-105">Data type</span></span>

<span data-ttu-id="02c69-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="02c69-106">**UINT32**</span></span>



| <span data-ttu-id="02c69-107">Valore</span><span class="sxs-lookup"><span data-stu-id="02c69-107">Value</span></span>                                                                                                | <span data-ttu-id="02c69-108">Significato</span><span class="sxs-lookup"><span data-stu-id="02c69-108">Meaning</span></span>                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="02c69-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="02c69-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="02c69-110">Non sono state aggiunte intestazioni di pacchetti di contenuto.</span><span class="sxs-lookup"><span data-stu-id="02c69-110">No Content Packet headers are added.</span></span><br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <span data-ttu-id="02c69-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="02c69-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="02c69-112">A intervalli di 200 – 1000 millisecondi, l'intestazione di un pacchetto di contenuto a 14 byte viene aggiunta all'inizio del pacchetto di trasporto, come definito dall'associazione dello standard radio Industries and business (ARIB).</span><span class="sxs-lookup"><span data-stu-id="02c69-112">At 200–1000 millisecond intervals, a 14-byte Content Packet header is added to the beginning of the transport packet, as defined by the Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02c69-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02c69-113">Requirements</span></span>



| <span data-ttu-id="02c69-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c69-114">Requirement</span></span> | <span data-ttu-id="02c69-115">Valore</span><span class="sxs-lookup"><span data-stu-id="02c69-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02c69-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02c69-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02c69-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="02c69-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="02c69-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02c69-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02c69-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="02c69-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="02c69-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02c69-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02c69-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="02c69-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c69-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02c69-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c69-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02c69-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




