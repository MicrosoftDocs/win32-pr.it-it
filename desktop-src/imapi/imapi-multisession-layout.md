---
title: Layout multisessione IMAPi
description: IMAPi fornisce agli sviluppatori di applicazioni la possibilità di creare immagini ISO 9660 e UDF file system e di masterizzarle su CD, DVD e Blu-Ray \ 8482; supporti ottici.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104568364"
---
# <a name="imapi-multisession-layout"></a><span data-ttu-id="e9b6b-103">Layout multisessione IMAPi</span><span class="sxs-lookup"><span data-stu-id="e9b6b-103">IMAPI Multisession Layout</span></span>

<span data-ttu-id="e9b6b-104">IMAPi fornisce agli sviluppatori di applicazioni la possibilità di creare immagini ISO 9660 e UDF file system e di masterizzarle su CD, DVD e Blu-Ray™ supporti ottici.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-104">IMAPI provides application developers with the ability to create ISO 9660 and UDF file system images and burn them onto CD, DVD and Blu-Ray™ optical media.</span></span> <span data-ttu-id="e9b6b-105">Con Windows 7, IMAPi fornisce supporto aggiuntivo per la masterizzazione multisessione su DVD e Blu-Ray™ supporti riscrivibili.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-105">With Windows 7, IMAPI provides additional support for multisession burning on DVD and Blu-Ray™ rewritable media.</span></span>

<span data-ttu-id="e9b6b-106">La documentazione seguente illustra in dettaglio il layout dei dischi usato da IMAPi per implementare la multisessione.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-106">The following documentation details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="e9b6b-107">Queste informazioni devono essere utilizzate per garantire l'interoperabilità tra IMAPi e altri software di masterizzazione, nonché consentire agli sviluppatori del software di creare immagini di dischi multisessione compatibili con IMAP.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-107">This information should be used to ensure interoperability between IMAPI and other burning software as well as allow the developers of this software to create IMAPI-compatible multisession disc images.</span></span>

> [!Note]  
> <span data-ttu-id="e9b6b-108">Per un esempio dettagliato della creazione di un disco a più sessioni, vedere [creazione di un disco a più sessioni](creating-a-multisession-disc.md).</span><span class="sxs-lookup"><span data-stu-id="e9b6b-108">For an example detailing the creation of a multisession disc, see [Creating a Multisession Disc](creating-a-multisession-disc.md).</span></span>

 

## <a name="multisession-on-sequential-media"></a><span data-ttu-id="e9b6b-109">Multisessione su supporti sequenziali</span><span class="sxs-lookup"><span data-stu-id="e9b6b-109">Multisession on Sequential Media</span></span>

<span data-ttu-id="e9b6b-110">L'implementazione di IMAPi di Multisession su supporti sequenziali è supportata per l'uso con CD-R, CD-RW, DVD-R, DVD + R e Blu-Ray™ supporti.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-110">The IMAPI implementation of multisession on sequential media is supported for use with CD-R, CD-RW, DVD-R, DVD+R and Blu-Ray™ media.</span></span> <span data-ttu-id="e9b6b-111">IMAPi usa la modalità di registrazione Session-at-once per CD-RW e, di conseguenza, in questo scenario il formato è considerato un tipo di supporto sequenziale.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-111">IMAPI uses the Session-At-Once recording mode for CD-RW, and as a result, in this scenario, the format is considered a sequential media type.</span></span>

<span data-ttu-id="e9b6b-112">In uno scenario che prevede la multisessione su supporti sequenziali mediante UDF, IMAPi scrive le strutture di ancoraggio (UDF Anchor volume descrittor Pointer-avoirdupois), le strutture dei volumi (UDF Volume Descriptor Sequence-VDS) e le strutture di metadati file system (UDF file set Descriptor-FSD) all'inizio di ogni nuova sessione, come illustrato nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="e9b6b-112">In a scenario involving multisession on sequential media using UDF, IMAPI writes out the anchor structures (UDF Anchor Volume Descriptor Pointer - AVDP), volume structures (UDF Volume Descriptor Sequence - VDS) , and the file system metadata structures (UDF File Set Descriptor - FSD) at the start of every new session as outlined in the following diagram:</span></span>

![Diagramma che mostra la struttura dei metadati di file system con il punto di montaggio "Import/F S" indicato con una freccia rossa in corrispondenza dell'ancoraggio della sessione fisica 2.](images/multises1.png)

> [!Note]  
> <span data-ttu-id="e9b6b-114">Questa figura illustra il layout del disco IMAPi quando si usa UDF 2,50 con metadati ridondanti.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-114">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="e9b6b-115">I dati archiviati in un supporto registrato in sequenza sono costituiti da una serie di sessioni fisiche.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-115">The data stored on sequentially recorded media consists of a number of physical sessions.</span></span> <span data-ttu-id="e9b6b-116">Ogni sessione contiene un file system completo che rappresenta i dati utente come un set di file organizzati in directory.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-116">Each session contains a complete file system representing user data as a set of files organized in directories.</span></span> <span data-ttu-id="e9b6b-117">Il file system metadati è costituito da una serie di strutture di dati organizzate gerarchicamente.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-117">The file system metadata consists of a number of hierarchically organized data structures.</span></span> <span data-ttu-id="e9b6b-118">Nella parte superiore della gerarchia risiedono le strutture di ancoraggio (avoirdupois) situate in indirizzi di blocco logico predefiniti (LBAs).</span><span class="sxs-lookup"><span data-stu-id="e9b6b-118">At the top of the hierarchy reside anchor structures (AVDP) located at pre-defined Logical Block Addresses (LBAs).</span></span> <span data-ttu-id="e9b6b-119">Le strutture di ancoraggio specificano i percorsi delle strutture di livello successivo che non hanno indirizzi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-119">The anchor structures specify the locations of the next level structures which do not have predefined addresses.</span></span> <span data-ttu-id="e9b6b-120">Il livello successivo della gerarchia dopo le strutture di ancoraggio contiene le strutture del volume (VDS) che descrivono le proprietà del volume e fanno riferimento alle strutture di metadati file system (FSD), che a loro volta descrivono i singoli file e directory.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-120">The next level of hierarchy after anchor structures contains the volume structures (VDS) that describe the properties of the volume and referencing the file system metadata structures (FSD), which in turn describe individual files and directories.</span></span>

## <a name="multisession-on-rewritable-media"></a><span data-ttu-id="e9b6b-121">Multisessione su supporti riscrivibili</span><span class="sxs-lookup"><span data-stu-id="e9b6b-121">Multisession on Rewritable Media</span></span>

<span data-ttu-id="e9b6b-122">L'approccio per i supporti sequenziali descritti nella sezione precedente è incompatibile con i supporti riscrivibili (non sequenziali).</span><span class="sxs-lookup"><span data-stu-id="e9b6b-122">The approach for sequential media outlined in the previous section is incompatible with rewritable (non-sequential) media.</span></span> <span data-ttu-id="e9b6b-123">Questi formati multimediali includono DVD-RW, DVD + RW, DVD-RAM, Blu-Ray™ riscrivibili e altri supporti scrivibili casuali, ad esempio i dischi Iomega REV.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-123">These media formats include DVD-RW, DVD+RW, DVD-RAM, Blu-Ray™ rewritable and other random writable media, such as Iomega REV disks.</span></span> <span data-ttu-id="e9b6b-124">Il supporto riscrivibile non supporta il concetto di sessioni fisiche corrispondenti a sessioni logiche, ovvero incrementi individuali sottoposte a commit da un'applicazione Master.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-124">Rewritable media does not support the concept of physical sessions corresponding to logical sessions, which are individual increments committed by a mastering application.</span></span> <span data-ttu-id="e9b6b-125">Viene esposta una sola sessione fisica, ovvero un'area a partire dall'inizio del disco che rappresenta l'intera area indirizzabile che può contenere più sessioni logiche.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-125">Only a single physical session is exposed, which is an area starting at the beginning of the disc representing the entire addressable area that has the potential to contain multiple logical sessions.</span></span>

> [!Note]  
> <span data-ttu-id="e9b6b-126">Mentre DVD-RW è un'eccezione in quanto supporta il concetto di sessione fisica in modalità sequenziale, questa funzionalità non è attualmente supportata da IMAPi.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-126">While DVD-RW is an exception in that it supports the concept of a physical session in the Sequential mode, this capability is currently not supported by IMAPI.</span></span>

 

<span data-ttu-id="e9b6b-127">Per risolvere la mancanza di mapping uno-a-uno tra sessioni fisiche e logiche in formati riscrivibili, IMAPi Aggiorna selettivamente le strutture di ancoraggio (avoirdupois) nella *prima* sessione logica in modo che punti alle nuove strutture di volumi (VDS) e alle strutture di metadati file System (FSD) all'inizio dell' *Ultima* sessione logica, come illustrato nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="e9b6b-127">To address the lack of one-to-one mapping between physical and logical sessions on rewritable formats, IMAPI selectively updates the anchor structures (AVDP) in the *first* logical session to point to the new volume structures (VDS) and file system metadata structures (FSD) at the beginning of the *last* logical session as outlined in the following diagram:</span></span>

![Diagramma che mostra la struttura dei metadati di file system con il punto di montaggio "Import/F S" indicato con una freccia rossa in corrispondenza dell'ancoraggio della sessione logica 1.](images/multises2.png)

> [!Note]  
> <span data-ttu-id="e9b6b-129">Questa figura illustra il layout del disco IMAPi quando si usa UDF 2,50 con metadati ridondanti.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-129">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="e9b6b-130">Quando si aggiunge una nuova sessione logica a un disco riscrivibile, IMAPi determina innanzitutto la fine dell'ultima sessione logica analizzando i metadati del volume (VDS).</span><span class="sxs-lookup"><span data-stu-id="e9b6b-130">When adding a new logical session to a rewritable disc, IMAPI first determines the end of the last logical session by analyzing the volume metadata (VDS).</span></span> <span data-ttu-id="e9b6b-131">IMAPi aggiunge quindi la nuova sessione logica, completa di nuovo ancoraggio (avoirdupois), volume (VDS) e file system Metadata Structures (FSD), fisicamente contiguo con la sessione logica registrata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-131">IMAPI then adds the new logical session, complete with new anchor (AVDP), volume (VDS) and file system metadata structures (FSD), physically contiguous with the previously recorded logical session.</span></span> <span data-ttu-id="e9b6b-132">Il passaggio finale richiede l'aggiornamento delle strutture di ancoraggio (avoirdupois) all'inizio della prima sessione logica in modo che puntino alle strutture del volume (VDS) nella *nuova* sessione logica.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-132">The final step requires that the anchor structures (AVDP) at the beginning of the first logical session are updated to point to the volume structures (VDS) in the *new* logical session.</span></span> <span data-ttu-id="e9b6b-133">Il risultato operativo è identico a quello dei supporti sequenziali.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-133">The operational result is the same as with sequential media.</span></span>

## <a name="additional-recommendations"></a><span data-ttu-id="e9b6b-134">Ulteriori indicazioni</span><span class="sxs-lookup"><span data-stu-id="e9b6b-134">Additional Recommendations</span></span>

-   <span data-ttu-id="e9b6b-135">**Layout partizione**</span><span class="sxs-lookup"><span data-stu-id="e9b6b-135">**Partition Layout**</span></span>

    <span data-ttu-id="e9b6b-136">Per ottenere IMAPi compatibilità, è consigliabile che gli sviluppatori di software di terze parti usino i layout dei dischi descritti in questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-136">To achieve IMAPI compatiblity, it is recommended that third-party burning software developers use the disc layouts outlined in this documentation.</span></span> <span data-ttu-id="e9b6b-137">Gli sviluppatori devono evitare i layout con file system partizioni che occupano l'intero disco, perché ciò richiede la registrazione delle applicazioni per individuare lo spazio disponibile all'interno delle partizioni esistenti ogni volta che i dati devono essere aggiunti al disco. Spesso, le applicazioni di registrazione a questo scopo utilizzano marcatori proprietari sul disco per indicare la quantità di spazio effettivamente occupata dai dati utente.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-137">Developers should avoid layouts with file system partitions occupying the entire disc, as this requires recording applications to locate free space within existing partitions whenever data needs to be appended to the disc. Oftentimes, the recording applications accomplish this by utilizing proprietary markers on the disc to indicate how much space is actually occupied by user data.</span></span> <span data-ttu-id="e9b6b-138">Questi layout di disco non sono compatibili con IMAPi perché i marcatori proprietari non sono riconosciuti all'esterno dell'applicazione per cui sono stati creati.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-138">Such disc layouts are incompatible with IMAPI as the proprietary markers are not recognized outside of the application they were created for.</span></span>

-   <span data-ttu-id="e9b6b-139">**Tipo di partizione UDF**</span><span class="sxs-lookup"><span data-stu-id="e9b6b-139">**UDF Partition Type**</span></span>

    <span data-ttu-id="e9b6b-140">IMAPi usa il tipo di partizione UDF di **sola lettura** nell'implementazione di Multisession su supporti riscrivibili.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-140">IMAPI uses the **Read-Only** UDF partition type in its implementation of multisession on rewritable media.</span></span> <span data-ttu-id="e9b6b-141">Gli sviluppatori di software di masterizzazione di terze parti devono usare il tipo di partizione UDF di **sola lettura** per ottenere compatibilità con la masterizzazione basata su Windows tramite IMAPI.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-141">Developers of third-party burning software should use the **Read-Only** UDF partition type to achieve compatiblity with Windows mastered burning via IMAPI.</span></span> <span data-ttu-id="e9b6b-142">Se viene usato un altro tipo di partizione UDF, ad esempio **riscrivibile** , IMAPI non è in grado di fornire supporto per la master.</span><span class="sxs-lookup"><span data-stu-id="e9b6b-142">If another UDF partition type such as **Rewritable** is used, IMAPI cannot provide mastering support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9b6b-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9b6b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9b6b-144">Creazione di un disco multisessione</span><span class="sxs-lookup"><span data-stu-id="e9b6b-144">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)
</dt> <dt>

[<span data-ttu-id="e9b6b-145">**IMultisessionRandomWrite**</span><span class="sxs-lookup"><span data-stu-id="e9b6b-145">**IMultisessionRandomWrite**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




