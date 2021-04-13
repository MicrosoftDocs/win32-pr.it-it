---
title: Operazioni asincrone
description: Quando RasDial viene richiamato come operazione asincrona, la funzione restituisce immediatamente.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396210"
---
# <a name="asynchronous-operations"></a><span data-ttu-id="e63d3-103">Operazioni asincrone</span><span class="sxs-lookup"><span data-stu-id="e63d3-103">Asynchronous Operations</span></span>

<span data-ttu-id="e63d3-104">Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) viene richiamato come operazione asincrona, la funzione restituisce immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e63d3-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as an asynchronous operation, the function returns immediately.</span></span> <span data-ttu-id="e63d3-105">In modalità asincrona la chiamata **RasDial** deve specificare un [gestore di notifiche](notification-handlers.md) usato dalla gestione connessione di accesso remoto per informare il client ogni volta che l'operazione di connessione cambia Stati o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="e63d3-105">In asynchronous mode, the **RasDial** call must specify a [notification handler](notification-handlers.md) that the Remote Access Connection Manager uses to inform the client whenever the connection operation changes states or an error occurs.</span></span>

<span data-ttu-id="e63d3-106">Il gestore delle notifiche può essere una finestra per la ricezione di messaggi o una funzione di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)o [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) .</span><span class="sxs-lookup"><span data-stu-id="e63d3-106">The notification handler can be a window to receive messages, or a [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1), or [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) callback function.</span></span> <span data-ttu-id="e63d3-107">La gestione connessione di accesso remoto esegue le notifiche asincrone nel contesto del thread che ha effettuato la chiamata a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .</span><span class="sxs-lookup"><span data-stu-id="e63d3-107">The Remote Access Connection Manager makes its asynchronous notifications in the context of the thread that made the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span> <span data-ttu-id="e63d3-108">Per questo motivo, il thread chiamante non deve terminare fino a quando l'operazione di connessione non è stata stabilita correttamente o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="e63d3-108">For this reason, the calling thread must not terminate until the connection operation has been successfully established or an error occurs.</span></span> <span data-ttu-id="e63d3-109">In modalità sincrona, l'applicazione client può terminare in modo sicuro una volta stabilita la connessione e [arrestare l'operazione di connessione](disconnecting.md) se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="e63d3-109">As in synchronous mode, the client application can safely terminate once the connection has been established, and it must [shut down the connection operation](disconnecting.md) if an error occurs.</span></span>

 

 




