---
title: Operazioni sincrone
description: Quando RasDial viene richiamato come operazione sincrona, la funzione non viene restituita fino a quando non viene stabilita la connessione o si verifica un errore.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045198"
---
# <a name="synchronous-operations"></a><span data-ttu-id="f2975-103">Operazioni sincrone</span><span class="sxs-lookup"><span data-stu-id="f2975-103">Synchronous Operations</span></span>

<span data-ttu-id="f2975-104">Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) viene richiamato come operazione sincrona, la funzione non viene restituita fino a quando non viene stabilita la connessione o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="f2975-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as a synchronous operation, the function does not return until the connection has been established or an error occurs.</span></span> <span data-ttu-id="f2975-105">La modalità sincrona consente a un client RAS di stabilire una connessione in modo semplice.</span><span class="sxs-lookup"><span data-stu-id="f2975-105">Synchronous mode provides a simple way for a RAS client to establish a connection.</span></span> <span data-ttu-id="f2975-106">Il client può semplicemente chiamare **RasDial**, attendere la restituzione della funzione e quindi chiamare la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per determinare se l'operazione di connessione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="f2975-106">The client can simply call **RasDial**, wait for the function to return, and then call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to determine whether the connection operation was successful.</span></span> <span data-ttu-id="f2975-107">Una volta stabilita la connessione, l'applicazione client può terminare senza interrompere la connessione.</span><span class="sxs-lookup"><span data-stu-id="f2975-107">Once the connection has been established, the client application can terminate without breaking the connection.</span></span> <span data-ttu-id="f2975-108">Se si verifica un errore, l'applicazione client deve [arrestare l'operazione di connessione](disconnecting.md) prima di terminare.</span><span class="sxs-lookup"><span data-stu-id="f2975-108">If an error occurs, the client application must [shut down the connection operation](disconnecting.md) before terminating.</span></span>

<span data-ttu-id="f2975-109">Lo svantaggio della modalità sincrona è che il client non riceve le notifiche di stato durante l'operazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="f2975-109">The disadvantage of synchronous mode is that the client does not receive progress notifications as the connection operation proceeds.</span></span> <span data-ttu-id="f2975-110">Come soluzione alternativa per questa mancanza di notifiche di stato, un client in modalità sincrona può usare un thread separato che chiama [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per eseguire il polling e visualizzare lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="f2975-110">As a workaround for this lack of progress notifications, a synchronous mode client can use a separate thread that calls [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) to poll for and display the current state.</span></span> <span data-ttu-id="f2975-111">Tuttavia, per i client RAS che desiderano ricevere informazioni sullo stato di avanzamento, la tecnica preferita consiste nel richiamare [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="f2975-111">However, for RAS clients that want to receive progress information, the preferred technique is to invoke [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchronously.</span></span>

 

 




