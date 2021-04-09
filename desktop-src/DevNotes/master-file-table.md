---
description: La tabella file master (MFT) archivia le informazioni necessarie per recuperare i file da una partizione NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Tabella file master (note per gli sviluppatori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965919"
---
# <a name="master-file-table"></a><span data-ttu-id="13473-103">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="13473-103">Master File Table</span></span>

<span data-ttu-id="13473-104">\[Questo documento si applica solo alla versione 3 dei volumi NTFS.\]</span><span class="sxs-lookup"><span data-stu-id="13473-104">\[This document applies only to version 3 of NTFS volumes.\]</span></span>

<span data-ttu-id="13473-105">La tabella file master (MFT) archivia le informazioni necessarie per recuperare i file da una partizione NTFS.</span><span class="sxs-lookup"><span data-stu-id="13473-105">The master file table (MFT) stores the information required to retrieve files from an NTFS partition.</span></span>

<span data-ttu-id="13473-106">Un file può avere uno o più record MFT e può contenere uno o più attributi.</span><span class="sxs-lookup"><span data-stu-id="13473-106">A file may have one or more MFT records, and can contain one or more attributes.</span></span> <span data-ttu-id="13473-107">In NTFS un riferimento al file è il riferimento del segmento MFT del record del file di base.</span><span class="sxs-lookup"><span data-stu-id="13473-107">In NTFS, a file reference is the MFT segment reference of the base file record.</span></span> <span data-ttu-id="13473-108">Per altre informazioni, vedere [**\_ \_ riferimento al segmento MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="13473-108">For more information, see [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

<span data-ttu-id="13473-109">Il file MFT contiene segmenti di record di file; i primi 16 di questi elementi sono riservati per i file speciali, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="13473-109">The MFT contains file record segments; the first 16 of these are reserved for special files, such as the following:</span></span>

-   <span data-ttu-id="13473-110">0: MFT ($Mft)</span><span class="sxs-lookup"><span data-stu-id="13473-110">0: MFT ($Mft)</span></span>
-   <span data-ttu-id="13473-111">5: directory radice ( \\ )</span><span class="sxs-lookup"><span data-stu-id="13473-111">5: root directory (\\)</span></span>
-   <span data-ttu-id="13473-112">6: file di allocazione cluster del volume ($Bitmap)</span><span class="sxs-lookup"><span data-stu-id="13473-112">6: volume cluster allocation file ($Bitmap)</span></span>
-   <span data-ttu-id="13473-113">8: file del cluster non valido ($BadClus)</span><span class="sxs-lookup"><span data-stu-id="13473-113">8: bad-cluster file ($BadClus)</span></span>

<span data-ttu-id="13473-114">Ogni segmento di record di file inizia con un'intestazione di segmento di record di file.</span><span class="sxs-lookup"><span data-stu-id="13473-114">Each file record segment starts with a file record segment header.</span></span> <span data-ttu-id="13473-115">Per altre informazioni, vedere [**\_ intestazione del \_ segmento \_ di record di file**](file-record-segment-header.md).</span><span class="sxs-lookup"><span data-stu-id="13473-115">For more information, see [**FILE\_RECORD\_SEGMENT\_HEADER**](file-record-segment-header.md).</span></span> <span data-ttu-id="13473-116">Ogni segmento di record di file è seguito da uno o più attributi.</span><span class="sxs-lookup"><span data-stu-id="13473-116">Each file record segment is followed by one or more attributes.</span></span> <span data-ttu-id="13473-117">Ogni attributo inizia con un'intestazione di record di attributo.</span><span class="sxs-lookup"><span data-stu-id="13473-117">Each attribute starts with an attribute record header.</span></span> <span data-ttu-id="13473-118">Per altre informazioni, vedere [**\_ \_ header record attribute**](attribute-record-header.md).</span><span class="sxs-lookup"><span data-stu-id="13473-118">For more information, see [**ATTRIBUTE\_RECORD\_HEADER**](attribute-record-header.md).</span></span> <span data-ttu-id="13473-119">Il record di attributo include il tipo di attributo, ad esempio $DATA o $BITMAP, un nome facoltativo e il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="13473-119">The attribute record includes the attribute type (such as $DATA or $BITMAP), an optional name, and the attribute value.</span></span> <span data-ttu-id="13473-120">Il flusso di dati utente è un attributo, così come tutti i flussi.</span><span class="sxs-lookup"><span data-stu-id="13473-120">The user data stream is an attribute, as are all streams.</span></span> <span data-ttu-id="13473-121">L'elenco di attributi viene terminato con 0xFFFFFFFF ($END).</span><span class="sxs-lookup"><span data-stu-id="13473-121">The attribute list is terminated with 0xFFFFFFFF ($END).</span></span>

<span data-ttu-id="13473-122">Di seguito sono riportati alcuni attributi di esempio.</span><span class="sxs-lookup"><span data-stu-id="13473-122">The following are some example attributes.</span></span>

-   <span data-ttu-id="13473-123">Il file di $Mft contiene un attributo $DATA senza nome che corrisponde alla sequenza dei segmenti di record MFT, in ordine.</span><span class="sxs-lookup"><span data-stu-id="13473-123">The $Mft file contains an unnamed $DATA attribute that is the sequence of MFT record segments, in order.</span></span>
-   <span data-ttu-id="13473-124">Il file di $Mft contiene un attributo $BITMAP senza nome che indica quali record MFT sono in uso.</span><span class="sxs-lookup"><span data-stu-id="13473-124">The $Mft file contains an unnamed $BITMAP attribute that indicates which MFT records are in use.</span></span>
-   <span data-ttu-id="13473-125">Il file di $Bitmap contiene un attributo $DATA senza nome che indica i cluster in uso.</span><span class="sxs-lookup"><span data-stu-id="13473-125">The $Bitmap file contains an unnamed $DATA attribute that indicates which clusters are in use.</span></span>
-   <span data-ttu-id="13473-126">Il file di $BadClus contiene un attributo $DATA denominato $BAD contenente una voce corrispondente a ogni cluster non valido.</span><span class="sxs-lookup"><span data-stu-id="13473-126">The $BadClus file contains a $DATA attribute named $BAD that contains an entry that corresponds to each bad cluster.</span></span>

<span data-ttu-id="13473-127">Quando non è più disponibile spazio per l'archiviazione degli attributi nel segmento di record di file, i segmenti di record di file aggiuntivi vengono allocati e inseriti nel primo segmento di record di file (o base) in un attributo denominato elenco attributi.</span><span class="sxs-lookup"><span data-stu-id="13473-127">When there is no more space for storing attributes in the file record segment, additional file record segments are allocated and inserted in the first (or base) file record segment in an attribute called the attribute list.</span></span> <span data-ttu-id="13473-128">L'elenco di attributi indica dove è possibile trovare ogni attributo associato al file.</span><span class="sxs-lookup"><span data-stu-id="13473-128">The attribute list indicates where each attribute associated with the file can be found.</span></span> <span data-ttu-id="13473-129">Sono inclusi tutti gli attributi nel record del file di base, ad eccezione dell'elenco di attributi.</span><span class="sxs-lookup"><span data-stu-id="13473-129">This includes all attributes in the base file record, except for the attribute list itself.</span></span> <span data-ttu-id="13473-130">Per ulteriori informazioni, vedere [**\_ \_ voce elenco attributi**](attribute-list-entry.md).</span><span class="sxs-lookup"><span data-stu-id="13473-130">For more information, see [**ATTRIBUTE\_LIST\_ENTRY**](attribute-list-entry.md).</span></span>

<span data-ttu-id="13473-131">Le strutture correlate a MFT includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="13473-131">Structures related to the MFT include the following:</span></span>

-   [<span data-ttu-id="13473-132">**\_voce elenco \_ attributi**</span><span class="sxs-lookup"><span data-stu-id="13473-132">**ATTRIBUTE\_LIST\_ENTRY**</span></span>](attribute-list-entry.md)
-   [<span data-ttu-id="13473-133">**\_intestazione record \_ attributo**</span><span class="sxs-lookup"><span data-stu-id="13473-133">**ATTRIBUTE\_RECORD\_HEADER**</span></span>](attribute-record-header.md)
-   [<span data-ttu-id="13473-134">**\_nome file**</span><span class="sxs-lookup"><span data-stu-id="13473-134">**FILE\_NAME**</span></span>](file-name.md)
-   [<span data-ttu-id="13473-135">**\_ \_ intestazione segmento record \_ file**</span><span class="sxs-lookup"><span data-stu-id="13473-135">**FILE\_RECORD\_SEGMENT\_HEADER**</span></span>](file-record-segment-header.md)
-   [<span data-ttu-id="13473-136">**\_riferimento al segmento MFT \_**</span><span class="sxs-lookup"><span data-stu-id="13473-136">**MFT\_SEGMENT\_REFERENCE**</span></span>](mft-segment-reference.md)
-   [<span data-ttu-id="13473-137">**\_intestazione multisettore \_**</span><span class="sxs-lookup"><span data-stu-id="13473-137">**MULTI\_SECTOR\_HEADER**</span></span>](multi-sector-header.md)
-   [<span data-ttu-id="13473-138">**\_informazioni standard**</span><span class="sxs-lookup"><span data-stu-id="13473-138">**STANDARD\_INFORMATION**</span></span>](standard-information.md)

## <a name="related-topics"></a><span data-ttu-id="13473-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13473-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="13473-140">[Riferimento tecnico per NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="13473-140">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

 
