---
description: La versione di PATCHWIZ.DLL rilasciata con Windows Installer&\# 160; 3.0 può generare automaticamente informazioni di sequenziazione delle patch e aggiungere alla tabella MsiPatchSequence una nuova patch.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Generazione di informazioni sulla sequenza di patch (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967800"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a><span data-ttu-id="81046-103">Generazione di informazioni sulla sequenza di patch (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="81046-103">Generating Patch Sequence Information (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="81046-104">La versione di [PATCHWIZ.DLL](patchwiz-dll.md) rilasciata con Windows Installer 3,0 può generare automaticamente informazioni di sequenziazione delle patch e aggiungere alla [tabella MsiPatchSequence](msipatchsequence-table.md) una nuova patch.</span><span class="sxs-lookup"><span data-stu-id="81046-104">The version of [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 can automatically generate patch sequencing information and add to the [MsiPatchSequence Table](msipatchsequence-table.md) a new patch.</span></span>

<span data-ttu-id="81046-105">Impostare la \_ \_ \_ Proprietà disabilitata generazione dati sequenza su 1 (uno) nella [tabella delle proprietà](properties-table-patchwiz-dll-.md) del file con estensione PCP per evitare la generazione automatica di informazioni di sequenziazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="81046-105">Set the SEQUENCE\_DATA\_GENERATION\_DISABLED property to 1 (one) in the [Properties Table](properties-table-patchwiz-dll-.md) of the .pcp file to prevent the automatic generation of patch sequencing information.</span></span> <span data-ttu-id="81046-106">Se questa proprietà è assente, le informazioni vengono generate e aggiunte automaticamente.</span><span class="sxs-lookup"><span data-stu-id="81046-106">If this property is absent, the information is automatically generated and added.</span></span>

<span data-ttu-id="81046-107">Quando il [PATCHWIZ.DLL](patchwiz-dll.md) rilasciato con Windows Installer 3,0 viene usato per generare automaticamente le informazioni di sequenziazione della patch, si verifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="81046-107">When the [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 is used to automatically generate the patch sequencing information, the following occurs:</span></span>

-   <span data-ttu-id="81046-108">Viene aggiunta una nuova riga alla [tabella MsiPatchSequence](msipatchsequence-table.md) per ogni codice prodotto di un'immagine di destinazione elencata nella [tabella TargetImages](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="81046-108">A new row is added to the [MsiPatchSequence Table](msipatchsequence-table.md) for each product code of a target image that is listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="81046-109">I valori aggiunti alla colonna PatchFamily nelle nuove righe corrispondono ai codici prodotto di destinazione delle immagini di destinazione elencate nella [tabella TargetImages](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="81046-109">The values added to the PatchFamily column in the new rows correspond to the target product codes of the target images that are listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="81046-110">I valori aggiunti alle colonne di sequenza nelle nuove righe vengono generati utilizzando la versione del prodotto più elevata di destinazione della patch e l'ora UTC in cui viene generata la patch.</span><span class="sxs-lookup"><span data-stu-id="81046-110">The values added to the Sequence columns in the new rows are generated using the highest product version targeted by the patch and the UTC time when the patch is generated.</span></span> <span data-ttu-id="81046-111">Il numero di sequenza è <Product Minor Version> . <Build Major Number> . <Time Stamp 1>. <timestamp 2>.</span><span class="sxs-lookup"><span data-stu-id="81046-111">The sequence number is <Product Minor Version>.<Build Major Number>.<Time Stamp 1>.<Time Stamp 2>.</span></span>
    -   <span data-ttu-id="81046-112">Il primo campo è la versione del prodotto della versione più recente del prodotto a cui è destinata la patch.</span><span class="sxs-lookup"><span data-stu-id="81046-112">The first field is the product version of the highest version of the product that is targeted by the patch.</span></span>
    -   <span data-ttu-id="81046-113">Il secondo campo è il numero di build principale della versione più recente del prodotto a cui è destinata la patch.</span><span class="sxs-lookup"><span data-stu-id="81046-113">The second field is the build major number of the highest version of the product that is targeted by the patch.</span></span>

    <span data-ttu-id="81046-114">I due campi timestamp rappresentano il timestamp di 32 bit necessario per conteggiare i secondi nell'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="81046-114">The two time stamp fields account for the 32 bit time stamp that is needed to count the seconds in Coordinated Universal Time (UTC).</span></span>
    > [!Note]  
    > <span data-ttu-id="81046-115">Le versioni del prodotto hanno il formato seguente: <Product Major Version> . <Product Minor Version> . <Build Major Number> . <Build Minor Number> e un prodotto con un numero di versione 2.1.0.0 è una versione successiva a un prodotto con numero di versione 1.2.0.0</span><span class="sxs-lookup"><span data-stu-id="81046-115">Product versions have the following format: <Product Major Version>.<Product Minor Version>.<Build Major Number>.<Build Minor Number> and a product with a version number 2.1.0.0 is a higher version than a product with version number 1.2.0.0</span></span>

     

-   <span data-ttu-id="81046-116">L'attributo msidbPatchSequenceSupersedeEarlier viene immesso nella colonna Attribute delle nuove righe generate per i Service Pack (SP) o per le patch di aggiornamento secondarie.</span><span class="sxs-lookup"><span data-stu-id="81046-116">The msidbPatchSequenceSupersedeEarlier attribute is entered into the Attribute column of new rows that are generated for service packs (SP) or minor upgrade patches.</span></span> <span data-ttu-id="81046-117">L'attributo msidbPatchSequenceSupersedeEarlier non viene aggiunto a una patch QFE o Small Update.</span><span class="sxs-lookup"><span data-stu-id="81046-117">The msidbPatchSequenceSupersedeEarlier attribute is not added to a QFE or small update patch.</span></span>
    > [!Note]  
    > <span data-ttu-id="81046-118">Un Service Pack (SP) deve contenere le correzioni di tutti i QFE che sono stati rilasciati prima.</span><span class="sxs-lookup"><span data-stu-id="81046-118">A service pack (SP) should contain the fixes of all the QFEs that were released prior to it.</span></span> <span data-ttu-id="81046-119">Tuttavia, se un autore della patch imposta la \_ Proprietà Sequence Data \_ sostituzione su 0 (zero) o 1 (uno) nel file con estensione PCP, la colonna attributi di tutte le righe della tabella MsiPatchSequence viene impostata sul valore specificato per i dati di \_ sequenza \_ sostituzione.</span><span class="sxs-lookup"><span data-stu-id="81046-119">However, if a patch author sets the SEQUENCE\_DATA\_SUPERSEDENCE property to 0 (zero) or 1 (one) in the .pcp file, the Attributes column of all rows in the MsiPatchSequence table is set to the value that is specified for SEQUENCE\_DATA\_SUPERSEDENCE.</span></span> <span data-ttu-id="81046-120">Gli autori delle patch che richiedono un maggiore controllo devono creare manualmente la colonna attributi.</span><span class="sxs-lookup"><span data-stu-id="81046-120">Patch authors who require more control must author the Attributes column manually.</span></span>

     

<span data-ttu-id="81046-121">Se si include una [tabella PatchSequence](patchsequence-table--patchwiz-dll-.md) nel file con estensione PCP, la \_ \_ \_ Proprietà disabilitata generazione dati sequenza viene ignorata e le informazioni fornite nella tabella PatchSequence possono essere aggiunte alla [tabella MsiPatchSequence](msipatchsequence-table.md) della patch.</span><span class="sxs-lookup"><span data-stu-id="81046-121">If you include a [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) in the .pcp file, the SEQUENCE\_DATA\_GENERATION\_DISABLED property is ignored and the information provided in the PatchSequence Table can be added to the [MsiPatchSequence Table](msipatchsequence-table.md) of the patch.</span></span>

 

 



