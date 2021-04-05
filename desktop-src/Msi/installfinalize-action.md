---
description: L'azione InstallFinalize esegue uno script che contiene tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'esecuzione delle azioni InstallExecute o InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Azione InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753519"
---
# <a name="installfinalize-action"></a><span data-ttu-id="c1f66-103">Azione InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="c1f66-103">InstallFinalize Action</span></span>

<span data-ttu-id="c1f66-104">L'azione InstallFinalize esegue uno script che contiene tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'esecuzione delle azioni [InstallExecute](installexecute-action.md) o [InstallExecuteAgain](installexecuteagain-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c1f66-104">The InstallFinalize action runs a script that contains all operations in the action sequence since either the start of the installation or the execution of the [InstallExecute](installexecute-action.md) or [InstallExecuteAgain](installexecuteagain-action.md) actions.</span></span> <span data-ttu-id="c1f66-105">Questa azione contrassegna la fine di una transazione che inizia con l'azione [InstallInitialize](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c1f66-105">This action marks the end of a transaction that begins with the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c1f66-106">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="c1f66-106">Sequence Restrictions</span></span>

<span data-ttu-id="c1f66-107">L'azione [InstallInitialize](installinitialize-action.md) deve precedere l'azione InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="c1f66-107">The [InstallInitialize](installinitialize-action.md) action must come before the InstallFinalize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c1f66-108">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="c1f66-108">ActionData Messages</span></span>

<span data-ttu-id="c1f66-109">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="c1f66-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1f66-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1f66-110">Remarks</span></span>

<span data-ttu-id="c1f66-111">Se viene rilevato che il prodotto è contrassegnato per la rimozione completa, le operazioni vengono aggiunte automaticamente allo script per rimuovere l' **Installazione applicazioni** nelle informazioni sul **Pannello di controllo** del prodotto, per annullare la registrazione e annullare la pubblicazione del prodotto e per rimuovere il database locale memorizzato nella cache da% Windows%, se esistente.</span><span class="sxs-lookup"><span data-stu-id="c1f66-111">If it is detected that the product is marked for complete removal, operations are automatically added to the script to remove the **Add/Remove Programs** in the **Control Panel** information for the product, to unregister and unpublish the product, and to remove the cached local database from %WINDOWS%, if it exists.</span></span>

<span data-ttu-id="c1f66-112">Le modifiche di sistema apportate prima dell'azione potrebbero non essere ripristinate dopo l'esecuzione dell'azione InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="c1f66-112">System changes made before the action may not be restored after the InstallFinalize action is executed.</span></span> <span data-ttu-id="c1f66-113">L'azione InstallFinalize aggiorna il sistema con tutte le operazioni determinate a tale punto e quindi termina la transazione.</span><span class="sxs-lookup"><span data-stu-id="c1f66-113">The InstallFinalize action updates the system with all operations determined to that point and then ends the transaction.</span></span>

 

 



