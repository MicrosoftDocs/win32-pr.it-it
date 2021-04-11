---
description: I cloud vengono usati dalle infrastrutture di raggruppamento e Graphing peer.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131695"
---
# <a name="clouds"></a>Cloud

I cloud vengono usati dalle infrastrutture di [raggruppamento](grouping-api.md) e [Graphing](graphing-api.md) peer. Il [protocollo PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) identifica un cloud come un set di peer che possono comunicare nello stesso ambito IPv6. I cloud sono strettamente correlati agli ambiti IPv6. L'elenco seguente identifica alcune delle funzionalità cloud univoche:

-   Un cloud è identificato da un nome e i cloud disponibili possono essere enumerati usando [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).
-   Se un computer è connesso a Internet, fa parte di un cloud globale, identificato dalla stringa "globale \_ ".
-   Se un computer è connesso a una o più reti locali (LAN), per ogni collegamento sono disponibili singoli cloud.
-   Un computer può essere connesso a molte reti con più schede di rete o tramite una rete privata virtuale (VPN), il che significa che un computer con un'interfaccia può essere visibile in molti cloud.
-   È possibile usare PNRP per registrare e risolvere i nomi di peer in un cloud specifico.

 

 



