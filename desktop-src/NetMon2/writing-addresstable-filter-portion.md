---
description: Il filtro indirizzi invia una notifica al driver Network Monitor per accettare i frame con una varietà di tipi di indirizzi MAC specificati (Ethernet, token ring e FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Scrittura della parte di filtro ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317748"
---
# <a name="writing-addresstable-filter-portion"></a><span data-ttu-id="d4e26-103">Scrittura della parte di filtro ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="d4e26-103">Writing ADDRESSTABLE Filter Portion</span></span>

<span data-ttu-id="d4e26-104">Il filtro indirizzi invia una notifica al driver Network Monitor per accettare i frame con una varietà di tipi di indirizzi MAC specificati (Ethernet, token ring e FDDI).</span><span class="sxs-lookup"><span data-stu-id="d4e26-104">The address filter notifies the Network Monitor driver to accept frames that have one of a variety of specified MAC address types (Ethernet, Token Ring, and FDDI).</span></span> <span data-ttu-id="d4e26-105">È possibile specificare un massimo di otto coppie di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="d4e26-105">You can specify a maximum of eight address pairs.</span></span> <span data-ttu-id="d4e26-106">Una coppia di indirizzi può specificare un'origine, una destinazione, entrambe o nessuna delle due.</span><span class="sxs-lookup"><span data-stu-id="d4e26-106">An address pair can specify a source, a destination, both, or neither.</span></span>

<span data-ttu-id="d4e26-107">La parte relativa all'indirizzo del filtro è costituita da due strutture: [**ADDRESSTABLE**](addresstable.md) e [**ADDRESSPAIR**](addresspair.md).</span><span class="sxs-lookup"><span data-stu-id="d4e26-107">The address portion of the filter consists of two structures: [**ADDRESSTABLE**](addresstable.md) and [**ADDRESSPAIR**](addresspair.md).</span></span>

<span data-ttu-id="d4e26-108">Se non si specifica alcun indirizzo, tutti i frame passeranno il filtro degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="d4e26-108">If you specify NO addresses, then ALL frames will pass the address filter.</span></span> <span data-ttu-id="d4e26-109">Tuttavia, se si specificano indirizzi, verranno superati solo i frame che passano il filtro di indirizzi specificato.</span><span class="sxs-lookup"><span data-stu-id="d4e26-109">However, if you specify any addresses, only those frames that pass the given address filter will pass.</span></span>

<span data-ttu-id="d4e26-110">La compilazione del filtro degli indirizzi comporta l'allocazione di una struttura [**ADDRESSTABLE**](addresstable.md) e la compilazione di membri della struttura [**ADDRESSPAIR**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e26-110">Building the address filter involves allocating an [**ADDRESSTABLE**](addresstable.md) structure and filling in members of the [**ADDRESSPAIR**](addresspair.md) structure.</span></span>

<span data-ttu-id="d4e26-111">**Per compilare la parte relativa all'indirizzo di un filtro di acquisizione**</span><span class="sxs-lookup"><span data-stu-id="d4e26-111">**To build the address portion of a capture filter**</span></span>

1.  <span data-ttu-id="d4e26-112">Usare il flag **capturefilter \_ flags \_ Local \_ only** della struttura [**capturefilter**](capturefilter.md) per limitare l'acquisizione al traffico da e verso il computer locale.</span><span class="sxs-lookup"><span data-stu-id="d4e26-112">Use the **CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY** flag of the [**CAPTUREFILTER**](capturefilter.md) structure to restrict the capture to traffic to and from your local computer.</span></span>

    <span data-ttu-id="d4e26-113">Impostando questo flag, la scheda di interfaccia di rete non verrà impostata su modalità promiscua; il file di acquisizione acquisirà solo il traffico locale.</span><span class="sxs-lookup"><span data-stu-id="d4e26-113">Setting this flag will not set the NIC to promiscuous mode; the capture file will capture only local traffic.</span></span>

2.  <span data-ttu-id="d4e26-114">Usare il codice di esempio seguente per definire la struttura [**ADDRESSTABLE**](addresstable.md) :</span><span class="sxs-lookup"><span data-stu-id="d4e26-114">Use the following example code to define the [**ADDRESSTABLE**](addresstable.md) structure:</span></span>

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  <span data-ttu-id="d4e26-115">Usare le informazioni elencate nella tabella seguente per selezionare un tipo di flag [**ADDRESSPAIR**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e26-115">Use the information, listed in the following table, to select an [**ADDRESSPAIR**](addresspair.md) flag type.</span></span> 

    | <span data-ttu-id="d4e26-116">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="d4e26-116">Flag</span></span>                             | <span data-ttu-id="d4e26-117">Significato</span><span class="sxs-lookup"><span data-stu-id="d4e26-117">Meaning</span></span>                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="d4e26-118">flag di indirizzo \_ \_ corrispondenti all' \_ ora legale</span><span class="sxs-lookup"><span data-stu-id="d4e26-118">ADDRESS\_FLAGS\_MATCH\_DST</span></span>       | <span data-ttu-id="d4e26-119">Corrisponde a un indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4e26-119">Matches a destination address.</span></span>                                                        |
    | <span data-ttu-id="d4e26-120">flag di indirizzo \_ \_ corrispondenti a \_ src</span><span class="sxs-lookup"><span data-stu-id="d4e26-120">ADDRESS\_FLAGS\_MATCH\_SRC</span></span>       | <span data-ttu-id="d4e26-121">Corrisponde a un indirizzo di origine</span><span class="sxs-lookup"><span data-stu-id="d4e26-121">Matches a source address</span></span>                                                              |
    | <span data-ttu-id="d4e26-122">\_Escludi flag di indirizzo \_</span><span class="sxs-lookup"><span data-stu-id="d4e26-122">ADDRESS\_FLAGS\_EXCLUDE</span></span>          | <span data-ttu-id="d4e26-123">Esclude il frame se l'indirizzo viene trovato, ovvero un'origine o una destinazione definita.</span><span class="sxs-lookup"><span data-stu-id="d4e26-123">Excludes the frame if this address is found (either a defined source or destination).</span></span> |
    | <span data-ttu-id="d4e26-124">INDIRIZZI \_ flag \_ del \_ gruppo \_ di indirizzi DST</span><span class="sxs-lookup"><span data-stu-id="d4e26-124">ADDRESS\_FLAGS\_DST\_GROUP\_ADDR</span></span> | <span data-ttu-id="d4e26-125">Corrisponde al bit del gruppo (dell'indirizzo di destinazione) solo per i messaggi di tipo broadcast.</span><span class="sxs-lookup"><span data-stu-id="d4e26-125">Matches group bit (of the destination address) only for broadcast-type messages.</span></span>      |
    | <span data-ttu-id="d4e26-126">i \_ flag di indirizzo \_ corrispondono a \_ entrambi</span><span class="sxs-lookup"><span data-stu-id="d4e26-126">ADDRESS\_FLAGS\_MATCH\_BOTH</span></span>      | <span data-ttu-id="d4e26-127">Corrisponde a entrambi gli indirizzi di destinazione e di origine.</span><span class="sxs-lookup"><span data-stu-id="d4e26-127">Matches both the destination and source addresses.</span></span>                                    |

    

     

4.  <span data-ttu-id="d4e26-128">Compilare un indirizzo di destinazione, che viene valutato rispetto al flag [**ADDRESSPAIR**](addresspair.md) selezionato.</span><span class="sxs-lookup"><span data-stu-id="d4e26-128">Fill in a destination address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
5.  <span data-ttu-id="d4e26-129">Compilare un indirizzo di origine, che viene valutato rispetto al flag [**ADDRESSPAIR**](addresspair.md) selezionato.</span><span class="sxs-lookup"><span data-stu-id="d4e26-129">Fill in a source address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
6.  <span data-ttu-id="d4e26-130">Popolare la struttura [**ADDRESSTABLE**](addresstable.md) con una matrice di strutture [**ADDRESSPAIR**](addresspair.md) , che include le coppie di indirizzi valutate dal driver.</span><span class="sxs-lookup"><span data-stu-id="d4e26-130">Populate the [**ADDRESSTABLE**](addresstable.md) structure with an array of [**ADDRESSPAIR**](addresspair.md) structures, which includes the address pairs that the driver evaluates.</span></span> <span data-ttu-id="d4e26-131">Tutte le coppie di indirizzi vengono valutate come un'istruzione OR logica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2).</span><span class="sxs-lookup"><span data-stu-id="d4e26-131">All address pairs are evaluated as a logical OR statement (ADDRESSPAIR 1 \|\| ADDRESSPAIR 2).</span></span> <span data-ttu-id="d4e26-132">È possibile includere un massimo di otto coppie di indirizzi in un filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d4e26-132">You can include a maximum of eight address pairs in a capture filter.</span></span>

 

 



