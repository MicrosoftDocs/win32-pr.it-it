---
description: Questa sezione viene copiata da &\# 0034;IPv6 Addressing Architecture&\# 0034; by R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Rappresentazione testuale degli indirizzi IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d71ad1f98652a0f00e4f14f957bcedc27316444ceabc3e5c35ee2bcf81b5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733351"
---
# <a name="text-representation-of-ipv6-addresses"></a>Rappresentazione testuale degli indirizzi IPv6

Questa sezione viene copiata da "Architettura di indirizzamento IPv6" di R. Hinden e S. Deering. Esistono tre forme convenzionali per rappresentare gli indirizzi IPv6 come stringhe di testo:

-   Il formato preferito è x:x:x:x:x:x:x:x, dove "x" sono i valori esadecimali delle otto parti a 16 bit dell'indirizzo.

    Esempi:

    <dl> FEDC:BA98:7654:3210:FEDC:BA98:7654:3210  
    1080:0:0:0:8:800:200C:417A  
    </dl>

> [!Note]  
> Non è necessario scrivere gli zeri iniziali in un singolo campo, ma deve essere presente almeno un numero in ogni campo (ad eccezione del caso descritto nel secondo formato).

 

-   A causa del metodo di allocazione di determinati stili di indirizzi IPv6, è comune che gli indirizzi contengano stringhe lunghe di zero bit. Per semplificare la scrittura di indirizzi contenenti zero bit, è disponibile una sintassi speciale per comprimere gli zeri. L'uso dei due punti doppie ("::") indica più gruppi di 16 bit di zeri.

    Ad esempio, l'indirizzo multicast

    <dl> FF01:0:0:0:0:0:0:0:43  
    </dl>

    può essere rappresentato come:

    <dl> FF01::43  
    </dl>

    Le virgolette doppie ("::") possono essere visualizzate una sola volta in un indirizzo. Possono essere usati per comprimere gli zeri iniziali o finali in un indirizzo.

-   Un formato alternativo che può essere più pratico quando si lavora con un ambiente misto di nodi IPv4 e IPv6 è x:x:x:x:x:x:d.d.d.d.d, dove "x" sono i valori esadecimali dei sei elementi a 16 bit più alti dell'indirizzo e "d" sono i valori decimali delle quattro parti a 8 bit di basso ordine dell'indirizzo (rappresentazione standard IPv4).

    Esempi:

    <dl> 0:0:0:0:0:0:13.1.68.3  
    0:0:0:0:0:FFFF:129.144.52.38  
    </dl>

    o in formato compresso:

    <dl> ::13.1.68.3  
    ::FFFF:129.144.52.38  
    </dl>

 

 



