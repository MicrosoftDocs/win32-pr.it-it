---
title: Formati di disco
description: IMAPi supporta tre formati file system ISO 9660, Joliet e UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330087"
---
# <a name="disc-formats"></a><span data-ttu-id="1f8be-103">Formati di disco</span><span class="sxs-lookup"><span data-stu-id="1f8be-103">Disc Formats</span></span>

<span data-ttu-id="1f8be-104">IMAPi supporta tre formati di file system: [ISO 9660](#iso-9660), [Joliet](#joliet)e [UDF](#universal-disk-format-udf).</span><span class="sxs-lookup"><span data-stu-id="1f8be-104">IMAPI supports three file system formats: [ISO 9660](#iso-9660), [Joliet](#joliet), and [UDF](#universal-disk-format-udf).</span></span>

## <a name="iso-9660"></a><span data-ttu-id="1f8be-105">ISO 9660</span><span class="sxs-lookup"><span data-stu-id="1f8be-105">ISO 9660</span></span>

<span data-ttu-id="1f8be-106">Il formato ISO 9660 è il file system standard originale per i dischi di dati CD.</span><span class="sxs-lookup"><span data-stu-id="1f8be-106">The ISO 9660 format is the original standard file system for CD data discs.</span></span> <span data-ttu-id="1f8be-107">Il formato è riconosciuto su diversi sistemi operativi, tra cui MSDOS, il Mac OS, UNIX e il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="1f8be-107">The format is recognized on several operating systems, including MSDOS, the Mac OS, UNIX, and the Windows operating system.</span></span> <span data-ttu-id="1f8be-108">Il formato ISO 9660 è pubblicato dal organizzazione internazionale per la standardizzazione (ISO).</span><span class="sxs-lookup"><span data-stu-id="1f8be-108">The ISO 9660 format is published by the International Organization for Standardization (ISO).</span></span>

<span data-ttu-id="1f8be-109">Il formato inizia in corrispondenza del settore 16 con l'intestazione del volume, CD0001; il resto dell'intestazione segue.</span><span class="sxs-lookup"><span data-stu-id="1f8be-109">The format begins at sector 16 with the volume header, CD0001; the remainder of the header follows.</span></span> <span data-ttu-id="1f8be-110">Anche altri formati derivati iniziano nel settore 16, ma usano un'altra stringa per l'intestazione del volume.</span><span class="sxs-lookup"><span data-stu-id="1f8be-110">Other derived formats also begin at sector 16, but use another string for the volume header.</span></span> <span data-ttu-id="1f8be-111">Ad esempio, i dischi High Sierra usano la stringa CD-ROM0001 e Compact Disc Interactive Format USA CD-I0001.</span><span class="sxs-lookup"><span data-stu-id="1f8be-111">For example, High Sierra discs use the string CD-ROM0001 and Compact Disc Interactive format uses CD-I0001.</span></span>

<span data-ttu-id="1f8be-112">L'intestazione punta alle aree del disco in cui sono archiviati i nomi dei file in formato ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="1f8be-112">The header points to areas of the disc that store the file names in ISO 9660 format.</span></span> <span data-ttu-id="1f8be-113">La convenzione di denominazione di file e directory è costituita da 8 caratteri, un punto e altri 3 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f8be-113">The file and directory naming convention consists of 8 characters, a period, and 3 more characters.</span></span> <span data-ttu-id="1f8be-114">Si tratta della stessa convenzione di denominazione utilizzata dal sistema operativo MSDOS.</span><span class="sxs-lookup"><span data-stu-id="1f8be-114">This is the same naming convention used by the MSDOS operating system.</span></span>

<span data-ttu-id="1f8be-115">Intestazioni file system aggiuntive, per formati come Joliet e UDF, possono coesistere in un disco senza influire sulla leggibilità del formato ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="1f8be-115">Additional file system headers, for formats such as Joliet and UDF, can co-exist on a disc without affecting the readability of the ISO 9660 format.</span></span> <span data-ttu-id="1f8be-116">Dopo gli indici, un set di file di dati occupa il disco. Gli indici per ogni file system i file di dati di riferimento in modo indipendente nel disco.</span><span class="sxs-lookup"><span data-stu-id="1f8be-116">After the indexes, a set of data files occupy the disc. The indexes for each file system independently reference data files on the disc.</span></span>

<span data-ttu-id="1f8be-117">La specifica ISO 9660 definisce tre livelli del formato:</span><span class="sxs-lookup"><span data-stu-id="1f8be-117">The ISO 9660 specification defines three levels of the format:</span></span>

-   <span data-ttu-id="1f8be-118">Il livello 1 definisce i nomi di file per l'utilizzo del formato carattere 8,3.</span><span class="sxs-lookup"><span data-stu-id="1f8be-118">Level 1 defines file names to use the 8.3 character format.</span></span>
-   <span data-ttu-id="1f8be-119">Il livello 2 consente nomi di file più lunghi, come si trova nelle piattaforme DOS 6. XX, MacIntosh e UNIX.</span><span class="sxs-lookup"><span data-stu-id="1f8be-119">Level 2 permits longer file names, as found on DOS 6.xx, MacIntosh, and UNIX platforms.</span></span>
-   <span data-ttu-id="1f8be-120">Il livello 3 consente ai file di dati e audio con interfoliazione di migliorare le prestazioni di recupero (riproduzione).</span><span class="sxs-lookup"><span data-stu-id="1f8be-120">Level 3 allows interleaved data and audio files to improve retrieval (playback) performance.</span></span> <span data-ttu-id="1f8be-121">Questo livello consente inoltre di rimuovere il limite di file da 2 GB.</span><span class="sxs-lookup"><span data-stu-id="1f8be-121">This level also removes the 2GB file limit.</span></span> <span data-ttu-id="1f8be-122">Questo livello **non** è supportato dall'API per la creazione di immagini master.</span><span class="sxs-lookup"><span data-stu-id="1f8be-122">This level is **not** supported by the Image Mastering API.</span></span>

<span data-ttu-id="1f8be-123">I dischi DVD possono anche usare ISO 9660; Tuttavia, la file system UDF è la file system più prevalente utilizzata con supporti DVD.</span><span class="sxs-lookup"><span data-stu-id="1f8be-123">DVD discs can also use ISO 9660; however, the UDF file system is the most prevalent file system used with DVD media.</span></span>

## <a name="joliet"></a><span data-ttu-id="1f8be-124">Joliet</span><span class="sxs-lookup"><span data-stu-id="1f8be-124">Joliet</span></span>

<span data-ttu-id="1f8be-125">Il formato Joliet è un derivato di ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="1f8be-125">The Joliet format is a derivative of ISO 9660.</span></span> <span data-ttu-id="1f8be-126">Questo formato scrive l'indice Joliet file system nell'immagine del disco, oltre all'indice file system ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="1f8be-126">This format writes the Joliet file system index to the disc image in addition to the ISO 9660 file system index.</span></span>

<span data-ttu-id="1f8be-127">L'indice Joliet fornisce i miglioramenti seguenti all'indice file system:</span><span class="sxs-lookup"><span data-stu-id="1f8be-127">The Joliet index provides the following improvements to the file system index:</span></span>

-   <span data-ttu-id="1f8be-128">Riconosce i nomi di file lunghi fino a 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f8be-128">Recognizes long file names up to 32 characters.</span></span>
-   <span data-ttu-id="1f8be-129">Distingue le lettere maiuscole e minuscole nei nomi dei file.</span><span class="sxs-lookup"><span data-stu-id="1f8be-129">Distinguishes between upper and lower case letters in the file names.</span></span>
-   <span data-ttu-id="1f8be-130">Supporta i caratteri Unicode nel nome file.</span><span class="sxs-lookup"><span data-stu-id="1f8be-130">Supports Unicode characters in the filename.</span></span>

<span data-ttu-id="1f8be-131">L'intestazione del formato Joliet inizia al settore 17 del disco.</span><span class="sxs-lookup"><span data-stu-id="1f8be-131">The Joliet format header begins at sector 17 of the disc.</span></span>

<span data-ttu-id="1f8be-132">Poiché il formato Joliet conserva la file system ISO 9660 su un disco, viene mantenuta la compatibilità con i dispositivi conformi a ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="1f8be-132">Because the Joliet format preserves the ISO 9660 file system on a disc, compatibility with ISO 9660-compliant devices is retained.</span></span>

## <a name="universal-disk-format-udf"></a><span data-ttu-id="1f8be-133">Universal Disk Format (UDF)</span><span class="sxs-lookup"><span data-stu-id="1f8be-133">Universal Disk Format (UDF)</span></span>

<span data-ttu-id="1f8be-134">Il formato UDF (Universal Disk Format) è un file system più recente sviluppato per supporti ottici da Optical Storage Technology Association (OSTA).</span><span class="sxs-lookup"><span data-stu-id="1f8be-134">The Universal Disk Format (UDF) is a newer file system developed for optical media by the Optical Storage Technology Association (OSTA).</span></span> <span data-ttu-id="1f8be-135">UDF è un formato portatile riconosciuto da diversi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="1f8be-135">UDF is a portable format that is recognized by several operating systems.</span></span> <span data-ttu-id="1f8be-136">La funzione UDF sostituisce ISO 9660 come nuovo standard, soprattutto con i supporti di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1f8be-136">UDF is replacing ISO 9660 as the new standard, especially with read/write media.</span></span>

<span data-ttu-id="1f8be-137">Le funzionalità di UDF includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1f8be-137">Features of UDF include the following:</span></span>

-   <span data-ttu-id="1f8be-138">Supporta supporti fino a 2 TB di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1f8be-138">Supports media up to 2TB in size.</span></span>
-   <span data-ttu-id="1f8be-139">Supporta Flash Media, dischi Iomega REV e dischi CD-MRW.</span><span class="sxs-lookup"><span data-stu-id="1f8be-139">Supports flash media, Iomega REV discs, and CD-MRW discs.</span></span>
-   <span data-ttu-id="1f8be-140">Archivia i file di lunghezza inferiore a 2 KB nel blocco di immissione file.</span><span class="sxs-lookup"><span data-stu-id="1f8be-140">Stores files less than 2 KB in length in the File Entry block.</span></span>
-   <span data-ttu-id="1f8be-141">Supporta file fino a 2 TB con nomi di file di lunghezza pari a 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f8be-141">Supports files up to 2TB with filenames as long as 255 characters.</span></span>
-   <span data-ttu-id="1f8be-142">Supporta un set completo di attributi di file adatti a diversi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="1f8be-142">Supports a rich set of file attributes that suit various operating systems.</span></span>
-   <span data-ttu-id="1f8be-143">Supporta un formato Bridge in cui tutti i formati ISO 9660, Joliet e UDF si trovano nello stesso disco. Questa operazione viene usata nelle applicazioni video, ad esempio DVD-video, DVD + VR e DVD-VR.</span><span class="sxs-lookup"><span data-stu-id="1f8be-143">Supports a bridge format where ISO 9660, Joliet, and UDF formats all reside on the same disc. This is used in video applications, such as DVD-Video, DVD+VR, and DVD-VR.</span></span>
-   <span data-ttu-id="1f8be-144">Supporta i flussi denominati e i file in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="1f8be-144">Supports named streams and 'Real-Time' files.</span></span>

 

 




