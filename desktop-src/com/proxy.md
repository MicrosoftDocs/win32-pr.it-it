---
title: Proxy
description: Un proxy risiede nello spazio degli indirizzi del processo chiamante e funge da surrogato per l'oggetto remoto.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0478ce9ad1e08d343f1536fcd4bba63e59ae0fd229390be31c978bd20f737b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130008"
---
# <a name="proxy"></a>Proxy

Un proxy risiede nello spazio degli indirizzi del processo chiamante e funge da surrogato per l'oggetto remoto. Dal punto di vista dell'oggetto chiamante, il proxy è l'oggetto . In genere, il ruolo del proxy è quello di creare un pacchetto dei parametri dell'interfaccia per le chiamate ai metodi nelle relative interfacce oggetto. Il proxy inserirà i parametri in un buffer dei messaggi e lo passa al canale, che gestisce il trasporto tra i processi. Il proxy viene implementato come oggetto aggregato, o composito. Contiene un componente di gestione fornito dal sistema denominato gestione proxy e uno o più componenti specifici dell'interfaccia denominati proxy di interfaccia. Il numero di proxy di interfaccia è uguale al numero di interfacce oggetto esposte a quel particolare client. Per il client conforme al modello a oggetti del componente, il proxy sembra essere l'oggetto reale.

> [!Note]  
> Con il marshalling personalizzato, il proxy può essere implementato in modo analogo oppure può comunicare direttamente con l'oggetto senza usare uno stub.

 

Ogni proxy di interfaccia è un oggetto componente che implementa il codice di marshalling per una delle interfacce dell'oggetto. Il proxy rappresenta l'oggetto per il quale fornisce il codice di marshalling. Ogni proxy implementa anche [**l'interfaccia IRpcProxyBuffer.**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) Anche se l'interfaccia dell'oggetto rappresentata dal proxy è pubblica, **l'implementazione di IRpcProxyBuffer** è privata e viene usata internamente all'interno del proxy. La gestione proxy tiene traccia dei proxy di interfaccia e contiene anche l'implementazione pubblica [**dell'interfaccia IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo per l'aggregazione. Ogni proxy di interfaccia può esistere in una DLL separata che viene caricata quando l'interfaccia che supporta viene materializzata nel client.

## <a name="structure-of-the-proxy"></a>Struttura del proxy

Il diagramma seguente illustra la struttura di un proxy che supporta il marshalling standard dei parametri appartenenti a due interfacce: IA1 e IA2. Ogni proxy di interfaccia implementa [**IRpcProxyBuffer per**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) la comunicazione interna tra le parti di aggregazione. Quando il proxy è pronto a passare i parametri di cui è stato effettuato il marshalling attraverso il limite del processo, chiama i metodi [**nell'interfaccia IRpcChannelBuffer,**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) implementata dal canale. Il canale inoltra a sua volta la chiamata alla libreria di runtime RPC in modo che possa raggiungere la destinazione nell'oggetto .

![Diagramma che mostra la struttura del proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

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

[Stub](stub.md)
</dt> </dl>

 

 