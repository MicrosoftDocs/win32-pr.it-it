---
description: Specifica una classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per i thread di elaborazione audio nel Reader di origine o nel writer del sink.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: Attributo MF_READWRITE_MMCSS_CLASS_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308464"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a><span data-ttu-id="1245d-103">\_ \_ \_ Attributo audio della classe MF ReadWrite MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="1245d-103">MF\_READWRITE\_MMCSS\_CLASS\_AUDIO attribute</span></span>

<span data-ttu-id="1245d-104">Specifica una classe di [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) per i thread di elaborazione audio nel Reader di origine o nel writer del sink.</span><span class="sxs-lookup"><span data-stu-id="1245d-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for audio-processing threads in the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="1245d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1245d-105">Data type</span></span>

<span data-ttu-id="1245d-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="1245d-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="1245d-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="1245d-107">Get/set</span></span>

<span data-ttu-id="1245d-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="1245d-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="1245d-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="1245d-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="1245d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1245d-110">Remarks</span></span>

<span data-ttu-id="1245d-111">Facoltativamente, impostare questo attributo quando si crea un'istanza di [Reader di origine](source-reader.md) o di [sink writer](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="1245d-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="1245d-112">Il valore dell'attributo deve essere un nome di classe MMCSS valido.</span><span class="sxs-lookup"><span data-stu-id="1245d-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="1245d-113">Se questo attributo è impostato, il writer di origine o il writer di sink registra i thread di elaborazione audio con la classe MMCSS specificata.</span><span class="sxs-lookup"><span data-stu-id="1245d-113">If this attribute is set, the Source Reader or Sink Writer registers its audio-processing threads with the specified MMCSS class.</span></span> <span data-ttu-id="1245d-114">Il MMCSS garantisce che l'elaborazione dei dati in Reader di origine o writer di sink abbia la priorità rispetto ad altre attività di sistema.</span><span class="sxs-lookup"><span data-stu-id="1245d-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="1245d-115">Per specificare la priorità di base per i thread audio, impostare l'attributo [MF \_ ReadWrite \_ MMCSS \_ Priority \_ audio](mf-readwrite-mmcss-priority-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="1245d-115">To specify the base priority for audio threads, set the [MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO](mf-readwrite-mmcss-priority-audio.md) attribute.</span></span> <span data-ttu-id="1245d-116">Se tale attributo non è impostato, la priorità di base per i thread audio è zero.</span><span class="sxs-lookup"><span data-stu-id="1245d-116">If that attribute is not set, the base priority for audio threads is zero.</span></span>

<span data-ttu-id="1245d-117">Questo attributo sostituisce l'attributo della [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) per i thread di elaborazione audio.</span><span class="sxs-lookup"><span data-stu-id="1245d-117">This attribute overrides the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute for audio-processing threads.</span></span> <span data-ttu-id="1245d-118">Se non è impostato alcun attributo, i thread audio non vengono registrati con MCSS.</span><span class="sxs-lookup"><span data-stu-id="1245d-118">If neither attribute is set, audio threads are not registered with MCSS.</span></span>

<span data-ttu-id="1245d-119">Per la maggior parte delle applicazioni, la glitching audio è molto più evidente all'utente rispetto alla glitch video e pertanto meno accettabile.</span><span class="sxs-lookup"><span data-stu-id="1245d-119">For most applications, audio glitching is much more noticeable to the user than video glitching, and therefore less acceptable.</span></span> <span data-ttu-id="1245d-120">Per questo motivo, un'applicazione deve in genere impostare \_ l' \_ \_ audio della classe MF ReadWrite MMCSS \_ su una classe MMCSS con priorità superiore rispetto alla [ \_ classe MF ReadWrite \_ MMCSS \_ ](mf-readwrite-mmcss-class.md).</span><span class="sxs-lookup"><span data-stu-id="1245d-120">For this reason, an application should typically set MF\_READWRITE\_MMCSS\_CLASS\_AUDIO to a higher-priority MMCSS class than [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md).</span></span> <span data-ttu-id="1245d-121">In questo modo si garantisce che l'elaborazione audio disponga di una priorità più elevata rispetto ad altre attività.</span><span class="sxs-lookup"><span data-stu-id="1245d-121">This ensures that audio processing is given higher priority than other tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="1245d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1245d-122">Requirements</span></span>



| <span data-ttu-id="1245d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1245d-123">Requirement</span></span> | <span data-ttu-id="1245d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1245d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1245d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1245d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1245d-126">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1245d-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="1245d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1245d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1245d-128">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1245d-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1245d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1245d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1245d-130"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="1245d-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1245d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1245d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1245d-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1245d-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
