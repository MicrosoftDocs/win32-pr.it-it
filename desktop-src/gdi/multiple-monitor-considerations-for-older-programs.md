---
description: In genere, le applicazioni meno recenti non necessitano di modifiche per lavorare su più sistemi di monitoraggio.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Considerazioni su più monitor per i programmi precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978522"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a><span data-ttu-id="88085-103">Considerazioni su più monitor per i programmi precedenti</span><span class="sxs-lookup"><span data-stu-id="88085-103">Multiple Monitor Considerations for Older Programs</span></span>

<span data-ttu-id="88085-104">In genere, le applicazioni meno recenti non necessitano di modifiche per lavorare su più sistemi di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="88085-104">Generally, older applications do not need changes to work on multiple monitor systems.</span></span> <span data-ttu-id="88085-105">Per la maggior parte, il sistema apparirà solo una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="88085-105">For most, the system will appear to have only one display.</span></span> <span data-ttu-id="88085-106">Le metriche di sistema riflettono lo schermo principale e le applicazioni a schermo intero vengono visualizzate nel database primario.</span><span class="sxs-lookup"><span data-stu-id="88085-106">System metrics reflect the primary display and fullscreen applications show up on the primary.</span></span> <span data-ttu-id="88085-107">Il sistema gestisce la riduzione a icona, la massimizzazione, i menu e le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="88085-107">The system handles minimization, maximization, menus, and dialog boxes.</span></span>

<span data-ttu-id="88085-108">Tuttavia, in alcuni programmi si verificano problemi.</span><span class="sxs-lookup"><span data-stu-id="88085-108">However, some programs will have problems.</span></span> <span data-ttu-id="88085-109">Alcune che potrebbero avere problemi sono le applicazioni di controllo remoto, quelle che dispongono di accesso diretto all'hardware e quelle con patch per GDI o driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="88085-109">Some that could have problems are remote control applications, those that have direct hardware access, and those that have patched the GDI or DISPLAY driver.</span></span> <span data-ttu-id="88085-110">In questi casi, è possibile che l'utente debba disabilitare qualsiasi monitoraggio oltre il monitor primario.</span><span class="sxs-lookup"><span data-stu-id="88085-110">In these cases, the user may be required to disable any monitor beyond the primary monitor.</span></span>

 

 



