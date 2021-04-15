---
description: L'azione ExecuteAction avvia la sequenza di esecuzione usando la proprietà EXECUTEACTION per determinare il tipo di installazione da eseguire.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Azione ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485388"
---
# <a name="executeaction-action"></a><span data-ttu-id="c4227-103">Azione ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="c4227-103">ExecuteAction Action</span></span>

<span data-ttu-id="c4227-104">L'azione ExecuteAction avvia la sequenza di esecuzione usando la proprietà [**ExecuteAction**](executeaction.md) per determinare il tipo di installazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c4227-104">The ExecuteAction action initiates the execution sequence using the [**EXECUTEACTION**](executeaction.md) property to determine which type of installation to perform.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c4227-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="c4227-105">Sequence Restrictions</span></span>

<span data-ttu-id="c4227-106">Questa azione deve essere sequenziata dopo il completamento di tutte le raccolte di informazioni necessarie per iniziare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c4227-106">This action should be sequenced after all information collection necessary to begin the installation is complete.</span></span> <span data-ttu-id="c4227-107">Le azioni aggiuntive possono essere sequenziate dopo l'azione ExecuteAction nella [tabella InstallUISequence](installuisequence-table.md)e la [tabella AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4227-107">Additional actions may be sequenced after ExecuteAction action in the [InstallUISequence table](installuisequence-table.md), and [AdminUISequence table](adminuisequence-table.md).</span></span> <span data-ttu-id="c4227-108">Una sequenza inizierà in genere con le azioni di [*determinazione del costo*](c-gly.md) , ad esempio l' [azione CostInitialize](costinitialize-action.md), seguita dalle azioni dell'interfaccia utente e quindi dall'azione ExecuteAction.</span><span class="sxs-lookup"><span data-stu-id="c4227-108">A sequence will typically begin with [*costing*](c-gly.md) actions, such as the [CostInitialize action](costinitialize-action.md), followed by the user interface actions, and then the ExecuteAction action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c4227-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="c4227-109">ActionData Messages</span></span>

<span data-ttu-id="c4227-110">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="c4227-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4227-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4227-111">Remarks</span></span>

<span data-ttu-id="c4227-112">L'azione ExecuteAction viene eseguita con i privilegi di sistema se il servizio del programma di installazione è abilitato.</span><span class="sxs-lookup"><span data-stu-id="c4227-112">The ExecuteAction action is run with system privileges if the installer service is enabled.</span></span> <span data-ttu-id="c4227-113">Le azioni di primo livello, ad esempio l'azione di [installazione](install-action.md), l'azione di [annuncio](advertise-action.md)e l' [azione amministrativa](admin-action.md) includono la logica interna che determina se la chiamata dell'azione ExecuteAction richiede la sequenza di esecuzione o la sequenza dell'interfaccia utente da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c4227-113">The top-level actions, such as the [INSTALL action](install-action.md), [ADVERTISE action](advertise-action.md), and [ADMIN action](admin-action.md) include internal logic that determines whether calling the ExecuteAction action requires either the execution sequence or the user interface sequence to run.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4227-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4227-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4227-115">Tabella InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="c4227-115">InstallUISequence table</span></span>](installuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="c4227-116">Tabella AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="c4227-116">AdminUISequence table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="c4227-117">Azione CostInitialize</span><span class="sxs-lookup"><span data-stu-id="c4227-117">CostInitialize action</span></span>](costinitialize-action.md)
</dt> </dl>

 

 



