---
title: Invio della chiamata al programma server
description: Una volta che il tempo di esecuzione RPC lato client si è connesso all'endpoint server, il marshalling degli argomenti e li invia al server.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- RPC (Remote Procedure Call), attività, invio della chiamata al server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331783"
---
# <a name="sending-the-call-to-the-server-program"></a><span data-ttu-id="1e066-104">Invio della chiamata al programma server</span><span class="sxs-lookup"><span data-stu-id="1e066-104">Sending the Call to the Server Program</span></span>

<span data-ttu-id="1e066-105">Una volta che il tempo di esecuzione RPC lato client si è connesso all'endpoint server, il marshalling degli argomenti e li invia al server.</span><span class="sxs-lookup"><span data-stu-id="1e066-105">Once the client side RPC run time has connected to the server endpoint, it marshalls the arguments and sends them to the server.</span></span> <span data-ttu-id="1e066-106">Il tempo di esecuzione RPC del server assegna gli argomenti con marshalling allo stub che li rimuove e li passa alle routine del server.</span><span class="sxs-lookup"><span data-stu-id="1e066-106">The server RPC run time gives the marshalled arguments to the stub that unmarshalls them, and then passes them to the server routines.</span></span> <span data-ttu-id="1e066-107">Quando le routine del server restituiscono, lo stub preleva i \[ parametri out \] e \[ in, out \] e il valore restituito, li Marshall e invia i dati di marshalling al runtime RPC del server.</span><span class="sxs-lookup"><span data-stu-id="1e066-107">When the server routines return, the stub picks up the \[out\] and \[in,out\] parameters and the return value, marshalls them, and sends the marshalled data to the server RPC run time.</span></span> <span data-ttu-id="1e066-108">Il tempo di esecuzione RPC invia i dati al client, in cui il tempo di esecuzione RPC del client li consegna allo stub lato client che li rimuove e li restituisce al chiamante.</span><span class="sxs-lookup"><span data-stu-id="1e066-108">The RPC run time sends the data back to the client, where the client RPC run time hands them off to the client side stub that unmarshalls them and returns them to the caller.</span></span>

 

 




