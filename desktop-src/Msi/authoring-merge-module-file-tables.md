---
description: In ogni modulo merge è necessaria una tabella di file e deve avere un record per ogni file che viene recapitato al pacchetto di installazione di destinazione dal modulo merge.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Creazione di tabelle di file del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049910"
---
# <a name="authoring-merge-module-file-tables"></a><span data-ttu-id="50602-103">Creazione di tabelle di file del modulo merge</span><span class="sxs-lookup"><span data-stu-id="50602-103">Authoring Merge Module File Tables</span></span>

<span data-ttu-id="50602-104">In ogni modulo merge è necessaria una [tabella di file](file-table.md) e deve avere un record per ogni file che viene recapitato al pacchetto di installazione di destinazione dal modulo merge.</span><span class="sxs-lookup"><span data-stu-id="50602-104">A [File Table](file-table.md) is required in every merge module, and should have a record for each file that is being delivered to the target installation package by the merge module.</span></span> <span data-ttu-id="50602-105">Quando il modulo merge viene unito in un file con estensione msi, ogni file nella tabella dei file del modulo merge viene archiviato in un [*file CAB*](c-gly.md) nel file con estensione MSM.</span><span class="sxs-lookup"><span data-stu-id="50602-105">When the merge module is merged into a .msi file, every file in the merge module File Table is stored inside a [*cabinet file*](c-gly.md) in the .msm file.</span></span> <span data-ttu-id="50602-106">Il nome del file CAB in un modulo merge è sempre il seguente: MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="50602-106">The name of the cabinet in a merge module is always the following: MergeModule.CABinet.</span></span>

<span data-ttu-id="50602-107">Per altre informazioni, vedere [generazione di file CAB di MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="50602-107">For more information, see [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).</span></span>

-   <span data-ttu-id="50602-108">Poiché i file di un modulo merge vengono sempre archiviati all'interno di un file CAB, non è necessario impostare i flag di bit **msidbFileAttributesNoncompressed** o **MsidbFileAttributesCompressed** nella colonna attributi della [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="50602-108">Because the files of a merge module are always stored inside a cabinet file, it is not necessary to set the **msidbFileAttributesNoncompressed** or **msidbFileAttributesCompressed** bit flags in the Attributes column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="50602-109">I nomi dei file in MergeModule.CABinet devono corrispondere alla chiave primaria nella [tabella dei file](file-table.md)del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="50602-109">The names of files in MergeModule.CABinet must match the primary key in the merge module's [File Table](file-table.md).</span></span>

    <span data-ttu-id="50602-110">La colonna file è la chiave primaria della [tabella file](file-table.md) e le voci di questo campo devono seguire la convenzione descritta in [denominazione di chiavi primarie nei database dei moduli di merge](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="50602-110">The File column is the primary key of the [File Table](file-table.md) and the entries in this field must follow the convention that is described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

-   <span data-ttu-id="50602-111">I numeri di sequenza del file vengono specificati nella colonna sequenza della [tabella dei file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="50602-111">File sequence numbers are specified in the Sequence column of the [File Table](file-table.md).</span></span>

    <span data-ttu-id="50602-112">I file devono essere elencati nella [tabella dei file](file-table.md) del modulo merge nella stessa sequenza in cui sono archiviati in MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="50602-112">Files must be listed in the merge module's [File Table](file-table.md) in the same sequence that they are stored in MergeModule.CABinet.</span></span> <span data-ttu-id="50602-113">I numeri di sequenza dei file non devono essere consecutivi, ma devono seguire la stessa sequenza dei file archiviati all'interno del cabinet.</span><span class="sxs-lookup"><span data-stu-id="50602-113">The sequence numbers of files do not need to be consecutive, but they must follow the same sequence as the files that are stored inside the cabinet.</span></span> <span data-ttu-id="50602-114">Ad esempio, il primo, il secondo e il terzo file archiviati nell'archivio possono avere i numeri di sequenza 100, 200 e 300.</span><span class="sxs-lookup"><span data-stu-id="50602-114">For example, the first, second, and third files stored in the cabinet can have the sequence numbers 100, 200, and 300.</span></span>

-   <span data-ttu-id="50602-115">Il programma di installazione ignora i file aggiuntivi inclusi in MergeModule.CABinet che non sono elencati nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="50602-115">The Installer skips extra files included in MergeModule.CABinet that are not listed in the [File Table](file-table.md).</span></span>

    <span data-ttu-id="50602-116">Un file CAB può contenere tutti i file necessari per un modulo merge che supporta più lingue usando le trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="50602-116">One cabinet file can contain all the files necessary for a merge module that supports multiple languages using transforms.</span></span> <span data-ttu-id="50602-117">A tutti i file della lingua può essere assegnato un numero di sequenza univoco nell'archivio, quindi una trasformazione può aggiungere o rimuovere file dalla [tabella file](file-table.md) quando necessario per una lingua specifica.</span><span class="sxs-lookup"><span data-stu-id="50602-117">All the language files can be given a unique sequence number in the cabinet, and then a transform can add or remove files from the [File Table](file-table.md) when needed for a specific language.</span></span> <span data-ttu-id="50602-118">Per ulteriori informazioni, vedere la pagina relativa alla creazione di modelli di [Unione di più linguaggi](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="50602-118">For more information, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="50602-119">Per ulteriori informazioni, vedere [file table](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="50602-119">For more information, see [File Table](file-table.md).</span></span>

 

 



