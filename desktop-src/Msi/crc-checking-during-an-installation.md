---
description: Con Windows Installer è disponibile un controllo di ridondanza ciclico (CRC) dei file.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Verifica CRC durante un'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232682"
---
# <a name="crc-checking-during-an-installation"></a><span data-ttu-id="891ff-103">Verifica CRC durante un'installazione</span><span class="sxs-lookup"><span data-stu-id="891ff-103">CRC Checking During an Installation</span></span>

<span data-ttu-id="891ff-104">Con Windows Installer è disponibile un controllo di ridondanza ciclico (CRC) dei file.</span><span class="sxs-lookup"><span data-stu-id="891ff-104">A Cyclic Redundancy Check (CRC) of files is available with Windows Installer.</span></span> <span data-ttu-id="891ff-105">Il controllo CRC è un meccanismo di controllo degli errori, simile a un checksum, che consente a un'applicazione di determinare se le informazioni in un file sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="891ff-105">CRC checking is an error-checking mechanism, similar to a checksum, that enables an application to determine whether the information in a file has been modified.</span></span> <span data-ttu-id="891ff-106">Al termine della copia di un file, il Windows Installer ottiene un valore CRC dai file di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="891ff-106">After the Windows Installer finishes copying a file, it gets a CRC value from both the source and destination files.</span></span> <span data-ttu-id="891ff-107">Il programma di installazione controlla il CRC originale timbrato nel file e lo confronta con il CRC calcolato dalla copia.</span><span class="sxs-lookup"><span data-stu-id="891ff-107">The installer checks the original CRC stamped into the file and compares this to the CRC calculated from the copy.</span></span> <span data-ttu-id="891ff-108">Il controllo CRC ha esito negativo se il valore CRC originale non è null ed è diverso dal CRC calcolato per la copia.</span><span class="sxs-lookup"><span data-stu-id="891ff-108">The CRC check fails if the original CRC value is non-null and is different from the CRC calculated on the copy.</span></span> <span data-ttu-id="891ff-109">Se il CRC originale è null, non viene eseguito alcun controllo.</span><span class="sxs-lookup"><span data-stu-id="891ff-109">If the original CRC is null, no check occurs.</span></span>

<span data-ttu-id="891ff-110">Il Windows Installer esegue un controllo CRC su un file nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="891ff-110">The Windows Installer does a CRC check on a file in the following cases:</span></span>

-   <span data-ttu-id="891ff-111">Se la [Proprietà MSICHECKCRCS](msicheckcrcs.md) è impostata e **msidbFileAttributesChecksum** è incluso nel campo Attributes del record del file nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="891ff-111">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md).</span></span> <span data-ttu-id="891ff-112">Il programma di installazione esegue il controllo CRC una volta dopo l'installazione, la duplicazione o lo stato di trasferimento del file.</span><span class="sxs-lookup"><span data-stu-id="891ff-112">The installer does the CRC check once after installing, duplicating, or moving the file.</span></span>
-   <span data-ttu-id="891ff-113">Se la [Proprietà MSICHECKCRCS](msicheckcrcs.md) è impostata e **msidbFileAttributesChecksum** è incluso nel campo Attributes del record del file nella [tabella file](file-table.md), il programma di installazione esegue un controllo CRC dopo l'applicazione di patch al file.</span><span class="sxs-lookup"><span data-stu-id="891ff-113">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check after patching the file.</span></span>
-   <span data-ttu-id="891ff-114">Se il **msidbFileAttributesChecksum** è incluso nel campo attributi del record del file nella [tabella file](file-table.md), il programma di installazione esegue un controllo CRC prima di associare le immagini.</span><span class="sxs-lookup"><span data-stu-id="891ff-114">If the **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check before binding images.</span></span>

<span data-ttu-id="891ff-115">Se il controllo ha esito negativo prima di associare un'immagine, il programma di installazione segnala i due errori seguenti nel file di log e continua l'installazione senza associare il file.</span><span class="sxs-lookup"><span data-stu-id="891ff-115">If the check fails before binding an image, the installer reports the following two errors in the log file and continues the installation without binding the file.</span></span>



| <span data-ttu-id="891ff-116">Codice</span><span class="sxs-lookup"><span data-stu-id="891ff-116">Code</span></span> | <span data-ttu-id="891ff-117">Message</span><span class="sxs-lookup"><span data-stu-id="891ff-117">Message</span></span>                                               |
|------|-------------------------------------------------------|
| <span data-ttu-id="891ff-118">2941</span><span class="sxs-lookup"><span data-stu-id="891ff-118">2941</span></span> | <span data-ttu-id="891ff-119">Non è possibile calcolare il CRC per il file \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="891ff-119">Unable to compute the CRC for file \[2\].</span></span>             |
| <span data-ttu-id="891ff-120">2942</span><span class="sxs-lookup"><span data-stu-id="891ff-120">2942</span></span> | <span data-ttu-id="891ff-121">L'azione azione BindImage sul non è stata eseguita su \[ 2 \] file.</span><span class="sxs-lookup"><span data-stu-id="891ff-121">BindImage action has not been executed on \[2\] file.</span></span> |



 

<span data-ttu-id="891ff-122">Se il controllo ha esito negativo dopo la copia, la duplicazione o la correzione di un file non compresso, il programma di installazione segnala l'errore seguente.</span><span class="sxs-lookup"><span data-stu-id="891ff-122">If the check fails after an uncompressed file had been copied, duplicated, or patched, the installer reports the following error.</span></span> <span data-ttu-id="891ff-123">Questo errore viene inoltre segnalato se il controllo ha esito negativo dopo la copia di un file compresso.</span><span class="sxs-lookup"><span data-stu-id="891ff-123">This error is also reported if the check fails after a compressed file is copied.</span></span> <span data-ttu-id="891ff-124">Se il file ha l'attributo **msidbFileAttributesVital** , il file è considerato vitale per l'installazione e l'utente ottiene l'opzione per riprovare o annullare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="891ff-124">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the user gets the option to retry or cancel the installation.</span></span> <span data-ttu-id="891ff-125">Se il file è contrassegnato come non vitale nella colonna attributi della [tabella file](file-table.md), l'utente può ignorare l'errore e continuare, riprovare o annullare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="891ff-125">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user may ignore the error and continue, retry, or cancel the installation.</span></span>



| <span data-ttu-id="891ff-126">Codice</span><span class="sxs-lookup"><span data-stu-id="891ff-126">Code</span></span> | <span data-ttu-id="891ff-127">Message</span><span class="sxs-lookup"><span data-stu-id="891ff-127">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="891ff-128">1331</span><span class="sxs-lookup"><span data-stu-id="891ff-128">1331</span></span> | <span data-ttu-id="891ff-129">Non è stato possibile copiare correttamente \[ 2 \] file: errore CRC.</span><span class="sxs-lookup"><span data-stu-id="891ff-129">Failed to correctly copy \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="891ff-130">Si noti che vengono spostati solo i file non compressi.</span><span class="sxs-lookup"><span data-stu-id="891ff-130">Note that only uncompressed files are moved.</span></span> <span data-ttu-id="891ff-131">Se il controllo ha esito negativo dopo lo spostamento di un file non compresso, il programma di installazione visualizzerà il seguente errore.</span><span class="sxs-lookup"><span data-stu-id="891ff-131">If the check fails after an uncompressed file is moved, the installer displays the following error.</span></span> <span data-ttu-id="891ff-132">Se il file ha l'attributo **msidbFileAttributesVital** , il file è considerato vitale per l'installazione e l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="891ff-132">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="891ff-133">Se il file è contrassegnato come non vitale nella colonna attributi della [tabella file](file-table.md), l'utente ottiene l'opzione per annullare o ignorare l'errore e continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="891ff-133">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="891ff-134">Codice</span><span class="sxs-lookup"><span data-stu-id="891ff-134">Code</span></span> | <span data-ttu-id="891ff-135">Message</span><span class="sxs-lookup"><span data-stu-id="891ff-135">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="891ff-136">1332</span><span class="sxs-lookup"><span data-stu-id="891ff-136">1332</span></span> | <span data-ttu-id="891ff-137">Non è stato possibile spostare correttamente \[ 2 \] file: errore CRC.</span><span class="sxs-lookup"><span data-stu-id="891ff-137">Failed to correctly move \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="891ff-138">Se il controllo ha esito negativo dopo la correzione di un file non compresso, il programma di installazione visualizzerà il seguente errore.</span><span class="sxs-lookup"><span data-stu-id="891ff-138">If the check fails after an uncompressed file is patched, the installer displays the following error.</span></span> <span data-ttu-id="891ff-139">Se il file ha l'attributo **msidbFileAttributesVital** , il file è considerato vitale per l'installazione e l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="891ff-139">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="891ff-140">Se il file è contrassegnato come non vitale nella colonna attributi della [tabella file](file-table.md), l'utente ottiene l'opzione per annullare o ignorare l'errore e continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="891ff-140">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="891ff-141">Codice</span><span class="sxs-lookup"><span data-stu-id="891ff-141">Code</span></span> | <span data-ttu-id="891ff-142">Message</span><span class="sxs-lookup"><span data-stu-id="891ff-142">Message</span></span>                                          |
|------|--------------------------------------------------|
| <span data-ttu-id="891ff-143">1333</span><span class="sxs-lookup"><span data-stu-id="891ff-143">1333</span></span> | <span data-ttu-id="891ff-144">Non è stato possibile correggere correttamente la patch \[ 2 \] file: errore CRC.</span><span class="sxs-lookup"><span data-stu-id="891ff-144">Failed to correctly patch \[2\] file: CRC error.</span></span> |



 

 

 



