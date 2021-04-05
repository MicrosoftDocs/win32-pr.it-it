---
title: Formati di input, impostazioni di input ed estensioni di unità dati
description: Formati di input, impostazioni di input ed estensioni di unità dati
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- Windows Media Format SDK, formati di input e impostazioni
- Windows Media Format SDK, estensioni di unità dati
- Windows Media Format SDK, sistemi di estensione del payload
- ASF (Advanced Systems Format), formati e impostazioni di input
- ASF (formato avanzato dei sistemi), formati e impostazioni di input
- ASF (Advanced Systems Format), estensioni di unità dati
- ASF (formato di sistemi avanzati), estensioni di unità dati
- ASF (Advanced Systems Format), sistemi di estensione del payload
- ASF (Advanced Systems Format), sistemi di estensione del payload
- estensioni unità dati, informazioni
- sistemi di estensione del payload
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955713"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a><span data-ttu-id="f9975-114">Formati di input, impostazioni di input ed estensioni di unità dati</span><span class="sxs-lookup"><span data-stu-id="f9975-114">Input Formats, Input Settings, and Data Unit Extensions</span></span>

<span data-ttu-id="f9975-115">L'oggetto Writer supporta le impostazioni di input, i formati di input e le estensioni dell'unità dati, che consentono di controllare le funzionalità del writer.</span><span class="sxs-lookup"><span data-stu-id="f9975-115">The writer object supports input settings, input formats, and data unit extensions, all of which enable you to control features of the writer.</span></span> <span data-ttu-id="f9975-116">Non è sempre ovvio quali metodi utilizzare per controllare una funzionalità specifica.</span><span class="sxs-lookup"><span data-stu-id="f9975-116">It is not always obvious which methods to use to control a specific feature.</span></span>

<span data-ttu-id="f9975-117">I formati di input sono formati multimediali che descrivono le proprietà di base del supporto passato al writer per la codifica.</span><span class="sxs-lookup"><span data-stu-id="f9975-117">Input formats are media formats that describe the basic properties of the media that you pass to the writer for encoding.</span></span> <span data-ttu-id="f9975-118">Ad esempio, le dimensioni del frame e lo spazio colore del video di input sono descritti dal formato di input.</span><span class="sxs-lookup"><span data-stu-id="f9975-118">For example, the frame size and color space of input video is described by the input format.</span></span>

<span data-ttu-id="f9975-119">Le impostazioni di input sono caratteristiche dei dati di input oltre le nozioni di base o informazioni sulle trasformazioni da eseguire sui dati.</span><span class="sxs-lookup"><span data-stu-id="f9975-119">Input settings are characteristics of the input data beyond the basics, or information about transforms to perform on the data.</span></span> <span data-ttu-id="f9975-120">Le impostazioni video interlacciate e le informazioni su un sistema di filigrana sono esempi di impostazioni di input.</span><span class="sxs-lookup"><span data-stu-id="f9975-120">Interlaced video settings and information about a watermarking system are examples of input settings.</span></span>

<span data-ttu-id="f9975-121">Le estensioni dell'unità dati, denominate anche sistemi di estensione del payload, sono valori collegati a singoli campioni nella sezione dati del file.</span><span class="sxs-lookup"><span data-stu-id="f9975-121">Data unit extensions, also called payload extension systems, are values that are attached to individual samples in the data section of the file.</span></span> <span data-ttu-id="f9975-122">I codici temporali SMPTE e le informazioni sui pixel non quadrati sono esempi di estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="f9975-122">SMPTE time codes and non-square pixel information are examples of data unit extensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9975-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9975-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9975-124">**Configurazione di estensioni delle unità dati**</span><span class="sxs-lookup"><span data-stu-id="f9975-124">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="f9975-125">**Estensioni unità dati**</span><span class="sxs-lookup"><span data-stu-id="f9975-125">**Data Unit Extensions**</span></span>](data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="f9975-126">**Funzionalità di scrittura di file**</span><span class="sxs-lookup"><span data-stu-id="f9975-126">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="f9975-127">**Enumerazione del formato di input**</span><span class="sxs-lookup"><span data-stu-id="f9975-127">**Input Format Enumeration**</span></span>](input-format-enumeration.md)
</dt> <dt>

[<span data-ttu-id="f9975-128">**Impostazioni di input**</span><span class="sxs-lookup"><span data-stu-id="f9975-128">**Input Settings**</span></span>](input-settings.md)
</dt> <dt>

[<span data-ttu-id="f9975-129">**Utilizzo degli input**</span><span class="sxs-lookup"><span data-stu-id="f9975-129">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




