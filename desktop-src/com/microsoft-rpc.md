---
title: RPC Microsoft
description: RPC Microsoft
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707252"
---
# <a name="microsoft-rpc"></a>RPC Microsoft

Microsoft RPC è un modello per la programmazione in un ambiente di elaborazione distribuito. L'obiettivo di RPC è fornire la comunicazione trasparente, in modo che il client sembri comunicare direttamente con il server. L'implementazione di RPC di Microsoft è compatibile con la RPC Open Software Foundation (OSF) Distributed Computing Environment (DCE).

È possibile configurare RPC per l'utilizzo di uno o più trasporti, uno o più servizi dei nomi e uno o più server di sicurezza. Le interfacce a tali provider sono gestite da RPC. Poiché Microsoft RPC è progettato per funzionare con più provider, è possibile scegliere i provider che funzionano meglio per la rete. Il trasporto è responsabile della trasmissione dei dati attraverso la rete. Il servizio nome accetta un nome di oggetto, ad esempio un moniker, e ne trova la posizione sulla rete. Il server di sicurezza offre alle applicazioni la possibilità di negare l'accesso a utenti e/o gruppi specifici. Per informazioni più dettagliate sulla sicurezza delle applicazioni, vedere [regole di progettazione dell'interfaccia](interface-design-rules.md) .

Oltre alle librerie di runtime RPC, Microsoft RPC include il linguaggio di definizione dell'interfaccia (IDL) e il relativo compilatore. Sebbene il file IDL sia una parte standard di RPC, Microsoft lo ha migliorato per estendere le funzionalità per supportare interfacce COM personalizzate. Il compilatore Microsoft Interface Definition Language (MIDL) utilizza il file IDL che descrive l'interfaccia personalizzata per generare più file descritti in [compilazione e registrazione di una DLL proxy](building-and-registering-a-proxy-dll.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Comunicazione tra oggetti](inter-object-communication.md)
</dt> <dt>

[Dettagli del marshalling](marshaling-details.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 




