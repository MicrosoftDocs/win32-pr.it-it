---
description: Esiste un'altra classe di eventi asincroni oltre a quelli descritti in precedenza.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Eventi spontanei asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314638"
---
# <a name="asynchronous-spontaneous-events"></a><span data-ttu-id="4552a-103">Eventi spontanei asincroni</span><span class="sxs-lookup"><span data-stu-id="4552a-103">Asynchronous Spontaneous Events</span></span>

<span data-ttu-id="4552a-104">Esiste un'altra classe di eventi asincroni oltre a quelli descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4552a-104">There is another class of asynchronous events besides those described above.</span></span> <span data-ttu-id="4552a-105">Questi eventi sono "spontanei" nel senso che non sono risultati diretti delle richieste corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="4552a-105">These events are "spontaneous" in the sense that they are not direct results of corresponding requests.</span></span> <span data-ttu-id="4552a-106">Questi eventi vengono rilevati in questi casi come quando arriva una chiamata in ingresso o quando una chiamata in uscita passa da uno "squillo" a uno stato di "risposta".</span><span class="sxs-lookup"><span data-stu-id="4552a-106">These events are detected in such cases as when an incoming call arrives, or when an outbound call goes from a "ringing" to an "answering" state.</span></span> <span data-ttu-id="4552a-107">Quando TAPI Inizializza innanzitutto le interazioni con TSPI per un particolare dispositivo, passa un puntatore a una routine di callback da chiamare per la segnalazione di eventi spontanei.</span><span class="sxs-lookup"><span data-stu-id="4552a-107">When TAPI first initializes interactions with the TSPI for a particular device, it passes a pointer to a callback procedure to be called for reporting such spontaneous events.</span></span> <span data-ttu-id="4552a-108">Insieme a questo puntatore di procedura è un handle di dispositivo che il provider di servizi include come uno dei parametri effettivi per il callback.</span><span class="sxs-lookup"><span data-stu-id="4552a-108">Along with this procedure pointer is a device handle that the service provider includes as one of the actual parameters to the callback.</span></span>

 

 



