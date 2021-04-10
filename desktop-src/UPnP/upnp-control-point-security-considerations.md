---
title: Considerazioni sulla sicurezza del punto di controllo
description: Quando si crea un punto di controllo, è necessario prendere in considerazione i seguenti problemi di sicurezza.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955684"
---
# <a name="control-point-security-considerations"></a><span data-ttu-id="34f2c-103">Considerazioni sulla sicurezza del punto di controllo</span><span class="sxs-lookup"><span data-stu-id="34f2c-103">Control Point Security Considerations</span></span>

<span data-ttu-id="34f2c-104">Quando si crea un punto di controllo, è necessario prendere in considerazione i seguenti problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="34f2c-104">When you are creating a control point, you need to take into consideration the following security issues.</span></span>

-   <span data-ttu-id="34f2c-105">Per impostazione predefinita, tutte le ricerche di punti di controllo sono inviate con un valore TTL pari a 1.</span><span class="sxs-lookup"><span data-stu-id="34f2c-105">All control point searches are by default sent with a TTL of 1.</span></span> <span data-ttu-id="34f2c-106">Ciò significa che vengono individuati solo i dispositivi all'interno della stessa subnet.</span><span class="sxs-lookup"><span data-stu-id="34f2c-106">This means that only devices within the same subnet are discovered.</span></span> <span data-ttu-id="34f2c-107">È possibile configurare una durata (TTL) superiore nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="34f2c-107">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="34f2c-108">La descrizione del dispositivo e del servizio di un dispositivo viene scaricata solo se è presente nello stesso dispositivo che ha inviato l'annuncio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34f2c-108">A device's device and service description is only downloaded if it is present on the same device which sent the device announcement.</span></span>
-   <span data-ttu-id="34f2c-109">Un dispositivo viene inviato solo per le richieste di controllo e sottoscrizione se gli URL di controllo e sottoscrizione si trovano nello stesso dispositivo che ha inviato gli annunci del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34f2c-109">A device is only sent control and subscription requests if its control and subscription URLs are on the same device that sent the device announcements.</span></span>

 

 




