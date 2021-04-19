---
description: L'azione RegisterClassInfo gestisce la registrazione delle informazioni della classe COM con il sistema. Usa la tabella AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Azione RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311712"
---
# <a name="registerclassinfo-action"></a><span data-ttu-id="ceaa5-104">Azione RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-104">RegisterClassInfo Action</span></span>

<span data-ttu-id="ceaa5-105">L'azione RegisterClassInfo gestisce la registrazione delle informazioni della classe COM con il sistema.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-105">The RegisterClassInfo action manages the registration of COM class information with the system.</span></span> <span data-ttu-id="ceaa5-106">Usa la [tabella AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="ceaa5-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ceaa5-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="ceaa5-107">Sequence Restrictions</span></span>

<span data-ttu-id="ceaa5-108">L'azione RegisterClassInfo deve essere successiva all'azione [InstallFiles](installfiles-action.md) e [UnregisterClassInfo](unregisterclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ceaa5-108">The RegisterClassInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterClassInfo](unregisterclassinfo-action.md) action.</span></span>

<span data-ttu-id="ceaa5-109">La sequenziazione delle azioni nel gruppo seguente è limitata.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-109">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="ceaa5-110">Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="ceaa5-110">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="ceaa5-111">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-111">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="ceaa5-112">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-112">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="ceaa5-113">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-113">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="ceaa5-114">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-114">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   <span data-ttu-id="ceaa5-115">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-115">RegisterClassInfo</span></span>
-   [<span data-ttu-id="ceaa5-116">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-116">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="ceaa5-117">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-117">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="ceaa5-118">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-118">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="ceaa5-119">Ad esempio, RegisterClassInfo deve essere seguito da [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-119">For example, RegisterClassInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ceaa5-120">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="ceaa5-120">ActionData Messages</span></span>



| <span data-ttu-id="ceaa5-121">Campo</span><span class="sxs-lookup"><span data-stu-id="ceaa5-121">Field</span></span> | <span data-ttu-id="ceaa5-122">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="ceaa5-122">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="ceaa5-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ceaa5-123">\[1\]</span></span> | <span data-ttu-id="ceaa5-124">Identificatore di classe GUID del server COM registrato.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-124">GUID class identifier of the registered COM server.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ceaa5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ceaa5-125">Remarks</span></span>

<span data-ttu-id="ceaa5-126">Se il sistema supporta l'installazione su richiesta per i server OLE, RegisterClassInfo registra tutte le classi COM nella [tabella della classe](class-table.md) associata a una funzionalità selezionata per l'installazione o l'annuncio.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-126">If the system supports install-on-demand for OLE servers, RegisterClassInfo registers all COM classes in the [Class table](class-table.md) associated with a feature selected to be installed or advertised.</span></span> <span data-ttu-id="ceaa5-127">In caso contrario, questa azione registra solo le classi COM associate a una funzionalità selezionata per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-127">Otherwise this action only registers the COM classes associated with a feature selected for installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ceaa5-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ceaa5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceaa5-129">**Proprietà OLEAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="ceaa5-129">**OLEAdvtSupport property**</span></span>](oleadvtsupport.md)
</dt> </dl>

 

 



