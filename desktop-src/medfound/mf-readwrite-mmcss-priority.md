---
description: Imposta la priorità del thread di base per il writer del sink o del lettore di origine.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: Attributo MF_READWRITE_MMCSS_PRIORITY (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058211"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a><span data-ttu-id="fdac7-103">\_Attributo di \_ priorità MMCSS MF ReadWrite \_</span><span class="sxs-lookup"><span data-stu-id="fdac7-103">MF\_READWRITE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="fdac7-104">Imposta la priorità del thread di base per il writer del sink o del lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="fdac7-104">Sets the base thread priority for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="fdac7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fdac7-105">Data type</span></span>

<span data-ttu-id="fdac7-106">**Int32** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fdac7-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="fdac7-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="fdac7-107">Get/set</span></span>

<span data-ttu-id="fdac7-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="fdac7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="fdac7-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="fdac7-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="fdac7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdac7-110">Remarks</span></span>

<span data-ttu-id="fdac7-111">Facoltativamente, impostare questo attributo quando si crea un'istanza di [Reader di origine](source-reader.md) o di [sink writer](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="fdac7-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="fdac7-112">Se si imposta questo attributo, impostare anche l'attributo della [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) .</span><span class="sxs-lookup"><span data-stu-id="fdac7-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute.</span></span> <span data-ttu-id="fdac7-113">In caso contrario, questo attributo viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="fdac7-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="fdac7-114">Quando i thread vengono registrati con il [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md), il valore di questo attributo viene specificato dalla priorità del thread di base.</span><span class="sxs-lookup"><span data-stu-id="fdac7-114">When the Source Reader or Sink Writer registers threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="fdac7-115">Se questo attributo non è impostato, il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="fdac7-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdac7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdac7-116">Requirements</span></span>



| <span data-ttu-id="fdac7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdac7-117">Requirement</span></span> | <span data-ttu-id="fdac7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fdac7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdac7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdac7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fdac7-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fdac7-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="fdac7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdac7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fdac7-122">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="fdac7-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="fdac7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdac7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdac7-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdac7-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdac7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdac7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdac7-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fdac7-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
