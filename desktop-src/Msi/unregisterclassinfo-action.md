---
description: L'azione UnregisterClassInfo gestisce la rimozione delle informazioni della classe COM dal registro di sistema. Usa la tabella AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Azione UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319423"
---
# <a name="unregisterclassinfo-action"></a><span data-ttu-id="d25ce-104">Azione UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-104">UnregisterClassInfo Action</span></span>

<span data-ttu-id="d25ce-105">L'azione UnregisterClassInfo gestisce la rimozione delle informazioni della classe COM dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d25ce-105">The UnregisterClassInfo action manages the removal of COM class information from the system registry.</span></span> <span data-ttu-id="d25ce-106">Usa la [tabella AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="d25ce-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d25ce-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="d25ce-107">Sequence Restrictions</span></span>

<span data-ttu-id="d25ce-108">L'azione UnregisterClassInfo deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) e prima dell'azione [registerClassInfo](registerclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d25ce-108">The UnregisterClassInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterClassInfo](registerclassinfo-action.md) action.</span></span>

<span data-ttu-id="d25ce-109">[RemoveRegistryValues](removeregistryvalues-action.md) deve precedere UnregisterClassInfo nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="d25ce-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterClassInfo in the sequence.</span></span>

<span data-ttu-id="d25ce-110">La sequenziazione delle azioni nel gruppo seguente è limitata.</span><span class="sxs-lookup"><span data-stu-id="d25ce-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="d25ce-111">Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che si trovino nella stessa sequenza relativa, come illustrato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="d25ce-111">If any subset of these actions occur together in a sequence table, they must occur in the same relative sequence as shown in the following table:</span></span>

-   <span data-ttu-id="d25ce-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-112">UnregisterClassInfo</span></span>
-   [<span data-ttu-id="d25ce-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="d25ce-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="d25ce-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-115">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="d25ce-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="d25ce-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="d25ce-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="d25ce-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="d25ce-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="d25ce-120">Ad esempio, [RegisterExtensionInfo](registerextensioninfo-action.md) deve precedere UnregisterClassInfo nella tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="d25ce-120">For example, [RegisterExtensionInfo](registerextensioninfo-action.md) must come before UnregisterClassInfo in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d25ce-121">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="d25ce-121">ActionData Messages</span></span>



| <span data-ttu-id="d25ce-122">Campo</span><span class="sxs-lookup"><span data-stu-id="d25ce-122">Field</span></span> | <span data-ttu-id="d25ce-123">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="d25ce-123">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="d25ce-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d25ce-124">\[1\]</span></span> | <span data-ttu-id="d25ce-125">GUID della classe COM non registrata.</span><span class="sxs-lookup"><span data-stu-id="d25ce-125">GUID of unregistered COM class.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d25ce-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d25ce-126">Remarks</span></span>

<span data-ttu-id="d25ce-127">Il programma di installazione imposta la proprietà [**OLEAdvtSupport**](oleadvtsupport.md) su true quando il sistema dell'utente corrente è stato aggiornato per funzionare con l'installazione su richiesta tramite com.</span><span class="sxs-lookup"><span data-stu-id="d25ce-127">The installer sets the [**OLEAdvtSupport**](oleadvtsupport.md) property to true when the current user's system has been upgraded to work with install-on-demand through COM.</span></span> <span data-ttu-id="d25ce-128">Se il sistema non supporta l'installazione su richiesta tramite COM, UnregisterClassInfo rimuove tutte le classi COM elencate nella tabella della [classe](class-table.md) associata alle funzionalità o funzionalità disinstallate installate come pubblicizzate dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d25ce-128">If the system does not support install-on-demand through COM, UnregisterClassInfo removes all COM classes listed in the [Class table](class-table.md) associated with either uninstalled features or features installed as advertised from the system registry.</span></span> <span data-ttu-id="d25ce-129">In caso contrario, questa azione rimuove solo le classi COM associate alle funzionalità selezionate per la disinstallazione dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d25ce-129">Otherwise, this action removes only the COM classes associated with features selected to be uninstalled from the system registry.</span></span>

 

 



