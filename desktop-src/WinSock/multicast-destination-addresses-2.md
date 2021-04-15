---
description: Quando si invia a un indirizzo di destinazione multicast, il protocollo IPv6 Microsoft richiede in genere che l'applicazione disponga di un'interfaccia in uscita specificata.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: Indirizzi di destinazione multicast IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484933"
---
# <a name="ipv6-multicast-destination-addresses"></a>Indirizzi di destinazione multicast IPv6

Quando si invia a un indirizzo di destinazione multicast, il protocollo IPv6 Microsoft richiede in genere che l'applicazione disponga di un'interfaccia in uscita specificata. Questa operazione viene eseguita con l'opzione del socket **IPv6 \_ multicast \_ if** o associando il socket a un indirizzo di origine specifico.

È inoltre possibile specificare un'interfaccia predefinita per un indirizzo multicast specifico, un intero ambito di indirizzi multicast o tutti gli indirizzi multicast. Questa operazione viene eseguita con una route che inserisce il prefisso multicast on-link all'interfaccia in uscita desiderata. Per gli esempi seguenti viene illustrato come è possibile specificare questo:

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



