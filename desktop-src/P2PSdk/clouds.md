---
description: I cloud vengono usati dalle infrastrutture di raggruppamento e grafi peer.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5ecbeee1f5b69d120c5f351f8a5bb200b6e3e5f60e4bacca5a4f5484f402dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932693"
---
# <a name="clouds"></a>Cloud

I cloud vengono usati dalle infrastrutture [di raggruppamento e](grouping-api.md) [grafi](graphing-api.md) peer. Il [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifica un cloud come un set di peer che possono comunicare all'interno dello stesso ambito IPv6. I cloud sono strettamente correlati agli ambiti IPv6. L'elenco seguente identifica alcune delle funzionalità cloud univoche:

-   Un cloud è identificato da un nome e i cloud disponibili possono essere enumerati usando [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).
-   Se un computer è connesso a Internet, fa parte di un cloud globale, identificato dalla stringa \_ "Global".
-   Se un computer è connesso a una o più reti locali (LAN), sono disponibili singoli cloud per ogni collegamento.
-   Un computer può essere connesso a molte reti con più schede di rete o usando una rete privata virtuale (VPN), il che significa che un computer con una sola interfaccia può essere visibile in molti cloud.
-   È possibile usare PNRP per registrare e risolvere i nomi di peer in un cloud specifico.

 

 



