---
description: Per generare un modulo merge, è necessario ottenere uno strumento software con cui modificare un file con estensione MSM.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Recupero di strumenti di creazione di moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308682"
---
# <a name="obtaining-merge-module-authoring-tools"></a><span data-ttu-id="db9e6-103">Recupero di strumenti di creazione di moduli merge</span><span class="sxs-lookup"><span data-stu-id="db9e6-103">Obtaining Merge Module Authoring Tools</span></span>

<span data-ttu-id="db9e6-104">Per generare un modulo merge, è necessario ottenere uno strumento software con cui modificare un file con estensione MSM.</span><span class="sxs-lookup"><span data-stu-id="db9e6-104">To generate a merge module, you need to obtain a software tool with which to edit an .msm file.</span></span> <span data-ttu-id="db9e6-105">Poiché un file con estensione MSM è fondamentalmente un file con estensione msi semplificato, potrebbe essere possibile utilizzare gli stessi strumenti utilizzati per creare un database di installazione.</span><span class="sxs-lookup"><span data-stu-id="db9e6-105">Because an .msm file is basically a simplified .msi file, you may be able to use the same tools used to create an installation database.</span></span> <span data-ttu-id="db9e6-106">Ad esempio, l'applicazione Orca.exe fornita con Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="db9e6-106">For example, the application Orca.exe provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="db9e6-107">In alternativa, è possibile acquistare uno degli strumenti per la creazione di pacchetti del programma di installazione di da fornitori di software indipendenti.</span><span class="sxs-lookup"><span data-stu-id="db9e6-107">An alternative is to purchase one of the installer packaging tools to be available from independent software vendors.</span></span> <span data-ttu-id="db9e6-108">Sono disponibili diversi strumenti di terze parti in fase di sviluppo che possono essere utilizzati per la creazione di moduli unione.</span><span class="sxs-lookup"><span data-stu-id="db9e6-108">There are several third-party tools under development that may be used for producing merge modules.</span></span> <span data-ttu-id="db9e6-109">Se si sceglie di utilizzare uno strumento di terze parti, è necessario verificare che generi moduli unione coerenti con lo standard descritto in questo documento.</span><span class="sxs-lookup"><span data-stu-id="db9e6-109">If you choose to use a third-party tool you should verify that it generates merge modules that are consistent with the standard described in this document.</span></span> <span data-ttu-id="db9e6-110">In particolare, è necessario determinare che gli strumenti di modifica non hanno eseguito alcuna delle operazioni seguenti nel modulo merge.</span><span class="sxs-lookup"><span data-stu-id="db9e6-110">In particular, you should determine that the editing tools have not done any of the following to the merge module.</span></span>

-   <span data-ttu-id="db9e6-111">Aggiunta di tabelle estranee al modulo merge a cui non viene fatto riferimento nella [tabella ModuleIgnoreTable](moduleignoretable-table.md).</span><span class="sxs-lookup"><span data-stu-id="db9e6-111">Added extraneous tables to the merge module that are not referenced in the [ModuleIgnoreTable table](moduleignoretable-table.md).</span></span>

    <span data-ttu-id="db9e6-112">Eliminare queste tabelle o aggiungerle alla tabella ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="db9e6-112">Delete these tables or add them to the ModuleIgnoreTable table.</span></span>

-   <span data-ttu-id="db9e6-113">Aggiunta di una [tabella TextStyle](textstyle-table.md) non necessaria al modulo merge.</span><span class="sxs-lookup"><span data-stu-id="db9e6-113">Added an unnecessary [TextStyle table](textstyle-table.md) to the merge module.</span></span>

    <span data-ttu-id="db9e6-114">Se il modulo merge non dispone di un'interfaccia utente (e in genere non lo è), è possibile eliminare la tabella in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="db9e6-114">If your merge module has no UI (and it generally should not) you can safely delete this table.</span></span>

-   <span data-ttu-id="db9e6-115">Aggiunta di voci non necessarie alla [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="db9e6-115">Added unnecessary entries to the [Directory table](directory-table.md).</span></span>

    <span data-ttu-id="db9e6-116">Rimuovere le voci non necessarie dalla tabella directory.</span><span class="sxs-lookup"><span data-stu-id="db9e6-116">Remove unnecessary entries from the Directory table.</span></span>

-   <span data-ttu-id="db9e6-117">Informazioni lasciate fuori dalla tabella di convalida del modulo di Unione \_ .</span><span class="sxs-lookup"><span data-stu-id="db9e6-117">Left information out of the merge module's \_Validation table.</span></span>

    <span data-ttu-id="db9e6-118">In questo modo si impedisce la convalida del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="db9e6-118">This prevents merge module validation.</span></span> <span data-ttu-id="db9e6-119">Aggiungere una \_ tabella di convalida completa.</span><span class="sxs-lookup"><span data-stu-id="db9e6-119">Add a complete \_Validation table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db9e6-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db9e6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db9e6-121">Creazione di interfacce utente nei moduli merge</span><span class="sxs-lookup"><span data-stu-id="db9e6-121">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="db9e6-122">Creazione di tabelle di directory del modulo merge</span><span class="sxs-lookup"><span data-stu-id="db9e6-122">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="db9e6-123">Convalida di moduli merge</span><span class="sxs-lookup"><span data-stu-id="db9e6-123">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> </dl>

 

 



