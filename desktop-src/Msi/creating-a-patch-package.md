---
description: Gli sviluppatori creano un pacchetto di patch generando un file di creazione della patch e usando Msimsp.exe per chiamare la funzione UiCreatePatchPackageEx in Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Creazione di un pacchetto di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231883"
---
# <a name="creating-a-patch-package"></a><span data-ttu-id="f4f19-103">Creazione di un pacchetto di patch</span><span class="sxs-lookup"><span data-stu-id="f4f19-103">Creating a Patch Package</span></span>

<span data-ttu-id="f4f19-104">Gli sviluppatori creano un pacchetto di patch generando un file di creazione della patch e usando [Msimsp.exe](msimsp-exe.md) per chiamare la funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="f4f19-104">Developers create a patch package by generating a patch creation file and using [Msimsp.exe](msimsp-exe.md) to call the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="f4f19-105">In Windows Installer SDK sono disponibili Msimsp.exe e Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="f4f19-105">Msimsp.exe and Patchwiz.dll are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="f4f19-106">Per ulteriori informazioni, vedere [un esempio di patch per l'aggiornamento di piccole dimensioni](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="f4f19-106">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="f4f19-107">Poiché l'applicazione di una patch a un pacchetto di Windows Installer comporta l'installazione delle origini originali utilizzando un nuovo file con estensione msi, il nuovo file con estensione msi deve rimanere compatibile con il layout dell'origine originale.</span><span class="sxs-lookup"><span data-stu-id="f4f19-107">Because the application of a patch to a Windows Installer package results in the installation of the original sources using a new .msi file, the new .msi file must remain compatible with the layout of the original source.</span></span>

<span data-ttu-id="f4f19-108">Quando si crea un pacchetto di patch, è necessario utilizzare un'immagine di installazione non compressa per creare una patch, ad esempio un'immagine amministrativa o un'immagine di configurazione non compressa da un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="f4f19-108">When you author a patch package you must use an uncompressed setup image to create a patch, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="f4f19-109">È necessario inoltre rispettare le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4f19-109">You must also adhere to the following restrictions:</span></span>

-   <span data-ttu-id="f4f19-110">Non spostare i file da una cartella a un'altra.</span><span class="sxs-lookup"><span data-stu-id="f4f19-110">Do not move files from one folder to another.</span></span>
-   <span data-ttu-id="f4f19-111">Non spostare i file da un file CAB a un altro.</span><span class="sxs-lookup"><span data-stu-id="f4f19-111">Do not move files from one cabinet to another.</span></span>
-   <span data-ttu-id="f4f19-112">Non modificare l'ordine dei file in un file CAB.</span><span class="sxs-lookup"><span data-stu-id="f4f19-112">Do not change the order of files in a cabinet.</span></span>
-   <span data-ttu-id="f4f19-113">Non modificare il numero di sequenza dei file esistenti.</span><span class="sxs-lookup"><span data-stu-id="f4f19-113">Do not change the sequence number of existing files.</span></span> <span data-ttu-id="f4f19-114">Il numero di sequenza è il valore specificato nella colonna sequenza della [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4f19-114">The sequence number is the value specified in the Sequence column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="f4f19-115">Tutti i nuovi file aggiunti dalla patch devono essere inseriti alla fine della sequenza di file esistente.</span><span class="sxs-lookup"><span data-stu-id="f4f19-115">Any new files that are added by the patch must be placed at the end of the existing file sequence.</span></span> <span data-ttu-id="f4f19-116">Il numero di sequenza di un nuovo file nell'immagine aggiornata deve essere maggiore del numero di sequenza più grande dei file esistenti nell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f4f19-116">The sequence number of any new file in the upgraded image must be greater than the largest sequence number of existing files in the target image.</span></span>
-   <span data-ttu-id="f4f19-117">Non modificare le chiavi primarie nella [tabella file](file-table.md) tra le versioni originali e nuove del file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="f4f19-117">Do not change the primary keys in the [File Table](file-table.md) between the original and new .msi file versions.</span></span>
    > [!Note]  
    > <span data-ttu-id="f4f19-118">Il file deve avere la stessa chiave nella [tabella file](file-table.md) dell'immagine di destinazione e dell'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="f4f19-118">The file must have the same key in the [File Table](file-table.md) of both the target image and the updated image.</span></span> <span data-ttu-id="f4f19-119">I valori stringa nella colonna file di entrambe le tabelle devono essere identici, inclusa la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f4f19-119">The string values in the File column of both tables must be identical, including the case.</span></span>

     

-   <span data-ttu-id="f4f19-120">Non creare un pacchetto con chiavi della [tabella file](file-table.md) che differiscono solo per le maiuscole/minuscole, ad esempio, evitare l'esempio di tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f4f19-120">Do not author a package with [File Table](file-table.md) keys that differ only in case, for example, avoid the following table example.</span></span>

    

    | <span data-ttu-id="f4f19-121">File</span><span class="sxs-lookup"><span data-stu-id="f4f19-121">File</span></span>       | <span data-ttu-id="f4f19-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="f4f19-122">Component\_</span></span> | <span data-ttu-id="f4f19-123">FileName</span><span class="sxs-lookup"><span data-stu-id="f4f19-123">FileName</span></span>   |
    |------------|-------------|------------|
    | <span data-ttu-id="f4f19-124">readme.txt</span><span class="sxs-lookup"><span data-stu-id="f4f19-124">readme.txt</span></span> | <span data-ttu-id="f4f19-125">Comp1</span><span class="sxs-lookup"><span data-stu-id="f4f19-125">Comp1</span></span>       | <span data-ttu-id="f4f19-126">readme.txt</span><span class="sxs-lookup"><span data-stu-id="f4f19-126">readme.txt</span></span> |
    | <span data-ttu-id="f4f19-127">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="f4f19-127">ReadMe.txt</span></span> | <span data-ttu-id="f4f19-128">Comp2</span><span class="sxs-lookup"><span data-stu-id="f4f19-128">Comp2</span></span>       | <span data-ttu-id="f4f19-129">readme.txt</span><span class="sxs-lookup"><span data-stu-id="f4f19-129">readme.txt</span></span> |

    

     

    <span data-ttu-id="f4f19-130">Il Windows Installer può consentire l'esempio di tabella precedente quando comp1 e comp2 sono installati in directory diverse, ma non è possibile usare [Msimsp.exe](msimsp-exe.md) o [Patchwiz.dll](patchwiz-dll.md) per generare una patch per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f4f19-130">The Windows Installer can allow the previous table example when Comp1 and Comp2 are installed on different directories, but then you cannot use [Msimsp.exe](msimsp-exe.md) or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package.</span></span> <span data-ttu-id="f4f19-131">Msimsp.exe e Patchwiz.dll chiamano Makecab.exe, senza distinzione tra maiuscole e minuscole e con esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f4f19-131">Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive and fails.</span></span>

    <span data-ttu-id="f4f19-132">Quando si usano i modelli merge nel programma di installazione, assicurarsi che i numeri di sequenza e il layout dei file rispettino le linee guida indicate sopra.</span><span class="sxs-lookup"><span data-stu-id="f4f19-132">When using merge modules in the setup, ensure that file sequence numbers and layout adhere to the above guidelines.</span></span>

 

 



