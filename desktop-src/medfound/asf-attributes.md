---
description: Attributi ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Attributi ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305526"
---
# <a name="asf-attributes"></a><span data-ttu-id="2dd98-103">Attributi ASF</span><span class="sxs-lookup"><span data-stu-id="2dd98-103">ASF Attributes</span></span>

### <a name="profile-attributes"></a><span data-ttu-id="2dd98-104">Attributi del profilo</span><span class="sxs-lookup"><span data-stu-id="2dd98-104">Profile Attributes</span></span>

<span data-ttu-id="2dd98-105">Ai profili ASF si applicano gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="2dd98-105">The following attributes apply to ASF profiles.</span></span>



| <span data-ttu-id="2dd98-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="2dd98-106">Attribute</span></span>                                                                      | <span data-ttu-id="2dd98-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dd98-107">Description</span></span>                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="2dd98-108">**MF \_ ASFPROFILE \_ MAXPACKETSIZE**</span><span class="sxs-lookup"><span data-stu-id="2dd98-108">**MF\_ASFPROFILE\_MAXPACKETSIZE**</span></span>](mf-asfprofile-maxpacketsize-attribute.md) | <span data-ttu-id="2dd98-109">Specifica la dimensione massima del pacchetto per un file ASF, in byte.</span><span class="sxs-lookup"><span data-stu-id="2dd98-109">Specifies the maximum packet size for an ASF file, in bytes.</span></span> |
| [<span data-ttu-id="2dd98-110">**MF \_ ASFPROFILE \_ MINPACKETSIZE**</span><span class="sxs-lookup"><span data-stu-id="2dd98-110">**MF\_ASFPROFILE\_MINPACKETSIZE**</span></span>](mf-asfprofile-minpacketsize-attribute.md) | <span data-ttu-id="2dd98-111">Specifica le dimensioni minime del pacchetto per un file ASF, in byte.</span><span class="sxs-lookup"><span data-stu-id="2dd98-111">Specifies the minimum packet size for an ASF file, in bytes.</span></span> |



 

### <a name="stream-configuration-attributes"></a><span data-ttu-id="2dd98-112">Attributi di configurazione del flusso</span><span class="sxs-lookup"><span data-stu-id="2dd98-112">Stream Configuration Attributes</span></span>

<span data-ttu-id="2dd98-113">Gli attributi seguenti si applicano all'oggetto di configurazione del flusso ASF.</span><span class="sxs-lookup"><span data-stu-id="2dd98-113">The following attributes apply to the ASF stream configuration object.</span></span>



| <span data-ttu-id="2dd98-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="2dd98-114">Attribute</span></span>                                                                              | <span data-ttu-id="2dd98-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dd98-115">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="2dd98-116">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="2dd98-116">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md) | <span data-ttu-id="2dd98-117">Imposta i parametri medi "bucket Leak" per la codifica di un file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2dd98-117">Sets the average "leaky bucket" parameters for encoding a Windows Media file.</span></span> |
| [<span data-ttu-id="2dd98-118">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="2dd98-118">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md) | <span data-ttu-id="2dd98-119">Imposta il picco dei parametri "leaky bucket" per la codifica di un file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2dd98-119">Sets the peak "leaky bucket" parameters for encoding a Windows Media file.</span></span>    |



 

### <a name="media-buffer-attributes"></a><span data-ttu-id="2dd98-120">Attributi del buffer multimediale</span><span class="sxs-lookup"><span data-stu-id="2dd98-120">Media Buffer Attributes</span></span>

<span data-ttu-id="2dd98-121">Gli attributi seguenti si applicano ai buffer multimediali per i pacchetti ASF.</span><span class="sxs-lookup"><span data-stu-id="2dd98-121">The following attributes apply to media buffers for ASF packets.</span></span>



| <span data-ttu-id="2dd98-122">Attributo</span><span class="sxs-lookup"><span data-stu-id="2dd98-122">Attribute</span></span>                                                                          | <span data-ttu-id="2dd98-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dd98-123">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dd98-124">**\_limite pacchetto \_ MFASFSPLITTER**</span><span class="sxs-lookup"><span data-stu-id="2dd98-124">**MFASFSPLITTER\_PACKET\_BOUNDARY**</span></span>](mfasfsplitter-packet-boundary-attribute.md) | <span data-ttu-id="2dd98-125">Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2dd98-125">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span> |



 

### <a name="presentation-descriptor-attributes"></a><span data-ttu-id="2dd98-126">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="2dd98-126">Presentation Descriptor Attributes</span></span>

<span data-ttu-id="2dd98-127">Per un elenco degli attributi applicabili ai descrittori di presentazione ASF, vedere la pagina relativa agli [attributi del descrittore di presentazione](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="2dd98-127">For a list of attributes that apply to ASF presentation descriptors, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dd98-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2dd98-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dd98-129">**IMFASFProfile**</span><span class="sxs-lookup"><span data-stu-id="2dd98-129">**IMFASFProfile**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[<span data-ttu-id="2dd98-130">**IMFASFStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="2dd98-130">**IMFASFStreamConfig**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[<span data-ttu-id="2dd98-131">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2dd98-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



