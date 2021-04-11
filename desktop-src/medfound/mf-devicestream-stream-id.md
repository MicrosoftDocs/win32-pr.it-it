---
description: Specifica l'identificatore del kernel streaming (KS) per un flusso in un dispositivo di acquisizione video.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: Attributo MF_DEVICESTREAM_STREAM_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049717"
---
# <a name="mf_devicestream_stream_id-attribute"></a><span data-ttu-id="e921d-103">\_ \_ Attributo ID flusso MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="e921d-103">MF\_DEVICESTREAM\_STREAM\_ID attribute</span></span>

<span data-ttu-id="e921d-104">Specifica l'identificatore del kernel streaming (KS) per un flusso in un dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="e921d-104">Specifies the kernel streaming (KS) identifier for a stream on a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="e921d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e921d-105">Data type</span></span>

<span data-ttu-id="e921d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e921d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e921d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e921d-107">Remarks</span></span>

<span data-ttu-id="e921d-108">Per ottenere questo attributo, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="e921d-108">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="e921d-109">Eseguire una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="e921d-109">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="e921d-110">Chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.</span><span class="sxs-lookup"><span data-stu-id="e921d-110">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="e921d-111">Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="e921d-111">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="e921d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e921d-112">Requirements</span></span>



| <span data-ttu-id="e921d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e921d-113">Requirement</span></span> | <span data-ttu-id="e921d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e921d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e921d-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e921d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e921d-116">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e921d-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e921d-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e921d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e921d-118">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e921d-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e921d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e921d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e921d-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e921d-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e921d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e921d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e921d-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e921d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




