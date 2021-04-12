---
title: Enumerazione del formato di input
description: Enumerazione del formato di input
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media Format SDK, enumerazioni del formato di input
- Windows Media Format SDK, enumerazione dei formati di input
- Advanced Systems Format (ASF), enumerazioni del formato di input
- ASF (formato avanzato dei sistemi), enumerazioni del formato di input
- Formato di sistemi avanzati (ASF), enumerazione dei formati di input
- ASF (Advanced Systems Format), enumerazione dei formati di input
- enumerazioni del formato di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471694"
---
# <a name="input-format-enumeration"></a><span data-ttu-id="3efa1-110">Enumerazione del formato di input</span><span class="sxs-lookup"><span data-stu-id="3efa1-110">Input Format Enumeration</span></span>

<span data-ttu-id="3efa1-111">L'oggetto writer ottiene le informazioni sul formato del flusso dal profilo fornito.</span><span class="sxs-lookup"><span data-stu-id="3efa1-111">The writer object gets stream format information from the profile you give it.</span></span> <span data-ttu-id="3efa1-112">Il flusso di informazioni di configurazione in un profilo fornisce al writer tutte le informazioni necessarie sulla modalità di scrittura dei dati nel file.</span><span class="sxs-lookup"><span data-stu-id="3efa1-112">Stream configuration information in a profile gives the writer all of the information it needs about how the data is to be written in the file.</span></span> <span data-ttu-id="3efa1-113">Il profilo non fornisce al writer informazioni sul formato degli esempi di input che l'applicazione recapita.</span><span class="sxs-lookup"><span data-stu-id="3efa1-113">The profile does not provide the writer with any information about the format of the input samples that your application delivers.</span></span> <span data-ttu-id="3efa1-114">I formati di input saranno sconosciuti solo per i flussi compressi con uno dei codec Windows Media. gli input per i tipi di flusso arbitrari sono prevedibili in base alle informazioni contenute nel profilo.</span><span class="sxs-lookup"><span data-stu-id="3efa1-114">Input formats will be unknown only for streams compressed with one of the Windows Media codecs; inputs for arbitrary stream types are predictable based on the information in the profile.</span></span>

<span data-ttu-id="3efa1-115">L'oggetto writer può comunicare con il codec per un flusso per determinare i tipi di input che è possibile usare.</span><span class="sxs-lookup"><span data-stu-id="3efa1-115">The writer object can communicate with the codec for a stream to determine the input types that can be used.</span></span> <span data-ttu-id="3efa1-116">Vengono forniti metodi per enumerare i possibili tipi di input.</span><span class="sxs-lookup"><span data-stu-id="3efa1-116">Methods are provided to enumerate the possible input types.</span></span> <span data-ttu-id="3efa1-117">È sempre necessario trovare il tipo di input che corrisponde al supporto di input enumerando i tipi supportati anziché impostare manualmente le proprietà del supporto di input.</span><span class="sxs-lookup"><span data-stu-id="3efa1-117">You should always find the input type that matches your input media by enumerating the supported types rather than setting the input media properties manually.</span></span> <span data-ttu-id="3efa1-118">Per ulteriori informazioni, vedere [per enumerare i formati di input](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="3efa1-118">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3efa1-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3efa1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3efa1-120">**Funzionalità di scrittura di file**</span><span class="sxs-lookup"><span data-stu-id="3efa1-120">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="3efa1-121">**Utilizzo degli input**</span><span class="sxs-lookup"><span data-stu-id="3efa1-121">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




