---
description: Specifica se le topologie hanno una data e un'ora di inizio e di fine globali.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Attributo MF_SESSION_GLOBAL_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314537"
---
# <a name="mf_session_global_time-attribute"></a><span data-ttu-id="5c381-103">\_ \_ Attributo time globale della sessione MF \_</span><span class="sxs-lookup"><span data-stu-id="5c381-103">MF\_SESSION\_GLOBAL\_TIME attribute</span></span>

<span data-ttu-id="5c381-104">Specifica se le topologie hanno una data e un'ora di inizio e di fine globali.</span><span class="sxs-lookup"><span data-stu-id="5c381-104">Specifies whether topologies have a global start and stop time.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c381-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5c381-105">Data type</span></span>

<span data-ttu-id="5c381-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5c381-106">**UINT32**</span></span>

<span data-ttu-id="5c381-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="5c381-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c381-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c381-108">Remarks</span></span>

<span data-ttu-id="5c381-109">È possibile impostare questo attributo quando si crea il file multimediale sesison utilizzando il parametro *pConfiguration* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="5c381-109">You can set this attribute when you create the media sesison by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="5c381-110">Se questo attributo è presente e diverso da zero, tutte le topologie passate alla sessione multimediale devono avere gli attributi della topologia [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) e MF topologia [**\_ \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5c381-110">If this attribute is present and nonzero, then all topologies passed to the Media Session must have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) and [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributes.</span></span> <span data-ttu-id="5c381-111">Questi attributi specificano l'ora di inizio e di fine per la topologia relativa all'intera presentazione.</span><span class="sxs-lookup"><span data-stu-id="5c381-111">These attributes specify the start and stop times for the topology relative to the entire presentation.</span></span>

<span data-ttu-id="5c381-112">Se questo attributo è assente o **false**, le topologie non devono avere l'attributo [**MF \_ topologia \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) o [**MF \_ topologia \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5c381-112">If this attribute is absent or **FALSE**, the topologies must not have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) or [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attribute.</span></span>

<span data-ttu-id="5c381-113">Utilizzare questo attributo per creare sequenze di modifica.</span><span class="sxs-lookup"><span data-stu-id="5c381-113">Use this attribute to create editing sequences.</span></span> <span data-ttu-id="5c381-114">Per altre informazioni, vedere [tempi di presentazione della sequenza](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="5c381-114">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="5c381-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5c381-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c381-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c381-116">Requirements</span></span>



| <span data-ttu-id="5c381-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c381-117">Requirement</span></span> | <span data-ttu-id="5c381-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5c381-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c381-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c381-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c381-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c381-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5c381-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c381-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c381-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c381-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5c381-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c381-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c381-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c381-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c381-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c381-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c381-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c381-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c381-127">Attributi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="5c381-127">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c381-128">Tempi di presentazione sequenza</span><span class="sxs-lookup"><span data-stu-id="5c381-128">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="5c381-129">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="5c381-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5c381-130">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="5c381-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5c381-131">**\_PROJECTSTART topologia MF \_**</span><span class="sxs-lookup"><span data-stu-id="5c381-131">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> <dt>

[<span data-ttu-id="5c381-132">**\_PROJECTSTOP topologia MF \_**</span><span class="sxs-lookup"><span data-stu-id="5c381-132">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




