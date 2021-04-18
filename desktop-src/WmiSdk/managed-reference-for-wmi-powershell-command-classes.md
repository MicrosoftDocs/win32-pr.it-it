---
description: Riferimenti gestiti per le classi di comandi WMI di Windows PowerShell
ms.assetid: 30e77956-8428-4259-9218-b93f143fd987
ms.tgt_platform: multiple
title: Riferimenti gestiti per le classi di comandi WMI di Windows PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb309a9ca421a3966f84ba1ae825bd0c81eee8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316565"
---
# <a name="managed-reference-for-wmi-windows-powershell-command-classes"></a><span data-ttu-id="5ce25-103">Riferimenti gestiti per le classi di comandi WMI di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ce25-103">Managed Reference for WMI Windows PowerShell Command Classes</span></span>

<span data-ttu-id="5ce25-104">Windows PowerShell implementa la funzionalità Strumentazione gestione Windows (WMI) tramite un set di cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ce25-104">Windows PowerShell implements Windows Management Instrumentation (WMI) functionality through a set of cmdlets.</span></span> <span data-ttu-id="5ce25-105">È possibile utilizzare questi cmdlet per completare le attività end-to-end necessarie per gestire i computer locali e remoti.</span><span class="sxs-lookup"><span data-stu-id="5ce25-105">You can use these cmdlets to complete the end-to-end tasks that are necessary to manage local and remote computers.</span></span>

<span data-ttu-id="5ce25-106">Per ulteriori informazioni, vedere [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5ce25-106">See [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) for more information.</span></span>

## <a name="wmi-powershell-classes"></a><span data-ttu-id="5ce25-107">Classi PowerShell WMI</span><span class="sxs-lookup"><span data-stu-id="5ce25-107">WMI PowerShell Classes</span></span>

<span data-ttu-id="5ce25-108">**Spazio dei nomi**: Microsoft. PowerShell. Commands</span><span class="sxs-lookup"><span data-stu-id="5ce25-108">**Namespace**: Microsoft.PowerShell.Commands</span></span>

<span data-ttu-id="5ce25-109">**Assembly**: Microsoft. PowerShell. Commands. Management</span><span class="sxs-lookup"><span data-stu-id="5ce25-109">**Assembly**: Microsoft.PowerShell.Commands.Management</span></span>

<span data-ttu-id="5ce25-110">**Dll**: Microsoft.PowerShell.Commands.Management.dll</span><span class="sxs-lookup"><span data-stu-id="5ce25-110">**DLL**: Microsoft.PowerShell.Commands.Management.dll</span></span>

<span data-ttu-id="5ce25-111">Queste classi di comandi WMI sono implementate da Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ce25-111">These WMI command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="5ce25-112">Queste classi sono incluse in questo Software Development Kit (SDK) solo per completezza.</span><span class="sxs-lookup"><span data-stu-id="5ce25-112">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="5ce25-113">I membri di queste classi non possono essere usati direttamente, né devono essere usati per derivare altre classi.</span><span class="sxs-lookup"><span data-stu-id="5ce25-113">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="5ce25-114">Classe</span><span class="sxs-lookup"><span data-stu-id="5ce25-114">Class</span></span>                   | <span data-ttu-id="5ce25-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ce25-115">Description</span></span>                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce25-116">GetWmiObjectCommand</span><span class="sxs-lookup"><span data-stu-id="5ce25-116">GetWmiObjectCommand</span></span>     | <span data-ttu-id="5ce25-117">Ottiene le istanze di classi WMI o informazioni sulle classi disponibili.</span><span class="sxs-lookup"><span data-stu-id="5ce25-117">Gets instances of WMI classes or information about the available classes.</span></span><br/> <span data-ttu-id="5ce25-118">Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="5ce25-118">See the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/> |
| <span data-ttu-id="5ce25-119">InvokeWmiMethod</span><span class="sxs-lookup"><span data-stu-id="5ce25-119">InvokeWmiMethod</span></span>         | <span data-ttu-id="5ce25-120">Chiama i metodi di WMI.</span><span class="sxs-lookup"><span data-stu-id="5ce25-120">Calls WMI methods.</span></span><br/> <span data-ttu-id="5ce25-121">Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="5ce25-121">See the [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                                     |
| <span data-ttu-id="5ce25-122">RegisterWmiEventCommand</span><span class="sxs-lookup"><span data-stu-id="5ce25-122">RegisterWmiEventCommand</span></span> | <span data-ttu-id="5ce25-123">Sottoscrive un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="5ce25-123">Subscribes to a WMI event.</span></span><br/> <span data-ttu-id="5ce25-124">Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="5ce25-124">See the [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                            |
| <span data-ttu-id="5ce25-125">RemoveWmiObject</span><span class="sxs-lookup"><span data-stu-id="5ce25-125">RemoveWmiObject</span></span>         | <span data-ttu-id="5ce25-126">Elimina un'istanza di una classe WMI esistente.</span><span class="sxs-lookup"><span data-stu-id="5ce25-126">Deletes an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="5ce25-127">Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="5ce25-127">See the [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                          |
| <span data-ttu-id="5ce25-128">SetWmiInstance</span><span class="sxs-lookup"><span data-stu-id="5ce25-128">SetWmiInstance</span></span>          | <span data-ttu-id="5ce25-129">Crea o aggiorna un'istanza di una classe WMI esistente.</span><span class="sxs-lookup"><span data-stu-id="5ce25-129">Creates or updates an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="5ce25-130">Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="5ce25-130">See the [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                |



 

 

