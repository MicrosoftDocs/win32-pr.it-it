---
title: Proxy
description: Un proxy risiede nello spazio degli indirizzi del processo chiamante e funge da surrogato per l'oggetto remoto.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320187"
---
# <a name="proxy"></a>Proxy

Un proxy risiede nello spazio degli indirizzi del processo chiamante e funge da surrogato per l'oggetto remoto. Dal punto di vista dell'oggetto chiamante, il proxy è l'oggetto. In genere, il ruolo del proxy consiste nel creare un pacchetto dei parametri di interfaccia per le chiamate ai metodi nelle interfacce degli oggetti. Il proxy inserisce i parametri in un buffer dei messaggi e passa il buffer sul canale, che gestisce il trasporto tra i processi. Il proxy viene implementato come oggetto aggregato o composito. Contiene una parte di gestione fornita dal sistema denominata Proxy Manager e uno o più componenti specifici dell'interfaccia chiamati proxy di interfaccia. Il numero di proxy di interfaccia è uguale al numero di interfacce oggetto esposte a quel particolare client. Per il client che rispetta il modello a oggetti del componente, il proxy sembra essere l'oggetto reale.

> [!Note]  
> Con il marshalling personalizzato, il proxy può essere implementato in modo analogo o può comunicare direttamente con l'oggetto senza usare uno stub.

 

Ogni proxy di interfaccia è un oggetto Component che implementa il codice di marshalling per una delle interfacce dell'oggetto. Il proxy rappresenta l'oggetto per il quale viene fornito il codice di marshalling. Ogni proxy implementa anche l'interfaccia [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) . Sebbene l'interfaccia oggetto rappresentata dal proxy sia pubblica, l'implementazione di **IRpcProxyBuffer** è privata e viene utilizzata internamente all'interno del proxy. Gestione proxy tiene traccia dei proxy di interfaccia e contiene anche l'implementazione pubblica dell'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo per l'aggregazione. Ogni proxy di interfaccia può esistere in una DLL separata che viene caricata quando l'interfaccia supportata viene materializzata nel client.

## <a name="structure-of-the-proxy"></a>Struttura del proxy

Il diagramma seguente illustra la struttura di un proxy che supporta il marshalling standard di parametri appartenenti a due interfacce: IA1 e IA2. Ogni proxy di interfaccia implementa [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) per la comunicazione interna tra le parti aggregate. Quando il proxy è pronto a passare i parametri di cui è stato effettuato il marshalling attraverso il limite del processo, chiama i metodi nell'interfaccia [**Metodo IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) , implementata dal canale. Il canale, a sua volta, trasmette la chiamata alla libreria di runtime RPC per poter raggiungere la destinazione nell'oggetto.

![Diagramma che mostra la struttura del proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

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

[Stub](stub.md)
</dt> </dl>

 

 