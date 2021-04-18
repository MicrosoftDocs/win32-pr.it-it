---
title: Nuova API consente alle app di inviare hint "TRIM e annullare" ai supporti di archiviazione
description: La nuova API consente alle app di inviare \ 0034; TRIM e annullare \ 0034; Suggerimenti per i supporti di archiviazione
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300562"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a><span data-ttu-id="5bee8-103">Nuova API consente alle app di inviare hint "TRIM e annullare" ai supporti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5bee8-103">New API allows apps to send "TRIM and Unmap" hints to storage media</span></span>

## <a name="platforms"></a><span data-ttu-id="5bee8-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="5bee8-104">Platforms</span></span>

<span data-ttu-id="5bee8-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="5bee8-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="5bee8-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5bee8-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="5bee8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bee8-107">Description</span></span>

<span data-ttu-id="5bee8-108">Gli hint TRIM segnalano all'unità che determinati settori precedentemente allocati non sono più necessari per l'app e possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="5bee8-108">TRIM hints notify the drive that certain sectors that previously were allocated are no longer needed by the app and can be purged.</span></span> <span data-ttu-id="5bee8-109">Questa operazione viene in genere usata quando un'app esegue allocazioni di spazio di grandi dimensioni tramite un file e quindi gestisce automaticamente le allocazioni al file, ad esempio i file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="5bee8-109">This is typically used when an app makes large space allocations via a file and then self-manages the allocations to the file (for example, Virtual Hard Disk files).</span></span>

<span data-ttu-id="5bee8-110">**Che cos'è TRIM?**</span><span class="sxs-lookup"><span data-stu-id="5bee8-110">**What is TRIM?**</span></span>

<span data-ttu-id="5bee8-111">Le unità SSD (Solid State Drive) sono in genere dispositivi con cancellazione blocchi basata sulla memoria flash; Ciò significa che quando i dati vengono scritti nell'unità SSD, non possono essere sovrascritti sul posto e devono essere scritti altrove fino a quando il blocco non può essere sottoposto a Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="5bee8-111">Solid state drives (SSDs) are typically flash memory based block-erased devices; this means that when data is written to the SSD, it cannot be over-written in place and must be written elsewhere until the block can be garbage collected.</span></span> <span data-ttu-id="5bee8-112">Poiché l'unità SSD non dispone di un meccanismo interno per determinare che determinati blocchi sono stati rimossi e ne sono necessari altri.</span><span class="sxs-lookup"><span data-stu-id="5bee8-112">Since the SSD has no internal mechanism for determining that certain blocks are removed and others are needed.</span></span> <span data-ttu-id="5bee8-113">L'unica volta in cui l'unità SSD può contrassegnare un settore ' Dirty ' è quando viene sovrascritta.</span><span class="sxs-lookup"><span data-stu-id="5bee8-113">The only time the SSD can mark a sector ‘dirty’ is when it is over-written.</span></span> <span data-ttu-id="5bee8-114">In altri casi, ad esempio quando un file viene eliminato, l'unità SSD mantiene questi settori perché l'eliminazione viene eseguita come solo modifica della tabella file master (MFT) e non come operazione a tutti i settori del file.</span><span class="sxs-lookup"><span data-stu-id="5bee8-114">In other cases, such as when a file is deleted, the SSD retains these sectors because the deletion is performed as a master file table (MFT) change only, and not as an operation to all the sectors of the file.</span></span> <span data-ttu-id="5bee8-115">In Windows 7 è stato introdotto un modo standard per comunicare con le unità SSD sui settori che non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="5bee8-115">In Windows 7, we introduced a standard way of communicating with SSDs about sectors that are not needed any more.</span></span> <span data-ttu-id="5bee8-116">Questo comando è definito nella [specifica T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) come comando Trim; NTFS invia il comando TRIM per alcune operazioni inline normali, ad esempio "DeleteFile".</span><span class="sxs-lookup"><span data-stu-id="5bee8-116">This command is defined in the [T13 specification](https://www.t13.org/Standards/Default.aspx?DocumentType=3) as the TRIM command; NTFS sends the TRIM command for some normal inline operations such as “deletefile.”</span></span>

<span data-ttu-id="5bee8-117">**Altri usi del TRIM nell'ambiente di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="5bee8-117">**Other uses of TRIM in the storage world**</span></span>

<span data-ttu-id="5bee8-118">Come le unità SSD, le reti San (Storage Area Network) e le nuove implementazioni di spazi software per le funzionalità di Windows 8 utilizzano hint di comando TRIM per gestire gli spazi in ambienti con thin provisioning.</span><span class="sxs-lookup"><span data-stu-id="5bee8-118">Like SSDs, storage area networks (SANs) and the new Windows 8 feature Software Spaces implementations consume TRIM command hints to manage their spaces in thinly provisioned environments.</span></span> <span data-ttu-id="5bee8-119">Gli spazi San e software allocano le aree di archiviazione in dimensioni maggiori di settori o cluster (da 1 MB a 1 GB).</span><span class="sxs-lookup"><span data-stu-id="5bee8-119">SANs and Software Spaces allocate regions of storage in sizes that are greater than sectors or clusters (anywhere from 1MB to 1GB).</span></span> <span data-ttu-id="5bee8-120">Quando ricevono hint TRIM per la dimensione di allocazione (o maggiore delle dimensioni di allocazione), la SAN/unità SSD può deallocare un'area per liberare spazio per gli altri file.</span><span class="sxs-lookup"><span data-stu-id="5bee8-120">When they receive TRIM hints for its allocation size (or greater than the allocation size), the SAN/SSD can de-allocate a region to free up the space for other files.</span></span> <span data-ttu-id="5bee8-121">In genere passano tutti gli hint TRIM ai supporti sottostanti (SSD o HDD), in modo che possano utilizzare lo spazio liberato in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="5bee8-121">They typically pass through all TRIM hints to the underlying media (SSD or HDD) so that they can consume the freed up space as appropriate.</span></span> <span data-ttu-id="5bee8-122">In genere non spostano i dati nelle aree deallocate, né tengono traccia delle aree di riduzione delle aree deallocate (quando l'area è vuota).</span><span class="sxs-lookup"><span data-stu-id="5bee8-122">They do not typically move data around to de-allocate regions, nor do they keep track of TRIM areas to de-allocated regions (when the region is empty).</span></span>

<span data-ttu-id="5bee8-123">Le reti San con thin provisioning usano gli hint TRIM che vengono passati per ridurre il footprint di archiviazione fisico complessivo, riducendo di conseguenza i costi.</span><span class="sxs-lookup"><span data-stu-id="5bee8-123">Thinly provisioned SANs use the TRIM hints that are passed to them to help reduce the overall physical storage footprint, hence reducing cost.</span></span> <span data-ttu-id="5bee8-124">La [specifica SCSI T10](https://www.t10.org) definisce il comando ' annullare ' (simile al comando Trim); qui il comando è applicabile a tutti i tipi di archiviazione, tra cui HDD, SSD e altri.</span><span class="sxs-lookup"><span data-stu-id="5bee8-124">The [T10 SCSI specification](https://www.t10.org) defines the ‘Unmap’ command (similar to the TRIM command); here the command is applicable to all kinds of storage including HDDs, SSDs, and others.</span></span> <span data-ttu-id="5bee8-125">Il comando annullare consente di rimuovere i blocchi fisici dall'allocazione della SAN.</span><span class="sxs-lookup"><span data-stu-id="5bee8-125">The UnMap command helps to remove physical blocks from the SAN’s allocation.</span></span>

## <a name="how-to-use-the-new-api"></a><span data-ttu-id="5bee8-126">Come usare la nuova API</span><span class="sxs-lookup"><span data-stu-id="5bee8-126">How to use the new API</span></span>


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



<span data-ttu-id="5bee8-127">L'eliminazione dei file viene passata tramite il buffer, se possibile, o in modo asincrono (non memorizzato nel buffer) al TRIM del comando IOCTL del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bee8-127">File TRIM is passed via the buffer if possible or asynchronously (non-buffered) to the Device IOCTL DSM command TRIM.</span></span> <span data-ttu-id="5bee8-128">Viene eseguito il mapping al comando TRIM per i dispositivi ATA e il comando annullare per i dispositivi SCSI.</span><span class="sxs-lookup"><span data-stu-id="5bee8-128">This is mapped to the TRIM command for ATA devices and UnMap command for SCSI devices.</span></span> <span data-ttu-id="5bee8-129">Il codice per l'eliminazione dei file Invia le aree una alla volta come specificato dagli extent precedenti.</span><span class="sxs-lookup"><span data-stu-id="5bee8-129">The file TRIM code sends the regions one-by-one as specified by the extents above.</span></span>

<span data-ttu-id="5bee8-130">Il TRIM del file non attende il ritorno dal dispositivo, perché i comandi TRIM e annullare sono definiti come hint per il supporto di archiviazione sottostante e i codici restituiti non sono previsti.</span><span class="sxs-lookup"><span data-stu-id="5bee8-130">File TRIM does not wait for returns from the device, because the TRIM and Unmap commands are defined as hints to the underlying storage media and return codes are not expected.</span></span>

<span data-ttu-id="5bee8-131">**Flusso di lavoro end-to-end:**</span><span class="sxs-lookup"><span data-stu-id="5bee8-131">**End-to-end workflow:**</span></span>

1.  <span data-ttu-id="5bee8-132">Taglia file di chiamata</span><span class="sxs-lookup"><span data-stu-id="5bee8-132">Call File Trim</span></span>
    1.  <span data-ttu-id="5bee8-133">TRIM file esamina gli input per gli errori</span><span class="sxs-lookup"><span data-stu-id="5bee8-133">File TRIM examines inputs for errors</span></span>
    2.  <span data-ttu-id="5bee8-134">Il TRIM del file suddivide gli extent nelle aree LCN</span><span class="sxs-lookup"><span data-stu-id="5bee8-134">File TRIM breaks up the extents into LCN regions</span></span>
    3.  <span data-ttu-id="5bee8-135">Il TRIM del file viene arrotondato per eccesso per le aree allineate a mis che vengono passate in TRIM</span><span class="sxs-lookup"><span data-stu-id="5bee8-135">File TRIM rounds up and down for mis-aligned regions that are passed into TRIM</span></span>
    4.  <span data-ttu-id="5bee8-136">Il TRIM del file Elimina le voci della cache correlate alle aree di taglio</span><span class="sxs-lookup"><span data-stu-id="5bee8-136">File TRIM purges entries in the cache that relate to the TRIM areas</span></span>
    5.  <span data-ttu-id="5bee8-137">Il TRIM file passa il \_ DSM IOCTL (Trim) per area</span><span class="sxs-lookup"><span data-stu-id="5bee8-137">File TRIM passes IOCTL\_DSM (Trim) per region</span></span>
2.  <span data-ttu-id="5bee8-138">Restituzione o errori di eliminazione file</span><span class="sxs-lookup"><span data-stu-id="5bee8-138">File TRIM returns or errors</span></span>
    1.  <span data-ttu-id="5bee8-139">Il controllo degli errori viene eseguito sulla validità dell'input</span><span class="sxs-lookup"><span data-stu-id="5bee8-139">Error checking is done on input validity</span></span>
    2.  <span data-ttu-id="5bee8-140">Se solo alcuni degli extent sono validi, viene restituito un errore per la chiamata API completa</span><span class="sxs-lookup"><span data-stu-id="5bee8-140">If only some of the extents are valid, one error is returned for the complete API call</span></span>

<span data-ttu-id="5bee8-141">**Casi d'uso**</span><span class="sxs-lookup"><span data-stu-id="5bee8-141">**Use cases**</span></span>

<span data-ttu-id="5bee8-142">**Disco rigido virtuale (VHD) del consumer montato su un'unità SSD:**</span><span class="sxs-lookup"><span data-stu-id="5bee8-142">**Consumer virtual hard disk (VHD) mounted on an SSD:**</span></span>

<span data-ttu-id="5bee8-143">Il disco rigido virtuale viene inizialmente montato sul supporto inutilizzato ' clean '.</span><span class="sxs-lookup"><span data-stu-id="5bee8-143">The VHD is initially mounted on ‘clean’ unused media.</span></span> <span data-ttu-id="5bee8-144">Quando si usa il disco rigido virtuale, il disco rigido virtuale utilizza parti del supporto di archiviazione per i file e così via. Quando elimina i file nei supporti di archiviazione, questi file non vengono rimossi dall'unità SSD poiché il VHD completo viene archiviato come un unico file nell'unità SSD.</span><span class="sxs-lookup"><span data-stu-id="5bee8-144">As the VHD is used, the VHD consumes parts of the storage media for files, etc. When it deletes files in the storage media, these files are not removed from the SSD since the complete VHD is stored as one file on the SSD.</span></span> <span data-ttu-id="5bee8-145">L'ambiente Hyper-V chiama il TRIM dei file per tutte le aree eliminate quando si verifica delete-file nell'ambiente VHD.</span><span class="sxs-lookup"><span data-stu-id="5bee8-145">The Hyper-V environment calls File TRIM for all regions that are deleted when delete-file occurs in the VHD environment.</span></span> <span data-ttu-id="5bee8-146">I trim dei file \_ vengono convertiti nell'unità SSD in modo da ottimizzare le prestazioni dell'unità SSD.</span><span class="sxs-lookup"><span data-stu-id="5bee8-146">The File\_TRIMs are translated to the SSD so that the SSD performance can be optimized.</span></span>

<span data-ttu-id="5bee8-147">**VHD del consumer montato su una SAN con thin provisioning:**</span><span class="sxs-lookup"><span data-stu-id="5bee8-147">**Consumer VHD mounted on a thinly provisioned SAN:**</span></span>

<span data-ttu-id="5bee8-148">Il disco rigido virtuale viene inizialmente montato in una lastra minima di un ambiente con thin provisioning.</span><span class="sxs-lookup"><span data-stu-id="5bee8-148">The VHD is initially mounted on one minimum slab of a thinly provisioned environment.</span></span> <span data-ttu-id="5bee8-149">Man mano che i file vengono archiviati nel disco rigido virtuale, il footprint di archiviazione del disco rigido virtuale cresce in multipli di lastre.</span><span class="sxs-lookup"><span data-stu-id="5bee8-149">As files are stored in the VHD, the storage footprint of the VHD grows in multiples of slabs.</span></span> <span data-ttu-id="5bee8-150">Quando i file vengono rimossi nel disco rigido virtuale, Hyper-V chiama il trim del file alla SAN sottoposta \_ a thin provisioning sottostante.</span><span class="sxs-lookup"><span data-stu-id="5bee8-150">When files are removed in the VHD, the Hyper-V calls File\_TRIM to the underlying thinly provisioned SAN.</span></span> <span data-ttu-id="5bee8-151">Se i TRIM sono più grandi della granularità di lastra, la SAN può ora rimuovere una lastra e quindi ridurre il footprint del disco rigido virtuale su tale SAN.</span><span class="sxs-lookup"><span data-stu-id="5bee8-151">If the TRIMs are bigger than the SLAB granularity, the SAN can now remove a SLAB and hence reduce the footprint of the VHD on that SAN.</span></span>

<span data-ttu-id="5bee8-152">Se il disco rigido virtuale è residente in un server basato su Windows 8, l'utilità di ottimizzazione dell'archiviazione invierà anche i TRIM per ridurre il footprint del disco rigido virtuale dall'interno del VHD montato.</span><span class="sxs-lookup"><span data-stu-id="5bee8-152">If the VHD is resident on a Windows 8 based server, the Storage Optimizer will also send TRIMs to reduce the slab footprint of the VHD from within the mounted VHD.</span></span>

## <a name="tests"></a><span data-ttu-id="5bee8-153">Test</span><span class="sxs-lookup"><span data-stu-id="5bee8-153">Tests</span></span>

<span data-ttu-id="5bee8-154">Nelle versioni precedenti del sistema operativo non sono presenti API confrontabili.</span><span class="sxs-lookup"><span data-stu-id="5bee8-154">There are no comparable APIs in earlier operating system releases.</span></span> <span data-ttu-id="5bee8-155">L'API effettiva non dovrebbe avere alcun effetto sulle prestazioni, anche se il supporto di archiviazione (se implementato correttamente) può mostrare migliori prestazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="5bee8-155">There should be no performance impact from the actual API itself, though the storage media (if implemented correctly) can show better write performance.</span></span> <span data-ttu-id="5bee8-156">L'API deve essere usata con molta attenzione. solo gli extent non più necessari devono essere passati perché tali extent verranno rimossi definitivamente dal supporto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5bee8-156">The API should be used very carefully; only extents that are no longer needed should be passed down as those extents will be permanently removed from the storage media.</span></span>

## <a name="resources"></a><span data-ttu-id="5bee8-157">Risorse</span><span class="sxs-lookup"><span data-stu-id="5bee8-157">Resources</span></span>

-   [<span data-ttu-id="5bee8-158">Specifica T13</span><span class="sxs-lookup"><span data-stu-id="5bee8-158">T13 specification</span></span>](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [<span data-ttu-id="5bee8-159">Specifica SCSI T10</span><span class="sxs-lookup"><span data-stu-id="5bee8-159">T10 SCSI specification</span></span>](https://www.t10.org/)

 

 




