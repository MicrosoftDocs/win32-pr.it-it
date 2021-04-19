---
title: Stub
description: Lo stub, come il proxy, è costituito da una o più parti dell'interfaccia e da un responsabile.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320194"
---
# <a name="stub"></a>Stub

Lo stub, come il proxy, è costituito da una o più parti dell'interfaccia e da un responsabile. Ogni stub di interfaccia fornisce codice per l'unmarshalling dei parametri e del codice che chiama una delle interfacce supportate dall'oggetto. Ogni stub fornisce anche un'interfaccia per la comunicazione interna. Il gestore Stub tiene traccia degli stub di interfaccia disponibili.

Esistono, tuttavia, le differenze seguenti tra lo stub e il proxy:

-   La differenza più importante è che lo stub rappresenta il client nello spazio degli indirizzi dell'oggetto.
-   Lo stub non è implementato come oggetto aggregato perché non è necessario che il client venga visualizzato come una singola unità. ogni parte nello stub è un componente separato.
-   Gli stub di interfaccia sono privati anziché pubblici.
-   Gli stub di interfaccia implementano [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), non [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).
-   Anziché creare il marshalling dei parametri, lo stub li rimuove dal pacchetto dopo che è stato eseguito il marshalling e quindi crea il pacchetto della risposta.

## <a name="structure-of-the-stub"></a>Struttura dello stub

Nel diagramma seguente viene illustrata la struttura dello stub. Ogni stub di interfaccia è connesso a un'interfaccia nell'oggetto. Il canale invia i messaggi in ingresso allo stub di interfaccia appropriato. Tutti i componenti comunicano con il canale tramite [**Metodo IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), l'interfaccia che fornisce l'accesso alla libreria di runtime RPC.

![Screenshot che mostra la struttura dello stub.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Comunicazione tra oggetti](inter-object-communication.md)
</dt> <dt>

[Dettagli del marshalling](marshaling-details.md)
</dt> <dt>

[RPC Microsoft](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> </dl>

 

 