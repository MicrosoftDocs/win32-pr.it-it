---
title: Procedure consigliate per il caricamento
description: Highloads può causare diverse condizioni di timeout del server, che a loro volta possono aumentare il carico quando il client tenta di riprovare.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044161"
---
# <a name="upload-best-practices"></a><span data-ttu-id="c028e-103">Procedure consigliate per il caricamento</span><span class="sxs-lookup"><span data-stu-id="c028e-103">Upload Best Practices</span></span>

<span data-ttu-id="c028e-104">Highloads può causare diverse condizioni di timeout del server, che a loro volta possono aumentare il carico quando il client tenta di riprovare.</span><span class="sxs-lookup"><span data-stu-id="c028e-104">Highloads may cause various server timeout conditions, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="c028e-105">Inoltre, un numero elevato di connessioni in attesa utilizzerà più risorse server e peggiorerà la situazione.</span><span class="sxs-lookup"><span data-stu-id="c028e-105">Also, a large number of outstanding connections will consume more server resources and make the situation worse.</span></span> <span data-ttu-id="c028e-106">A questo punto, se l'app back-end non è scritta per gestire le condizioni di carico elevato, è possibile che si verifichi un arresto anomalo o un comportamento anomalo.</span><span class="sxs-lookup"><span data-stu-id="c028e-106">On top of that, if backend app is not written to handle high load conditions, it may crash or mal-behave.</span></span> <span data-ttu-id="c028e-107">L'app deve eseguire la procedura seguente per limitare il carico sul back-end.</span><span class="sxs-lookup"><span data-stu-id="c028e-107">The app shall perform the following steps to limit the load on the backend.</span></span>

<span data-ttu-id="c028e-108">Se l'applicazione server non è scritta per gestire volumi elevati, è possibile che si verifichino condizioni di timeout, che a loro volta aumentano il carico al nuovo tentativo del client.</span><span class="sxs-lookup"><span data-stu-id="c028e-108">If the server application is not written to handle high volumes, timeout conditions may occur, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="c028e-109">Inoltre, un numero elevato di connessioni in attesa utilizzerà più risorse server.</span><span class="sxs-lookup"><span data-stu-id="c028e-109">Also, a large number of outstanding connections will consume more server resources.</span></span>

<span data-ttu-id="c028e-110">Quando si esegue il test dell'applicazione server, testare con il carico più elevato possibile.</span><span class="sxs-lookup"><span data-stu-id="c028e-110">When testing your server application, test with highest load possible.</span></span> <span data-ttu-id="c028e-111">È consigliabile usare più computer client, ognuno con diversi processi di bit in primo piano simultanei e misurare la velocità effettiva massima nel back-end.</span><span class="sxs-lookup"><span data-stu-id="c028e-111">You should use multiple client machines, each with several concurrent, foreground BITS jobs, and measure the maximum throughput at the backend.</span></span> <span data-ttu-id="c028e-112">Se non è possibile misurare la velocità effettiva, sarà necessario stimare la velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="c028e-112">If you cannot measure the throughput, you will have to estimate the throughput.</span></span>

<span data-ttu-id="c028e-113">L'applicazione server deve risiedere in un URL diverso dall'URL di caricamento (vedere la proprietà di IIS BITS, **BITSServerNotificationURL**).</span><span class="sxs-lookup"><span data-stu-id="c028e-113">The server application should reside on a different URL from the upload URL (see the BITS IIS property, **BITSServerNotificationURL**).</span></span>

<span data-ttu-id="c028e-114">È consigliabile limitare il carico sul server applicazioni in base ai valori di velocità effettiva comprovati.</span><span class="sxs-lookup"><span data-stu-id="c028e-114">It is good practice to limit the load on the application server based on proven throughput values.</span></span> <span data-ttu-id="c028e-115">È necessario utilizzare le proprietà IIS, **MaxBandwidth** e **MaxConnections**, per limitare il carico sul server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c028e-115">You should use the IIS properties, **MaxBandwidth** and **MaxConnections**, to limit the load on the application server.</span></span>

 

 




