---
title: Riferimenti gestiti per i comandi PowerShell di BITS
description: Servizio trasferimento intelligente in background (BITS) 4,0 può utilizzare i cmdlet di Windows PowerShell per gestire i processi di trasferimento.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bd195d2202849c2bf2df580d159ee401911c51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872750"
---
# <a name="managed-reference-for-bits-powershell-commands"></a><span data-ttu-id="b8532-103">Riferimenti gestiti per i comandi PowerShell di BITS</span><span class="sxs-lookup"><span data-stu-id="b8532-103">Managed Reference for BITS PowerShell Commands</span></span>

<span data-ttu-id="b8532-104">Servizio trasferimento intelligente in background (BITS) 4,0 può utilizzare i cmdlet di Windows PowerShell per creare e gestire i processi di download e caricamento dei file.</span><span class="sxs-lookup"><span data-stu-id="b8532-104">Background Intelligent Transfer Service (BITS) 4.0 can use Windows PowerShell cmdlets to create and manage file download and upload transfer jobs.</span></span>

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

<span data-ttu-id="b8532-105">I cmdlet di Windows PowerShell per BITS forniscono gran parte delle funzionalità dell'utilità della riga di comando Bitsadmin.</span><span class="sxs-lookup"><span data-stu-id="b8532-105">Windows PowerShell cmdlets for BITS provide much of the same functionality as the bitsadmin command-line utility.</span></span> <span data-ttu-id="b8532-106">Tuttavia, Windows PowerShell esegue anche le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8532-106">However, Windows PowerShell also does the following:</span></span>

-   <span data-ttu-id="b8532-107">Automatizza le attività BITS in un linguaggio di scripting estendibile e orientato alla gestione.</span><span class="sxs-lookup"><span data-stu-id="b8532-107">Automates BITS tasks in an extensible and management-oriented scripting language.</span></span>
-   <span data-ttu-id="b8532-108">Fornisce un unico strumento per tutte le attività correlate ai processi.</span><span class="sxs-lookup"><span data-stu-id="b8532-108">Provides a single tool for all job-related tasks.</span></span>

> [!Note]  
> <span data-ttu-id="b8532-109">Per usare questi comandi, è necessario prima importare il modulo PowerShell BITS, usando il `Import-Module BitsTransfer` comando.</span><span class="sxs-lookup"><span data-stu-id="b8532-109">To use these commands, you must first import the BITS PowerShell module, using the `Import-Module BitsTransfer` command.</span></span> <span data-ttu-id="b8532-110">Per ulteriori informazioni, vedere l' [articolo TechNet](/previous-versions/technet-magazine/ff382721(v=msdn.10))seguente.</span><span class="sxs-lookup"><span data-stu-id="b8532-110">For more information, see the following [TechNet article](/previous-versions/technet-magazine/ff382721(v=msdn.10)).</span></span>

 

<span data-ttu-id="b8532-111">Per ulteriori informazioni sull'utilizzo di Windows PowerShell, vedere [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="b8532-111">For more information on using Windows Powershell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).</span></span>

## <a name="bits-powershell-classes"></a><span data-ttu-id="b8532-112">Classi PowerShell BITS</span><span class="sxs-lookup"><span data-stu-id="b8532-112">BITS PowerShell Classes</span></span>

<span data-ttu-id="b8532-113">**Spazio dei nomi**: Microsoft. BackgroundIntelligentTransfer. Management</span><span class="sxs-lookup"><span data-stu-id="b8532-113">**Namespace**: Microsoft.BackgroundIntelligentTransfer.Management</span></span>

<span data-ttu-id="b8532-114">**Assembly**: System. Management. Automation</span><span class="sxs-lookup"><span data-stu-id="b8532-114">**Assembly**: System.Management.Automation</span></span>

<span data-ttu-id="b8532-115">Queste classi di comandi BITS sono implementate da Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b8532-115">These BITS command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="b8532-116">Queste classi sono incluse in questo Software Development Kit (SDK) solo per completezza.</span><span class="sxs-lookup"><span data-stu-id="b8532-116">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="b8532-117">I membri di queste classi non possono essere usati direttamente, né devono essere usati per derivare altre classi.</span><span class="sxs-lookup"><span data-stu-id="b8532-117">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="b8532-118">Classe</span><span class="sxs-lookup"><span data-stu-id="b8532-118">Class</span></span>                           | <span data-ttu-id="b8532-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8532-119">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8532-120">**AddBitsFileCommand**</span><span class="sxs-lookup"><span data-stu-id="b8532-120">**AddBitsFileCommand**</span></span>          | <span data-ttu-id="b8532-121">Aggiunge uno o più file a un processo di trasferimento BITS esistente.</span><span class="sxs-lookup"><span data-stu-id="b8532-121">Adds one or more files to an existing BITS transfer job.</span></span><br/> <span data-ttu-id="b8532-122">Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Add-BitsFile](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8532-122">See the [Add-BitsFile](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                       |
| <span data-ttu-id="b8532-123">**ClearBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="b8532-123">**ClearBitsTransferCommand**</span></span>    | <span data-ttu-id="b8532-124">Annulla un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="b8532-124">Cancels a BITS transfer job.</span></span><br/> <span data-ttu-id="b8532-125">Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8532-125">See the [Clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                          |
| <span data-ttu-id="b8532-126">**CompleteBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="b8532-126">**CompleteBitsTransferCommand**</span></span> | <span data-ttu-id="b8532-127">Completa un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="b8532-127">Completes a BITS transfer job.</span></span><br/> <span data-ttu-id="b8532-128">Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8532-128">See the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                     |
| <span data-ttu-id="b8532-129">**GetBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="b8532-129">**GetBitsTransferCommand**</span></span>      | <span data-ttu-id="b8532-130">Recupera l'oggetto BitsJob associato per un processo di trasferimento BITS esistente.</span><span class="sxs-lookup"><span data-stu-id="b8532-130">Retrieves the associated BitsJob object for an existing BITS transfer job.</span></span><br/> <span data-ttu-id="b8532-131">Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Get-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8532-131">See the [Get-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/> |
| <span data-ttu-id="b8532-132">**NewBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="b8532-132">**NewBitsTransferCommand**</span></span>      | <span data-ttu-id="b8532-133">Crea un nuovo processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="b8532-133">Creates a new BITS transfer job.</span></span><br/> <span data-ttu-id="b8532-134">Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8532-134">See the [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                           |
| <span data-ttu-id="b8532-135">**ResumeBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="b8532-135">**ResumeBitsTransferCommand**</span></span>   | <span data-ttu-id="b8532-136">Riprende un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="b8532-136">Resumes a BITS transfer job.</span></span><br/> <span data-ttu-id="b8532-137">Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8532-137">See the [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                            |
| <span data-ttu-id="b8532-138">**SetBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="b8532-138">**SetBitsTransferCommand**</span></span>      | <span data-ttu-id="b8532-139">Modifica le proprietà di un processo di trasferimento BITS esistente.</span><span class="sxs-lookup"><span data-stu-id="b8532-139">Modifies the properties of an existing BITS transfer job.</span></span><br/> <span data-ttu-id="b8532-140">Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8532-140">See the [Set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                  |
| <span data-ttu-id="b8532-141">**SuspendBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="b8532-141">**SuspendBitsTransferCommand**</span></span>  | <span data-ttu-id="b8532-142">Sospende un processo di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="b8532-142">Suspends a BITS transfer job.</span></span><br/> <span data-ttu-id="b8532-143">Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8532-143">See the [Suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                          |



 

 

