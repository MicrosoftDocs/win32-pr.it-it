---
description: Consente al lettore di origine di utilizzare le trasformazioni di Media Foundation (MFTs) ottimizzate per la transcodifica.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: Attributo MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525992"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a><span data-ttu-id="01944-103">MF \_ source \_ Reader \_ Abilita l' \_ attributo TRANScode \_ only \_ Transformations</span><span class="sxs-lookup"><span data-stu-id="01944-103">MF\_SOURCE\_READER\_ENABLE\_TRANSCODE\_ONLY\_TRANSFORMS attribute</span></span>

<span data-ttu-id="01944-104">Consente al [lettore di origine](source-reader.md) di utilizzare le trasformazioni di Media Foundation (MFTS) ottimizzate per la transcodifica.</span><span class="sxs-lookup"><span data-stu-id="01944-104">Enables the [Source Reader](source-reader.md) to use Media Foundation transforms (MFTs) that are optimized for transcoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="01944-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="01944-105">Data type</span></span>

<span data-ttu-id="01944-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="01944-106">**UINT32**</span></span>

<span data-ttu-id="01944-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="01944-107">Treat as Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="01944-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="01944-108">Remarks</span></span>

<span data-ttu-id="01944-109">Alcuni MFTs, in particolare i decodificatori, sono ottimizzati per la transcodifica anziché per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="01944-109">Some MFTs, particularly decoders, are optimized for transcoding rather than playback.</span></span> <span data-ttu-id="01944-110">Per impostazione predefinita, il lettore di origine non caricherà tali trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="01944-110">By default, the Source Reader will not load such transforms.</span></span> <span data-ttu-id="01944-111">Impostare questo attributo su **true** se si desidera utilizzare la transcodifica di MFTS con il lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="01944-111">Set this attribute to **TRUE** if you want to use transcoding MFTs with the Source Reader.</span></span>

<span data-ttu-id="01944-112">Un'applicazione potrebbe impostare questo attributo se non elabora i dati in tempo reale (per la transcodifica o scenari simili).</span><span class="sxs-lookup"><span data-stu-id="01944-112">An application might set this attribute if it does not process the data in real time (for transcoding or similar scenarios).</span></span> <span data-ttu-id="01944-113">In caso contrario, per la riproduzione in tempo reale, utilizzare il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="01944-113">Otherwise, for real-time playback, use the default behavior.</span></span>

<span data-ttu-id="01944-114">Internamente, questo attributo fa in modo che il lettore di origine includa il flag del **\_ flag enum di enumerazione MFT \_ \_ \_ solo** quando chiama [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="01944-114">Internally, this attribute causes the Source Reader to include the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when it calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

## <a name="requirements"></a><span data-ttu-id="01944-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01944-115">Requirements</span></span>



| <span data-ttu-id="01944-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="01944-116">Requirement</span></span> | <span data-ttu-id="01944-117">Valore</span><span class="sxs-lookup"><span data-stu-id="01944-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01944-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01944-118">Minimum supported client</span></span><br/> | <span data-ttu-id="01944-119">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="01944-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="01944-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01944-120">Minimum supported server</span></span><br/> | <span data-ttu-id="01944-121">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="01944-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="01944-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01944-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="01944-123"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="01944-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01944-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01944-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01944-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01944-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01944-126">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="01944-126">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




