---
description: Barra di divisione ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Barra di divisione ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128003"
---
# <a name="asf-splitter"></a><span data-ttu-id="7cfd1-103">Barra di divisione ASF</span><span class="sxs-lookup"><span data-stu-id="7cfd1-103">ASF Splitter</span></span>

<span data-ttu-id="7cfd1-104">L'oggetto *splitter* ASF è un componente di livello WMContainer che analizza l'oggetto dati ASF di un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="7cfd1-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="7cfd1-105">È possibile utilizzare la barra di divisione per leggere i pacchetti di dati nell'oggetto dati e generare esempi di flusso.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-105">You can use the splitter to read the data packets in the Data Object and generate stream samples.</span></span> <span data-ttu-id="7cfd1-106">Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7cfd1-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="7cfd1-107">La barra di divisione espone l'interfaccia [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-107">The splitter exposes the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span> <span data-ttu-id="7cfd1-108">La barra di divisione analizza i pacchetti di dati ASF per i flussi selezionati e li riassembla in singoli oggetti di esempio che espongono l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-108">The splitter parses ASF data packets for the selected streams and repackages them into individual sample objects that expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="7cfd1-109">La barra di divisione è uno dei componenti a livello di piattaforma di Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-109">The splitter is one of the platform-level components of Media Foundation.</span></span> <span data-ttu-id="7cfd1-110">Per analizzare i file ASF, l'origine dei supporti ASF usa internamente la barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-110">The ASF media source uses the splitter internally to parse ASF files.</span></span>

<span data-ttu-id="7cfd1-111">Il diagramma seguente illustra la generazione di esempi per un file ASF tramite la barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-111">The following diagram illustrates sample generation for an ASF file through the splitter.</span></span>

![diagramma che illustra la generazione di esempio di un file ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

<span data-ttu-id="7cfd1-113">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="7cfd1-113">This section contains the following topics:</span></span>



| <span data-ttu-id="7cfd1-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="7cfd1-114">Topic</span></span>                                                                                                                        | <span data-ttu-id="7cfd1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cfd1-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="7cfd1-116">Creazione dell'oggetto Splitter ASF</span><span class="sxs-lookup"><span data-stu-id="7cfd1-116">Creating the ASF Splitter Object</span></span>](creating-the-asf-splitter-object.md)                                                     | <span data-ttu-id="7cfd1-117">Come creare e inizializzare la barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-117">How to create and initialize the splitter.</span></span>                              |
| [<span data-ttu-id="7cfd1-118">Configurazione dell'oggetto Splitter ASF</span><span class="sxs-lookup"><span data-stu-id="7cfd1-118">Configuring the ASF Splitter Object</span></span>](configuring-the-asf-splitter-object.md)                                               | <span data-ttu-id="7cfd1-119">Impostazioni di configurazione per la barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-119">Configuration settings for the splitter.</span></span>                                |
| [<span data-ttu-id="7cfd1-120">Generazione di esempi di flusso da un oggetto dati ASF esistente</span><span class="sxs-lookup"><span data-stu-id="7cfd1-120">Generating Stream Samples from an Existing ASF Data Object</span></span>](generating-stream-samples-from-an-existing-asf-data-object.md) | <span data-ttu-id="7cfd1-121">Come analizzare l'oggetto dati ASF e generare esempi di vapore in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-121">How to parse the ASF Data Object and generate packetized steam samples.</span></span> |



 

<span data-ttu-id="7cfd1-122">Nella tabella seguente vengono illustrati gli attributi dell'oggetto dati rilevanti.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-122">The following table shows the relevant Data Object attributes.</span></span>



| <span data-ttu-id="7cfd1-123">Attributo</span><span class="sxs-lookup"><span data-stu-id="7cfd1-123">Attribute</span></span>                                                                                                    | <span data-ttu-id="7cfd1-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cfd1-124">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cfd1-125">**\_ \_ \_ pacchetti FileProperties ASF MF \_ PD**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-125">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)                   | <span data-ttu-id="7cfd1-126">Numero di pacchetti di dati nell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-126">Number of data packets in the ASF Data Object.</span></span>                                                       |
| [<span data-ttu-id="7cfd1-127">**\_ \_ \_ \_ dimensioni minime del \_ pacchetto \_ per le proprietà ASF del valore MF PD ASF**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-127">**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | <span data-ttu-id="7cfd1-128">Dimensioni minime dei pacchetti di dati nel file, in byte.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-128">Minimum size of the data packets in the file, in bytes.</span></span>                                              |
| [<span data-ttu-id="7cfd1-129">**\_dimensioni del \_ \_ \_ pacchetto max PD ASF FileProperties \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-129">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | <span data-ttu-id="7cfd1-130">Dimensioni massime dei pacchetti di dati nel file, in byte</span><span class="sxs-lookup"><span data-stu-id="7cfd1-130">Maximum size of the data packets in the file, in bytes</span></span>                                               |
| [<span data-ttu-id="7cfd1-131">**\_ \_ \_ lunghezza dei dati MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-131">**MF\_PD\_ASF\_DATA\_LENGTH**</span></span>](mf-pd-asf-data-length-attribute.md)                                         | <span data-ttu-id="7cfd1-132">Dimensioni dell'oggetto dati ASF, in byte.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-132">Size of the ASF Data Object, in bytes.</span></span>                                                               |
| [<span data-ttu-id="7cfd1-133">**\_ \_ \_ \_ offset avvio dati ASF MF PD \_**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-133">**MF\_PD\_ASF\_DATA\_START\_OFFSET**</span></span>](mf-pd-asf-data-start-offset-attribute.md)                            | <span data-ttu-id="7cfd1-134">Offset, in byte, per il primo pacchetto di dati nell'oggetto dati ASF relativo all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-134">Offset, in bytes, to the first data packet in the ASF Data Object relative to the start of the file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7cfd1-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cfd1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cfd1-136">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="7cfd1-136">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="7cfd1-137">Esercitazione: lettura di un file ASF</span><span class="sxs-lookup"><span data-stu-id="7cfd1-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="7cfd1-138">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7cfd1-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



