---
description: La tabella MsiFileHash viene utilizzata per archiviare un hash a 128 bit di un file di origine fornito dal pacchetto Windows Installer. L'hash viene suddiviso in valori a 4 32 bit e archiviato in colonne separate della tabella.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Tabella MsiFileHash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306578"
---
# <a name="msifilehash-table"></a><span data-ttu-id="9ab3d-104">Tabella MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="9ab3d-104">MsiFileHash Table</span></span>

<span data-ttu-id="9ab3d-105">La tabella **MsiFileHash** viene utilizzata per archiviare un hash a 128 bit di un file di origine fornito dal pacchetto Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-105">The **MsiFileHash** table is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span> <span data-ttu-id="9ab3d-106">L'hash viene suddiviso in valori a 4 32 bit e archiviato in colonne separate della tabella.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-106">The hash is split into four 32-bit values and stored in separate columns of the table.</span></span>

<span data-ttu-id="9ab3d-107">Windows Installer possibile utilizzare l'hashing dei file come mezzo per rilevare ed eliminare la copia di file non necessaria.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-107">Windows Installer can use file hashing as a means to detect and eliminate unnecessary file copying.</span></span> <span data-ttu-id="9ab3d-108">Un hash di file archiviato nella tabella **MsiFileHash** può essere confrontato con un hash di un file esistente nel computer dell'utente ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="9ab3d-108">A file hash stored in the **MsiFileHash** table may be compared to a hash of an existing file on the user's computer obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="9ab3d-109">La tabella **MsiFileHash** può essere utilizzata solo con file senza versione.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-109">The **MsiFileHash** table can only be used with unversioned files.</span></span>

<span data-ttu-id="9ab3d-110">La tabella **MsiFileHash** include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-110">The **MsiFileHash** table has the following columns.</span></span>



| <span data-ttu-id="9ab3d-111">Colonna</span><span class="sxs-lookup"><span data-stu-id="9ab3d-111">Column</span></span>    | <span data-ttu-id="9ab3d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ab3d-112">Type</span></span>                               | <span data-ttu-id="9ab3d-113">Chiave</span><span class="sxs-lookup"><span data-stu-id="9ab3d-113">Key</span></span> | <span data-ttu-id="9ab3d-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="9ab3d-114">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="9ab3d-115">file\_</span><span class="sxs-lookup"><span data-stu-id="9ab3d-115">File\_</span></span>    | [<span data-ttu-id="9ab3d-116">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9ab3d-116">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9ab3d-117">S</span><span class="sxs-lookup"><span data-stu-id="9ab3d-117">Y</span></span>   | <span data-ttu-id="9ab3d-118">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-118">N</span></span>        |
| <span data-ttu-id="9ab3d-119">Opzioni</span><span class="sxs-lookup"><span data-stu-id="9ab3d-119">Options</span></span>   | [<span data-ttu-id="9ab3d-120">Integer</span><span class="sxs-lookup"><span data-stu-id="9ab3d-120">Integer</span></span>](integer.md)             | <span data-ttu-id="9ab3d-121">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-121">N</span></span>   | <span data-ttu-id="9ab3d-122">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-122">N</span></span>        |
| <span data-ttu-id="9ab3d-123">HashPart1</span><span class="sxs-lookup"><span data-stu-id="9ab3d-123">HashPart1</span></span> | [<span data-ttu-id="9ab3d-124">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="9ab3d-124">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9ab3d-125">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-125">N</span></span>   | <span data-ttu-id="9ab3d-126">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-126">N</span></span>        |
| <span data-ttu-id="9ab3d-127">HashPart2</span><span class="sxs-lookup"><span data-stu-id="9ab3d-127">HashPart2</span></span> | [<span data-ttu-id="9ab3d-128">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="9ab3d-128">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9ab3d-129">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-129">N</span></span>   | <span data-ttu-id="9ab3d-130">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-130">N</span></span>        |
| <span data-ttu-id="9ab3d-131">HashPart3</span><span class="sxs-lookup"><span data-stu-id="9ab3d-131">HashPart3</span></span> | [<span data-ttu-id="9ab3d-132">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="9ab3d-132">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9ab3d-133">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-133">N</span></span>   | <span data-ttu-id="9ab3d-134">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-134">N</span></span>        |
| <span data-ttu-id="9ab3d-135">Hashpart4</span><span class="sxs-lookup"><span data-stu-id="9ab3d-135">Hashpart4</span></span> | [<span data-ttu-id="9ab3d-136">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="9ab3d-136">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9ab3d-137">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-137">N</span></span>   | <span data-ttu-id="9ab3d-138">N</span><span class="sxs-lookup"><span data-stu-id="9ab3d-138">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9ab3d-139">Colonne</span><span class="sxs-lookup"><span data-stu-id="9ab3d-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9ab3d-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="9ab3d-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="9ab3d-141">Chiave esterna per la [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="9ab3d-141">Foreign key to [File table](file-table.md).</span></span> <span data-ttu-id="9ab3d-142">72 stringa char.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-142">72 char string.</span></span>

</dd> <dt>

<span data-ttu-id="9ab3d-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opzioni</span><span class="sxs-lookup"><span data-stu-id="9ab3d-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="9ab3d-144">Questa colonna deve essere 0 ed è riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-144">This column must be 0 and is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="9ab3d-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span><span class="sxs-lookup"><span data-stu-id="9ab3d-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span></span>
</dt> <dd>

<span data-ttu-id="9ab3d-146">Primi 32 bit di hash.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-146">First 32 bits of hash.</span></span> <span data-ttu-id="9ab3d-147">L'hash di file immesso in questo campo deve essere ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o il [**Metodo filehash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="9ab3d-147">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="9ab3d-148">Non usare altri metodi.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-148">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="9ab3d-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span><span class="sxs-lookup"><span data-stu-id="9ab3d-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span></span>
</dt> <dd>

<span data-ttu-id="9ab3d-150">Secondo 32 bit di hash.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-150">Second 32 bits of hash.</span></span> <span data-ttu-id="9ab3d-151">L'hash di file immesso in questo campo deve essere ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o il [**Metodo filehash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="9ab3d-151">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="9ab3d-152">Non usare altri metodi di hashing.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-152">Do not use other hashing methods.</span></span>

</dd> <dt>

<span data-ttu-id="9ab3d-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span><span class="sxs-lookup"><span data-stu-id="9ab3d-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span></span>
</dt> <dd>

<span data-ttu-id="9ab3d-154">Terzo 32 bit di hash.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-154">Third 32 bits of hash.</span></span> <span data-ttu-id="9ab3d-155">L'hash di file immesso in questo campo deve essere ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o il [**Metodo filehash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="9ab3d-155">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="9ab3d-156">Non usare altri metodi.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-156">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="9ab3d-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span><span class="sxs-lookup"><span data-stu-id="9ab3d-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span></span>
</dt> <dd>

<span data-ttu-id="9ab3d-158">Quarto 32 bit di hash.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-158">Fourth 32 bits of hash.</span></span> <span data-ttu-id="9ab3d-159">L'hash di file immesso in questo campo deve essere ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o il [**Metodo filehash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="9ab3d-159">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="9ab3d-160">Non usare altri metodi.</span><span class="sxs-lookup"><span data-stu-id="9ab3d-160">Do not use other methods.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="9ab3d-161">Convalida</span><span class="sxs-lookup"><span data-stu-id="9ab3d-161">Validation</span></span>

<dl>

[<span data-ttu-id="9ab3d-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="9ab3d-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9ab3d-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="9ab3d-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9ab3d-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="9ab3d-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="9ab3d-165">ICE60</span><span class="sxs-lookup"><span data-stu-id="9ab3d-165">ICE60</span></span>](ice60.md)  
[<span data-ttu-id="9ab3d-166">ICE66</span><span class="sxs-lookup"><span data-stu-id="9ab3d-166">ICE66</span></span>](ice66.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="9ab3d-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ab3d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ab3d-168">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="9ab3d-168">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[<span data-ttu-id="9ab3d-169">Controllo delle versioni dei file predefinito</span><span class="sxs-lookup"><span data-stu-id="9ab3d-169">Default File Versioning</span></span>](default-file-versioning.md)
</dt> </dl>

 

 



