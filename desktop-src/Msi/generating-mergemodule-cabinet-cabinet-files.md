---
description: Ogni file che viene recapitato al pacchetto di installazione di destinazione dal modulo merge deve essere archiviato all'interno di un file CAB incorporato come flusso all'interno del file. msm. Il nome di questo file CAB è sempre MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Generazione di MergeModule.CABfile CAB inet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314264"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a><span data-ttu-id="88c27-104">Generazione di MergeModule.CABfile CAB inet</span><span class="sxs-lookup"><span data-stu-id="88c27-104">Generating MergeModule.CABinet Cabinet Files</span></span>

<span data-ttu-id="88c27-105">Ogni file che viene recapitato al pacchetto di installazione di destinazione dal modulo merge deve essere archiviato all'interno di un file CAB incorporato come flusso all'interno del file. msm.</span><span class="sxs-lookup"><span data-stu-id="88c27-105">Every file that is delivered to the target installation package by the merge module must be stored inside of a cabinet file embedded as a stream inside the .msm file.</span></span> <span data-ttu-id="88c27-106">Il nome di questo file CAB è sempre MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="88c27-106">The name of this cabinet is always MergeModule.CABinet.</span></span>

<span data-ttu-id="88c27-107">I nomi dei file in MergeModule.CABinet devono corrispondere alle chiavi primarie utilizzate nella [tabella dei file](file-table.md) del modulo merge e devono rispettare la convenzione descritta in [denominazione delle chiavi primarie nei database dei moduli di merge](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="88c27-107">The names of files in MergeModule.CABinet must match the primary keys used in the merge module's [File table](file-table.md) and must adhere to the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="88c27-108">Il programma di installazione ignora i file aggiuntivi inclusi in MergeModule.CABinet che non sono elencati nella [tabella file](file-table.md)del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="88c27-108">The installer skips extra files included in MergeModule.CABinet that are not listed in the merge module's [File table](file-table.md).</span></span> <span data-ttu-id="88c27-109">I numeri di sequenza dei file specificati nella tabella file non devono essere consecutivi, ma devono seguire la stessa sequenza dei file archiviati all'interno di MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="88c27-109">The sequence numbers of files specified in the File table do not need to be consecutive, but they must follow the same sequence as the files stored inside MergeModule.CABinet.</span></span> <span data-ttu-id="88c27-110">Per ulteriori informazioni, vedere [creazione di tabelle di file del modulo merge](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="88c27-110">For more information, see [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

<span data-ttu-id="88c27-111">Ciò significa che un singolo file CAB può contenere tutti i file necessari per il supporto di più lingue da parte di un modulo merge.</span><span class="sxs-lookup"><span data-stu-id="88c27-111">This means that a single cabinet file can contain all the files needed for a merge module to support multiple languages.</span></span> <span data-ttu-id="88c27-112">A tutti i file della lingua è possibile assegnare numeri di sequenza univoci nel file CAB, quindi è possibile utilizzare una trasformazione lingua per aggiungere o rimuovere file dalla tabella file per ottenere un modulo merge per una determinata lingua.</span><span class="sxs-lookup"><span data-stu-id="88c27-112">All the language files can be given unique sequence numbers in the cabinet and then a language transform can be used to add or remove files from the File table to obtain a merge module for a particular language.</span></span> <span data-ttu-id="88c27-113">Per informazioni dettagliate, vedere la pagina relativa alla creazione di modelli di [Unione di più linguaggi](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="88c27-113">For details, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="88c27-114">È possibile aggiungere MergeModule.CABinet al modulo merge aprendo una [ \_ tabella dei flussi](-streams-table.md)temporanei.</span><span class="sxs-lookup"><span data-stu-id="88c27-114">MergeModule.CABinet can be added to the merge module by opening a temporary [\_Streams Table](-streams-table.md).</span></span> <span data-ttu-id="88c27-115">Ad esempio, lo strumento Msidb.exe fornito con Windows Installer SDK può essere usato per aggiungere il MergeModule.CABinet al modulo merge.</span><span class="sxs-lookup"><span data-stu-id="88c27-115">For example, the tool Msidb.exe provided with the Windows Installer SDK can be used to add the MergeModule.CABinet to the merge module.</span></span> <span data-ttu-id="88c27-116">Per ulteriori informazioni, vedere [inclusione di un file CAB in un'installazione](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="88c27-116">For more information, see [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



