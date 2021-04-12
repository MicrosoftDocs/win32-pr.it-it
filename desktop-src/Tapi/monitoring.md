---
description: Il monitoraggio è una funzionalità definita dal provider di servizi che rileva i segnali che indicano altri supporti.
ms.assetid: 77735a42-049a-4f16-a502-ff6d31ef3cd0
title: Monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1bca5e4287d0aeb3aee89cceb72f725e95a3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344261"
---
# <a name="monitoring"></a><span data-ttu-id="071ac-103">Monitoraggio</span><span class="sxs-lookup"><span data-stu-id="071ac-103">Monitoring</span></span>

<span data-ttu-id="071ac-104">Il monitoraggio è una funzionalità definita dal provider di servizi che rileva i segnali che indicano altri supporti.</span><span class="sxs-lookup"><span data-stu-id="071ac-104">Monitoring is a service-provider defined feature that detects signals that indicate other media.</span></span> <span data-ttu-id="071ac-105">Ad esempio, è possibile che un'applicazione rilasci un messaggio vocale in uscita mentre la chiamata in ingresso inizia a inviare un segnale di "chiamata" del fax e attenda un handshake.</span><span class="sxs-lookup"><span data-stu-id="071ac-105">For example, one application can be playing an outgoing "leave a message" voice message while the incoming call starts sending a fax "calling" tone and waits for a handshake.</span></span> <span data-ttu-id="071ac-106">Per non perdere la chiamata fax, l'applicazione locale monitora questo tono durante la riproduzione del messaggio vocale.</span><span class="sxs-lookup"><span data-stu-id="071ac-106">In order not to lose the fax call, the local application monitors for this tone while playing the voice message.</span></span>

<span data-ttu-id="071ac-107">Il monitoraggio comprende il monitoraggio [dei supporti](/previous-versions/windows/desktop/legacy/ms725242(v=vs.85)), il [monitoraggio delle cifre](/previous-versions/windows/desktop/legacy/ms725185(v=vs.85))e il [monitoraggio dei toni](/previous-versions/windows/desktop/legacy/ms725520(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="071ac-107">Monitoring comprises [media monitoring](/previous-versions/windows/desktop/legacy/ms725242(v=vs.85)), [digit monitoring](/previous-versions/windows/desktop/legacy/ms725185(v=vs.85)), and [tone monitoring](/previous-versions/windows/desktop/legacy/ms725520(v=vs.85)).</span></span>

 

 
