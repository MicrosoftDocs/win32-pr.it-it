---
description: I moduli merge sono essenzialmente file con estensione msi semplificati, ovvero l'estensione del nome file per un pacchetto di installazione Windows Installer. Un modulo merge standard ha un'estensione del nome di file MSM.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Informazioni sui moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345171"
---
# <a name="about-merge-modules"></a><span data-ttu-id="5290a-104">Informazioni sui moduli merge</span><span class="sxs-lookup"><span data-stu-id="5290a-104">About Merge Modules</span></span>

<span data-ttu-id="5290a-105">I moduli merge sono essenzialmente file con estensione msi semplificati, ovvero l'estensione del nome file per un pacchetto di installazione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5290a-105">Merge modules are essentially simplified .msi files, which is the file name extension for a Windows Installer installation package.</span></span> <span data-ttu-id="5290a-106">Un modulo merge standard ha un'estensione del nome di file MSM.</span><span class="sxs-lookup"><span data-stu-id="5290a-106">A standard merge module has an .msm file name extension.</span></span>

<span data-ttu-id="5290a-107">Un modulo merge non può essere installato da solo perché mancano alcune tabelle di database fondamentali presenti in un database di installazione.</span><span class="sxs-lookup"><span data-stu-id="5290a-107">A merge module cannot be installed alone because its lacks some vital database tables that are present in an installation database.</span></span> <span data-ttu-id="5290a-108">I moduli merge contengono anche tabelle aggiuntive univoche per se stesse.</span><span class="sxs-lookup"><span data-stu-id="5290a-108">Merge modules also contain additional tables that are unique to themselves.</span></span> <span data-ttu-id="5290a-109">Per installare le informazioni fornite da un modulo merge con un'applicazione, è necessario innanzitutto eseguire il merge del modulo nel file con estensione msi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5290a-109">To install the information delivered by a merge module with an application, the module must first be merged into the application's .msi file.</span></span>

<span data-ttu-id="5290a-110">Un modulo merge è costituito dalle parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="5290a-110">A merge module consists of the following parts:</span></span>

-   <span data-ttu-id="5290a-111">Un [database del modulo merge](merge-module-database.md) contenente le proprietà di installazione e la logica di installazione fornita dal modulo merge.</span><span class="sxs-lookup"><span data-stu-id="5290a-111">A [Merge Module Database](merge-module-database.md) containing the installation properties and setup logic being delivered by the merge module.</span></span>
-   <span data-ttu-id="5290a-112">[Riferimento al flusso di informazioni di riepilogo del modulo merge](merge-module-summary-information-stream-reference.md) che descrive il modulo.</span><span class="sxs-lookup"><span data-stu-id="5290a-112">A [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md) describing the module.</span></span>
-   <span data-ttu-id="5290a-113">Un file CAB [MergeModule.CABinet](mergemodule-cabinet.md) archiviato come flusso all'interno del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="5290a-113">A [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file stored as a stream inside the merge module.</span></span> <span data-ttu-id="5290a-114">Questo cabinet contiene tutti i file necessari per i componenti forniti dal modulo merge.</span><span class="sxs-lookup"><span data-stu-id="5290a-114">This cabinet contains all the files required by the components delivered by the merge module.</span></span>

<span data-ttu-id="5290a-115">I [moduli di Unione con più](multiple-language-merge-modules.md) lingue possono fornire componenti a un pacchetto di installazione in più linguaggi.</span><span class="sxs-lookup"><span data-stu-id="5290a-115">[Multiple language merge modules](multiple-language-merge-modules.md) can deliver components to an installation package in multiple languages.</span></span> <span data-ttu-id="5290a-116">In un modulo di Unione a più lingue il database contiene le proprietà di installazione e la logica per più di un linguaggio e il cabinet MergeModule.CABinet include tutti i file necessari per installare i componenti con tutte le lingue supportate dal modulo.</span><span class="sxs-lookup"><span data-stu-id="5290a-116">In a multiple language merge module the database contains the installation properties and logic for more than one language and the MergeModule.CABinet cabinet includes all the files necessary to install components with all the languages supported by the module.</span></span>

 

 



