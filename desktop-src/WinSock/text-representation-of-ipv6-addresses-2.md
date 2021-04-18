---
description: Questa sezione viene copiata da &\# 0034; architettura di indirizzamento IPv6&\# 0034; da R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Rappresentazione testuale degli indirizzi IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310416"
---
# <a name="text-representation-of-ipv6-addresses"></a>Rappresentazione testuale degli indirizzi IPv6

Questa sezione viene copiata da "architettura di indirizzamento IPv6" di R. Hinden e S. Deering. Esistono tre moduli convenzionali per rappresentare gli indirizzi IPv6 come stringhe di testo:

-   Il formato preferito è x:x: x:x: x:x: x:x, dove "x" sono i valori esadecimali delle parti a 8 16 bit dell'indirizzo.

    Esempi:

    <dl> FEDC: BA98:7654:3210: FEDC: BA98:7654:3210  
    1080:0: 0:0: 8:800:200C: 417A  
    </dl>

> [!Note]  
> Non è necessario scrivere gli zeri iniziali in un singolo campo, ma deve essere presente almeno un numero in ogni campo (ad eccezione del caso descritto nella seconda forma).

 

-   A causa del metodo di allocazione di determinati stili di indirizzi IPv6, è normale che gli indirizzi contengano stringhe lunghe di zero bit. Per rendere più semplice la scrittura di indirizzi contenenti zero bit, è disponibile una sintassi speciale per comprimere gli zeri. L'uso di due punti ("::") indica più gruppi di 16 bit di zero.

    Ad esempio, l'indirizzo multicast

    <dl> FF01:0: 0:0: 0:0: 0:43  
    </dl>

    può essere rappresentato come:

    <dl> FF01:: 43  
    </dl>

    Le virgolette doppie ("::") possono essere visualizzate una sola volta in un indirizzo. Possono essere usati per comprimere gli zeri iniziali o finali in un indirizzo.

-   Una forma alternativa che può essere più utile quando si gestiscono un ambiente misto di nodi IPv4 e IPv6 è x:x: x:x: x:x: d. d. d. d, in cui i valori di "x" sono i valori esadecimali delle sei parti a 16 bit più importanti dell'indirizzo e i valori decimali delle quattro parti a 8 bit di ordine inferiore dell'indirizzo (rappresentazione IPv4 standard).

    Esempi:

    <dl> 0:0: 0:0: 0:0: 13.1.68.3  
    0:0: 0:0: 0: FFFF: 129.144.52.38  
    </dl>

    o in formato compresso:

    <dl> ::13.1.68.3  
    :: FFFF: 129.144.52.38  
    </dl>

 

 



