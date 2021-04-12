---
title: Proprietà Message e Message Queue
description: Un messaggio dispone di proprietà che specificano un'etichetta, un corpo del messaggio e un numero di opzioni.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330951"
---
# <a name="message-and-message-queue-properties"></a><span data-ttu-id="af832-103">Proprietà Message e Message Queue</span><span class="sxs-lookup"><span data-stu-id="af832-103">Message and Message Queue Properties</span></span>

<span data-ttu-id="af832-104">Un messaggio dispone di proprietà che specificano un'etichetta, un corpo del messaggio e un numero di opzioni.</span><span class="sxs-lookup"><span data-stu-id="af832-104">A message has properties, which specify a label, a message body, and a number of options.</span></span> <span data-ttu-id="af832-105">Le opzioni delle proprietà dei messaggi possono includere la qualità del servizio, la priorità, il journaling, la privacy e i livelli di autenticazione e la durata del messaggio.</span><span class="sxs-lookup"><span data-stu-id="af832-105">Message property options can include quality of service, priority, journaling, privacy and authentication levels, and the lifetime of the message.</span></span> <span data-ttu-id="af832-106">Nelle applicazioni di Accodamento messaggi convenzionali (non RPC), è possibile specificare queste proprietà chiamando le funzioni dell'API MSMQ o i metodi dell'oggetto COM, descritti nella documentazione di MSMQ SDK.</span><span class="sxs-lookup"><span data-stu-id="af832-106">In conventional (non-RPC) message-queuing applications, you specify these properties by calling the MSMQ API functions or COM object methods, which are described in the MSMQ SDK documentation.</span></span> <span data-ttu-id="af832-107">Le applicazioni client RPC possono impostare determinate proprietà per le chiamate a procedure remote chiamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) e [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="af832-107">RPC client applications can set certain properties for remote procedure calls by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) and [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span> <span data-ttu-id="af832-108">Una volta impostate, le proprietà rimangono attive per ogni messaggio fino a quando non vengono reimpostate dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="af832-108">Once set, the properties remain in effect for each message until the client application resets them.</span></span>

<span data-ttu-id="af832-109">Una coda di messaggi dispone di un proprio set di proprietà, oltre a quelle dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="af832-109">A message queue has its own set of properties, apart from those of the messages.</span></span> <span data-ttu-id="af832-110">Queste proprietà identificano in modo univoco una coda e definiscono la classe di servizio fornita dalla coda, i livelli di privacy e autenticazione necessari per i messaggi in questa coda e se i messaggi devono far parte di una transazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="af832-110">These properties uniquely identify a queue and define the class of service that the queue provides, the privacy and authentication levels required for messages in this queue, and whether the messages are to be part of a distributed transaction.</span></span> <span data-ttu-id="af832-111">Come per le proprietà dei messaggi, è possibile specificare le proprietà di una coda di messaggi chiamando le funzioni dell'API MSMQ o i metodi dell'oggetto COM, descritti nella documentazione di MSMQ.</span><span class="sxs-lookup"><span data-stu-id="af832-111">As with message properties, you specify the properties of a message queue by calling the MSMQ API functions or COM object methods, which are described in the MSMQ documentation.</span></span> <span data-ttu-id="af832-112">Tuttavia, un'applicazione server RPC può specificare le proprietà della propria coda di ricezione quando chiama [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) per stabilire l'associazione.</span><span class="sxs-lookup"><span data-stu-id="af832-112">However, an RPC server application can specify properties of its own receive queue when it calls [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) to establish the binding.</span></span>

 

 




