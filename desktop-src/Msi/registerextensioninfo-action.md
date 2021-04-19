---
description: L'azione RegisterExtensionInfo gestisce la registrazione delle informazioni relative all'estensione con il sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Azione RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311710"
---
# <a name="registerextensioninfo-action"></a><span data-ttu-id="52c77-103">Azione RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-103">RegisterExtensionInfo Action</span></span>

<span data-ttu-id="52c77-104">L'azione RegisterExtensionInfo gestisce la registrazione delle informazioni relative all'estensione con il sistema.</span><span class="sxs-lookup"><span data-stu-id="52c77-104">The RegisterExtensionInfo action manages the registration of extension related information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="52c77-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="52c77-105">Sequence Restrictions</span></span>

<span data-ttu-id="52c77-106">L'azione RegisterExtensionInfo deve essere successiva all'azione [InstallFiles](installfiles-action.md) e [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="52c77-106">The RegisterExtensionInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action.</span></span>

<span data-ttu-id="52c77-107">La sequenziazione delle azioni nel gruppo seguente è limitata.</span><span class="sxs-lookup"><span data-stu-id="52c77-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="52c77-108">Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="52c77-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="52c77-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="52c77-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="52c77-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="52c77-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="52c77-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   <span data-ttu-id="52c77-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-114">RegisterExtensionInfo</span></span>
-   [<span data-ttu-id="52c77-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="52c77-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="52c77-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="52c77-117">Ad esempio, RegisterExtensionInfo deve essere seguito da [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="52c77-117">For example, RegisterExtensionInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="52c77-118">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="52c77-118">ActionData Messages</span></span>



| <span data-ttu-id="52c77-119">Campo</span><span class="sxs-lookup"><span data-stu-id="52c77-119">Field</span></span> | <span data-ttu-id="52c77-120">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="52c77-120">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="52c77-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="52c77-121">\[1\]</span></span> | <span data-ttu-id="52c77-122">Estensione registrata.</span><span class="sxs-lookup"><span data-stu-id="52c77-122">Registered extension.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="52c77-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="52c77-123">Remarks</span></span>

<span data-ttu-id="52c77-124">Se il sistema supporta l'installazione su richiesta per i server di estensione, RegisterExtensionInfo registra tutti i server di estensione nella [tabella di estensione](extension-table.md) associata alle funzionalità impostate per l'installazione o l'annuncio.</span><span class="sxs-lookup"><span data-stu-id="52c77-124">If the system supports installation-on-demand for extension servers, RegisterExtensionInfo registers all extension servers in the [Extension table](extension-table.md) associated with features set for installation or advertisement.</span></span> <span data-ttu-id="52c77-125">In caso contrario, questa azione registra solo i server di estensione associati alle funzionalità impostate sull'installazione.</span><span class="sxs-lookup"><span data-stu-id="52c77-125">Otherwise this action only registers extension servers associated with features set to installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52c77-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52c77-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52c77-127">**Proprietà ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="52c77-127">**ShellAdvtSupport property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



