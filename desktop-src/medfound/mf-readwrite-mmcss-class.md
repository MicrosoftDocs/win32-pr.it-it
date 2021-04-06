---
description: Specifica una classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per il writer del sink o del lettore di origine.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: Attributo MF_READWRITE_MMCSS_CLASS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759077"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a><span data-ttu-id="0c4ab-103">\_Attributo della classe MF ReadWrite \_ MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="0c4ab-103">MF\_READWRITE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="0c4ab-104">Specifica una classe di [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) per il writer del sink o del lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="0c4ab-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c4ab-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0c4ab-105">Data type</span></span>

<span data-ttu-id="0c4ab-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="0c4ab-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="0c4ab-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="0c4ab-107">Get/set</span></span>

<span data-ttu-id="0c4ab-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="0c4ab-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="0c4ab-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="0c4ab-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c4ab-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c4ab-110">Remarks</span></span>

<span data-ttu-id="0c4ab-111">Facoltativamente, impostare questo attributo quando si crea un'istanza di [Reader di origine](source-reader.md) o di [sink writer](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="0c4ab-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="0c4ab-112">Il valore dell'attributo deve essere un nome di classe MMCSS valido.</span><span class="sxs-lookup"><span data-stu-id="0c4ab-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="0c4ab-113">Se questo attributo è impostato, il writer di origine o di sink registra tutti i relativi thread con la classe MMCSS specificata.</span><span class="sxs-lookup"><span data-stu-id="0c4ab-113">If this attribute is set, the Source Reader or Sink Writer registers all of its threads with the specified MMCSS class.</span></span> <span data-ttu-id="0c4ab-114">Il MMCSS garantisce che l'elaborazione dei dati in Reader di origine o writer di sink abbia la priorità rispetto ad altre attività di sistema.</span><span class="sxs-lookup"><span data-stu-id="0c4ab-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="0c4ab-115">Per specificare la priorità di base, impostare l'attributo di [ \_ \_ \_ Priorità MF ReadWrite MMCSS](mf-readwrite-mmcss-priority.md) .</span><span class="sxs-lookup"><span data-stu-id="0c4ab-115">To specify the base priority, set the [MF\_READWRITE\_MMCSS\_PRIORITY](mf-readwrite-mmcss-priority.md) attribute.</span></span> <span data-ttu-id="0c4ab-116">Se tale attributo non è impostato, la priorità di base è zero.</span><span class="sxs-lookup"><span data-stu-id="0c4ab-116">If that attribute is not set, the base priority is zero.</span></span>

<span data-ttu-id="0c4ab-117">Per i thread di elaborazione audio, l'attributo [ \_ audio della classe MF ReadWrite \_ MMCSS \_ \_ ](mf-readwrite-mmcss-class-audio.md) (se impostato) esegue l'override di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="0c4ab-117">For audio-processing threads, the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute (if set) overrides this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4ab-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c4ab-118">Requirements</span></span>



| <span data-ttu-id="0c4ab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c4ab-119">Requirement</span></span> | <span data-ttu-id="0c4ab-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0c4ab-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c4ab-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c4ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c4ab-122">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0c4ab-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0c4ab-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c4ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c4ab-124">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0c4ab-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0c4ab-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c4ab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c4ab-126"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c4ab-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c4ab-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c4ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c4ab-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c4ab-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
