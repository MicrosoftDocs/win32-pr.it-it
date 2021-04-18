---
description: Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: Attributo MFASFSPLITTER_PACKET_BOUNDARY (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308419"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a><span data-ttu-id="66fef-103">\_Attributo limite del pacchetto MFASFSPLITTER \_</span><span class="sxs-lookup"><span data-stu-id="66fef-103">MFASFSPLITTER\_PACKET\_BOUNDARY attribute</span></span>

<span data-ttu-id="66fef-104">Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="66fef-104">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="66fef-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="66fef-105">Data type</span></span>

<span data-ttu-id="66fef-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="66fef-106">**UINT32**</span></span>

<span data-ttu-id="66fef-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="66fef-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66fef-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="66fef-108">Remarks</span></span>

<span data-ttu-id="66fef-109">Se un buffer multimediale espone l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) tramite **QueryInterface** e il valore di questo attributo è diverso da zero, il separatore ASF considera il buffer come l'inizio di un nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="66fef-109">If a media buffer exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface through **QueryInterface**, and the value of this attribute is nonzero, the ASF splitter treats the buffer as the start of a new packet.</span></span>

<span data-ttu-id="66fef-110">Questo attributo si applica se si utilizza la barra di divisione ASF per analizzare i dati ASF.</span><span class="sxs-lookup"><span data-stu-id="66fef-110">This attribute applies if you are using the ASF splitter to parse ASF data.</span></span> <span data-ttu-id="66fef-111">Se i dati ASF hanno lunghezze di pacchetti variabili, è necessario impostare questo attributo sui buffer multimediali passati al metodo [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="66fef-111">If your ASF data has variable packet lengths, you must set this attribute on the media buffers that you pass to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="66fef-112">Impostare l'attributo su **true** se il buffer contiene l'inizio di un nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="66fef-112">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="66fef-113">Se il buffer contiene una continuazione del pacchetto precedente, impostare l'attributo su **false**.</span><span class="sxs-lookup"><span data-stu-id="66fef-113">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="66fef-114">I buffer non possono estendersi su più pacchetti.</span><span class="sxs-lookup"><span data-stu-id="66fef-114">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="66fef-115">Per i dati ASF con dimensioni di pacchetto fisse, questo attributo non è obbligatorio e un buffer può estendersi a più pacchetti.</span><span class="sxs-lookup"><span data-stu-id="66fef-115">For ASF data with fixed packet sizes, this attribute is not required, and a buffer can can span multiple packets.</span></span>

<span data-ttu-id="66fef-116">Si noti che le implementazioni standard di [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) fornite da Media Foundation non espongono [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="66fef-116">Note that the standard implementations of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) provided by Media Foundation do not expose [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="66fef-117">Per usare questo attributo, è necessario fornire un'implementazione personalizzata di **IMFMediaBuffer**; ad esempio, eseguendo il wrapping dei buffer restituiti da [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span><span class="sxs-lookup"><span data-stu-id="66fef-117">To use this attribute, you must provide your own implementation of **IMFMediaBuffer**; for example, by wrapping the buffers returned by [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span></span>

## <a name="requirements"></a><span data-ttu-id="66fef-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66fef-118">Requirements</span></span>



| <span data-ttu-id="66fef-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="66fef-119">Requirement</span></span> | <span data-ttu-id="66fef-120">Valore</span><span class="sxs-lookup"><span data-stu-id="66fef-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fef-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66fef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66fef-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66fef-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="66fef-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66fef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66fef-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66fef-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66fef-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66fef-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="66fef-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="66fef-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66fef-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66fef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fef-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66fef-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66fef-129">Attributi ASF</span><span class="sxs-lookup"><span data-stu-id="66fef-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="66fef-130">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="66fef-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="66fef-131">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="66fef-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="66fef-132">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="66fef-132">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




