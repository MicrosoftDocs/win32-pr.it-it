---
description: ICE60 convalida la tabella file di un database Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314794"
---
# <a name="ice60"></a><span data-ttu-id="ee276-103">ICE60</span><span class="sxs-lookup"><span data-stu-id="ee276-103">ICE60</span></span>

<span data-ttu-id="ee276-104">ICE60 verifica che i file nella [tabella file](file-table.md) soddisfino la condizione seguente:</span><span class="sxs-lookup"><span data-stu-id="ee276-104">ICE60 checks that files in the [File table](file-table.md) meet the following condition:</span></span>

-   <span data-ttu-id="ee276-105">Se il file non è un tipo di carattere e presenta una versione, è necessario che disponga di una lingua.</span><span class="sxs-lookup"><span data-stu-id="ee276-105">If the file is not a font and has a version, then it must have a language.</span></span>
-   <span data-ttu-id="ee276-106">ICE60 verifica che non siano elencati file con versione nella [tabella MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee276-106">ICE60 checks that no versioned files are listed in the [MsiFileHash table](msifilehash-table.md).</span></span>

<span data-ttu-id="ee276-107">Se si verifica un errore durante la correzione di un avviso segnalato da ICE60, in genere il file viene reinstallato inutilmente quando viene eseguito un ripristino del prodotto.</span><span class="sxs-lookup"><span data-stu-id="ee276-107">Failure to fix a warning reported by ICE60 generally leads to a file being needlessly reinstalled when a product repair is done.</span></span> <span data-ttu-id="ee276-108">Questo problema si verifica perché il file da installare nel ripristino e il file esistente sul disco hanno la stessa versione (si tratta dello stesso file) ma linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="ee276-108">This happens because the file to be installed in the repair and the existing file on disk have the same version (they are the same file) but different languages.</span></span> <span data-ttu-id="ee276-109">La tabella file elenca la lingua come null, ma il file ha un valore di lingua nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee276-109">The file table lists the language as null, but the file itself has a language value in the resource.</span></span> <span data-ttu-id="ee276-110">In base alle [regole di controllo delle versioni dei file](file-versioning-rules.md), il programma di installazione predilige il file da installare, quindi viene ricopiato inutilmente.</span><span class="sxs-lookup"><span data-stu-id="ee276-110">Based on the [file versioning rules](file-versioning-rules.md), the installer favors the file to be installed, so it is recopied needlessly.</span></span>

## <a name="result"></a><span data-ttu-id="ee276-111">Risultato</span><span class="sxs-lookup"><span data-stu-id="ee276-111">Result</span></span>

<span data-ttu-id="ee276-112">ICE60 Invia un avviso o un errore se un file nella [tabella file](file-table.md) che non è un tipo di carattere e ha una versione, non dispone di un linguaggio.</span><span class="sxs-lookup"><span data-stu-id="ee276-112">ICE60 posts a warning or an error if a file in the [File table](file-table.md) that is not a font and has a version, does not have a language.</span></span>

<span data-ttu-id="ee276-113">ICE60 invia il seguente errore se un file elencato nella tabella MsiFileHash è sottoposto a controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="ee276-113">ICE60 posts the following error if a file listed in the MsiFileHash table is versioned.</span></span>

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a><span data-ttu-id="ee276-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="ee276-114">Example</span></span>

<span data-ttu-id="ee276-115">ICE60 segnala l'errore e l'avviso seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="ee276-115">ICE60 reports the following error and warning for the example shown.</span></span> <span data-ttu-id="ee276-116">Il file B è un tipo di carattere. gli altri file non lo sono.</span><span class="sxs-lookup"><span data-stu-id="ee276-116">(File B is a font; the other files are not.)</span></span>

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

<span data-ttu-id="ee276-117">Filea ha una versione e un linguaggio; pertanto non viene generato alcun avviso o errore.</span><span class="sxs-lookup"><span data-stu-id="ee276-117">FileA has both a version and a language; therefore no warning or error is generated.</span></span>

<span data-ttu-id="ee276-118">FileB dispone di una versione ma non di un linguaggio.</span><span class="sxs-lookup"><span data-stu-id="ee276-118">FileB has a version but no language.</span></span> <span data-ttu-id="ee276-119">Tuttavia, non viene generato alcun avviso o errore perché è un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="ee276-119">No warning or error is generated, however, because it is a font.</span></span>

<span data-ttu-id="ee276-120">FileC è un riferimento complementare, pertanto non è necessario disporre di un linguaggio.</span><span class="sxs-lookup"><span data-stu-id="ee276-120">FileC is a companion reference, so it does not have to have a language.</span></span> <span data-ttu-id="ee276-121">Non viene generato alcun avviso o errore.</span><span class="sxs-lookup"><span data-stu-id="ee276-121">No warning or error is generated.</span></span>

<span data-ttu-id="ee276-122">Il file archiviato non ha una versione, quindi non è necessario disporre di un linguaggio.</span><span class="sxs-lookup"><span data-stu-id="ee276-122">FileD has no version, so it does not need to have a language.</span></span> <span data-ttu-id="ee276-123">Non viene generato alcun avviso o errore.</span><span class="sxs-lookup"><span data-stu-id="ee276-123">No warning or error is generated.</span></span>

<span data-ttu-id="ee276-124">Il file ha una versione ma nessuna lingua.</span><span class="sxs-lookup"><span data-stu-id="ee276-124">FileE has a version but no language.</span></span> <span data-ttu-id="ee276-125">Viene pertanto generato un avviso.</span><span class="sxs-lookup"><span data-stu-id="ee276-125">Therefore a warning is generated.</span></span>

<span data-ttu-id="ee276-126">Per correggere il problema, aggiungere una lingua al file.</span><span class="sxs-lookup"><span data-stu-id="ee276-126">To fix this warning, add a language to FileE.</span></span>

<span data-ttu-id="ee276-127">I file devono avere i valori della lingua archiviati nella risorsa di versione laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="ee276-127">Files should have language values stored in the version resource whenever possible.</span></span> <span data-ttu-id="ee276-128">Se un file è indipendente dalla lingua, usare [LangID](column-data-types.md) 0.</span><span class="sxs-lookup"><span data-stu-id="ee276-128">If a file is language neutral, use the [LANGID](column-data-types.md) 0.</span></span>

<span data-ttu-id="ee276-129">[File table](file-table.md) (fileB è un tipo di carattere; gli altri file non lo sono).</span><span class="sxs-lookup"><span data-stu-id="ee276-129">[File Table](file-table.md) (FileB is a font; the other files are not.)</span></span>



| <span data-ttu-id="ee276-130">File</span><span class="sxs-lookup"><span data-stu-id="ee276-130">File</span></span>  | <span data-ttu-id="ee276-131">Versione</span><span class="sxs-lookup"><span data-stu-id="ee276-131">Version</span></span> | <span data-ttu-id="ee276-132">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="ee276-132">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="ee276-133">FileA</span><span class="sxs-lookup"><span data-stu-id="ee276-133">FileA</span></span> | <span data-ttu-id="ee276-134">1.0</span><span class="sxs-lookup"><span data-stu-id="ee276-134">1.0</span></span>     | <span data-ttu-id="ee276-135">1033</span><span class="sxs-lookup"><span data-stu-id="ee276-135">1033</span></span>     |
| <span data-ttu-id="ee276-136">FileB</span><span class="sxs-lookup"><span data-stu-id="ee276-136">FileB</span></span> | <span data-ttu-id="ee276-137">1.0</span><span class="sxs-lookup"><span data-stu-id="ee276-137">1.0</span></span>     |          |
| <span data-ttu-id="ee276-138">FileC</span><span class="sxs-lookup"><span data-stu-id="ee276-138">FileC</span></span> | <span data-ttu-id="ee276-139">FileA</span><span class="sxs-lookup"><span data-stu-id="ee276-139">FileA</span></span>   |          |
| <span data-ttu-id="ee276-140">Campo</span><span class="sxs-lookup"><span data-stu-id="ee276-140">FileD</span></span> |         |          |
| <span data-ttu-id="ee276-141">File</span><span class="sxs-lookup"><span data-stu-id="ee276-141">FileE</span></span> | <span data-ttu-id="ee276-142">1.0</span><span class="sxs-lookup"><span data-stu-id="ee276-142">1.0</span></span>     |          |



 

[<span data-ttu-id="ee276-143">Tabella dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="ee276-143">Font Table</span></span>](font-table.md)



| <span data-ttu-id="ee276-144">File</span><span class="sxs-lookup"><span data-stu-id="ee276-144">File</span></span>  | <span data-ttu-id="ee276-145">FontTitle</span><span class="sxs-lookup"><span data-stu-id="ee276-145">FontTitle</span></span>  |
|-------|------------|
| <span data-ttu-id="ee276-146">FileB</span><span class="sxs-lookup"><span data-stu-id="ee276-146">FileB</span></span> | <span data-ttu-id="ee276-147">Titolo carattere</span><span class="sxs-lookup"><span data-stu-id="ee276-147">Font Title</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ee276-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee276-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee276-149">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="ee276-149">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



