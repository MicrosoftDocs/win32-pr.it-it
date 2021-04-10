---
description: L'azione InstallExecuteAgain esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallExecuteAgain o dall'ultima azione InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Azione InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966604"
---
# <a name="installexecuteagain-action"></a><span data-ttu-id="f4478-103">Azione InstallExecuteAgain</span><span class="sxs-lookup"><span data-stu-id="f4478-103">InstallExecuteAgain Action</span></span>

<span data-ttu-id="f4478-104">L'azione InstallExecuteAgain esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallExecuteAgain o dall'ultima [azione InstallExecute](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="f4478-104">The InstallExecuteAgain action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecuteAgain action or the last [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="f4478-105">L'azione InstallExecute aggiorna il sistema senza terminare la transazione.</span><span class="sxs-lookup"><span data-stu-id="f4478-105">The InstallExecute action updates the system without ending the transaction.</span></span> <span data-ttu-id="f4478-106">InstallExecuteAgain esegue la stessa operazione dell' [azione InstallExecute](installexecute-action.md) , ma deve essere utilizzata solo dopo InstallExecute.</span><span class="sxs-lookup"><span data-stu-id="f4478-106">InstallExecuteAgain performs the same operation as the [InstallExecute action](installexecute-action.md) but should only be used after InstallExecute.</span></span>

<span data-ttu-id="f4478-107">InstallExecuteAgain deve sempre essere impostato in modo che non venga eseguito durante la rimozione.</span><span class="sxs-lookup"><span data-stu-id="f4478-107">InstallExecuteAgain should always be set so that it does not run during removal.</span></span> <span data-ttu-id="f4478-108">Per informazioni, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="f4478-108">For information, see [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f4478-109">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="f4478-109">Sequence Restrictions</span></span>

<span data-ttu-id="f4478-110">L'azione InstallExecute viene eseguita tra l' [azione InstallInitialize](installinitialize-action.md) e l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f4478-110">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f4478-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="f4478-111">ActionData Messages</span></span>

<span data-ttu-id="f4478-112">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="f4478-112">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4478-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4478-113">Remarks</span></span>

<span data-ttu-id="f4478-114">L'azione InstallExecuteAgain esegue la stessa operazione dell' [azione InstallExecute](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="f4478-114">The InstallExecuteAgain action does the same thing as the [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="f4478-115">Poiché le tabelle di sequenza includono solo una chiave primaria, la colonna azione non può essere ripetuta in una determinata tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="f4478-115">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="f4478-116">Esistono due azioni che eseguono la stessa operazione, InstallExecute e InstallExecuteAgain, per i casi in cui la funzionalità di InstallExecute è necessaria due volte nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4478-116">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="f4478-117">Per ulteriori informazioni, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4478-117">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



