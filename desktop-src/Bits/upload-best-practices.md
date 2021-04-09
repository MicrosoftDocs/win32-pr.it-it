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
# <a name="upload-best-practices"></a>Procedure consigliate per il caricamento

Highloads può causare diverse condizioni di timeout del server, che a loro volta possono aumentare il carico quando il client tenta di riprovare. Inoltre, un numero elevato di connessioni in attesa utilizzerà più risorse server e peggiorerà la situazione. A questo punto, se l'app back-end non è scritta per gestire le condizioni di carico elevato, è possibile che si verifichi un arresto anomalo o un comportamento anomalo. L'app deve eseguire la procedura seguente per limitare il carico sul back-end.

Se l'applicazione server non è scritta per gestire volumi elevati, è possibile che si verifichino condizioni di timeout, che a loro volta aumentano il carico al nuovo tentativo del client. Inoltre, un numero elevato di connessioni in attesa utilizzerà più risorse server.

Quando si esegue il test dell'applicazione server, testare con il carico più elevato possibile. È consigliabile usare più computer client, ognuno con diversi processi di bit in primo piano simultanei e misurare la velocità effettiva massima nel back-end. Se non è possibile misurare la velocità effettiva, sarà necessario stimare la velocità effettiva.

L'applicazione server deve risiedere in un URL diverso dall'URL di caricamento (vedere la proprietà di IIS BITS, **BITSServerNotificationURL**).

È consigliabile limitare il carico sul server applicazioni in base ai valori di velocità effettiva comprovati. È necessario utilizzare le proprietà IIS, **MaxBandwidth** e **MaxConnections**, per limitare il carico sul server applicazioni.

 

 




