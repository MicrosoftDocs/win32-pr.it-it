---
description: L'azione RegisterMIMEInfo registra le informazioni del registro di sistema correlate a MIME con il sistema.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Azione RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756467"
---
# <a name="registermimeinfo-action"></a><span data-ttu-id="52fd7-103">Azione RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-103">RegisterMIMEInfo Action</span></span>

<span data-ttu-id="52fd7-104">L'azione RegisterMIMEInfo registra le informazioni del registro di sistema correlate a MIME con il sistema.</span><span class="sxs-lookup"><span data-stu-id="52fd7-104">The RegisterMIMEInfo action registers MIME-related registry information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="52fd7-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="52fd7-105">Sequence Restrictions</span></span>

<span data-ttu-id="52fd7-106">L'azione RegisterMIMEInfo deve provenire dopo l'azione [InstallFiles](installfiles-action.md) , l'azione [UnregisterMIMEInfo](unregistermimeinfo-action.md) , l'azione [registerClassInfo](registerclassinfo-action.md) e l'azione [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="52fd7-106">The RegisterMIMEInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterMIMEInfo](unregistermimeinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="52fd7-107">La sequenziazione delle azioni nel gruppo seguente è limitata.</span><span class="sxs-lookup"><span data-stu-id="52fd7-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="52fd7-108">Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="52fd7-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="52fd7-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="52fd7-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="52fd7-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="52fd7-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="52fd7-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="52fd7-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="52fd7-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   <span data-ttu-id="52fd7-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="52fd7-116">RegisterMIMEInfo</span></span>

<span data-ttu-id="52fd7-117">Ad esempio, RegisterMIMEInfo deve essere seguito da [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="52fd7-117">For example, RegisterMIMEInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="52fd7-118">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="52fd7-118">ActionData Messages</span></span>



| <span data-ttu-id="52fd7-119">Campo</span><span class="sxs-lookup"><span data-stu-id="52fd7-119">Field</span></span> | <span data-ttu-id="52fd7-120">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="52fd7-120">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="52fd7-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="52fd7-121">\[1\]</span></span> | <span data-ttu-id="52fd7-122">Identificatore del tipo di contenuto MIME registrato.</span><span class="sxs-lookup"><span data-stu-id="52fd7-122">Identifier of registered MIME content type.</span></span>  |
| <span data-ttu-id="52fd7-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="52fd7-123">\[2\]</span></span> | <span data-ttu-id="52fd7-124">Estensione associata al tipo di contenuto MIME.</span><span class="sxs-lookup"><span data-stu-id="52fd7-124">Extension associated with MIME content type.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="52fd7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="52fd7-125">Remarks</span></span>

<span data-ttu-id="52fd7-126">L'azione RegisterMIMEInfo registra tutte le informazioni MIME per i server dalla [tabella MIME](mime-table.md) per cui è stato selezionato il server di classe o il server di estensione corrispondente da installare.</span><span class="sxs-lookup"><span data-stu-id="52fd7-126">The RegisterMIMEInfo action registers all MIME information for servers from the [MIME table](mime-table.md) for which the corresponding class server or extension server has been selected to be installed.</span></span>

 

 



