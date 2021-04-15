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
# <a name="ipv6-multicast-destination-addresses"></a><span data-ttu-id="106a6-103">Indirizzi di destinazione multicast IPv6</span><span class="sxs-lookup"><span data-stu-id="106a6-103">IPv6 Multicast Destination Addresses</span></span>

<span data-ttu-id="106a6-104">Quando si invia a un indirizzo di destinazione multicast, il protocollo IPv6 Microsoft richiede in genere che l'applicazione disponga di un'interfaccia in uscita specificata.</span><span class="sxs-lookup"><span data-stu-id="106a6-104">When sending to a multicast destination address, the Microsoft IPv6 protocol normally requires that the application have an outgoing interface specified.</span></span> <span data-ttu-id="106a6-105">Questa operazione viene eseguita con l'opzione del socket **IPv6 \_ multicast \_ if** o associando il socket a un indirizzo di origine specifico.</span><span class="sxs-lookup"><span data-stu-id="106a6-105">This is done with the **IPV6\_MULTICAST\_IF** socket option or by binding the socket to a specific source address.</span></span>

<span data-ttu-id="106a6-106">È inoltre possibile specificare un'interfaccia predefinita per un indirizzo multicast specifico, un intero ambito di indirizzi multicast o tutti gli indirizzi multicast.</span><span class="sxs-lookup"><span data-stu-id="106a6-106">You can also specify a default interface for a specific multicast address, an entire multicast address scope, or all multicast addresses.</span></span> <span data-ttu-id="106a6-107">Questa operazione viene eseguita con una route che inserisce il prefisso multicast on-link all'interfaccia in uscita desiderata.</span><span class="sxs-lookup"><span data-stu-id="106a6-107">This is done with a route that places the multicast prefix on-link to the desired outgoing interface.</span></span> <span data-ttu-id="106a6-108">Per gli esempi seguenti viene illustrato come è possibile specificare questo:</span><span class="sxs-lookup"><span data-stu-id="106a6-108">For following examples show how this can be specified:</span></span>

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



