---
title: Stub
description: Lo stub, come il proxy, è costituito da una o più parti dell'interfaccia e da un gestore.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f182cd2d47eec18f129d53d57c283d54862660a126d2d9e171989695418b3a8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678427"
---
# <a name="stub"></a>Stub

Lo stub, come il proxy, è costituito da una o più parti dell'interfaccia e da un gestore. Ogni stub di interfaccia fornisce il codice per eseguire l'unmarshaling dei parametri e del codice che chiama una delle interfacce supportate dell'oggetto. Ogni stub fornisce anche un'interfaccia per la comunicazione interna. Il gestore stub tiene traccia degli stub di interfaccia disponibili.

Esistono tuttavia le differenze seguenti tra lo stub e il proxy:

-   La differenza più importante è che lo stub rappresenta il client nello spazio indirizzi dell'oggetto.
-   Lo stub non viene implementato come oggetto aggregato perché non è necessario che il client sia visualizzato come singola unità. ogni parte dello stub è un componente separato.
-   Gli stub di interfaccia sono privati anziché pubblici.
-   Gli stub di interfaccia [**implementano IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), non [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).
-   Invece di creare il pacchetto dei parametri di cui effettuare il marshalling, lo stub li decompackagea dopo che sono stati sottoposti a marshalling e quindi esegue il pacchetto della risposta.

## <a name="structure-of-the-stub"></a>Struttura dello stub

Il diagramma seguente illustra la struttura dello stub. Ogni stub di interfaccia è connesso a un'interfaccia nell'oggetto . Il canale invia i messaggi in arrivo al stub di interfaccia appropriato. Tutti i componenti conversano con il canale tramite [**IRpcChannelBuffer,**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer)l'interfaccia che fornisce l'accesso alla libreria di runtime RPC.

![Screenshot che mostra la struttura dello stub.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Comunicazione tra oggetti](inter-object-communication.md)
</dt> <dt>

[Dettagli del marshalling](marshaling-details.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> </dl>

 

 