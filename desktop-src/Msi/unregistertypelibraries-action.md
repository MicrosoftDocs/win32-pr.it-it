---
description: L'azione UnregisterTypeLibraries Annulla la registrazione delle librerie dei tipi dal sistema. Questa azione viene applicata a ogni file elencato nella tabella TypeLib attivata per la disinstallazione.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Azione UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319417"
---
# <a name="unregistertypelibraries-action"></a><span data-ttu-id="8f575-104">Azione UnregisterTypeLibraries</span><span class="sxs-lookup"><span data-stu-id="8f575-104">UnregisterTypeLibraries Action</span></span>

<span data-ttu-id="8f575-105">L'azione UnregisterTypeLibraries Annulla la registrazione delle librerie dei tipi dal sistema.</span><span class="sxs-lookup"><span data-stu-id="8f575-105">The UnregisterTypeLibraries action unregisters type libraries from the system.</span></span> <span data-ttu-id="8f575-106">Questa azione viene applicata a ogni file elencato nella tabella [typelib](typelib-table.md) attivata per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="8f575-106">This action is applied to each file listed in the [TypeLib](typelib-table.md) table that is triggered to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8f575-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="8f575-107">Sequence Restrictions</span></span>

<span data-ttu-id="8f575-108">L'azione UnregisterTypeLibraries deve precedere l'azione [RemoveFiles](removefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8f575-108">The UnregisterTypeLibraries action must come before the [RemoveFiles](removefiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8f575-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="8f575-109">ActionData Messages</span></span>



| <span data-ttu-id="8f575-110">Campo</span><span class="sxs-lookup"><span data-stu-id="8f575-110">Field</span></span> | <span data-ttu-id="8f575-111">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="8f575-111">Description of action data</span></span>                        |
|-------|---------------------------------------------------|
| <span data-ttu-id="8f575-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8f575-112">\[1\]</span></span> | <span data-ttu-id="8f575-113">[GUID](guid.md) di una libreria dei tipi non registrata.</span><span class="sxs-lookup"><span data-stu-id="8f575-113">[GUID](guid.md) of an unregistered type library.</span></span> |



 

 

 



