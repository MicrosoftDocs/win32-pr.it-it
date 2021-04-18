---
description: Le opzioni di ripristino consentono ai richiedenti di comunicare opzioni di ripristino personalizzate ai writer.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Impostazione delle opzioni di ripristino VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310667"
---
# <a name="setting-vss-restore-options"></a><span data-ttu-id="7bb61-103">Impostazione delle opzioni di ripristino VSS</span><span class="sxs-lookup"><span data-stu-id="7bb61-103">Setting VSS Restore Options</span></span>

<span data-ttu-id="7bb61-104">Le opzioni di ripristino consentono ai richiedenti di comunicare opzioni di ripristino personalizzate ai writer.</span><span class="sxs-lookup"><span data-stu-id="7bb61-104">Restore options allow requesters to communicate customized restore options to writers.</span></span>

## <a name="restore-options"></a><span data-ttu-id="7bb61-105">Opzioni di ripristino</span><span class="sxs-lookup"><span data-stu-id="7bb61-105">Restore Options</span></span>

<span data-ttu-id="7bb61-106">La standardizzazione del formato delle opzioni di ripristino consente a writer e richiedenti di gestire richieste personalizzate comuni.</span><span class="sxs-lookup"><span data-stu-id="7bb61-106">Standardizing the format of the restore options allow writers and requesters to handle common custom requests.</span></span> <span data-ttu-id="7bb61-107">Le opzioni di ripristino vengono impostate dal richiedente chiamando il metodo [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) fino a una volta per ogni componente selezionato per il backup prima di chiamare il metodo [**rerestore IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .</span><span class="sxs-lookup"><span data-stu-id="7bb61-107">Restore options are set by the requester by calling the [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method up to once per selected-for-backup component before calling the [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) method.</span></span> <span data-ttu-id="7bb61-108">La stringa passata nel parametro *wszRestoreOptions* al metodo **SetRestoreOptions** può contenere più valori, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="7bb61-108">The string passed in the *wszRestoreOptions* parameter to the **SetRestoreOptions** method can contain multiple values, as described below.</span></span>

## <a name="format"></a><span data-ttu-id="7bb61-109">Formato</span><span class="sxs-lookup"><span data-stu-id="7bb61-109">Format</span></span>

<span data-ttu-id="7bb61-110">Il formato delle opzioni di ripristino è costituito da una o più coppie nome/valore separate da virgole e il nome è facoltativamente preceduto dal nome del sottocomponente a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="7bb61-110">The format of restore options, is one or more comma-separated name/value pairs, and the name is optionally prefixed with the name of the subcomponent to which it applies.</span></span> <span data-ttu-id="7bb61-111">I nomi dei componenti e i nomi delle opzioni non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7bb61-111">The component names and option names are case-insensitive.</span></span> <span data-ttu-id="7bb61-112">La distinzione tra maiuscole e minuscole dei valori è determinata dal writer.</span><span class="sxs-lookup"><span data-stu-id="7bb61-112">The case-sensitivity of the values is determined by the writer.</span></span> <span data-ttu-id="7bb61-113">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7bb61-113">For example:</span></span>

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

<span data-ttu-id="7bb61-114">In questo esempio "opzione1" si applica solo al sottocomponente "child1" e ai relativi discendenti, "opzione2" si applica a tutti i componenti e ai relativi discendenti e "Option3" si applica solo ai \\ sottocomponenti "child2 Grandchild3" e ai relativi discendenti.</span><span class="sxs-lookup"><span data-stu-id="7bb61-114">In this example, "Option1" only applies to the "Child1" subcomponent and its descendants, "Option2" applies to all components and their descendants, and "Option3" applies only to the "Child2\\Grandchild3" subcomponents and its descendants.</span></span>

<span data-ttu-id="7bb61-115">Il metodo [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) può essere chiamato solo su componenti selezionabili per il backup, mentre i nodi discendenti non possono essere selezionati per il backup, possono essere selezionati per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="7bb61-115">The [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method can only be called on components that are selectable for backup, while descendant nodes may not be selectable for backup, they may be selectable for restore.</span></span>

## <a name="common-restore-options"></a><span data-ttu-id="7bb61-116">Opzioni di ripristino comuni</span><span class="sxs-lookup"><span data-stu-id="7bb61-116">Common Restore Options</span></span>

<span data-ttu-id="7bb61-117">Queste opzioni di ripristino comuni sono state definite per aumentare l'interoperabilità tra writer e richiedenti.</span><span class="sxs-lookup"><span data-stu-id="7bb61-117">These common restore options have been defined to increase interoperability between writers and requesters.</span></span>

-   <span data-ttu-id="7bb61-118">Autorevole</span><span class="sxs-lookup"><span data-stu-id="7bb61-118">Authoritative</span></span>

    <span data-ttu-id="7bb61-119">L'opzione "autorevole" supporta più valori "Item", ma solo un valore "All".</span><span class="sxs-lookup"><span data-stu-id="7bb61-119">The "Authoritative" option supports multiple "Item" values, but only one "All" value.</span></span>

    <span data-ttu-id="7bb61-120">Questo intero componente è autorevole.</span><span class="sxs-lookup"><span data-stu-id="7bb61-120">This entire component is authoritative.</span></span>

    ``` syntax
    "Authoritative"="All"
    ```

    <span data-ttu-id="7bb61-121">Solo l'elemento specificato è autorevole.</span><span class="sxs-lookup"><span data-stu-id="7bb61-121">Only the specified item is authoritative.</span></span> <span data-ttu-id="7bb61-122">Il formato dell'elemento denominato è definito dal writer.</span><span class="sxs-lookup"><span data-stu-id="7bb61-122">The format of the named item is defined by the writer.</span></span> <span data-ttu-id="7bb61-123">Le designazioni comuni sono " \* " per indicare tutti i file, "..." per indicare tutti i file e le sottodirectory del componente specificato.</span><span class="sxs-lookup"><span data-stu-id="7bb61-123">Common designations are "\*" to indicate all files, "..." to indicate all files and subdirectories of the specified component.</span></span>

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   <span data-ttu-id="7bb61-124">Rollforward</span><span class="sxs-lookup"><span data-stu-id="7bb61-124">Roll Forward</span></span>

    <span data-ttu-id="7bb61-125">Dopo il ripristino di un database, in genere i writer eseguono il rollforward dei log per rendere aggiornato il database.</span><span class="sxs-lookup"><span data-stu-id="7bb61-125">After a database is restored, writers usually roll forward through logs to bring the database up to date.</span></span> <span data-ttu-id="7bb61-126">Nel caso di ripristini incrementali o differenziali, il richiedente usa il metodo [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) per controllare parzialmente il comportamento di gestione dei log. questa opzione di ripristino consente un controllo più granulare.</span><span class="sxs-lookup"><span data-stu-id="7bb61-126">In the case of incremental or differential restores, the requester uses the [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) method to partially control the log-handling behavior - this restore option allows more granular control.</span></span>

    <span data-ttu-id="7bb61-127">Non eseguire il rollup dei log.</span><span class="sxs-lookup"><span data-stu-id="7bb61-127">Do not roll through logs.</span></span>

    ``` syntax
    "Roll Forward"="None"
    ```

    <span data-ttu-id="7bb61-128">Scorrere tutti i log.</span><span class="sxs-lookup"><span data-stu-id="7bb61-128">Roll through all logs.</span></span>

    ``` syntax
    "Roll Forward"="All"
    ```

    <span data-ttu-id="7bb61-129">Eseguire il rollup dei log fino al punto specificato.</span><span class="sxs-lookup"><span data-stu-id="7bb61-129">Roll through logs up to specified point.</span></span> <span data-ttu-id="7bb61-130">Il formato del punto specificato è definito dal writer.</span><span class="sxs-lookup"><span data-stu-id="7bb61-130">The format of the specified point is defined by the writer.</span></span>

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   <span data-ttu-id="7bb61-131">Nome nuovo componente</span><span class="sxs-lookup"><span data-stu-id="7bb61-131">New Component Name</span></span>

    <span data-ttu-id="7bb61-132">Un writer potrebbe voler ripristinare un componente in un nuovo nome.</span><span class="sxs-lookup"><span data-stu-id="7bb61-132">A writer may want to restore a component to a new name.</span></span> <span data-ttu-id="7bb61-133">Ad esempio, il ripristino di un database con un nome diverso per il ripristino di un singolo elemento. il ripristino con lo stesso nome richiederebbe a tutti i dati che i writer accettino un percorso logico e un nome di componente validi come valore di questa opzione.</span><span class="sxs-lookup"><span data-stu-id="7bb61-133">For example, restoring a database to a different name to restore an individual item; restoring to the same name would please all data We recommend that writers accept a valid logical path and component name as this options' value.</span></span> <span data-ttu-id="7bb61-134">Questa operazione viene spesso usata con una [*destinazione diretta*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="7bb61-134">This will often be used with a [*directed target*](vssgloss-d.md).</span></span>

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



