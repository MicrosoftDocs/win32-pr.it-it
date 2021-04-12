---
title: Tipo di avvio BITS
description: Il tipo di avvio per BITS è l'avvio automatico ritardato. Prima di Windows Vista, il tipo di avvio per BITS è manuale. Quando viene creato un processo BITS, il tipo di avvio passa a automatico. Il tipo di avvio torna a manuale quando tutti i processi vengono completati o annullati.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1ce1dcd2f939237142a0afd44e49b4b63df419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395358"
---
# <a name="bits-startup-type"></a><span data-ttu-id="6065d-106">Tipo di avvio BITS</span><span class="sxs-lookup"><span data-stu-id="6065d-106">BITS Startup Type</span></span>

<span data-ttu-id="6065d-107">Il **tipo di avvio** per BITS è l'avvio automatico ritardato (se sono presenti processi BITS attivi) o l'avvio della richiesta (se non sono presenti processi attivi).</span><span class="sxs-lookup"><span data-stu-id="6065d-107">The **Startup Type** for BITS is delayed auto-start (if there are active BITS jobs) or demand start (if there are no active jobs).</span></span> <span data-ttu-id="6065d-108">Nelle versioni di Windows precedenti all'aggiornamento di novembre veniva utilizzato solo il tipo di avvio a avvio automatico ritardato; nelle versioni precedenti a vista è stato utilizzato il tipo di avvio manuale.</span><span class="sxs-lookup"><span data-stu-id="6065d-108">Versions of Windows prior to the November Update used only the delayed auto-start startup type; versions prior to Vista used the manual startup type.</span></span>

<span data-ttu-id="6065d-109">Non impostare il tipo di **avvio** su disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6065d-109">You should not set the **Startup Type** to Disabled.</span></span> <span data-ttu-id="6065d-110">La disabilitazione di BITS potrebbe interrompere le applicazioni che si basano sui bit per trasferire i file.</span><span class="sxs-lookup"><span data-stu-id="6065d-110">Disabling BITS may break applications that rely on BITS to transfer files.</span></span>

 

 




