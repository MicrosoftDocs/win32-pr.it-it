---
description: L'azione InstallExecute esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallExecute o InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Azione InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128379"
---
# <a name="installexecute-action"></a><span data-ttu-id="b9a0f-103">Azione InstallExecute</span><span class="sxs-lookup"><span data-stu-id="b9a0f-103">InstallExecute Action</span></span>

<span data-ttu-id="b9a0f-104">L'azione InstallExecute esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallExecute o [InstallExecuteAgain](installexecuteagain-action.md).</span><span class="sxs-lookup"><span data-stu-id="b9a0f-104">The InstallExecute action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecute action or [InstallExecuteAgain action](installexecuteagain-action.md).</span></span> <span data-ttu-id="b9a0f-105">L'azione InstallExecute aggiorna il sistema senza terminare la transazione.</span><span class="sxs-lookup"><span data-stu-id="b9a0f-105">The InstallExecute action updates the system without ending the transaction.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b9a0f-106">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="b9a0f-106">Sequence Restrictions</span></span>

<span data-ttu-id="b9a0f-107">L'azione InstallExecute viene eseguita tra l' [azione InstallInitialize](installinitialize-action.md) e l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="b9a0f-107">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b9a0f-108">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="b9a0f-108">ActionData Messages</span></span>

<span data-ttu-id="b9a0f-109">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="b9a0f-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a0f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9a0f-110">Remarks</span></span>

<span data-ttu-id="b9a0f-111">L' [azione InstallExecuteAgain](installexecuteagain-action.md) esegue la stessa operazione dell'azione InstallExecute.</span><span class="sxs-lookup"><span data-stu-id="b9a0f-111">The [InstallExecuteAgain action](installexecuteagain-action.md) does the same thing as the InstallExecute action.</span></span> <span data-ttu-id="b9a0f-112">Poiché le tabelle di sequenza includono solo una chiave primaria, la colonna azione non può essere ripetuta in una determinata tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="b9a0f-112">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="b9a0f-113">Esistono due azioni che eseguono la stessa operazione, InstallExecute e InstallExecuteAgain, per i casi in cui la funzionalità di InstallExecute è necessaria due volte nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b9a0f-113">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="b9a0f-114">Per ulteriori informazioni, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b9a0f-114">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



