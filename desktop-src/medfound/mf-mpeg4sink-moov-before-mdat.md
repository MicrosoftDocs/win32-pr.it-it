---
description: Indica che Moov verrà scritto prima della casella mdat nel file generato.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Attributo MF_MPEG4SINK_MOOV_BEFORE_MDAT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313052"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a><span data-ttu-id="628d4-103">MF \_ MPEG4SINK \_ Moov \_ prima dell' \_ attributo mdat</span><span class="sxs-lookup"><span data-stu-id="628d4-103">MF\_MPEG4SINK\_MOOV\_BEFORE\_MDAT attribute</span></span>

<span data-ttu-id="628d4-104">Indica che "Moov" verrà scritto prima della casella "mdat" nel file generato.</span><span class="sxs-lookup"><span data-stu-id="628d4-104">Indicates that 'moov' will be written before 'mdat' box in the generated file.</span></span>

## <a name="data-type"></a><span data-ttu-id="628d4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="628d4-105">Data type</span></span>

<span data-ttu-id="628d4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="628d4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="628d4-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="628d4-107">Remarks</span></span>

<span data-ttu-id="628d4-108">Il comportamento predefinito del sink multimediale MPEG4 consiste nel scrivere ' Moov ' dopo ' mdat ' box.</span><span class="sxs-lookup"><span data-stu-id="628d4-108">The default behavior of the mpeg4 media sink is to write 'moov' after 'mdat' box.</span></span> <span data-ttu-id="628d4-109">Se si imposta questo attributo, il file generato scriverà' Moov ' prima della casella ' mdat '.</span><span class="sxs-lookup"><span data-stu-id="628d4-109">Setting this attribute causes the generated file to write 'moov' before 'mdat' box.</span></span>

<span data-ttu-id="628d4-110">Affinché il sink MPEG4 usi questo attributo, il flusso di byte passato non deve essere una ricerca lenta o remota per.</span><span class="sxs-lookup"><span data-stu-id="628d4-110">In order for the mpeg4 sink to use this attribute, the byte stream passed in must not be slow seek or remote for .</span></span>

<span data-ttu-id="628d4-111">Questa funzionalità prevede un file di copia/remuxing aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="628d4-111">This feature involves an additional file copying/remuxing.</span></span>

## <a name="requirements"></a><span data-ttu-id="628d4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="628d4-112">Requirements</span></span>



| <span data-ttu-id="628d4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="628d4-113">Requirement</span></span> | <span data-ttu-id="628d4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="628d4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="628d4-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="628d4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="628d4-116">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="628d4-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="628d4-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="628d4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="628d4-118">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="628d4-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="628d4-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="628d4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="628d4-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="628d4-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="628d4-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="628d4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="628d4-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="628d4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="628d4-123">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="628d4-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




