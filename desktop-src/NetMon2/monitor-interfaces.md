---
description: Per sviluppare i monitoraggi vengono utilizzate le seguenti interfacce COM.
ms.assetid: 619991f5-1db1-400a-bf18-d4a6dd6999a8
title: Interfacce di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66bb06e6153d18c7b0a4291df1c7520380a29844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307711"
---
# <a name="monitor-interfaces"></a><span data-ttu-id="2765b-103">Interfacce di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="2765b-103">Monitor Interfaces</span></span>

<span data-ttu-id="2765b-104">Per sviluppare i monitoraggi vengono utilizzate le seguenti interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="2765b-104">The following COM interfaces are used to develop monitors.</span></span>



| <span data-ttu-id="2765b-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="2765b-105">Interface</span></span>                              | <span data-ttu-id="2765b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2765b-106">Description</span></span>                                                                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2765b-107">IMonitor</span><span class="sxs-lookup"><span data-stu-id="2765b-107">IMonitor</span></span>](imonitor.md)               | <span data-ttu-id="2765b-108">Fornisce metodi che controllano l'operazione di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="2765b-108">Provides methods that control monitor operation.</span></span> <span data-ttu-id="2765b-109">Questa interfaccia deve essere implementata dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="2765b-109">This interface must be implemented by the monitor.</span></span>                                                     |
| [<span data-ttu-id="2765b-110">IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="2765b-110">IMonitorEventer</span></span>](imonitoreventer.md) | <span data-ttu-id="2765b-111">Fornisce i metodi utilizzati per inviare eventi.</span><span class="sxs-lookup"><span data-stu-id="2765b-111">Provides methods used to send events.</span></span> <span data-ttu-id="2765b-112">Questa interfaccia viene fornita dal [*servizio di controllo di monitoraggio*](m.md) (MCSVC).</span><span class="sxs-lookup"><span data-stu-id="2765b-112">This interface is provided by the [*Monitor Control Service*](m.md) (MCSVC).</span></span> |



 

 

 



