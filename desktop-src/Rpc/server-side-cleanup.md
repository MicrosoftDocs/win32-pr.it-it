---
title: Pulizia lato server
description: Pulizia lato server e RPC (Remote Procedure Call).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044973"
---
# <a name="server-side-cleanup"></a>Pulizia lato server

Si immagini lo scenario seguente:

Un client apre un handle di contesto e quindi interrompe o perde la connettività al server. In che modo il server rileva che il client ha avuto esito negativo e l'handle del contesto dovrebbe essere disattivato? Esistono due Sottoscenari: uno è che il client viene arrestato in modo ordinato. In tal caso, viene inviata una notifica al server che sta per essere arrestata e il server è in grado di eseguire la pulizia, incluse le esecuzioni del contesto. Se il client non viene arrestato in modo ordinato o non può inviare una notifica al server, il server utilizza keep alive per determinare se il client è ancora disponibile. Sul lato server, la funzione [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) non ha alcun effetto. Al contrario, il server usa l'impostazione globale per computer-Keep-Alive, che per impostazione predefinita è di circa due ore. Se il client non risponde alle Keep-Alive del server, la connessione viene chiusa. Quando tutte le connessioni a un determinato processo client vengono chiuse, il server pulisce ed esegue gli handle di contesto in attesa.

 

 




