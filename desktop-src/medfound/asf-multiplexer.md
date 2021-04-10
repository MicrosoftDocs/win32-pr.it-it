---
description: Multiplexer ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexer ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049327"
---
# <a name="asf-multiplexer"></a><span data-ttu-id="567a6-103">Multiplexer ASF</span><span class="sxs-lookup"><span data-stu-id="567a6-103">ASF Multiplexer</span></span>

<span data-ttu-id="567a6-104">Il *multiplexing* ASF è un oggetto livello WMContainer che funziona con l' [oggetto dati ASF](asf-file-structure.md) e fornisce a un'applicazione la possibilità di generare pacchetti di dati per un contenitore ASF.</span><span class="sxs-lookup"><span data-stu-id="567a6-104">The ASF *multiplexer* is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate data packets for an ASF container.</span></span> <span data-ttu-id="567a6-105">Il multiplexer accetta dati multimediali sotto forma di [esempi di supporti](media-samples.md) e genera esempi di supporti basati sui parametri dei pacchetti ASF e di streaming definiti nell' [oggetto intestazione ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="567a6-105">The multiplexer accepts media data in the form of [Media Samples](media-samples.md) and outputs media samples based on streaming and ASF packet parameters defined in the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="567a6-106">Gli esempi di supporti di output contengono riferimenti a uno o più buffer multimediali contenenti dati multimediali digitali in pacchetto. È possibile utilizzare questo oggetto in uno scenario di codifica dei file in cui vengono ricevuti esempi di flusso codificati dal codificatore o per la transcodifica ASF-ASF (remuxing).</span><span class="sxs-lookup"><span data-stu-id="567a6-106">The output media samples hold references to one or more media buffers that contain packetized digital media data.You can use this object in a file encoding scenario where it receives encoded stream samples from the encoder or for ASF-ASF transcoding (remuxing).</span></span>

<span data-ttu-id="567a6-107">Il diagramma seguente illustra la generazione di pacchetti di dati ASF per un file ASF usando multiplexer.</span><span class="sxs-lookup"><span data-stu-id="567a6-107">The following diagram illustrates ASF data packet generation for an ASF file using the multiplexer.</span></span>

![diagramma che mostra la generazione di pacchetti di dati ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

<span data-ttu-id="567a6-109">Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="567a6-109">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="567a6-110">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="567a6-110">This section contains the following topics:</span></span>



| <span data-ttu-id="567a6-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="567a6-111">Topic</span></span>                                                                  | <span data-ttu-id="567a6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="567a6-112">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="567a6-113">Creazione dell'oggetto multiplexer</span><span class="sxs-lookup"><span data-stu-id="567a6-113">Creating the Multiplexer Object</span></span>](creating-the-multiplexer-object.md) | <span data-ttu-id="567a6-114">Come creare e inizializzare il multiplexer.</span><span class="sxs-lookup"><span data-stu-id="567a6-114">How to create and initialize the multiplexer.</span></span>                     |
| [<span data-ttu-id="567a6-115">Generazione di nuovi pacchetti di dati ASF</span><span class="sxs-lookup"><span data-stu-id="567a6-115">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md) | <span data-ttu-id="567a6-116">Come generare pacchetti di dati per costituire un nuovo oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="567a6-116">How to generate data packets to constitute a new ASF Data Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="567a6-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="567a6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="567a6-118">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="567a6-118">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="567a6-119">Esercitazione: copia di flussi ASF da un file a un altro</span><span class="sxs-lookup"><span data-stu-id="567a6-119">Tutorial: Copying ASF Streams from One File to Another</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="567a6-120">Esercitazione: scrittura di un file WMA usando la codifica CBR</span><span class="sxs-lookup"><span data-stu-id="567a6-120">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



