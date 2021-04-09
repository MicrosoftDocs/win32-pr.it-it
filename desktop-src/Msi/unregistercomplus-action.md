---
description: L'azione UnregisterComPlus rimuove le applicazioni COM+ dal registro di sistema.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Azione UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968670"
---
# <a name="unregistercomplus-action"></a><span data-ttu-id="6cf43-103">Azione UnregisterComPlus</span><span class="sxs-lookup"><span data-stu-id="6cf43-103">UnregisterComPlus Action</span></span>

<span data-ttu-id="6cf43-104">L'azione UnregisterComPlus rimuove le applicazioni COM+ dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6cf43-104">The UnregisterComPlus action removes COM+ applications from the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6cf43-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="6cf43-105">Sequence Restrictions</span></span>

<span data-ttu-id="6cf43-106">L'azione [RegisterComPlus](registercomplus-action.md) deve seguire l'azione [InstallFiles](installfiles-action.md) e l'azione UnregisterComPlus.</span><span class="sxs-lookup"><span data-stu-id="6cf43-106">The [RegisterComPlus action](registercomplus-action.md) must follow the [InstallFiles action](installfiles-action.md) and the UnregisterComPlus action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6cf43-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="6cf43-107">ActionData Messages</span></span>



| <span data-ttu-id="6cf43-108">Campo</span><span class="sxs-lookup"><span data-stu-id="6cf43-108">Field</span></span> | <span data-ttu-id="6cf43-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="6cf43-109">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="6cf43-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6cf43-110">\[1\]</span></span> | <span data-ttu-id="6cf43-111">Identificatore dell'applicazione COM+ da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6cf43-111">Application identifier of the COM+ application being removed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6cf43-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6cf43-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cf43-113">Azione RegisterComPlus</span><span class="sxs-lookup"><span data-stu-id="6cf43-113">RegisterComPlus action</span></span>](registercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="6cf43-114">Tabella ComPlus</span><span class="sxs-lookup"><span data-stu-id="6cf43-114">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="6cf43-115">Installazione di un'applicazione COM+ con la Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6cf43-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



