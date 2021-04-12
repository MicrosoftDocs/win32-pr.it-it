---
description: L'azione UnregisterMIMEInfo Annulla la registrazione delle informazioni del registro di sistema correlate a MIME dal sistema. L'azione annulla la registrazione delle informazioni MIME per i server dalla tabella MIME per cui è attualmente selezionata la funzionalità corrispondente per la disinstallazione.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Azione UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234177"
---
# <a name="unregistermimeinfo-action"></a><span data-ttu-id="b461b-104">Azione UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-104">UnregisterMIMEInfo Action</span></span>

<span data-ttu-id="b461b-105">L'azione UnregisterMIMEInfo Annulla la registrazione delle informazioni del registro di sistema correlate a MIME dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b461b-105">The UnregisterMIMEInfo action unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="b461b-106">L'azione annulla la registrazione delle informazioni MIME per i server dalla [tabella MIME](mime-table.md) per cui è attualmente selezionata la funzionalità corrispondente per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="b461b-106">The action unregisters MIME information for servers from the [MIME table](mime-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b461b-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="b461b-107">Sequence Restrictions</span></span>

<span data-ttu-id="b461b-108">L'azione UnregisterMIMEInfo deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) , [UnregisterClassInfo](unregisterclassinfo-action.md) Action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) Action e before the [RegisterMIMEInfo](registermimeinfo-action.md) Action.</span><span class="sxs-lookup"><span data-stu-id="b461b-108">The UnregisterMIMEInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action, and before the [RegisterMIMEInfo](registermimeinfo-action.md) action.</span></span>

<span data-ttu-id="b461b-109">[RemoveRegistryValues](removeregistryvalues-action.md) deve precedere UnregisterMIMEInfo nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="b461b-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterMIMEInfo in the sequence.</span></span>

<span data-ttu-id="b461b-110">La sequenziazione delle azioni nel gruppo seguente è limitata.</span><span class="sxs-lookup"><span data-stu-id="b461b-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="b461b-111">Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="b461b-111">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="b461b-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-112">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="b461b-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="b461b-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   <span data-ttu-id="b461b-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-115">UnregisterMIMEInfo</span></span>
-   [<span data-ttu-id="b461b-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="b461b-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="b461b-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="b461b-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b461b-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="b461b-120">Ad esempio, UnregisterMIMEInfo deve precedere [RegisterExtensionInfo](registerextensioninfo-action.md) nella tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="b461b-120">For example, UnregisterMIMEInfo must come before [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b461b-121">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="b461b-121">ActionData Messages</span></span>



| <span data-ttu-id="b461b-122">Campo</span><span class="sxs-lookup"><span data-stu-id="b461b-122">Field</span></span> | <span data-ttu-id="b461b-123">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="b461b-123">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="b461b-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b461b-124">\[1\]</span></span> | <span data-ttu-id="b461b-125">Identificatore del tipo di contenuto MIME non registrato.</span><span class="sxs-lookup"><span data-stu-id="b461b-125">Identifier of unregistered MIME content type.</span></span> |
| <span data-ttu-id="b461b-126">\[2\]</span><span class="sxs-lookup"><span data-stu-id="b461b-126">\[2\]</span></span> | <span data-ttu-id="b461b-127">Estensione associata al tipo di contenuto MIME.</span><span class="sxs-lookup"><span data-stu-id="b461b-127">Extension associated with MIME content type.</span></span>  |



 

 

 



