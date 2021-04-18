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
# <a name="text-representation-of-ipv6-addresses"></a><span data-ttu-id="c634b-103">Rappresentazione testuale degli indirizzi IPv6</span><span class="sxs-lookup"><span data-stu-id="c634b-103">Text Representation of IPv6 Addresses</span></span>

<span data-ttu-id="c634b-104">Questa sezione viene copiata da "architettura di indirizzamento IPv6" di R. Hinden e S. Deering.</span><span class="sxs-lookup"><span data-stu-id="c634b-104">This section is copied from "IPv6 Addressing Architecture" by R. Hinden and S. Deering.</span></span> <span data-ttu-id="c634b-105">Esistono tre moduli convenzionali per rappresentare gli indirizzi IPv6 come stringhe di testo:</span><span class="sxs-lookup"><span data-stu-id="c634b-105">There are three conventional forms for representing IPv6 addresses as text strings:</span></span>

-   <span data-ttu-id="c634b-106">Il formato preferito è x:x: x:x: x:x: x:x, dove "x" sono i valori esadecimali delle parti a 8 16 bit dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="c634b-106">The preferred form is x:x:x:x:x:x:x:x, where the 'x's are the hexadecimal values of the eight 16-bit pieces of the address.</span></span>

    <span data-ttu-id="c634b-107">Esempi:</span><span class="sxs-lookup"><span data-stu-id="c634b-107">Examples:</span></span>

    <dl> <span data-ttu-id="c634b-108">FEDC: BA98:7654:3210: FEDC: BA98:7654:3210</span><span class="sxs-lookup"><span data-stu-id="c634b-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span></span>  
    <span data-ttu-id="c634b-109">1080:0: 0:0: 8:800:200C: 417A</span><span class="sxs-lookup"><span data-stu-id="c634b-109">1080:0:0:0:8:800:200C:417A</span></span>  
    </dl>

> [!Note]  
> <span data-ttu-id="c634b-110">Non è necessario scrivere gli zeri iniziali in un singolo campo, ma deve essere presente almeno un numero in ogni campo (ad eccezione del caso descritto nella seconda forma).</span><span class="sxs-lookup"><span data-stu-id="c634b-110">It is not necessary to write the leading zeros in an individual field, but there must be at least one numeral in every field (except for the case described in the second form).</span></span>

 

-   <span data-ttu-id="c634b-111">A causa del metodo di allocazione di determinati stili di indirizzi IPv6, è normale che gli indirizzi contengano stringhe lunghe di zero bit.</span><span class="sxs-lookup"><span data-stu-id="c634b-111">Due to the method of allocating certain styles of IPv6 addresses, it is common for addresses to contain long strings of zero bits.</span></span> <span data-ttu-id="c634b-112">Per rendere più semplice la scrittura di indirizzi contenenti zero bit, è disponibile una sintassi speciale per comprimere gli zeri.</span><span class="sxs-lookup"><span data-stu-id="c634b-112">In order to make writing addresses containing zero bits easier, a special syntax is available to compress the zeros.</span></span> <span data-ttu-id="c634b-113">L'uso di due punti ("::") indica più gruppi di 16 bit di zero.</span><span class="sxs-lookup"><span data-stu-id="c634b-113">The use of double colons ("::") indicates multiple groups of 16-bits of zeros.</span></span>

    <span data-ttu-id="c634b-114">Ad esempio, l'indirizzo multicast</span><span class="sxs-lookup"><span data-stu-id="c634b-114">For example, the multicast address</span></span>

    <dl> <span data-ttu-id="c634b-115">FF01:0: 0:0: 0:0: 0:43</span><span class="sxs-lookup"><span data-stu-id="c634b-115">FF01:0:0:0:0:0:0:43</span></span>  
    </dl>

    <span data-ttu-id="c634b-116">può essere rappresentato come:</span><span class="sxs-lookup"><span data-stu-id="c634b-116">may be represented as:</span></span>

    <dl> <span data-ttu-id="c634b-117">FF01:: 43</span><span class="sxs-lookup"><span data-stu-id="c634b-117">FF01::43</span></span>  
    </dl>

    <span data-ttu-id="c634b-118">Le virgolette doppie ("::") possono essere visualizzate una sola volta in un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="c634b-118">The double quotation marks ("::") can only appear once in an address.</span></span> <span data-ttu-id="c634b-119">Possono essere usati per comprimere gli zeri iniziali o finali in un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="c634b-119">They can be used to compress leading or trailing zeros in an address.</span></span>

-   <span data-ttu-id="c634b-120">Una forma alternativa che può essere più utile quando si gestiscono un ambiente misto di nodi IPv4 e IPv6 è x:x: x:x: x:x: d. d. d. d, in cui i valori di "x" sono i valori esadecimali delle sei parti a 16 bit più importanti dell'indirizzo e i valori decimali delle quattro parti a 8 bit di ordine inferiore dell'indirizzo (rappresentazione IPv4 standard).</span><span class="sxs-lookup"><span data-stu-id="c634b-120">An alternative form that may be more convenient when dealing with a mixed environment of IPv4 and IPv6 nodes is x:x:x:x:x:x:d.d.d.d, where the 'x's are the hexadecimal values of the six high-order 16-bit pieces of the address, and the 'd's are the decimal values of the four low-order 8-bit pieces of the address (standard IPv4 representation).</span></span>

    <span data-ttu-id="c634b-121">Esempi:</span><span class="sxs-lookup"><span data-stu-id="c634b-121">Examples:</span></span>

    <dl> <span data-ttu-id="c634b-122">0:0: 0:0: 0:0: 13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="c634b-122">0:0:0:0:0:0:13.1.68.3</span></span>  
    <span data-ttu-id="c634b-123">0:0: 0:0: 0: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="c634b-123">0:0:0:0:0:FFFF:129.144.52.38</span></span>  
    </dl>

    <span data-ttu-id="c634b-124">o in formato compresso:</span><span class="sxs-lookup"><span data-stu-id="c634b-124">or in compressed form:</span></span>

    <dl> <span data-ttu-id="c634b-125">::13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="c634b-125">::13.1.68.3</span></span>  
    <span data-ttu-id="c634b-126">:: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="c634b-126">::FFFF:129.144.52.38</span></span>  
    </dl>

 

 



