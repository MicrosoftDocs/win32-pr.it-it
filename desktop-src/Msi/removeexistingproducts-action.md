---
description: L'azione RemoveExistingProducts passa attraverso i codici prodotto elencati nella colonna ActionProperty della tabella di aggiornamento e rimuove i prodotti in sequenza richiamando le installazioni simultanee.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Azione RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312321"
---
# <a name="removeexistingproducts-action"></a><span data-ttu-id="e9bc3-103">Azione RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="e9bc3-103">RemoveExistingProducts Action</span></span>

<span data-ttu-id="e9bc3-104">L'azione RemoveExistingProducts passa attraverso i codici prodotto elencati nella colonna ActionProperty della tabella di [aggiornamento](upgrade-table.md) e rimuove i prodotti in sequenza richiamando le installazioni simultanee.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-104">The RemoveExistingProducts action goes through the product codes listed in the ActionProperty column of the [Upgrade table](upgrade-table.md) and removes the products in sequence by invoking concurrent installations.</span></span> <span data-ttu-id="e9bc3-105">Per ogni installazione simultanea, il programma di installazione imposta la proprietà [**ProductCode**](productcode.md) sul codice del prodotto e imposta la proprietà [**Remove**](remove.md) sul valore nel campo Remove della tabella upgrade.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-105">For each concurrent installation the installer sets the [**ProductCode**](productcode.md) property to the product code and sets the [**REMOVE**](remove.md) property to the value in the Remove field of the Upgrade table.</span></span> <span data-ttu-id="e9bc3-106">Se il campo Rimuovi è vuoto, il valore predefinito è tutti e il programma di installazione rimuove l'intero prodotto.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-106">If the Remove field is blank, its value defaults to ALL and the installer removes the entire product.</span></span>

<span data-ttu-id="e9bc3-107">Il programma di installazione esegue l'azione RemoveExistingProducts alla prima installazione di un prodotto.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-107">The installer only runs the RemoveExistingProducts action the first time it installs a product.</span></span> <span data-ttu-id="e9bc3-108">Non esegue l'azione durante un'installazione o una disinstallazione di [manutenzione](maintenance-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="e9bc3-108">It does not run the action during a [maintenance installation](maintenance-installation.md) or uninstallation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e9bc3-109">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="e9bc3-109">Sequence Restrictions</span></span>

<span data-ttu-id="e9bc3-110">L'azione RemoveExistingProducts deve essere pianificata nella sequenza di azione in una delle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-110">The RemoveExistingProducts action must be scheduled in the action sequence in one of the following locations.</span></span>

-   <span data-ttu-id="e9bc3-111">Tra l' [azione InstallValidate](installvalidate-action.md) e l' [azione InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e9bc3-111">Between the [InstallValidate action](installvalidate-action.md) and the [InstallInitialize action](installinitialize-action.md).</span></span> <span data-ttu-id="e9bc3-112">In questo caso, il programma di installazione rimuove completamente le applicazioni precedenti prima di installare le nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-112">In this case, the installer removes the old applications entirely before installing the new applications.</span></span> <span data-ttu-id="e9bc3-113">Si tratta di una posizione non efficiente per l'azione perché tutti i file riutilizzati devono essere ricopiati.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-113">This is an inefficient placement for the action because all reused files have to be recopied.</span></span>
-   <span data-ttu-id="e9bc3-114">Dopo l' [azione InstallInitialize](installinitialize-action.md) e prima di qualsiasi azione che genera lo script di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-114">After the [InstallInitialize action](installinitialize-action.md) and before any actions that generate execution script.</span></span>
-   <span data-ttu-id="e9bc3-115">Tra l'azione [InstallExecute](installexecute-action.md)o l'azione [InstallExecuteAgain](installexecuteagain-action.md)e l'azione [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e9bc3-115">Between the [InstallExecute action](installexecute-action.md), or the [InstallExecuteAgain action](installexecuteagain-action.md), and the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="e9bc3-116">In genere le ultime tre azioni sono pianificate subito dopo un'altra: InstallExecute, RemoveExistingProducts e InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-116">Generally the last three actions are scheduled right after one another: InstallExecute, RemoveExistingProducts, and InstallFinalize.</span></span> <span data-ttu-id="e9bc3-117">In questo caso i file aggiornati vengono installati per primi e i file obsoleti vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-117">In this case the updated files are installed first and then the old files are removed.</span></span> <span data-ttu-id="e9bc3-118">Tuttavia, se la rimozione dell'applicazione precedente ha esito negativo, il programma di installazione esegue il rollback sia della rimozione dell'applicazione precedente sia dell'installazione della nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-118">However, if the removal of the old application fails, then the installer rolls back both the removal of the old application and the install of the new application.</span></span>
-   <span data-ttu-id="e9bc3-119">Dopo l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e9bc3-119">After the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="e9bc3-120">Si tratta del posizionamento più efficiente per l'azione.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-120">This is the most efficient placement for the action.</span></span> <span data-ttu-id="e9bc3-121">In questo caso, il programma di installazione aggiorna i file prima di rimuovere le applicazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-121">In this case, the installer updates files before removing the old applications.</span></span> <span data-ttu-id="e9bc3-122">Solo i file aggiornati vengono installati durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-122">Only the files being updated get installed during the installation.</span></span> <span data-ttu-id="e9bc3-123">Se la rimozione dell'applicazione precedente ha esito negativo, il programma di installazione esegue solo il rollback della disinstallazione dell'applicazione precedente.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-123">If the removal of the old application fails, then the installer only rolls back the uninstallation of the old application.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e9bc3-124">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="e9bc3-124">ActionData Messages</span></span>



| <span data-ttu-id="e9bc3-125">Campo</span><span class="sxs-lookup"><span data-stu-id="e9bc3-125">Field</span></span> | <span data-ttu-id="e9bc3-126">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="e9bc3-126">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="e9bc3-127">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e9bc3-127">\[1\]</span></span> | <span data-ttu-id="e9bc3-128">Prodotto rimosso.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-128">Removed product.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="e9bc3-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9bc3-129">Remarks</span></span>

<span data-ttu-id="e9bc3-130">Windows Installer imposta la proprietà [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) durante l'esecuzione di questa azione.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-130">Windows Installer sets the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) Property when it runs this action.</span></span>

 

 



