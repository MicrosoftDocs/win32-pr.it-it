---
description: Specifica se il sink di file MPEG-4 filtra i set di parametri di sequenza (SPS) e il set di parametri immagine (PPS) NALUs.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Attributo MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754274"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a><span data-ttu-id="7bbad-103">\_ \_ Attributo passthrough MPEG4SINK SPSPPS MF \_</span><span class="sxs-lookup"><span data-stu-id="7bbad-103">MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute</span></span>

<span data-ttu-id="7bbad-104">Specifica se il [**sink di file MPEG-4**](mpeg-4-file-sink.md) filtra i set di parametri di sequenza (SPS) e il set di parametri immagine (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="7bbad-104">Specifies whether the [**MPEG-4 File Sink**](mpeg-4-file-sink.md) filters out sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

## <a name="data-type"></a><span data-ttu-id="7bbad-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7bbad-105">Data type</span></span>

<span data-ttu-id="7bbad-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbad-106">**BOOL** stored as **UINT32**</span></span>

## <a name="applies-to"></a><span data-ttu-id="7bbad-107">Si applica a</span><span class="sxs-lookup"><span data-stu-id="7bbad-107">Applies to</span></span>

[<span data-ttu-id="7bbad-108">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="7bbad-108">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a><span data-ttu-id="7bbad-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bbad-109">Remarks</span></span>

<span data-ttu-id="7bbad-110">Il [**sink di file MPEG-4**](mpeg-4-file-sink.md) scrive i parametri SPS e PPS nella casella Descrizione di esempio del file MP4.</span><span class="sxs-lookup"><span data-stu-id="7bbad-110">The [**MPEG-4 File Sink**](mpeg-4-file-sink.md) writes the SPS and PPS parameters into the sample description box of the MP4 file.</span></span> <span data-ttu-id="7bbad-111">Per impostazione predefinita, filtra i NALUs SPS e PPS dal flusso video.</span><span class="sxs-lookup"><span data-stu-id="7bbad-111">By default, it filters out the SPS and PPS NALUs from the video stream.</span></span> <span data-ttu-id="7bbad-112">Per eseguire l'override di questo comportamento, impostare l' \_ \_ attributo passthrough MF MPEG4SINK SPSPPS \_ su **true**.</span><span class="sxs-lookup"><span data-stu-id="7bbad-112">To override this behavior, set the MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbad-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bbad-113">Requirements</span></span>



| <span data-ttu-id="7bbad-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bbad-114">Requirement</span></span> | <span data-ttu-id="7bbad-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7bbad-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbad-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bbad-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7bbad-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7bbad-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7bbad-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bbad-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7bbad-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="7bbad-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7bbad-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bbad-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bbad-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bbad-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbad-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bbad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbad-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7bbad-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




