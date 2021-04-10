---
title: Transmit_as e Represent_as
description: Trasmettere \_ come e rappresentare \_ come condividono lo stesso layout ad eccezione del token principale. il token legge la \_ trasmissione FC \_ come o FC \_ rappresenta \_ come, ma il codice sottostante è comune.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963124"
---
# <a name="transmit_as-and-represent_as"></a><span data-ttu-id="8a5ed-103">Trasmettere \_ come e rappresentare \_ come</span><span class="sxs-lookup"><span data-stu-id="8a5ed-103">Transmit\_as and Represent\_as</span></span>

<span data-ttu-id="8a5ed-104">Trasmettere \_ come e rappresentare \_ come condividono lo stesso layout ad eccezione del token principale. il token legge la \_ trasmissione FC \_ come o FC \_ rappresenta \_ come, ma il codice sottostante è comune.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-104">Transmit\_as and represent\_as share the same layout except for the leading token; the token reads FC\_TRANSMIT\_AS or FC\_REPRESENT\_AS, but the underlying code is common.</span></span>

<span data-ttu-id="8a5ed-105">Il layout della descrizione è il seguente:</span><span class="sxs-lookup"><span data-stu-id="8a5ed-105">The description has the following layout:</span></span>

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

<span data-ttu-id="8a5ed-106">I flag<1> byte sono costituiti dal contrassegno superiore e dal bocconcino di allineamento inferiore.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-106">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="8a5ed-107">Il bocconcino di allineamento mantiene l'allineamento del tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-107">The alignment nibble keeps the wire alignment of the transmitted type.</span></span> <span data-ttu-id="8a5ed-108">Questa operazione è necessaria in caso di ridimensionamento del buffer e di utilizzo della dimensione del tipo trasmesso dal codice del formato.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-108">This is needed when buffer sizing and using the transmitted type size from the format code.</span></span>

<span data-ttu-id="8a5ed-109">Il flag rosicchia può includere i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a5ed-109">The flag nibble can have the following flags:</span></span>

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

<span data-ttu-id="8a5ed-110">Il \_ tipo presentato \_ è \_ flag di matrice contrassegna un argomento di trasmissione di primo livello (o rappresenta come) come una matrice di elementi e un valore passato per.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-110">The PRESENTED\_TYPE\_IS\_ARRAY flag marks a top-level transmit as (or represent as) argument being an array of something and passed-by value.</span></span> <span data-ttu-id="8a5ed-111">L'interprete [**-OI**](/windows/desktop/Midl/-oi) usa questo flag per eseguire un'istruzione/routine di questo tipo (che è in realtà un puntatore sullo stack, non sulla matrice).</span><span class="sxs-lookup"><span data-stu-id="8a5ed-111">The [**–Oi**](/windows/desktop/Midl/-oi) interpreter uses this flag to step over such an argument (which is actually a pointer on stack, not the array).</span></span> <span data-ttu-id="8a5ed-112">Gli altri due flag vengono usati anche solo negli interpreti precedenti per eseguire correttamente il passaggio a un tipo presentato nello stack.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-112">The other two flags are also used only in previous interpreters to step correctly over a presented type on the stack.</span></span>

<span data-ttu-id="8a5ed-113">L' \_ Indice quintupla<2> è un indice della routine di callback Quintupla (si tratta in realtà di una quadrupla) di funzioni.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-113">The quintuple\_index<2> is an index of the callback routine quintuple (this is actually a quadruple) of functions.</span></span> <span data-ttu-id="8a5ed-114">La tabella è comune sia per trasmettere come che per rappresentare come ed esiste un mapping ovvio per la posizione delle routine, in quanto lo stesso servizio punti di ingresso trasmette e rappresenta come codici.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-114">The table is common to both transmit as and represent as and there is an obvious mapping for the position of the routines, as the same entry points service transmit as and represent as codes.</span></span> <span data-ttu-id="8a5ed-115">Il mapping è da \_ local => a \_ Xmit, a \_ local => from \_ Xmit, Free \_ inst => Free \_ Xmit, Free \_ local => Free \_ inst.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-115">The mapping is from\_local => to\_xmit, to\_local => from\_xmit, free\_inst => free\_xmit, free\_local => free\_inst.</span></span>

<span data-ttu-id="8a5ed-116">La \_ \_ dimensione di memoria del tipo presentata \_<2> fornisce sempre una dimensione per il tipo presentato/locale, inclusi quelli sconosciuti come tipi.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-116">The presented\_type\_memory\_size<2> always provides a size for the presented/local type, including unknown represent as types.</span></span>

<span data-ttu-id="8a5ed-117">Le \_ dimensioni del buffer dei tipi trasmessi \_ \_<2> sono pari a zero, quando le dimensioni sono variabili o le dimensioni fisse effettive.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-117">The transmitted\_type\_buffer\_size<2> is either zero, when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="8a5ed-118">Si tratta di un'ottimizzazione che consente di ignorare alcuni callback durante il ridimensionamento del buffer.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-118">This is an optimization that enables skipping some callbacks when sizing the buffer.</span></span>

<span data-ttu-id="8a5ed-119">L' \_ offset del tipo trasmesso \_<2> è il consueto offset del tipo relativo alla stringa di formato del tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="8a5ed-119">The transmitted\_type\_offset<2> is the usual relative type offset to the transmitted type format string.</span></span>

 

 