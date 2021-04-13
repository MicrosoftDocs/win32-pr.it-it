---
title: Informazioni di riferimento su DirectShow QASF
description: Informazioni di riferimento su DirectShow QASF
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media Format SDK, QASF
- Windows Media Format SDK, DirectShow
- DirectShow, riferimento QASF
- Filtri QASF, riferimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399344"
---
# <a name="directshow-qasf-reference"></a><span data-ttu-id="91a93-107">Informazioni di riferimento su DirectShow QASF</span><span class="sxs-lookup"><span data-stu-id="91a93-107">DirectShow QASF Reference</span></span>

<span data-ttu-id="91a93-108">Questa sezione contiene i riferimenti di programmazione per i filtri, le interfacce e le enumerazioni di DirectShow QASF seguenti.</span><span class="sxs-lookup"><span data-stu-id="91a93-108">This section contains programming references for the following DirectShow QASF filters, interfaces and enumerations.</span></span> <span data-ttu-id="91a93-109">La documentazione di DirectShow SDK contiene i materiali di riferimento e guida alla programmazione per interfacce generiche aggiuntive esposte da questi filtri, ad esempio **IBaseFilter** e **Ipin**, e per le versioni precedenti dei componenti qasf.</span><span class="sxs-lookup"><span data-stu-id="91a93-109">The DirectShow SDK documentation contains reference and programming guide materials for additional generic interfaces exposed by these filters, such as **IBaseFilter** and **IPin**, and for earlier versions of the QASF components.</span></span>

<span data-ttu-id="91a93-110">Per una spiegazione del nome del QASF, vedere [informazioni su DirectShow](about-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="91a93-110">For an explanation of the QASF name, see [About DirectShow](about-directshow.md).</span></span>

<span data-ttu-id="91a93-111">Con i componenti di QASF DirectShow sono inclusi i filtri seguenti.</span><span class="sxs-lookup"><span data-stu-id="91a93-111">The following filters are included with the DirectShow QASF components.</span></span>



| <span data-ttu-id="91a93-112">Filtra</span><span class="sxs-lookup"><span data-stu-id="91a93-112">Filter</span></span>                                           | <span data-ttu-id="91a93-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91a93-113">Description</span></span>                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="91a93-114">Filtro di lettura ASF WM</span><span class="sxs-lookup"><span data-stu-id="91a93-114">WM ASF Reader Filter</span></span>](wm-asf-reader-filter.md) | <span data-ttu-id="91a93-115">Legge e analizza i file ASF locali o remoti.</span><span class="sxs-lookup"><span data-stu-id="91a93-115">Reads and parses local or remote ASF files.</span></span>                      |
| [<span data-ttu-id="91a93-116">Filtro writer ASF WM</span><span class="sxs-lookup"><span data-stu-id="91a93-116">WM ASF Writer Filter</span></span>](wm-asf-writer-filter.md) | <span data-ttu-id="91a93-117">Crea file ASF da flussi di input compressi o non compressi.</span><span class="sxs-lookup"><span data-stu-id="91a93-117">Creates ASF files from compressed or uncompressed input streams.</span></span> |



 

<span data-ttu-id="91a93-118">Le interfacce seguenti sono definite per l'uso con i componenti DirectShow QASF.</span><span class="sxs-lookup"><span data-stu-id="91a93-118">The following interfaces are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="91a93-119">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="91a93-119">Interface</span></span>                                                  | <span data-ttu-id="91a93-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91a93-120">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91a93-121">**IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="91a93-121">**IAMWMBufferPass**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | <span data-ttu-id="91a93-122">Fornisce un metodo che consente alle applicazioni di eseguire la registrazione per i callback dai pin di input del [writer ASF WM](wm-asf-writer-filter.md) o dei pin di output del filtro [WM ASF Reader](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="91a93-122">Provides a method that enables applications to register for callbacks from the input pins of the [WM ASF Writer](wm-asf-writer-filter.md) or the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="91a93-123">Usato nell'indicizzazione e quando si aggiungono estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="91a93-123">Used in indexing and when adding data unit extensions.</span></span> |
| [<span data-ttu-id="91a93-124">**IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="91a93-124">**IAMWMBufferPassCallback**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | <span data-ttu-id="91a93-125">Implementato dalle applicazioni e chiamato dai filtri.</span><span class="sxs-lookup"><span data-stu-id="91a93-125">Implemented by applications and called by the filters.</span></span> <span data-ttu-id="91a93-126">Le applicazioni usano il metodo One su questa interfaccia per ottenere informazioni sui singoli esempi nel flusso.</span><span class="sxs-lookup"><span data-stu-id="91a93-126">Applications use the one method on this interface to obtain information about individual samples in the stream.</span></span> <span data-ttu-id="91a93-127">Usato nell'indicizzazione e quando si aggiungono estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="91a93-127">Used in indexing and when adding data unit extensions.</span></span>                                                 |
| <span data-ttu-id="91a93-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91a93-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>               | <span data-ttu-id="91a93-129">Implementato nel writer ASF WM.</span><span class="sxs-lookup"><span data-stu-id="91a93-129">Implemented on the WM ASF Writer.</span></span> <span data-ttu-id="91a93-130">Utilizzato dalle applicazioni per specificare i profili e i parametri di indicizzazione per il file.</span><span class="sxs-lookup"><span data-stu-id="91a93-130">Used by applications to specify profiles and indexing parameters for the file.</span></span>                                                                                                                                                              |
| <span data-ttu-id="91a93-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91a93-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>             | <span data-ttu-id="91a93-132">Fornisce funzioni di configurazione aggiuntive sul writer ASF WM.</span><span class="sxs-lookup"><span data-stu-id="91a93-132">Provides additional configuration functions on the WM ASF Writer.</span></span>                                                                                                                                                                                                             |



 

<span data-ttu-id="91a93-133">L'enumerazione, la struttura e gli eventi seguenti vengono definiti per l'uso con i componenti DirectShow QASF.</span><span class="sxs-lookup"><span data-stu-id="91a93-133">The following enumeration, structure, and events are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="91a93-134">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="91a93-134">Enumeration</span></span>                                                               | <span data-ttu-id="91a93-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91a93-135">Description</span></span>                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91a93-136">[\_\_param ASFWRITERCONFIG \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91a93-136">[\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span></span> | <span data-ttu-id="91a93-137">Definisce i parametri di configurazione del filtro utilizzati nei metodi [**IConfigAsfWriter2:: Getparat**](iconfigasfwriter2-getparam.md) e [**separar**](iconfigasfwriter2-setparam.md) .</span><span class="sxs-lookup"><span data-stu-id="91a93-137">Defines filter configuration parameters used in the [**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md) and [**SetParam**](iconfigasfwriter2-setparam.md) methods.</span></span> |



 



| <span data-ttu-id="91a93-138">Struttura</span><span class="sxs-lookup"><span data-stu-id="91a93-138">Structure</span></span>                                         | <span data-ttu-id="91a93-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91a93-139">Description</span></span>                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91a93-140">**\_ \_ dati evento WMT \_**</span><span class="sxs-lookup"><span data-stu-id="91a93-140">**AM\_WMT\_EVENT\_DATA**</span></span>](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | <span data-ttu-id="91a93-141">Contiene informazioni relative a un evento [**di \_ stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) e al codice di stato associato restituito da Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="91a93-141">Contains information pertaining to a [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) event and the associated status code returned by the Windows Media Format SDK.</span></span> |



 



| <span data-ttu-id="91a93-142">Event</span><span class="sxs-lookup"><span data-stu-id="91a93-142">Event</span></span>                                           | <span data-ttu-id="91a93-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91a93-143">Description</span></span>                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91a93-144">\_evento WMT \_ EC</span><span class="sxs-lookup"><span data-stu-id="91a93-144">EC\_WMT\_EVENT</span></span>](ec-wmt-event.md)              | <span data-ttu-id="91a93-145">Evento inviato da Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="91a93-145">Event forwarded from the Windows Media Format SDK.</span></span>                                                              |
| [<span data-ttu-id="91a93-146">\_evento di \_ indice \_ WMT EC</span><span class="sxs-lookup"><span data-stu-id="91a93-146">EC\_WMT\_INDEX\_EVENT</span></span>](ec-wmt-index-event.md) | <span data-ttu-id="91a93-147">Inviato quando un'applicazione usa il [writer ASF WM](wm-asf-writer-filter.md) per indicizzare i file di Windows Media video.</span><span class="sxs-lookup"><span data-stu-id="91a93-147">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) to index Windows Media Video files.</span></span> |



 

 

 