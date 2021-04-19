---
description: L'azione MsiConfigureServices configura un servizio per il sistema. Questa azione esegue una query sulle tabelle MsiServiceConfig e MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Azione MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319965"
---
# <a name="msiconfigureservices-action"></a><span data-ttu-id="ee146-104">Azione MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="ee146-104">MsiConfigureServices Action</span></span>

<span data-ttu-id="ee146-105">L'azione MsiConfigureServices configura un servizio per il sistema.</span><span class="sxs-lookup"><span data-stu-id="ee146-105">The MsiConfigureServices action configures a service for the system.</span></span> <span data-ttu-id="ee146-106">Questa azione esegue una query sulle tabelle [MsiServiceConfig](msiserviceconfig-table.md) e [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ee146-106">This action queries the [MsiServiceConfig](msiserviceconfig-table.md) and the [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) tables.</span></span>

<span data-ttu-id="ee146-107">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ee146-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="ee146-108">Questa azione è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee146-108">This action is available beginning with Windows Installer 5.0.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ee146-109">Servizi Windows offre la possibilità di eseguire automaticamente azioni predefinite in risposta a un errore in un servizio.</span><span class="sxs-lookup"><span data-stu-id="ee146-109">Windows Services provides the ability to automatically perform predefined actions in response to a failure in a service.</span></span> <span data-ttu-id="ee146-110">Per supportare l'impostazione a livello di codice di queste **azioni di ripristino** in caso di errore di un servizio, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) è stato aggiunto a msi nella versione MSI 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee146-110">To support programmatically setting up these **Recovery Actions** when a service fails, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) was added to MSI in version MSI 5.0.</span></span> <span data-ttu-id="ee146-111">Tuttavia, questa funzionalità non funziona come previsto.</span><span class="sxs-lookup"><span data-stu-id="ee146-111">However, this functionality is not working as expected.</span></span>
>
> <span data-ttu-id="ee146-112">Per aggirare questo problema, uno sviluppatore di applicazioni deve utilizzare la funzionalità **azione personalizzata** in MSI per eseguire **sc.exe** e impostare le **Opzioni di ripristino** in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="ee146-112">To workaround this issue, an application developer should use the **Custom Action** functionality in MSI to run **sc.exe** and set the **Recovery Options** appropriately.</span></span>

 

## <a name="sequence-restrictions"></a><span data-ttu-id="ee146-113">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="ee146-113">Sequence Restrictions</span></span>

<span data-ttu-id="ee146-114">Questa azione standard deve essere utilizzata nella sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="ee146-114">This standard action must be used in the following sequence.</span></span>

[<span data-ttu-id="ee146-115">StopServices</span><span class="sxs-lookup"><span data-stu-id="ee146-115">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="ee146-116">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="ee146-116">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="ee146-117">Una delle azioni seguenti: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ee146-117">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

[<span data-ttu-id="ee146-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="ee146-118">InstallServices</span></span>](installservices-action.md)

<span data-ttu-id="ee146-119">MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="ee146-119">MsiConfigureServices</span></span>

[<span data-ttu-id="ee146-120">StartServices</span><span class="sxs-lookup"><span data-stu-id="ee146-120">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="ee146-121">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="ee146-121">ActionData Messages</span></span>

<span data-ttu-id="ee146-122">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="ee146-122">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee146-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee146-123">Remarks</span></span>

<span data-ttu-id="ee146-124">Per questa azione è necessario che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per installare i servizi o che l'applicazione faccia parte di un'installazione gestita.</span><span class="sxs-lookup"><span data-stu-id="ee146-124">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



