---
description: Se l'opzione di elaborazione msidbCustomActionTypeContinue return non è impostata, l'azione personalizzata deve restituire un codice di stato Integer, come illustrato nella tabella seguente.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valori restituiti dell'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319019"
---
# <a name="custom-action-return-values"></a><span data-ttu-id="96078-103">Valori restituiti dell'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="96078-103">Custom Action Return Values</span></span>

<span data-ttu-id="96078-104">Se l'opzione di elaborazione **msidbCustomActionTypeContinue** return non è impostata, l'azione personalizzata deve restituire un codice di stato Integer, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="96078-104">If the **msidbCustomActionTypeContinue** return processing option is not set, the custom action must return an integer status code as shown in the following table.</span></span>



| <span data-ttu-id="96078-105">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96078-105">Return value</span></span>                 | <span data-ttu-id="96078-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96078-106">Description</span></span>                           |
|------------------------------|---------------------------------------|
| <span data-ttu-id="96078-107">funzione di errore \_ \_ non \_ chiamata</span><span class="sxs-lookup"><span data-stu-id="96078-107">ERROR\_FUNCTION\_NOT\_CALLED</span></span> | <span data-ttu-id="96078-108">L'azione non è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="96078-108">Action not executed.</span></span>                  |
| <span data-ttu-id="96078-109">ERRORE \_ riuscito</span><span class="sxs-lookup"><span data-stu-id="96078-109">ERROR\_SUCCESS</span></span>               | <span data-ttu-id="96078-110">Azioni completate correttamente.</span><span class="sxs-lookup"><span data-stu-id="96078-110">Completed actions successfully.</span></span>       |
| <span data-ttu-id="96078-111">ERRORE di \_ installazione di \_ USEREXIT</span><span class="sxs-lookup"><span data-stu-id="96078-111">ERROR\_INSTALL\_USEREXIT</span></span>     | <span data-ttu-id="96078-112">L'utente è stato terminato in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="96078-112">User terminated prematurely.</span></span>          |
| <span data-ttu-id="96078-113">ERRORE di \_ installazione \_</span><span class="sxs-lookup"><span data-stu-id="96078-113">ERROR\_INSTALL\_FAILURE</span></span>      | <span data-ttu-id="96078-114">Si è verificato un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="96078-114">Unrecoverable error occurred.</span></span>         |
| <span data-ttu-id="96078-115">ERRORE \_ nessun \_ altro \_ elemento</span><span class="sxs-lookup"><span data-stu-id="96078-115">ERROR\_NO\_MORE\_ITEMS</span></span>       | <span data-ttu-id="96078-116">Ignorare le azioni rimanenti, non un errore.</span><span class="sxs-lookup"><span data-stu-id="96078-116">Skip remaining actions, not an error.</span></span> |



 

<span data-ttu-id="96078-117">Si noti che le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire un valore pari a 0 per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="96078-117">Note that custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="96078-118">Il programma di installazione interpreta qualsiasi altro valore restituito come errore.</span><span class="sxs-lookup"><span data-stu-id="96078-118">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="96078-119">Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="96078-119">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="96078-120">Per altre informazioni sull'opzione **msidbCustomActionTypeContinue** e su altre opzioni di elaborazione, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="96078-120">For more information about the **msidbCustomActionTypeContinue** option and other return processing options, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="96078-121">Si noti che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log.</span><span class="sxs-lookup"><span data-stu-id="96078-121">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="96078-122">Se, ad esempio, il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito l'errore \_ Success.</span><span class="sxs-lookup"><span data-stu-id="96078-122">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="96078-123">Per ulteriori informazioni su questa traduzione, vedere [registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="96078-123">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96078-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96078-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96078-125">Codici errore</span><span class="sxs-lookup"><span data-stu-id="96078-125">Error Codes</span></span>](error-codes.md)
</dt> <dt>

[<span data-ttu-id="96078-126">Registrazione dei valori restituiti dell'azione</span><span class="sxs-lookup"><span data-stu-id="96078-126">Logging of Action Return Values</span></span>](logging-of-action-return-values.md)
</dt> </dl>

 

 



