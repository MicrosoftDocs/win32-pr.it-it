---
title: Estensioni unità dati
description: Estensioni unità dati
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media Format SDK, estensioni di unità dati
- ASF (Advanced Systems Format), estensioni di unità dati
- ASF (formato di sistemi avanzati), estensioni di unità dati
- Windows Media Format SDK, sistemi di estensione del payload
- ASF (Advanced Systems Format), sistemi di estensione del payload
- ASF (Advanced Systems Format), sistemi di estensione del payload
- estensioni unità dati, informazioni
- estensioni unità di payload
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723495"
---
# <a name="data-unit-extensions"></a><span data-ttu-id="772a3-111">Estensioni unità dati</span><span class="sxs-lookup"><span data-stu-id="772a3-111">Data Unit Extensions</span></span>

<span data-ttu-id="772a3-112">Windows Media Format SDK consente di integrare i dati negli esempi con le *estensioni di unità dati*, denominate anche sistemi di estensione del payload.</span><span class="sxs-lookup"><span data-stu-id="772a3-112">The Windows Media Format SDK enables you to supplement data in samples with *data unit extensions*, also called payload extension systems.</span></span> <span data-ttu-id="772a3-113">Questa documentazione usa il termine "estensioni dell'unità dati" per mantenere la coerenza con i nomi dei metodi, ad esempio [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="772a3-113">This documentation uses the term "data unit extensions" in order to remain consistent with method names such as [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span> <span data-ttu-id="772a3-114">Un'estensione dell'unità dati è una coppia nome/valore collegata all'esempio nella sezione dati del file.</span><span class="sxs-lookup"><span data-stu-id="772a3-114">A data unit extension is a name/value pair that is attached to the sample in the data section of the file.</span></span> <span data-ttu-id="772a3-115">È possibile accedere ai dati estesi utilizzando i metodi dell'oggetto buffer quando l'esempio viene recuperato dal reader.</span><span class="sxs-lookup"><span data-stu-id="772a3-115">You can access the extended data using methods of the buffer object when the sample is retrieved by the reader.</span></span>

<span data-ttu-id="772a3-116">È possibile creare estensioni di unità dati per le specifiche, ma molti tipi sono predefiniti e supportati dagli oggetti di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="772a3-116">You can create data unit extensions to your own specifications, but several types are predefined and supported by the objects of this SDK.</span></span> <span data-ttu-id="772a3-117">Queste estensioni standard vengono usate per fornire dati aggiuntivi per i nomi di file (nei flussi di script e Web), i dati del codice in tempo SMPTE, le proporzioni dei pixel non quadrati, la durata e il tipo di interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="772a3-117">These standard extensions are used to provide additional data for file names (in script and Web streams), SMPTE time code data, non-square pixel aspect ratio, duration, and type of interlacing.</span></span>

<span data-ttu-id="772a3-118">Per usare le estensioni dell'unità dati, è necessario configurare il flusso per accettarle e quindi aggiungere estensioni a ogni esempio per il flusso.</span><span class="sxs-lookup"><span data-stu-id="772a3-118">To use data unit extensions, you must configure the stream to accept them, and then add extensions to each sample for that stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="772a3-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="772a3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="772a3-120">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="772a3-120">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="772a3-121">**Configurazione di estensioni delle unità dati**</span><span class="sxs-lookup"><span data-stu-id="772a3-121">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="772a3-122">**Impostazione delle estensioni delle unità dati**</span><span class="sxs-lookup"><span data-stu-id="772a3-122">**Setting Data Unit Extensions**</span></span>](setting-data-unit-extensions.md)
</dt> </dl>

 

 




