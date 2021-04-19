---
title: Eventi SystemMonitor
description: La classe SystemMonitor presenta gli eventi seguenti
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297635"
---
# <a name="systemmonitor-events"></a><span data-ttu-id="1fbe5-103">Eventi SystemMonitor</span><span class="sxs-lookup"><span data-stu-id="1fbe5-103">SystemMonitor Events</span></span>

<span data-ttu-id="1fbe5-104">La classe [**SystemMonitor**](systemmonitor.md) presenta gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1fbe5-104">The [**SystemMonitor**](systemmonitor.md) class has the following events:</span></span>

-   [<span data-ttu-id="1fbe5-105">**OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="1fbe5-105">**OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
-   [<span data-ttu-id="1fbe5-106">**OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="1fbe5-106">**OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
-   [<span data-ttu-id="1fbe5-107">**OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="1fbe5-107">**OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
-   [<span data-ttu-id="1fbe5-108">**OnDblClick**</span><span class="sxs-lookup"><span data-stu-id="1fbe5-108">**OnDblClick**</span></span>](-systemmonitor-ondblclick.md)
-   [<span data-ttu-id="1fbe5-109">**OnSampleCollected**</span><span class="sxs-lookup"><span data-stu-id="1fbe5-109">**OnSampleCollected**</span></span>](-systemmonitor-onsamplecollected.md)

> [!Note]  
> <span data-ttu-id="1fbe5-110">È necessario restituire dal gestore eventi prima della scadenza dell' [**intervallo di aggiornamento**](systemmonitor-updateinterval.md) ; in caso contrario, SYSMON Visualizza una finestra di messaggio che indica all'utente che non è stato possibile campionare i valori dei contatori per l'intervallo di aggiornamento precedente.</span><span class="sxs-lookup"><span data-stu-id="1fbe5-110">You must return from the event handler before the [**update interval**](systemmonitor-updateinterval.md) expires; otherwise, SYSMON displays a message box indicating to the user that it was unable to sample counter values for the previous update interval.</span></span>

 

 

 




