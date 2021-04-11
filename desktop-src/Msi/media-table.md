---
description: La tabella media descrive il set di dischi che costituiscono il supporto di origine per l'installazione.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Tabella supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351256"
---
# <a name="media-table"></a><span data-ttu-id="f7b73-103">Tabella supporti</span><span class="sxs-lookup"><span data-stu-id="f7b73-103">Media Table</span></span>

<span data-ttu-id="f7b73-104">La tabella media descrive il set di dischi che costituiscono il supporto di origine per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f7b73-104">The Media table describes the set of disks that make up the source media for the installation.</span></span>

<span data-ttu-id="f7b73-105">La tabella media contiene le colonne mostrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f7b73-105">The Media table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="f7b73-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="f7b73-106">Column</span></span>       | <span data-ttu-id="f7b73-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7b73-107">Type</span></span>                     | <span data-ttu-id="f7b73-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="f7b73-108">Key</span></span> | <span data-ttu-id="f7b73-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f7b73-109">Nullable</span></span> |
|--------------|--------------------------|-----|----------|
| <span data-ttu-id="f7b73-110">DiskId</span><span class="sxs-lookup"><span data-stu-id="f7b73-110">DiskId</span></span>       | [<span data-ttu-id="f7b73-111">Integer</span><span class="sxs-lookup"><span data-stu-id="f7b73-111">Integer</span></span>](integer.md)   | <span data-ttu-id="f7b73-112">S</span><span class="sxs-lookup"><span data-stu-id="f7b73-112">Y</span></span>   | <span data-ttu-id="f7b73-113">N</span><span class="sxs-lookup"><span data-stu-id="f7b73-113">N</span></span>        |
| <span data-ttu-id="f7b73-114">LastSequence</span><span class="sxs-lookup"><span data-stu-id="f7b73-114">LastSequence</span></span> | [<span data-ttu-id="f7b73-115">Integer</span><span class="sxs-lookup"><span data-stu-id="f7b73-115">Integer</span></span>](integer.md)   | <span data-ttu-id="f7b73-116">N</span><span class="sxs-lookup"><span data-stu-id="f7b73-116">N</span></span>   | <span data-ttu-id="f7b73-117">N</span><span class="sxs-lookup"><span data-stu-id="f7b73-117">N</span></span>        |
| <span data-ttu-id="f7b73-118">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="f7b73-118">DiskPrompt</span></span>   | [<span data-ttu-id="f7b73-119">Text</span><span class="sxs-lookup"><span data-stu-id="f7b73-119">Text</span></span>](text.md)         | <span data-ttu-id="f7b73-120">N</span><span class="sxs-lookup"><span data-stu-id="f7b73-120">N</span></span>   | <span data-ttu-id="f7b73-121">S</span><span class="sxs-lookup"><span data-stu-id="f7b73-121">Y</span></span>        |
| <span data-ttu-id="f7b73-122">CAB</span><span class="sxs-lookup"><span data-stu-id="f7b73-122">Cabinet</span></span>      | [<span data-ttu-id="f7b73-123">CAB</span><span class="sxs-lookup"><span data-stu-id="f7b73-123">Cabinet</span></span>](cabinet.md)   | <span data-ttu-id="f7b73-124">N</span><span class="sxs-lookup"><span data-stu-id="f7b73-124">N</span></span>   | <span data-ttu-id="f7b73-125">S</span><span class="sxs-lookup"><span data-stu-id="f7b73-125">Y</span></span>        |
| <span data-ttu-id="f7b73-126">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="f7b73-126">VolumeLabel</span></span>  | [<span data-ttu-id="f7b73-127">Text</span><span class="sxs-lookup"><span data-stu-id="f7b73-127">Text</span></span>](text.md)         | <span data-ttu-id="f7b73-128">N</span><span class="sxs-lookup"><span data-stu-id="f7b73-128">N</span></span>   | <span data-ttu-id="f7b73-129">S</span><span class="sxs-lookup"><span data-stu-id="f7b73-129">Y</span></span>        |
| <span data-ttu-id="f7b73-130">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="f7b73-130">Source</span></span>       | [<span data-ttu-id="f7b73-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7b73-131">Property</span></span>](property.md) | <span data-ttu-id="f7b73-132">N</span><span class="sxs-lookup"><span data-stu-id="f7b73-132">N</span></span>   | <span data-ttu-id="f7b73-133">S</span><span class="sxs-lookup"><span data-stu-id="f7b73-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f7b73-134">Colonne</span><span class="sxs-lookup"><span data-stu-id="f7b73-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f7b73-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span><span class="sxs-lookup"><span data-stu-id="f7b73-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span></span>
</dt> <dd>

<span data-ttu-id="f7b73-136">Determina il tipo di ordinamento per la tabella.</span><span class="sxs-lookup"><span data-stu-id="f7b73-136">Determines the sort order for the table.</span></span> <span data-ttu-id="f7b73-137">Questo numero deve essere maggiore o uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="f7b73-137">This number must be equal to or greater than 1.</span></span>

</dd> <dt>

<span data-ttu-id="f7b73-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span><span class="sxs-lookup"><span data-stu-id="f7b73-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span></span>
</dt> <dd>

<span data-ttu-id="f7b73-139">Numero di sequenza del file per l'ultimo file per questo supporto.</span><span class="sxs-lookup"><span data-stu-id="f7b73-139">File sequence number for the last file for this media.</span></span> <span data-ttu-id="f7b73-140">I numeri nella colonna LastSequence specificano quali file della tabella [file](file-table.md) si trovano in un determinato disco di origine.</span><span class="sxs-lookup"><span data-stu-id="f7b73-140">The numbers in the LastSequence column specify which of the files in the [File](file-table.md) table are found on a particular source disk.</span></span> <span data-ttu-id="f7b73-141">Ogni disco di origine contiene tutti i file con numeri di sequenza (come illustrato nella colonna sequenza della tabella file) minore o uguale al valore nella colonna LastSequence e maggiore del valore LastSequence del disco precedente (o maggiore di 0, per la prima voce nella tabella Media).</span><span class="sxs-lookup"><span data-stu-id="f7b73-141">Each source disk contains all files with sequence numbers (as shown in the Sequence column of the File table) less than or equal to the value in the LastSequence column, and greater than the LastSequence value of the previous disk (or greater than 0, for the first entry in the Media table).</span></span> <span data-ttu-id="f7b73-142">Questo numero deve essere non negativo. il limite massimo è 32767 file.</span><span class="sxs-lookup"><span data-stu-id="f7b73-142">This number must be non-negative; the maximum limit is 32767 files.</span></span> <span data-ttu-id="f7b73-143">Per ulteriori informazioni sulla creazione di un pacchetto di Windows Installer con più file, vedere Creazione di [un pacchetto di grandi dimensioni](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="f7b73-143">For more information about creating a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7b73-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="f7b73-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span></span>
</dt> <dd>

<span data-ttu-id="f7b73-145">Nome del disco, che in genere è il testo visibile stampato sul disco.</span><span class="sxs-lookup"><span data-stu-id="f7b73-145">The disk name, which is usually the visible text printed on the disk.</span></span> <span data-ttu-id="f7b73-146">Questo testo localizzabile viene usato per richiedere all'utente quando è necessario inserire il disco.</span><span class="sxs-lookup"><span data-stu-id="f7b73-146">This localizable text is used to prompt the user when this disk needs to be inserted.</span></span>

</dd> <dt>

<span data-ttu-id="f7b73-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>CAB</span><span class="sxs-lookup"><span data-stu-id="f7b73-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Cabinet</span></span>
</dt> <dd>

<span data-ttu-id="f7b73-148">Nome del file CAB se alcuni o tutti i file archiviati nel supporto vengono compressi in un file CAB.</span><span class="sxs-lookup"><span data-stu-id="f7b73-148">The name of the cabinet if some or all of the files stored on the media are compressed into a cabinet file.</span></span> <span data-ttu-id="f7b73-149">Se non viene utilizzato alcun cabinet, questa colonna deve essere vuota.</span><span class="sxs-lookup"><span data-stu-id="f7b73-149">If no cabinets are used, this column must be blank.</span></span> <span data-ttu-id="f7b73-150">Il nome del file CAB deve usare la sintassi del tipo di dati [CAB](cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b73-150">The name of the cabinet must use the syntax of the [Cabinet](cabinet.md) data type.</span></span> <span data-ttu-id="f7b73-151">Windows Installer richiede sempre un'origine valida per ripristinare i file inclusi nei file CAB incorporati.</span><span class="sxs-lookup"><span data-stu-id="f7b73-151">Windows Installer always requires a valid source to repair files included in embedded cabinet files.</span></span> <span data-ttu-id="f7b73-152">Quando Windows Installer installa un pacchetto contenente un file CAB incorporato, una copia del file CAB può essere salvata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f7b73-152">When Windows Installer installs a package containing an embedded cabinet file, a copy of the cabinet file can be saved by the system.</span></span> <span data-ttu-id="f7b73-153">Non è possibile utilizzare questa copia per ripristinare il file CAB.</span><span class="sxs-lookup"><span data-stu-id="f7b73-153">This copy cannot be used to repair the cabinet file.</span></span> <span data-ttu-id="f7b73-154">Per conservare spazio su disco, utilizzare file CAB esterni anziché file CAB incorporati.</span><span class="sxs-lookup"><span data-stu-id="f7b73-154">To conserve disk space, use external cabinet files instead of embedded cabinet files.</span></span>

</dd> <dt>

<span data-ttu-id="f7b73-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="f7b73-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span></span>
</dt> <dd>

<span data-ttu-id="f7b73-156">Etichetta attribuita al volume.</span><span class="sxs-lookup"><span data-stu-id="f7b73-156">The label attributed to the volume.</span></span> <span data-ttu-id="f7b73-157">Si tratta dell'etichetta del volume restituita dalla funzione [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) .</span><span class="sxs-lookup"><span data-stu-id="f7b73-157">This is the volume label returned by the [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="f7b73-158">Se la proprietà [**SourceDir**](sourcedir.md) fa riferimento a un volume rimovibile (floppy o CD-ROM), questa etichetta del volume viene utilizzata per verificare che il disco appropriato si trovi nell'unità prima di tentare di installare i file.</span><span class="sxs-lookup"><span data-stu-id="f7b73-158">If the [**SourceDir**](sourcedir.md) property refers to a removable (floppy or CD-ROM) volume, then this volume label is used to verify that the proper disk is in the drive before attempting to install files.</span></span> <span data-ttu-id="f7b73-159">La voce in questa colonna deve corrispondere all'etichetta del volume del supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="f7b73-159">The entry in this column must match the volume label of the physical media.</span></span>

</dd> <dt>

<span data-ttu-id="f7b73-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Origine</span><span class="sxs-lookup"><span data-stu-id="f7b73-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="f7b73-161">Questo campo viene usato solo con l'applicazione di patch e in caso contrario viene lasciato vuoto.</span><span class="sxs-lookup"><span data-stu-id="f7b73-161">This field is only used by patching and is otherwise left blank.</span></span> <span data-ttu-id="f7b73-162">Una trasformazione patch può immettere una proprietà che rappresenta il percorso del file CAB contenente i file della patch o i nuovi file aggiunti dalla patch.</span><span class="sxs-lookup"><span data-stu-id="f7b73-162">A patch transform can enter a property here that is the location of the cabinet file containing the patch files or any new files added by the patch.</span></span> <span data-ttu-id="f7b73-163">Per questi file è necessario specificare un'origine diversa, perché l'origine del pacchetto di patch può essere archiviata separatamente dall'origine del prodotto.</span><span class="sxs-lookup"><span data-stu-id="f7b73-163">A different source needs to be specified for these files because the source of the patch package can be stored separately from the product's source.</span></span> <span data-ttu-id="f7b73-164">Se il campo cabinet è vuoto, il programma di installazione ignorerà il valore in questa colonna.</span><span class="sxs-lookup"><span data-stu-id="f7b73-164">If the Cabinet field is empty, the installer ignores the value in this column.</span></span> <span data-ttu-id="f7b73-165">Se questo campo è vuoto, il programma di installazione usa il valore della proprietà [**SourceDir**](sourcedir.md) come origine del file CAB.</span><span class="sxs-lookup"><span data-stu-id="f7b73-165">If this field is empty, the installer uses the value of the [**SourceDir**](sourcedir.md) property as the source of the cabinet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7b73-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7b73-166">Remarks</span></span>

<span data-ttu-id="f7b73-167">Se il nome del cabinet è preceduto da un simbolo di cancelletto ( \# ), i file che fanno riferimento a questo record della tabella multimediale vengono compressi in un file CAB archiviato nel database come flusso separato.</span><span class="sxs-lookup"><span data-stu-id="f7b73-167">If the cabinet name is preceded by a number sign (\#), then the files referencing this Media table record are packed in a cabinet file that is stored within the database as a separate stream.</span></span>

<span data-ttu-id="f7b73-168">Per ulteriori informazioni su come aggiungere i file CAB alle tabelle di file e alle tabelle multimediali, vedere [utilizzo di archivi e origini compresse](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="f7b73-168">For more information about how to add cabinets to the File tables and Media tables, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="f7b73-169">Windows Installer richiede che il file con estensione msi si trovi nel primo disco del supporto rimovibile (CD, DVD o floppy) usato per l'installazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="f7b73-169">Windows Installer requires that the .msi file be on the first disk of removable media (CD, DVD or floppy) used for the product's installation.</span></span>

<span data-ttu-id="f7b73-170">**Determinazione del SourceMode**</span><span class="sxs-lookup"><span data-stu-id="f7b73-170">**Determining the SourceMode**</span></span>

<span data-ttu-id="f7b73-171">La proprietà [**riepilogo Conteggio parole**](word-count-summary.md) determina la modalità di origine per l'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f7b73-171">The [**Word Count Summary**](word-count-summary.md) property determines the source mode for the current install.</span></span> <span data-ttu-id="f7b73-172">Se questa proprietà è impostata su 2 o 3, viene utilizzata un'installazione del cabinet.</span><span class="sxs-lookup"><span data-stu-id="f7b73-172">If this property is set to 2 or 3, a cabinet install is assumed.</span></span> <span data-ttu-id="f7b73-173">In questa modalità, si presuppone che i file CAB esistano nella directory indicata dalla proprietà [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b73-173">In this mode, the cabinet files are assumed to exist in the directory indicated by the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="f7b73-174">Se il valore del tipo di origine è 0 o 1, si presuppone che tutti i file di origine esistano nell'albero la cui radice è indicata dalla proprietà **SourceDir** .</span><span class="sxs-lookup"><span data-stu-id="f7b73-174">If the Source Type value is 0 or 1, all source files are assumed to exist in the tree whose root is indicated by the **SourceDir** property.</span></span>

<span data-ttu-id="f7b73-175">Si noti che questo si applica solo ai file della tabella file che non dispongono del set di bit compresso o non compresso nella colonna attributi.</span><span class="sxs-lookup"><span data-stu-id="f7b73-175">Note that this only applies to files in the File table that do not have either the Compressed or Uncompressed bits set in the attributes column.</span></span> <span data-ttu-id="f7b73-176">Questi bit eseguono l'override del valore della proprietà [**riepilogo Conteggio parole**](word-count-summary.md) per determinare se un determinato file viene compresso o decompresso.</span><span class="sxs-lookup"><span data-stu-id="f7b73-176">These bits override the value of the [**Word Count Summary**](word-count-summary.md) property when determining if a particular file is compressed or uncompressed.</span></span>

## <a name="validation"></a><span data-ttu-id="f7b73-177">Convalida</span><span class="sxs-lookup"><span data-stu-id="f7b73-177">Validation</span></span>

<dl>

[<span data-ttu-id="f7b73-178">ICE03</span><span class="sxs-lookup"><span data-stu-id="f7b73-178">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f7b73-179">ICE04</span><span class="sxs-lookup"><span data-stu-id="f7b73-179">ICE04</span></span>](ice04.md)  
[<span data-ttu-id="f7b73-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="f7b73-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f7b73-181">ICE35</span><span class="sxs-lookup"><span data-stu-id="f7b73-181">ICE35</span></span>](ice35.md)  
[<span data-ttu-id="f7b73-182">ICE58</span><span class="sxs-lookup"><span data-stu-id="f7b73-182">ICE58</span></span>](ice58.md)  
[<span data-ttu-id="f7b73-183">ICE71</span><span class="sxs-lookup"><span data-stu-id="f7b73-183">ICE71</span></span>](ice71.md)  
[<span data-ttu-id="f7b73-184">ICE81</span><span class="sxs-lookup"><span data-stu-id="f7b73-184">ICE81</span></span>](ice81.md)  
</dl>

 

 
