---
title: Limitazioni dell'autenticazione reciproca con Kerberos
description: Sia l'account del client che l'account del servizio devono trovarsi in domini Windows 2000 nativi o in modalità mista perché i servizi Kerberos non sono disponibili nei domini di livello inferiore.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470859"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a><span data-ttu-id="4cbd8-103">Limitazioni dell'autenticazione reciproca con Kerberos</span><span class="sxs-lookup"><span data-stu-id="4cbd8-103">Limitations of Mutual Authentication with Kerberos</span></span>

<span data-ttu-id="4cbd8-104">Sia l'account del client che l'account del servizio devono trovarsi in domini Windows 2000 nativi o in modalità mista perché i servizi Kerberos non sono disponibili nei domini di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="4cbd8-104">Both the client's account and the service's account must be in Windows 2000 native or mixed-mode domains because Kerberos services are not available in downlevel domains.</span></span> <span data-ttu-id="4cbd8-105">Inoltre, sia gli account client che quelli del servizio devono trovarsi nella stessa foresta, perché il KDC del client usa il catalogo globale per cercare il nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="4cbd8-105">In addition, both client and service accounts must be in the same forest because the client's KDC uses the global catalog to search for the service principal name.</span></span>

<span data-ttu-id="4cbd8-106">Sia il servizio che il client devono essere in esecuzione in Windows 2000; in caso contrario, l'autenticazione reciproca con Kerberos avrà esito negativo perché le versioni precedenti di Windows non supportano Kerberos.</span><span class="sxs-lookup"><span data-stu-id="4cbd8-106">Both service and client must be running on Windows 2000, otherwise mutual authentication with Kerberos will fail because earlier versions of Windows do not support Kerberos.</span></span>

<span data-ttu-id="4cbd8-107">I nomi dell'entità servizio devono includere il nome DNS del server host in cui è in esecuzione il servizio.</span><span class="sxs-lookup"><span data-stu-id="4cbd8-107">Service principal names must include the DNS name of the host server on which the service is running.</span></span> <span data-ttu-id="4cbd8-108">È necessario usare il nome DNS.</span><span class="sxs-lookup"><span data-stu-id="4cbd8-108">You must use the DNS name.</span></span>

 

 




