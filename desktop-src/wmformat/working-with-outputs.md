---
title: Uso degli output
description: Uso degli output
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media Format SDK, uso degli output
- Formato di sistemi avanzati (ASF), utilizzo degli output
- ASF (Advanced Systems Format), utilizzo di output
- ASF (Advanced Systems Format), numeri di output e formati
- ASF (formato avanzato dei sistemi), numeri e formati di output
- numeri di output e formati, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723455"
---
# <a name="working-with-outputs"></a><span data-ttu-id="b872e-109">Uso degli output</span><span class="sxs-lookup"><span data-stu-id="b872e-109">Working with Outputs</span></span>

<span data-ttu-id="b872e-110">Per impostazione predefinita, ogni esempio ricevuto da uno dei due oggetti Reader è associato a un numero di output.</span><span class="sxs-lookup"><span data-stu-id="b872e-110">As a default, every sample you receive from either reader object is associated with an output number.</span></span> <span data-ttu-id="b872e-111">Ogni numero di output corrisponde a un flusso nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="b872e-111">Each output number corresponds to a stream in the ASF file.</span></span> <span data-ttu-id="b872e-112">Il lettore assegna i numeri di output ai flussi nel file quando il file viene aperto.</span><span class="sxs-lookup"><span data-stu-id="b872e-112">The reader assigns output numbers to the streams in the file when the file is opened.</span></span> <span data-ttu-id="b872e-113">In genere è presente un output per ogni flusso in un file.</span><span class="sxs-lookup"><span data-stu-id="b872e-113">Normally there is one output for each stream in a file.</span></span> <span data-ttu-id="b872e-114">Se il file usa l'esclusione reciproca, tuttavia, a ogni gruppo di flussi che si escludono a vicenda viene assegnato un singolo numero di output.</span><span class="sxs-lookup"><span data-stu-id="b872e-114">If the file uses mutual exclusion, however, each group of mutually exclusive streams is assigned a single output number.</span></span> <span data-ttu-id="b872e-115">Il flusso che corrisponde al numero di output dei flussi che si escludono a vicenda è determinato dal lettore, nel caso di file con velocità in bit multipla (MBR) o dall'applicazione, se si utilizza la selezione del flusso manuale.</span><span class="sxs-lookup"><span data-stu-id="b872e-115">The stream that corresponds to the output number of the mutually exclusive streams is determined either by the reader, in the case of multiple bit rate (MBR) files, or by your application, if you are using manual stream selection.</span></span>

<span data-ttu-id="b872e-116">Poiché il nome della connessione impostato nel profilo non è salvato in modo permanente nel file, il Reader crea un nome di connessione predefinito per ogni output che è semplicemente una rappresentazione di stringa del numero di output, ad esempio "1", "2", "3" e così via.</span><span class="sxs-lookup"><span data-stu-id="b872e-116">Because the connection name set in the profile is not persisted in the file, the reader creates a default connection name for each output that is simply a string representation of the output number, for example "1", "2", "3" and so on.</span></span> <span data-ttu-id="b872e-117">I nomi di connessione consentono alle applicazioni e al lettore stesso di correlare gli output ai flussi.</span><span class="sxs-lookup"><span data-stu-id="b872e-117">The connection names enable applications, and the reader itself, to correlate outputs to streams.</span></span> <span data-ttu-id="b872e-118">In un file a più velocità in bit, diversi flussi condividono un nome di connessione.</span><span class="sxs-lookup"><span data-stu-id="b872e-118">In a multiple bit rate file, several streams share a connection name.</span></span> <span data-ttu-id="b872e-119">Questa operazione non è rilevante per il lettore, perché le proprietà di output per ogni flusso MBR sono identiche.</span><span class="sxs-lookup"><span data-stu-id="b872e-119">This does not matter to the reader, because the output properties for each MBR stream are identical.</span></span>

<span data-ttu-id="b872e-120">Ogni output ha uno o più formati di output supportati.</span><span class="sxs-lookup"><span data-stu-id="b872e-120">Each output has one or more supported output formats.</span></span> <span data-ttu-id="b872e-121">Un formato di output è il formato utilizzato dai campioni non compressi forniti dal reader.</span><span class="sxs-lookup"><span data-stu-id="b872e-121">An output format is the format that the uncompressed samples delivered by the reader use.</span></span> <span data-ttu-id="b872e-122">Quando il lettore apre un file, imposta il formato di ogni output sul valore predefinito per il sottotipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="b872e-122">When the reader opens a file, it sets the format of each output to the default for the media subtype.</span></span> <span data-ttu-id="b872e-123">Il numero e il tipo di formati di output supportati sono determinati dal codec che decomprime i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="b872e-123">The number and type of output formats supported is determined by the codec that decompresses the media data.</span></span>

<span data-ttu-id="b872e-124">Negli argomenti seguenti viene illustrato come utilizzare gli output:</span><span class="sxs-lookup"><span data-stu-id="b872e-124">The following topics explain how to work with outputs:</span></span>

-   [<span data-ttu-id="b872e-125">Per identificare i numeri di output</span><span class="sxs-lookup"><span data-stu-id="b872e-125">To Identify Output Numbers</span></span>](to-identify-output-numbers.md)
-   [<span data-ttu-id="b872e-126">Assegnazione di formati di output</span><span class="sxs-lookup"><span data-stu-id="b872e-126">Assigning Output Formats</span></span>](assigning-output-formats.md)

## <a name="related-topics"></a><span data-ttu-id="b872e-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b872e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b872e-128">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="b872e-128">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="b872e-129">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="b872e-129">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="b872e-130">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="b872e-130">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




