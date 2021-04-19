---
description: L'azione UnregisterExtensionInfo gestisce la rimozione delle informazioni relative all'estensione dal registro di sistema.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Azione UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319419"
---
# <a name="unregisterextensioninfo-action"></a><span data-ttu-id="dbaf5-103">Azione UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-103">UnregisterExtensionInfo Action</span></span>

<span data-ttu-id="dbaf5-104">L'azione UnregisterExtensionInfo gestisce la rimozione delle informazioni relative all'estensione dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dbaf5-104">The UnregisterExtensionInfo action manages the removal of extension-related information from the system registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="dbaf5-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="dbaf5-105">Sequence Restrictions</span></span>

<span data-ttu-id="dbaf5-106">L'azione UnregisterExtensionInfo deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) e prima dell'azione [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="dbaf5-106">The UnregisterExtensionInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="dbaf5-107">[RemoveRegistryValues](removeregistryvalues-action.md) deve precedere UnregisterExtensionInfo nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="dbaf5-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterExtensionInfo in the sequence.</span></span>

<span data-ttu-id="dbaf5-108">La sequenziazione delle azioni nel gruppo seguente è limitata.</span><span class="sxs-lookup"><span data-stu-id="dbaf5-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="dbaf5-109">Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="dbaf5-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="dbaf5-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   <span data-ttu-id="dbaf5-111">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-111">UnregisterExtensionInfo</span></span>
-   [<span data-ttu-id="dbaf5-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-112">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="dbaf5-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="dbaf5-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="dbaf5-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="dbaf5-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="dbaf5-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="dbaf5-118">Ad esempio, UnregisterExtensionInfo deve precedere [UnregisterProgIdInfo](unregisterprogidinfo-action.md) nella tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="dbaf5-118">For example, UnregisterExtensionInfo must come before [UnregisterProgIdInfo](unregisterprogidinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="dbaf5-119">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="dbaf5-119">ActionData Messages</span></span>



| <span data-ttu-id="dbaf5-120">Campo</span><span class="sxs-lookup"><span data-stu-id="dbaf5-120">Field</span></span> | <span data-ttu-id="dbaf5-121">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="dbaf5-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="dbaf5-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="dbaf5-122">\[1\]</span></span> | <span data-ttu-id="dbaf5-123">Estensione rimossa.</span><span class="sxs-lookup"><span data-stu-id="dbaf5-123">Removed extension.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="dbaf5-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbaf5-124">Remarks</span></span>

<span data-ttu-id="dbaf5-125">Se il sistema non supporta l'installazione su richiesta dei server di estensione, UnregisterExtensionInfo rimuove tutti i server di estensione nella [tabella di estensione](extension-table.md) associata a una funzionalità disinstallata o a una funzionalità installata come annunciato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dbaf5-125">If the system does not support the install-on-demand of extension servers, UnregisterExtensionInfo removes all extension servers in the [Extension table](extension-table.md) associated with either an uninstalled feature or a feature installed as advertised from the registry.</span></span> <span data-ttu-id="dbaf5-126">In caso contrario, questa azione rimuoverà i server di estensione associati a una funzionalità selezionata per la rimozione dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dbaf5-126">Otherwise, this action removes the extension servers associated with a feature that is selected to be removed from the registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbaf5-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dbaf5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbaf5-128">**Proprietà ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="dbaf5-128">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



