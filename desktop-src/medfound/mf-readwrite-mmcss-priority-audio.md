---
description: Imposta la priorità di base per i thread di elaborazione audio creati dal reader di origine o dal writer del sink.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: Attributo MF_READWRITE_MMCSS_PRIORITY_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308463"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a><span data-ttu-id="5cb0c-103">\_ \_ \_ Attributo audio Priority ReadWrite MMCSS MF \_</span><span class="sxs-lookup"><span data-stu-id="5cb0c-103">MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO attribute</span></span>

<span data-ttu-id="5cb0c-104">Imposta la priorità di base per i thread di elaborazione audio creati dal reader di origine o dal writer del sink.</span><span class="sxs-lookup"><span data-stu-id="5cb0c-104">Sets the base priority for audio-processing threads created by the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="5cb0c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5cb0c-105">Data type</span></span>

<span data-ttu-id="5cb0c-106">**Int32** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5cb0c-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5cb0c-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="5cb0c-107">Get/set</span></span>

<span data-ttu-id="5cb0c-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5cb0c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5cb0c-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="5cb0c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cb0c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cb0c-110">Remarks</span></span>

<span data-ttu-id="5cb0c-111">Facoltativamente, impostare questo attributo quando si crea un'istanza di [Reader di origine](source-reader.md) o di [sink writer](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="5cb0c-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="5cb0c-112">Se si imposta questo attributo, impostare anche l' [attributo \_ \_ audio della \_ classe \_ MF ReadWrite MMCSS](mf-readwrite-mmcss-class-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="5cb0c-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute.</span></span> <span data-ttu-id="5cb0c-113">In caso contrario, questo attributo viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="5cb0c-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="5cb0c-114">Quando l'utilità di lettura di origine o il writer di sink registra i thread di elaborazione audio con il [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md), il valore di questo attributo specifica la priorità del thread di base.</span><span class="sxs-lookup"><span data-stu-id="5cb0c-114">When the Source Reader or Sink Writer registers audio-processing threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="5cb0c-115">Se questo attributo non è impostato, il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="5cb0c-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb0c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cb0c-116">Requirements</span></span>



| <span data-ttu-id="5cb0c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb0c-117">Requirement</span></span> | <span data-ttu-id="5cb0c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5cb0c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb0c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb0c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5cb0c-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5cb0c-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5cb0c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb0c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5cb0c-122">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="5cb0c-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5cb0c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cb0c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cb0c-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cb0c-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cb0c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cb0c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb0c-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5cb0c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
