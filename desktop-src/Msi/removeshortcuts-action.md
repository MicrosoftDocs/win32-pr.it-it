---
description: L'azione RemoveShortcuts gestisce la rimozione di un collegamento annunciato la cui funzionalità è selezionata per la disinstallazione o un collegamento non annunciato il cui componente è selezionato per la disinstallazione. Per ulteriori informazioni, vedere la tabella dei collegamenti.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Azione RemoveShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313802"
---
# <a name="removeshortcuts-action"></a><span data-ttu-id="090c6-104">Azione RemoveShortcuts</span><span class="sxs-lookup"><span data-stu-id="090c6-104">RemoveShortcuts Action</span></span>

<span data-ttu-id="090c6-105">L'azione RemoveShortcuts gestisce la rimozione di un collegamento annunciato la cui funzionalità è selezionata per la disinstallazione o un collegamento non annunciato il cui componente è selezionato per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="090c6-105">The RemoveShortcuts action manages the removal of an advertised shortcut whose feature is selected for uninstallation or a nonadvertised shortcut whose component is selected for uninstallation.</span></span> <span data-ttu-id="090c6-106">Per ulteriori informazioni, vedere la [tabella dei collegamenti](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="090c6-106">For more information, see the [Shortcut Table](shortcut-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="090c6-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="090c6-107">Sequence Restrictions</span></span>

<span data-ttu-id="090c6-108">L'azione RemoveShortcuts deve precedere l'azione [CreateShortcuts](createshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="090c6-108">The RemoveShortcuts action must come before the [CreateShortcuts](createshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="090c6-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="090c6-109">ActionData Messages</span></span>



| <span data-ttu-id="090c6-110">Campo</span><span class="sxs-lookup"><span data-stu-id="090c6-110">Field</span></span> | <span data-ttu-id="090c6-111">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="090c6-111">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="090c6-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="090c6-112">\[1\]</span></span> | <span data-ttu-id="090c6-113">Identificatore del collegamento rimosso.</span><span class="sxs-lookup"><span data-stu-id="090c6-113">Identifier of removed shortcut.</span></span> |



 

 

 



