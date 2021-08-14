---
title: Pulizia lato server
description: Pulizia lato server e chiamata di procedura remota (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 223cd15eb659a62c4a758098e9b0f70e977ebb069a2a305d2909b97b5fb12010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925293"
---
# <a name="server-side-cleanup"></a>Pulizia lato server

Imagine scenario seguente:

Un client apre un handle di contesto e quindi arresta o perde la connettività al server. In che modo il server rileva che il client ha avuto esito negativo e che l'handle di contesto deve essere arrestato? Esistono due sottoscenario: uno è che il client viene arrestato in modo ordinato. In tal caso, notifica al server che è in corso l'arresto e il server può eseguire la pulizia, inclusa l'esecuzione di run down del contesto. Se il client non viene arrestato in modo ordinato o non è in grado di inviare una notifica al server, il server usa keep-alive per determinare se il client è ancora disponibile. Sul lato server, la [**funzione RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) non ha alcun effetto. Al contrario, il server usa l'impostazione globale per computer-keep-alive, che per impostazione predefinita è di circa due ore. Se il client non risponde ai keep-alive del server, la connessione viene chiusa. Quando tutte le connessioni a un determinato processo client vengono chiuse, il server pulisce ed esegue gli handle di contesto in sospeso.

 

 




