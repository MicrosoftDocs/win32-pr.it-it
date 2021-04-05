---
description: L'azione UnregisterProgIdInfo gestisce l'annullamento della registrazione delle informazioni del ProgId OLE con il sistema.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Azione UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885681"
---
# <a name="unregisterprogidinfo-action"></a><span data-ttu-id="bc55a-103">Azione UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-103">UnregisterProgIdInfo Action</span></span>

<span data-ttu-id="bc55a-104">L'azione UnregisterProgIdInfo gestisce l'annullamento della registrazione delle informazioni del ProgId OLE con il sistema.</span><span class="sxs-lookup"><span data-stu-id="bc55a-104">The UnregisterProgIdInfo action manages the unregistration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="bc55a-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="bc55a-105">Sequence Restrictions</span></span>

<span data-ttu-id="bc55a-106">L'azione UnregisterProgIdInfo deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) , [UnregisterClassInfo](unregisterclassinfo-action.md) Action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) Action e before the [RegisterProgIdInfo](registerprogidinfo-action.md) Action.</span><span class="sxs-lookup"><span data-stu-id="bc55a-106">The UnregisterProgIdInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action, and before the [RegisterProgIdInfo](registerprogidinfo-action.md) action.</span></span>

<span data-ttu-id="bc55a-107">[RemoveRegistryValues](removeregistryvalues-action.md) deve precedere UnregisterProgIdInfo nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="bc55a-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterProgIdInfo in the sequence.</span></span>

<span data-ttu-id="bc55a-108">La sequenziazione delle azioni nel gruppo seguente è limitata.</span><span class="sxs-lookup"><span data-stu-id="bc55a-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="bc55a-109">Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="bc55a-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="bc55a-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="bc55a-111">UnregisterExtensioninfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-111">UnregisterExtensioninfo</span></span>](unregisterextensioninfo-action.md)
-   <span data-ttu-id="bc55a-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-112">UnregisterProgIdInfo</span></span>
-   [<span data-ttu-id="bc55a-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="bc55a-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="bc55a-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="bc55a-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="bc55a-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="bc55a-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="bc55a-118">Ad esempio, UnregisterProgIdInfo deve precedere [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="bc55a-118">For example, UnregisterProgIdInfo must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="bc55a-119">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="bc55a-119">ActionData Messages</span></span>



| <span data-ttu-id="bc55a-120">Campo</span><span class="sxs-lookup"><span data-stu-id="bc55a-120">Field</span></span> | <span data-ttu-id="bc55a-121">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="bc55a-121">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="bc55a-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="bc55a-122">\[1\]</span></span> | <span data-ttu-id="bc55a-123">Identificatore del programma registrato.</span><span class="sxs-lookup"><span data-stu-id="bc55a-123">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bc55a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc55a-124">Remarks</span></span>

<span data-ttu-id="bc55a-125">L'azione UnregisterProgIdInfo rimuove le informazioni sul ProgId dal registro di sistema ([tabella ProgId](progid-table.md)) per le funzionalità connesse alle informazioni sull'estensione ([tabella di estensione](extension-table.md)) o alle informazioni sulla classe ([tabella delle classi](class-table.md)) e attualmente selezionate per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="bc55a-125">The UnregisterProgIdInfo action removes ProgId information from the registry ([ProgId Table](progid-table.md)) for features that are connected to the extension information ([Extension table](extension-table.md)) or the Class information ([Class table](class-table.md)) and are currently selected to be uninstalled.</span></span>

 

 



