---
title: Pacchetti di risposta BITS
description: Pacchetti di risposta BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855485"
---
# <a name="bits-response-packets"></a><span data-ttu-id="36e42-103">Pacchetti di risposta BITS</span><span class="sxs-lookup"><span data-stu-id="36e42-103">BITS Response Packets</span></span>

<span data-ttu-id="36e42-104">La tabella seguente elenca i pacchetti di risposta inviati al client BITS per i processi di caricamento e caricamento-risposta.</span><span class="sxs-lookup"><span data-stu-id="36e42-104">The following table lists the response packets sent to the BITS client for upload and upload-reply jobs.</span></span> <span data-ttu-id="36e42-105">La tabella elenca i pacchetti nella sequenza tipica che vengono inviati al client.</span><span class="sxs-lookup"><span data-stu-id="36e42-105">The table lists the packets in the typical sequence they are sent to the client.</span></span>



| <span data-ttu-id="36e42-106">Pacchetto di risposta</span><span class="sxs-lookup"><span data-stu-id="36e42-106">Response packet</span></span>                                      | <span data-ttu-id="36e42-107">Scopo</span><span class="sxs-lookup"><span data-stu-id="36e42-107">Purpose</span></span>                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36e42-108">ACK per ping</span><span class="sxs-lookup"><span data-stu-id="36e42-108">Ack for Ping</span></span>](ack-for-ping.md)                     | <span data-ttu-id="36e42-109">Riconosce la richiesta di [ping](ping.md) .</span><span class="sxs-lookup"><span data-stu-id="36e42-109">Acknowledges the [Ping](ping.md) request.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="36e42-110">ACK per create-Session</span><span class="sxs-lookup"><span data-stu-id="36e42-110">Ack for Create-Session</span></span>](ack-for-create-session.md) | <span data-ttu-id="36e42-111">Conferma la richiesta di [creazione della sessione](create-session.md) e restituisce un identificatore di sessione utilizzato dal client BITS per tutte le richieste successive per identificare questa sessione di trasferimento file.</span><span class="sxs-lookup"><span data-stu-id="36e42-111">Acknowledges the [Create-Session](create-session.md) request and returns a session identifier that the BITS client uses on all subsequent requests to identify this file transfer session.</span></span> |
| [<span data-ttu-id="36e42-112">ACK per il frammento</span><span class="sxs-lookup"><span data-stu-id="36e42-112">Ack for Fragment</span></span>](ack-for-fragment.md)             | <span data-ttu-id="36e42-113">Riconosce la richiesta del [frammento](fragment.md) e scrive il frammento nel file di caricamento sul server.</span><span class="sxs-lookup"><span data-stu-id="36e42-113">Acknowledges the [Fragment](fragment.md) request and writes the fragment to the upload file on the server.</span></span>                                                                                 |
| [<span data-ttu-id="36e42-114">ACK per chiusura sessione</span><span class="sxs-lookup"><span data-stu-id="36e42-114">Ack for Close-Session</span></span>](ack-for-close-session.md)   | <span data-ttu-id="36e42-115">Conferma la richiesta di [chiusura della sessione](close-session.md) e rilascia tutte le risorse associate alla sessione.</span><span class="sxs-lookup"><span data-stu-id="36e42-115">Acknowledges the [Close-Session](close-session.md) request and releases all resources associated with the session.</span></span>                                                                         |
| [<span data-ttu-id="36e42-116">ACK per la sessione di annullamento</span><span class="sxs-lookup"><span data-stu-id="36e42-116">Ack for Cancel-Session</span></span>](ack-for-cancel-session.md) | <span data-ttu-id="36e42-117">Riconosce la richiesta di [annullamento della sessione](cancel-session.md) e rilascia tutte le risorse associate alla sessione.</span><span class="sxs-lookup"><span data-stu-id="36e42-117">Acknowledges the [Cancel-Session](cancel-session.md) request and releases all resources associated with the session.</span></span>                                                                       |



 

 

 




