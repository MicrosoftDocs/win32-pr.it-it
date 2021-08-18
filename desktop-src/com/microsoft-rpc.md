---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed515b1ca8e58e8e9daaa2bb037dbb9c33ad1d6bb15bd7dc42abd52771e8267a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130173"
---
# <a name="microsoft-rpc"></a>Microsoft RPC

Microsoft RPC è un modello per la programmazione in un ambiente di elaborazione distribuita. L'obiettivo di RPC è fornire una comunicazione trasparente in modo che il client sembra comunicare direttamente con il server. L'implementazione di RPC da parte di Microsoft è compatibile con LA RPC (Distributed Computing Environment) OSF (Open Software Foundation).

È possibile configurare RPC per l'utilizzo di uno o più trasporti, uno o più servizi dei nomi e uno o più server di sicurezza. Le interfacce per tali provider vengono gestite da RPC. Poiché RPC Microsoft è progettato per funzionare con più provider, è possibile scegliere i provider più adatta alla propria rete. Il trasporto è responsabile della trasmissione dei dati attraverso la rete. Il servizio dei nomi accetta un nome di oggetto, ad esempio un moniker, e ne trova la posizione nella rete. Il server di sicurezza offre alle applicazioni la possibilità di negare l'accesso a utenti e/o gruppi specifici. Per [informazioni più dettagliate sulla](interface-design-rules.md) sicurezza delle applicazioni, vedere Interface Design Rules (Regole di progettazione dell'interfaccia).

Oltre alle librerie di runtime RPC, Microsoft RPC include il linguaggio IDL (Interface Definition Language) e il relativo compilatore. Anche se il file IDL è una parte standard di RPC, Microsoft lo ha migliorato per estendere le funzionalità per supportare le interfacce COM personalizzate. Il compilatore Microsoft Interface Definition Language (MIDL) usa il file IDL che descrive l'interfaccia personalizzata per generare diversi file descritti in Compilazione e registrazione di [una DLL proxy.](building-and-registering-a-proxy-dll.md)

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

 

 




