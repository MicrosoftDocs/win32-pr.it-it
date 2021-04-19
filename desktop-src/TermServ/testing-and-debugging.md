---
title: Test e debug
description: È presente un \ 0034; Echo \ 0034; listener implementato dal client Connessione Desktop remoto (RDC), che è sempre presente e in ascolto delle connessioni in ingresso.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297882"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="cb698-103">Test e debug</span><span class="sxs-lookup"><span data-stu-id="cb698-103">Testing and Debugging</span></span>

<span data-ttu-id="cb698-104">È presente un listener "echo" implementato dal client Connessione Desktop remoto (RDC), che è sempre presente e in ascolto delle connessioni in ingresso.</span><span class="sxs-lookup"><span data-stu-id="cb698-104">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span> <span data-ttu-id="cb698-105">Quando si scrive il lato server di un modulo canale virtuale dinamico (DVC), come test rapido è possibile aprire un endpoint denominato "ECHO".</span><span class="sxs-lookup"><span data-stu-id="cb698-105">When you are writing the server side of a dynamic virtual channel (DVC) module, as a quick test you can open an endpoint named "ECHO".</span></span> <span data-ttu-id="cb698-106">Qualsiasi operazione di scrittura su un canale di cui viene creata un'istanza da questo endpoint comporterà la ricezione degli stessi dati.</span><span class="sxs-lookup"><span data-stu-id="cb698-106">Any write to a channel that is instantiated from this endpoint will result in the receipt of the same data.</span></span>

<span data-ttu-id="cb698-107">È possibile utilizzare questa tecnica per testare un'implementazione di input/output (I/O) del modulo lato server, per misurare il tempo di risposta per un plug-in del client Connessione Desktop remoto (RDC) o per misurare il ritardo di rete per il client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="cb698-107">You can use this technique to test an input/output (I/O) implementation of the server-side module, to measure the response time for a Remote Desktop Connection (RDC) client plug-in, or to measure the network delay for the Remote Desktop Connection (RDC) client.</span></span> <span data-ttu-id="cb698-108">Non esiste alcuna limitazione sulla quantità di dati che è possibile inviare su questo canale.</span><span class="sxs-lookup"><span data-stu-id="cb698-108">There is no limitation on the amount of data that can be sent over this channel.</span></span>

 

 




