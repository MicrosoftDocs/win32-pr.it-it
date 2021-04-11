---
description: Attributi del nodo della topologia
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Attributi del nodo della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967121"
---
# <a name="topology-node-attributes"></a><span data-ttu-id="1540d-103">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="1540d-103">Topology Node Attributes</span></span>

<span data-ttu-id="1540d-104">Gli attributi seguenti si applicano ai nodi della topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-104">The following attributes apply to topology nodes.</span></span>

## <a name="general-topology-node-attributes"></a><span data-ttu-id="1540d-105">Attributi generali del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="1540d-105">General Topology Node Attributes</span></span>



| <span data-ttu-id="1540d-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="1540d-106">Attribute</span></span>                                                                       | <span data-ttu-id="1540d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1540d-107">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1540d-108">**\_Metodo MF TOPONODE \_ Connect \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-108">**MF\_TOPONODE\_CONNECT\_METHOD**</span></span>](mf-toponode-connect-method-attribute.md)   | <span data-ttu-id="1540d-109">Specifica il modo in cui il caricatore della topologia connette il nodo della topologia e se il nodo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1540d-109">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>                                                        |
| [<span data-ttu-id="1540d-110">**\_decodificatore MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-110">**MF\_TOPONODE\_DECODER**</span></span>](mf-toponode-decoder-attribute.md)                  | <span data-ttu-id="1540d-111">Specifica se l'oggetto di un nodo della topologia è un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="1540d-111">Specifies whether a toplogy node's object is a decoder.</span></span>                                                                                                  |
| [<span data-ttu-id="1540d-112">**\_Decryptor MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-112">**MF\_TOPONODE\_DECRYPTOR**</span></span>](mf-toponode-decryptor-attribute.md)              | <span data-ttu-id="1540d-113">Specifica se l'oggetto sottostante di un nodo della topologia è un decrittografia.</span><span class="sxs-lookup"><span data-stu-id="1540d-113">Specifies whether a toplogy node's underlying object is a decryptor.</span></span>                                                                                     |
| [<span data-ttu-id="1540d-114">**MF \_ TOPONODE \_ scartabile**</span><span class="sxs-lookup"><span data-stu-id="1540d-114">**MF\_TOPONODE\_DISCARDABLE**</span></span>](mf-toponode-discardable-attribute.md)          | <span data-ttu-id="1540d-115">Specifica se la pipeline può eliminare campioni da un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-115">Specifies whether the pipeline can drop samples from a topology node.</span></span>                                                                                    |
| [<span data-ttu-id="1540d-116">**\_MAJORTYPE di \_ errore MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-116">**MF\_TOPONODE\_ERROR\_MAJORTYPE**</span></span>](mf-toponode-error-majortype-attribute.md) | <span data-ttu-id="1540d-117">Contiene il tipo di supporto principale per un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-117">Contains the major media type for a topology node.</span></span> <span data-ttu-id="1540d-118">Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.</span><span class="sxs-lookup"><span data-stu-id="1540d-118">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span> |
| [<span data-ttu-id="1540d-119">**sottotipo di \_ errore MF TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-119">**MF\_TOPONODE\_ERROR\_SUBTYPE**</span></span>](mf-toponode-error-subtype-attribute.md)     | <span data-ttu-id="1540d-120">Contiene il sottotipo di supporto per un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-120">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="1540d-121">Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.</span><span class="sxs-lookup"><span data-stu-id="1540d-121">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>    |
| [<span data-ttu-id="1540d-122">**\_ErrorCode MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-122">**MF\_TOPONODE\_ERRORCODE**</span></span>](mf-toponode-errorcode-attribute.md)              | <span data-ttu-id="1540d-123">Contiene il codice di errore dell'ultimo errore di connessione per questo nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-123">Contains the error code from the most recent connection failure for this topology node.</span></span>                                                                  |
| [<span data-ttu-id="1540d-124">**MF \_ TOPONODE \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="1540d-124">**MF\_TOPONODE\_LOCKED**</span></span>](mf-toponode-locked-attribute.md)                    | <span data-ttu-id="1540d-125">Specifica se i tipi di supporto possono essere modificati in questo nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-125">Specifies whether the media types can be changed on this topology node.</span></span>                                                                                  |
| [<span data-ttu-id="1540d-126">**MF \_ TOPONODE \_ Markin \_ qui**</span><span class="sxs-lookup"><span data-stu-id="1540d-126">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)         | <span data-ttu-id="1540d-127">Specifica se la pipeline applica Mark-in a questo nodo.</span><span class="sxs-lookup"><span data-stu-id="1540d-127">Specifies whether the pipeline applies mark-in at this node.</span></span>                                                                                             |
| [<span data-ttu-id="1540d-128">**TOPONODE di MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-128">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)       | <span data-ttu-id="1540d-129">Specifica se la pipeline applica Mark-out a questo nodo.</span><span class="sxs-lookup"><span data-stu-id="1540d-129">Specifies whether the pipeline applies mark-out at this node.</span></span>                                                                                            |



 

## <a name="source-node-attributes"></a><span data-ttu-id="1540d-130">Attributi del nodo di origine</span><span class="sxs-lookup"><span data-stu-id="1540d-130">Source Node Attributes</span></span>



| <span data-ttu-id="1540d-131">Attributo</span><span class="sxs-lookup"><span data-stu-id="1540d-131">Attribute</span></span>                                                                                       | <span data-ttu-id="1540d-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1540d-132">Description</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1540d-133">**MF \_ TOPONODE \_ MEDIASTART**</span><span class="sxs-lookup"><span data-stu-id="1540d-133">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)                            | <span data-ttu-id="1540d-134">Specifica l'ora di inizio di una presentazione, relativa all'avvio del file di origine del supporto, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="1540d-134">Specifies the start time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="1540d-135">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="1540d-135">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)                              | <span data-ttu-id="1540d-136">Specifica l'ora di arresto di una presentazione, relativa all'avvio del file di origine del supporto, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="1540d-136">Specifies the stop time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span>  |
| [<span data-ttu-id="1540d-137">**descrittore di presentazione MF \_ TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-137">**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**</span></span>](mf-toponode-presentation-descriptor-attribute.md) | <span data-ttu-id="1540d-138">Contiene un puntatore al descrittore di presentazione per l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="1540d-138">Contains a pointer to the presentation descriptor for the media source.</span></span>                                           |
| [<span data-ttu-id="1540d-139">**\_ \_ ElementID sequenza MF \_ TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="1540d-139">**MF\_TOPONODE\_SEQUENCE\_ELEMENTID**</span></span>](mf-toponode-sequence-elementid-attribute.md)           | <span data-ttu-id="1540d-140">Specifica l'elemento che contiene un nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="1540d-140">Specifies the element that contains a source node.</span></span>                                                                |
| [<span data-ttu-id="1540d-141">**\_origine MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-141">**MF\_TOPONODE\_SOURCE**</span></span>](mf-toponode-source-attribute.md)                                    | <span data-ttu-id="1540d-142">Contiene un puntatore all'origine multimediale associata a un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-142">Contains a pointer to the media source associated with a topology node.</span></span>                                           |
| [<span data-ttu-id="1540d-143">**\_ \_ descrittore flusso MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-143">**MF\_TOPONODE\_STREAM\_DESCRIPTOR**</span></span>](mf-toponode-stream-descriptor-attribute.md)             | <span data-ttu-id="1540d-144">Contiene un puntatore al descrittore di flusso per l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="1540d-144">Contains a pointer to the stream descriptor for the media source.</span></span>                                                 |
| [<span data-ttu-id="1540d-145">**\_ \_ ID WORKQUEUE MF \_ TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="1540d-145">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)                       | <span data-ttu-id="1540d-146">Specifica una coda di lavoro per un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-146">Specifies a work queue for a topology node.</span></span>                                                                       |
| [<span data-ttu-id="1540d-147">**Classe MMCSS di MF \_ TOPONODE \_ WORKQUEUE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1540d-147">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)    | <span data-ttu-id="1540d-148">Specifica un'attività MMCSS (Multimedia Class Scheduler Service) per un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-148">Specifies a Multimedia Class Scheduler Service (MMCSS) task for a topology node.</span></span>                                  |
| [<span data-ttu-id="1540d-149">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**</span><span class="sxs-lookup"><span data-stu-id="1540d-149">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | <span data-ttu-id="1540d-150">Specifica un identificatore di attività MMCSS per un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-150">Specifies a MMCSS task identifier for a topology node.</span></span>                                                            |



 

## <a name="transform-node-attributes"></a><span data-ttu-id="1540d-151">Trasforma attributi nodo</span><span class="sxs-lookup"><span data-stu-id="1540d-151">Transform Node Attributes</span></span>



| <span data-ttu-id="1540d-152">Attributo</span><span class="sxs-lookup"><span data-stu-id="1540d-152">Attribute</span></span>                                                                             | <span data-ttu-id="1540d-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1540d-153">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1540d-154">**MF \_ TOPONODE \_ D3DAWARE**</span><span class="sxs-lookup"><span data-stu-id="1540d-154">**MF\_TOPONODE\_D3DAWARE**</span></span>](mf-toponode-d3daware-attribute.md)                      | <span data-ttu-id="1540d-155">Specifica se la trasformazione associata a un nodo della topologia supporta l'accelerazione video DirectX (DXVA)</span><span class="sxs-lookup"><span data-stu-id="1540d-155">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA)</span></span> |
| [<span data-ttu-id="1540d-156">**\_ \_ scaricamento MF TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="1540d-156">**MF\_TOPONODE\_DRAIN**</span></span>](mf-toponode-drain-attribute.md)                            | <span data-ttu-id="1540d-157">Specifica quando una trasformazione viene svuotata.</span><span class="sxs-lookup"><span data-stu-id="1540d-157">Specifies when a transform is drained.</span></span>                                                                     |
| [<span data-ttu-id="1540d-158">**\_ \_ scaricamento MF TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="1540d-158">**MF\_TOPONODE\_FLUSH**</span></span>](mf-toponode-flush-attribute.md)                            | <span data-ttu-id="1540d-159">Specifica quando una trasformazione viene scaricata.</span><span class="sxs-lookup"><span data-stu-id="1540d-159">Specifies when a transform is flushed.</span></span>                                                                     |
| [<span data-ttu-id="1540d-160">**\_ \_ ObjectID trasformazione MF \_ TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="1540d-160">**MF\_TOPONODE\_TRANSFORM\_OBJECTID**</span></span>](mf-toponode-transform-objectid-attribute.md) | <span data-ttu-id="1540d-161">Identificatore di classe (CLSID) della trasformazione associata a questo nodo della topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-161">The class identifier (CLSID) of the transform associated with this topology node.</span></span>                          |



 

## <a name="output-node-attributes"></a><span data-ttu-id="1540d-162">Attributi del nodo di output</span><span class="sxs-lookup"><span data-stu-id="1540d-162">Output Node Attributes</span></span>



| <span data-ttu-id="1540d-163">Attributo</span><span class="sxs-lookup"><span data-stu-id="1540d-163">Attribute</span></span>                                                                                  | <span data-ttu-id="1540d-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1540d-164">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1540d-165">**MF \_ TOPONODE \_ Disabilita \_ preroll**</span><span class="sxs-lookup"><span data-stu-id="1540d-165">**MF\_TOPONODE\_DISABLE\_PREROLL**</span></span>](mf-toponode-disable-preroll-attribute.md)            | <span data-ttu-id="1540d-166">Specifica se la sessione multimediale usa il preroll sul sink multimediale rappresentato da questo nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-166">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>            |
| [<span data-ttu-id="1540d-167">**MF \_ TOPONODE \_ noshutdown \_ al \_ rimozione**</span><span class="sxs-lookup"><span data-stu-id="1540d-167">**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**</span></span>](mf-toponode-noshutdown-on-remove-attribute.md) | <span data-ttu-id="1540d-168">Specifica se la sessione multimediale arresta il sink multimediale quando il nodo di output viene rimosso dalla topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-168">Specifies whether the Media Session shuts down the media sink when the output node is removed from the topology.</span></span> |
| [<span data-ttu-id="1540d-169">**MF \_ TOPONODE \_ senza frequenza**</span><span class="sxs-lookup"><span data-stu-id="1540d-169">**MF\_TOPONODE\_RATELESS**</span></span>](mf-toponode-rateless-attribute.md)                           | <span data-ttu-id="1540d-170">Specifica se il sink multimediale associato a questo nodo della topologia è senza frequenza.</span><span class="sxs-lookup"><span data-stu-id="1540d-170">Specifies whether the media sink associated with this topology node is rateless.</span></span>                                 |
| [<span data-ttu-id="1540d-171">**MF \_ TOPONODE \_ STREAMID**</span><span class="sxs-lookup"><span data-stu-id="1540d-171">**MF\_TOPONODE\_STREAMID**</span></span>](mf-toponode-streamid-attribute.md)                           | <span data-ttu-id="1540d-172">Identificatore di flusso del sink di flusso associato a questo nodo della topologia.</span><span class="sxs-lookup"><span data-stu-id="1540d-172">The stream identifier of the stream sink associated with this topology node.</span></span>                                     |



 

## <a name="tee-node-attributes"></a><span data-ttu-id="1540d-173">Attributi del nodo Tee</span><span class="sxs-lookup"><span data-stu-id="1540d-173">Tee Node Attributes</span></span>



| <span data-ttu-id="1540d-174">Attributo</span><span class="sxs-lookup"><span data-stu-id="1540d-174">Attribute</span></span>                                                                  | <span data-ttu-id="1540d-175">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1540d-175">Description</span></span>                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="1540d-176">**MF \_ TOPONODE \_ PrimaryOutput poiché provocherebbe**</span><span class="sxs-lookup"><span data-stu-id="1540d-176">**MF\_TOPONODE\_PRIMARYOUTPUT**</span></span>](mf-toponode-primaryoutput-attribute.md) | <span data-ttu-id="1540d-177">Indica quale output è l'output primario in un nodo tee.</span><span class="sxs-lookup"><span data-stu-id="1540d-177">Indicates which output is the primary output on a tee node.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1540d-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1540d-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1540d-179">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="1540d-179">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="1540d-180">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1540d-180">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1540d-181">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="1540d-181">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 



