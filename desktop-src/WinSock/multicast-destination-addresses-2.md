---
description: Quando si invia a un indirizzo di destinazione multicast, il protocollo IPv6 Microsoft richiede in genere che all'applicazione sia specificata un'interfaccia in uscita.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: Indirizzi di destinazione multicast IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814411c89acc6eda759926f581066f939d4e9ac455e7d84789dbd9316c597a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822696"
---
# <a name="ipv6-multicast-destination-addresses"></a>Indirizzi di destinazione multicast IPv6

Quando si invia a un indirizzo di destinazione multicast, il protocollo IPv6 Microsoft richiede in genere che all'applicazione sia specificata un'interfaccia in uscita. Questa operazione viene eseguita con l'opzione del socket **\_ \_ IF MULTICAST IPV6** o associando il socket a un indirizzo di origine specifico.

È anche possibile specificare un'interfaccia predefinita per un indirizzo multicast specifico, un intero ambito di indirizzi multicast o tutti gli indirizzi multicast. Questa operazione viene eseguita con una route che inserisce il prefisso multicast sul collegamento all'interfaccia in uscita desiderata. Per gli esempi seguenti viene illustrato come è possibile specificare questa opzione:

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



