---
description: La tabella patch specifica il file che deve ricevere una particolare patch e il percorso fisico dei file della patch nelle immagini multimediali.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Tabella patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760151"
---
# <a name="patch-table"></a><span data-ttu-id="61e86-103">Tabella patch</span><span class="sxs-lookup"><span data-stu-id="61e86-103">Patch Table</span></span>

<span data-ttu-id="61e86-104">La tabella patch specifica il file che deve ricevere una particolare patch e il percorso fisico dei file della patch nelle immagini multimediali.</span><span class="sxs-lookup"><span data-stu-id="61e86-104">The Patch table specifies the file that is to receive a particular patch and the physical location of the patch files on the media images.</span></span>

<span data-ttu-id="61e86-105">La tabella patch contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="61e86-105">The Patch table has the following columns.</span></span>



| <span data-ttu-id="61e86-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="61e86-106">Column</span></span>      | <span data-ttu-id="61e86-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="61e86-107">Type</span></span>                               | <span data-ttu-id="61e86-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="61e86-108">Key</span></span> | <span data-ttu-id="61e86-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="61e86-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="61e86-110">file\_</span><span class="sxs-lookup"><span data-stu-id="61e86-110">File\_</span></span>      | [<span data-ttu-id="61e86-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="61e86-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="61e86-112">S</span><span class="sxs-lookup"><span data-stu-id="61e86-112">Y</span></span>   | <span data-ttu-id="61e86-113">N</span><span class="sxs-lookup"><span data-stu-id="61e86-113">N</span></span>        |
| <span data-ttu-id="61e86-114">Sequenza</span><span class="sxs-lookup"><span data-stu-id="61e86-114">Sequence</span></span>    | [<span data-ttu-id="61e86-115">Integer</span><span class="sxs-lookup"><span data-stu-id="61e86-115">Integer</span></span>](integer.md)             | <span data-ttu-id="61e86-116">S</span><span class="sxs-lookup"><span data-stu-id="61e86-116">Y</span></span>   | <span data-ttu-id="61e86-117">N</span><span class="sxs-lookup"><span data-stu-id="61e86-117">N</span></span>        |
| <span data-ttu-id="61e86-118">PatchSize</span><span class="sxs-lookup"><span data-stu-id="61e86-118">PatchSize</span></span>   | [<span data-ttu-id="61e86-119">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="61e86-119">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="61e86-120">N</span><span class="sxs-lookup"><span data-stu-id="61e86-120">N</span></span>   | <span data-ttu-id="61e86-121">N</span><span class="sxs-lookup"><span data-stu-id="61e86-121">N</span></span>        |
| <span data-ttu-id="61e86-122">Attributi</span><span class="sxs-lookup"><span data-stu-id="61e86-122">Attributes</span></span>  | [<span data-ttu-id="61e86-123">Integer</span><span class="sxs-lookup"><span data-stu-id="61e86-123">Integer</span></span>](integer.md)             | <span data-ttu-id="61e86-124">N</span><span class="sxs-lookup"><span data-stu-id="61e86-124">N</span></span>   | <span data-ttu-id="61e86-125">N</span><span class="sxs-lookup"><span data-stu-id="61e86-125">N</span></span>        |
| <span data-ttu-id="61e86-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61e86-126">Header</span></span>      | [<span data-ttu-id="61e86-127">Binario</span><span class="sxs-lookup"><span data-stu-id="61e86-127">Binary</span></span>](binary.md)               | <span data-ttu-id="61e86-128">N</span><span class="sxs-lookup"><span data-stu-id="61e86-128">N</span></span>   | <span data-ttu-id="61e86-129">S</span><span class="sxs-lookup"><span data-stu-id="61e86-129">Y</span></span>        |
| <span data-ttu-id="61e86-130">StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="61e86-130">StreamRef\_</span></span> | [<span data-ttu-id="61e86-131">Identificatore</span><span class="sxs-lookup"><span data-stu-id="61e86-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="61e86-132">N</span><span class="sxs-lookup"><span data-stu-id="61e86-132">N</span></span>   | <span data-ttu-id="61e86-133">S</span><span class="sxs-lookup"><span data-stu-id="61e86-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="61e86-134">Colonne</span><span class="sxs-lookup"><span data-stu-id="61e86-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="61e86-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="61e86-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="61e86-136">La patch viene applicata al file specificato dall'identificatore in questa colonna.</span><span class="sxs-lookup"><span data-stu-id="61e86-136">The patch is applied to the file specified by the identifier in this column.</span></span> <span data-ttu-id="61e86-137">Si tratta di una chiave primaria per la tabella ed è una chiave esterna per la [tabella dei file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="61e86-137">This is a primary key for the table and it is a foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="61e86-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="61e86-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="61e86-139">Si tratta della posizione del file di correzione nell'ordine di sequenza dei file nelle immagini multimediali.</span><span class="sxs-lookup"><span data-stu-id="61e86-139">This is the position of the patch file in the sequence order of files on the media images.</span></span> <span data-ttu-id="61e86-140">L'ordine di sequenza deve corrispondere all'ordine dei file nel file CAB del pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="61e86-140">The sequence order must correspond to the order of the files in the patch package cabinet file.</span></span> <span data-ttu-id="61e86-141">Si tratta di una chiave primaria per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="61e86-141">This is a primary key for this table.</span></span> <span data-ttu-id="61e86-142">Il limite massimo è 32767 file, per creare un pacchetto di Windows Installer con più file, vedere la pagina relativa alla [creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="61e86-142">The maximum limit is 32767 files, to create a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="61e86-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span><span class="sxs-lookup"><span data-stu-id="61e86-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span></span>
</dt> <dd>

<span data-ttu-id="61e86-144">Questa colonna indica la dimensione della patch in byte scritta come valore long integer.</span><span class="sxs-lookup"><span data-stu-id="61e86-144">This column gives the size of the patch in bytes written as a long integer.</span></span>

</dd> <dt>

<span data-ttu-id="61e86-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="61e86-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="61e86-146">Integer contenente i flag di bit che rappresentano gli attributi della patch.</span><span class="sxs-lookup"><span data-stu-id="61e86-146">Integer containing bit flags representing patch attributes.</span></span> <span data-ttu-id="61e86-147">Inserire il valore 1 in questa colonna per indicare che l'errore di applicazione della patch non è un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="61e86-147">Insert a value of 1 in this column to indicate that the failure to apply this patch is not a fatal error.</span></span>



| <span data-ttu-id="61e86-148">Costante</span><span class="sxs-lookup"><span data-stu-id="61e86-148">Constant</span></span>                         | <span data-ttu-id="61e86-149">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="61e86-149">Hexadecimal</span></span> | <span data-ttu-id="61e86-150">Decimal</span><span class="sxs-lookup"><span data-stu-id="61e86-150">Decimal</span></span> | <span data-ttu-id="61e86-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61e86-151">Description</span></span>                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| <span data-ttu-id="61e86-152">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="61e86-152">(none)</span></span>                           | <span data-ttu-id="61e86-153">0x000</span><span class="sxs-lookup"><span data-stu-id="61e86-153">0x000</span></span>       | <span data-ttu-id="61e86-154">0</span><span class="sxs-lookup"><span data-stu-id="61e86-154">0</span></span>       | <span data-ttu-id="61e86-155">L'impossibilità di applicare questa patch è un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="61e86-155">Failure to apply this patch is a fatal error.</span></span>                        |
| <span data-ttu-id="61e86-156">**msidbPatchAttributesNonVital**</span><span class="sxs-lookup"><span data-stu-id="61e86-156">**msidbPatchAttributesNonVital**</span></span> | <span data-ttu-id="61e86-157">0x001</span><span class="sxs-lookup"><span data-stu-id="61e86-157">0x001</span></span>       | <span data-ttu-id="61e86-158">1</span><span class="sxs-lookup"><span data-stu-id="61e86-158">1</span></span>       | <span data-ttu-id="61e86-159">Indica che l'errore di applicazione della patch non è un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="61e86-159">Indicates that the failure to apply this patch is not a fatal error.</span></span> |



 

</dd> <dt>

<span data-ttu-id="61e86-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Intestazione</span><span class="sxs-lookup"><span data-stu-id="61e86-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="61e86-161">Questa colonna è l'intestazione patch del flusso binario utilizzata per la convalida delle patch.</span><span class="sxs-lookup"><span data-stu-id="61e86-161">This column is the binary stream patch header used for patch validation.</span></span> <span data-ttu-id="61e86-162">Questa colonna deve essere null se la \_ colonna StreamRef non è null.</span><span class="sxs-lookup"><span data-stu-id="61e86-162">This column should be null if the StreamRef\_ column is not null.</span></span> <span data-ttu-id="61e86-163">In questo caso, il flusso dell'intestazione patch viene archiviato nella [tabella MsiPatchHeaders](msipatchheaders-table.md) per superare la limitazione del nome del flusso descritta in [limitazioni OLE sui flussi](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="61e86-163">In this case, the patch header stream is stored in the [MsiPatchHeaders table](msipatchheaders-table.md) to overcome the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

</dd> <dt>

<span data-ttu-id="61e86-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="61e86-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span></span>
</dt> <dd>

<span data-ttu-id="61e86-165">Chiave esterna nella tabella MsiPatchHeaders che specifica la riga che contiene il flusso dell'intestazione della patch.</span><span class="sxs-lookup"><span data-stu-id="61e86-165">External key into the MsiPatchHeaders table specifying the row that contains the patch header stream.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61e86-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="61e86-166">Remarks</span></span>

<span data-ttu-id="61e86-167">Questa tabella viene elaborata dall' [azione PatchFiles](patchfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="61e86-167">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="61e86-168">Viene in genere aggiunto al pacchetto di installazione da una trasformazione da un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="61e86-168">It is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="61e86-169">Non viene in genere creato direttamente in un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="61e86-169">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="61e86-170">Convalida</span><span class="sxs-lookup"><span data-stu-id="61e86-170">Validation</span></span>

<dl>

[<span data-ttu-id="61e86-171">ICE03</span><span class="sxs-lookup"><span data-stu-id="61e86-171">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="61e86-172">ICE06</span><span class="sxs-lookup"><span data-stu-id="61e86-172">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="61e86-173">ICE29</span><span class="sxs-lookup"><span data-stu-id="61e86-173">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="61e86-174">ICE45</span><span class="sxs-lookup"><span data-stu-id="61e86-174">ICE45</span></span>](ice45.md)  
</dl>

 

 



