---
description: L'azione LaunchConditions esegue una query sulla tabella LaunchCondition e valuta le singole istruzioni condizionali registrate. Se una di queste istruzioni condizionali ha esito negativo, viene visualizzato un messaggio di errore all'utente e l'installazione viene terminata.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Azione LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307254"
---
# <a name="launchconditions-action"></a><span data-ttu-id="0cff1-104">Azione LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="0cff1-104">LaunchConditions Action</span></span>

<span data-ttu-id="0cff1-105">L'azione LaunchConditions esegue una query sulla [tabella LaunchCondition](launchcondition-table.md) e valuta le singole istruzioni condizionali registrate.</span><span class="sxs-lookup"><span data-stu-id="0cff1-105">The LaunchConditions action queries the [LaunchCondition table](launchcondition-table.md) and evaluates each conditional statement recorded there.</span></span> <span data-ttu-id="0cff1-106">Se una di queste istruzioni condizionali ha esito negativo, viene visualizzato un messaggio di errore all'utente e l'installazione viene terminata.</span><span class="sxs-lookup"><span data-stu-id="0cff1-106">If any of these conditional statements fail, an error message is displayed to the user and the installation is terminated.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0cff1-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="0cff1-107">Sequence Restrictions</span></span>

<span data-ttu-id="0cff1-108">L'azione LaunchConditions è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="0cff1-108">The LaunchConditions action is optional.</span></span> <span data-ttu-id="0cff1-109">Questa azione è in genere la prima nella sequenza, ma l' [azione AppSearch](appsearch-action.md) può essere sequenziata prima dell'azione LaunchConditions.</span><span class="sxs-lookup"><span data-stu-id="0cff1-109">This action is normally the first in the sequence, but the [AppSearch Action](appsearch-action.md) may be sequenced before the LaunchConditions action.</span></span> <span data-ttu-id="0cff1-110">Se sono presenti condizioni di avvio che non si applicano a tutte le modalità di installazione, è necessario utilizzare la proprietà modalità di installazione appropriata in un'espressione condizionale nella tabella di sequenza appropriata.</span><span class="sxs-lookup"><span data-stu-id="0cff1-110">If there are launch conditions that do not apply to all installation modes, the appropriate installation mode property should be used in a conditional expression in the appropriate sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0cff1-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="0cff1-111">ActionData Messages</span></span>

<span data-ttu-id="0cff1-112">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="0cff1-112">There are no ActionData messages.</span></span>

 

 



