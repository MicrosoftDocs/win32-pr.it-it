---
description: L'azione RegisterProgIdInfo gestisce la registrazione delle informazioni OLE ProgId con il sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Azione RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311707"
---
# <a name="registerprogidinfo-action"></a><span data-ttu-id="26701-103">Azione RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="26701-103">RegisterProgIdInfo Action</span></span>

<span data-ttu-id="26701-104">L'azione RegisterProgIdInfo gestisce la registrazione delle informazioni OLE ProgId con il sistema.</span><span class="sxs-lookup"><span data-stu-id="26701-104">The RegisterProgIdInfo action manages the registration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="26701-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="26701-105">Sequence Restrictions</span></span>

<span data-ttu-id="26701-106">L'azione RegisterProgIdInfo deve provenire dopo l'azione [InstallFiles](installfiles-action.md) , l'azione [UnregisterProgIdInfo](unregisterprogidinfo-action.md) , l'azione [registerClassInfo](registerclassinfo-action.md) e l'azione [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="26701-106">The RegisterProgIdInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterProgIdInfo](unregisterprogidinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="26701-107">La sequenziazione delle azioni nel gruppo seguente è limitata.</span><span class="sxs-lookup"><span data-stu-id="26701-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="26701-108">Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="26701-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="26701-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="26701-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="26701-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="26701-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="26701-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="26701-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="26701-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="26701-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="26701-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="26701-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="26701-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="26701-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   <span data-ttu-id="26701-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="26701-115">RegisterProgIdInfo</span></span>
-   [<span data-ttu-id="26701-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="26701-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="26701-117">Ad esempio, RegisterProgIdInfo deve essere seguito da [RegisterExtensionInfo](registerextensioninfo-action.md) nella tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="26701-117">For example, RegisterProgIdInfo must come after [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="26701-118">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="26701-118">ActionData Messages</span></span>



| <span data-ttu-id="26701-119">Campo</span><span class="sxs-lookup"><span data-stu-id="26701-119">Field</span></span> | <span data-ttu-id="26701-120">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="26701-120">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="26701-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="26701-121">\[1\]</span></span> | <span data-ttu-id="26701-122">Identificatore del programma registrato.</span><span class="sxs-lookup"><span data-stu-id="26701-122">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="26701-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="26701-123">Remarks</span></span>

<span data-ttu-id="26701-124">L'azione RegisterProgIdInfo registra tutte le informazioni sul ProgId per i server specificati nella [tabella ProgId](progid-table.md) e per cui è stato selezionato il server di classe o il server di estensione corrispondente da installare.</span><span class="sxs-lookup"><span data-stu-id="26701-124">The RegisterProgIdInfo action registers all ProgId information for servers that are specified in the [ProgId table](progid-table.md) and for which the corresponding class server or extension server has been selected to be installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26701-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26701-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26701-126">Tabella classi</span><span class="sxs-lookup"><span data-stu-id="26701-126">Class table</span></span>](class-table.md)
</dt> <dt>

[<span data-ttu-id="26701-127">Tabella di estensione</span><span class="sxs-lookup"><span data-stu-id="26701-127">Extension table</span></span>](extension-table.md)
</dt> </dl>

 

 



