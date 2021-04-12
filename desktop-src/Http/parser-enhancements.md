---
title: Miglioramenti del parser
description: Miglioramenti del parser
ms.assetid: b520aebe-9182-4e60-9111-49af09cdbd79
keywords:
- Miglioramenti del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a22f4b4dced29e25662a6fc521057a055b56f70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396350"
---
# <a name="parser-enhancements"></a><span data-ttu-id="370f8-104">Miglioramenti del parser</span><span class="sxs-lookup"><span data-stu-id="370f8-104">Parser Enhancements</span></span>

<span data-ttu-id="370f8-105">In Windows Server 2003 con Service Pack 1 (SP1), l'API server HTTP consente le richieste seguenti dai client HTTP.</span><span class="sxs-lookup"><span data-stu-id="370f8-105">In Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API allows the following requests from HTTP clients.</span></span>

-   <span data-ttu-id="370f8-106">Richieste che utilizzano un singolo avanzamento riga (LF) come terminatori di riga.</span><span class="sxs-lookup"><span data-stu-id="370f8-106">Requests that use a single Line Feed (LF) as line terminators.</span></span>
-   <span data-ttu-id="370f8-107">Richieste che contengono gli spazi vuoti lineari (dichiarazione di conformità) tra la riga di richiesta HTTP e l'inizio di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="370f8-107">Requests that contain linear white space (LWS) between the HTTP request line and start of headers.</span></span>

<span data-ttu-id="370f8-108">Questi comportamenti sono abilitati per impostazione predefinita e non sono controllati dalle impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="370f8-108">These behaviors are enabled by default and are not controlled by registry settings.</span></span>

 

 




