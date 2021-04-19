---
description: Dopo aver creato un documento HTML di origine della pagina di riferimento a un evento, è necessario denominarlo prima che Network Monitor possa visualizzarlo nella Visualizzatore eventi.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Denominazione di una pagina di riferimento a un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319934"
---
# <a name="naming-an-event-reference-page"></a><span data-ttu-id="0f928-103">Denominazione di una pagina di riferimento a un evento</span><span class="sxs-lookup"><span data-stu-id="0f928-103">Naming an Event Reference Page</span></span>

<span data-ttu-id="0f928-104">Dopo aver creato un documento HTML di origine della pagina di riferimento a un evento, è necessario denominarlo prima che Network Monitor possa visualizzarlo nella Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="0f928-104">After you author an event reference page (ERP) source HTML document, you must name it before Network Monitor can display it in the Event Viewer.</span></span>

<span data-ttu-id="0f928-105">Nome e file ERP di esperti con il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="0f928-105">Name monitor and expert ERP files with this format:</span></span>

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span data-ttu-id="0f928-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**Expertname**</span><span class="sxs-lookup"><span data-stu-id="0f928-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span></span>
</dt> <dd>

<span data-ttu-id="0f928-107">Nome del file DLL, esclusa l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="0f928-107">DLL file name, excluding the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="0f928-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="0f928-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="0f928-109">Identificatore dell'evento ERP esperto.</span><span class="sxs-lookup"><span data-stu-id="0f928-109">Event identifier of the expert ERP.</span></span>

<span data-ttu-id="0f928-110">L'identificatore di evento è disponibile anche nel membro **EventIdent** della struttura **NMEVENTDATA** .</span><span class="sxs-lookup"><span data-stu-id="0f928-110">The event identifier is also found in the **EventIdent** member of the **NMEVENTDATA** structure.</span></span>

</dd> </dl>

<span data-ttu-id="0f928-111">Per ulteriori informazioni sulla creazione di un ERP, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0f928-111">For more information about creating an ERP, see the following topics:</span></span>

-   [<span data-ttu-id="0f928-112">Creazione di pagine di riferimento per gli eventi Expert e monitor</span><span class="sxs-lookup"><span data-stu-id="0f928-112">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="0f928-113">Scrittura di una pagina di riferimento a un evento</span><span class="sxs-lookup"><span data-stu-id="0f928-113">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="0f928-114">Test di una pagina di riferimento a un evento</span><span class="sxs-lookup"><span data-stu-id="0f928-114">Testing an Event Reference Page</span></span>](testing-an-event-reference-page.md)

 

 



