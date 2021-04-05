---
title: Condivisione connessione Internet
description: BITS può forzare una connessione remota per le reti domestiche che usano Microsoft Internet sharing se la condivisione della connessione è configurata per la connessione quando i computer nella rete accedono a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707840"
---
# <a name="internet-connection-sharing"></a><span data-ttu-id="82291-103">Condivisione connessione Internet</span><span class="sxs-lookup"><span data-stu-id="82291-103">Internet Connection Sharing</span></span>

<span data-ttu-id="82291-104">BITS può forzare una connessione remota per le reti domestiche che usano Microsoft Internet sharing se la condivisione della connessione è configurata per la connessione quando i computer nella rete accedono a Internet.</span><span class="sxs-lookup"><span data-stu-id="82291-104">BITS can force a dial-up connection for home networks that use Microsoft Internet Connection Sharing if Connection Sharing is configured to dial out when computers on the network access the Internet.</span></span> <span data-ttu-id="82291-105">Per evitare una connessione remota forzata, disabilitare la **connessione remota ogni volta che un computer della rete tenta di accedere all'opzione Internet** nel computer host di condivisione della connessione che condivide la connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="82291-105">To prevent a forced dial-up connection, disable the **Establish a dial-up connection whenever a computer on my network attempts to access the Internet** option on the Connection Sharing host computer that shares its Internet connection.</span></span>

<span data-ttu-id="82291-106">I computer connessi al computer host che condivide la connessione presuppongono che dispongano di una connessione di rete, quindi BITS tenterà di trasferire i file.</span><span class="sxs-lookup"><span data-stu-id="82291-106">Computers connected to the Connection Sharing host computer assume they have a network connection, so BITS will try to transfer files.</span></span> <span data-ttu-id="82291-107">Se l'opzione di connessione remota è disabilitata nel computer host e il computer host non dispone di una connessione attiva, i trasferimenti avranno esito negativo con un errore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="82291-107">If the dial-up option is disabled on the host computer and the host computer does not have an active connection, the transfers will fail with a transient error.</span></span> <span data-ttu-id="82291-108">BITS tenterà periodicamente di eseguire i trasferimenti.</span><span class="sxs-lookup"><span data-stu-id="82291-108">BITS will retry the transfers periodically.</span></span>

 

 




