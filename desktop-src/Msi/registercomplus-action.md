---
description: L'azione RegisterComPlus registra le applicazioni COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Azione RegisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131618"
---
# <a name="registercomplus-action"></a><span data-ttu-id="a9300-103">Azione RegisterComPlus</span><span class="sxs-lookup"><span data-stu-id="a9300-103">RegisterComPlus Action</span></span>

<span data-ttu-id="a9300-104">L'azione RegisterComPlus registra le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="a9300-104">The RegisterComPlus action registers COM+ applications.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a9300-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="a9300-105">Sequence Restrictions</span></span>

<span data-ttu-id="a9300-106">L'azione RegisterComPlus deve seguire l'azione [InstallFiles](installfiles-action.md) e l'azione [UnregisterComPlus](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="a9300-106">The RegisterComPlus action must follow the [InstallFiles action](installfiles-action.md) and the [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a9300-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="a9300-107">ActionData Messages</span></span>



| <span data-ttu-id="a9300-108">Campo</span><span class="sxs-lookup"><span data-stu-id="a9300-108">Field</span></span> | <span data-ttu-id="a9300-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="a9300-109">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="a9300-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a9300-110">\[1\]</span></span> | <span data-ttu-id="a9300-111">ID applicazione dell'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="a9300-111">Application ID of the COM+ application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a9300-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9300-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9300-113">Tabella ComPlus</span><span class="sxs-lookup"><span data-stu-id="a9300-113">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="a9300-114">Azione UnregisterComPlus</span><span class="sxs-lookup"><span data-stu-id="a9300-114">UnregisterComPlus action</span></span>](unregistercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="a9300-115">Installazione di un'applicazione COM+ con la Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a9300-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



