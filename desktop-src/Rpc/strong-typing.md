---
title: Tipizzazione forte
description: C è un linguaggio debolmente tipizzato, ovvero il compilatore consente operazioni quali l'assegnazione e il confronto tra variabili di tipi diversi.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- RPC (Remote Procedure Call), descrizione, tipizzazione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955812"
---
# <a name="strong-typing"></a><span data-ttu-id="b83ea-104">Tipizzazione forte</span><span class="sxs-lookup"><span data-stu-id="b83ea-104">Strong Typing</span></span>

<span data-ttu-id="b83ea-105">C è un linguaggio debolmente tipizzato, ovvero il compilatore consente operazioni quali l'assegnazione e il confronto tra variabili di tipi diversi.</span><span class="sxs-lookup"><span data-stu-id="b83ea-105">C is a weakly typed language, that is, the compiler allows operations such as assignment and comparison among variables of different types.</span></span> <span data-ttu-id="b83ea-106">Ad esempio, C consente il cast del valore di una variabile a un altro tipo.</span><span class="sxs-lookup"><span data-stu-id="b83ea-106">For example, C allows the value of a variable to be cast to another type.</span></span> <span data-ttu-id="b83ea-107">La possibilità di usare variabili di tipi diversi nella stessa espressione promuove la flessibilità e l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="b83ea-107">The ability to use variables of different types in the same expression promotes flexibility as well as efficiency.</span></span>

<span data-ttu-id="b83ea-108">Un linguaggio fortemente tipizzato impone restrizioni sulle operazioni tra variabili di tipi diversi.</span><span class="sxs-lookup"><span data-stu-id="b83ea-108">A strongly typed language imposes restrictions on operations among variables of different types.</span></span> <span data-ttu-id="b83ea-109">In questi casi, il compilatore genera un errore che impedisce l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b83ea-109">In those cases, the compiler issues an error prohibiting the operation.</span></span> <span data-ttu-id="b83ea-110">Queste rigide linee guida relative ai tipi di dati sono progettate per evitare potenziali errori.</span><span class="sxs-lookup"><span data-stu-id="b83ea-110">These strict guidelines regarding data types are designed to avoid potential errors.</span></span>

<span data-ttu-id="b83ea-111">La difficoltà nell'utilizzo di un linguaggio con tipizzazione debole, ad esempio C, per le chiamate a procedure remote è che le applicazioni distribuite possono essere eseguite in più computer diversi con compilatori C diversi e architetture diverse.</span><span class="sxs-lookup"><span data-stu-id="b83ea-111">The difficulty with using a weakly typed language such as C for remote procedure calls is that distributed applications can run on several different computers with different C compilers and different architectures.</span></span> <span data-ttu-id="b83ea-112">Quando un'applicazione viene eseguita in un solo computer, non è necessario preoccuparsi del formato dati interno perché i dati vengono gestiti in modo coerente.</span><span class="sxs-lookup"><span data-stu-id="b83ea-112">When an application runs on only one computer, you don't have to be concerned with the internal data format because the data is handled in a consistent manner.</span></span> <span data-ttu-id="b83ea-113">Tuttavia, in un ambiente di elaborazione distribuita, computer diversi possono usare definizioni diverse per i tipi di dati di base.</span><span class="sxs-lookup"><span data-stu-id="b83ea-113">However, in a distributed computing environment, different computers can use different definitions for their base data types.</span></span> <span data-ttu-id="b83ea-114">Alcuni computer, ad esempio, definiscono il tipo **int** , quindi la rappresentazione interna è 16 bit, mentre altri computer utilizzano 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b83ea-114">For example, some computers define the **int** type, so its internal representation is 16 bits, while other computers use 32 bits.</span></span> <span data-ttu-id="b83ea-115">Un'architettura di computer, nota come "little endian", assegna il byte di dati meno significativo all'indirizzo di memoria più basso e il byte più significativo all'indirizzo più elevato.</span><span class="sxs-lookup"><span data-stu-id="b83ea-115">One computer architecture, known as "little endian," assigns the least significant byte of data to the lowest memory address and the most significant byte to the highest address.</span></span> <span data-ttu-id="b83ea-116">Un'altra architettura, nota come "big endian", assegna il byte meno significativo all'indirizzo di memoria massimo associato a tali dati.</span><span class="sxs-lookup"><span data-stu-id="b83ea-116">Another architecture, known as "big endian," assigns the least significant byte to the highest memory address associated with that data.</span></span>

<span data-ttu-id="b83ea-117">Le chiamate a procedure remote richiedono un controllo rigoroso sui tipi di parametro.</span><span class="sxs-lookup"><span data-stu-id="b83ea-117">Remote procedure calls require strict control over parameter types.</span></span> <span data-ttu-id="b83ea-118">Per gestire la trasmissione e la conversione dei dati in rete, MIDL impone rigorosamente restrizioni sui tipi per i dati trasferiti in rete.</span><span class="sxs-lookup"><span data-stu-id="b83ea-118">To handle data transmission and conversion over the network, MIDL strictly enforces type restrictions for data transferred over the network.</span></span> <span data-ttu-id="b83ea-119">Per questo motivo, MIDL include un set di [tipi di base](base-types.md)ben definiti.</span><span class="sxs-lookup"><span data-stu-id="b83ea-119">For this reason, MIDL includes a set of well-defined [base types](base-types.md).</span></span> <span data-ttu-id="b83ea-120">MIDL impone la tipizzazione forte imponendo l'uso di parole chiave che definiscono in modo univoco le dimensioni e il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="b83ea-120">MIDL enforces strong typing by mandating the use of keywords that unambiguously define the size and type of data.</span></span> <span data-ttu-id="b83ea-121">L'effetto più visibile della tipizzazione forte è che MIDL non consente le variabili del tipo **void \***.</span><span class="sxs-lookup"><span data-stu-id="b83ea-121">The most visible effect of strong typing is that MIDL does not allow variables of the type **void \***.</span></span>

<span data-ttu-id="b83ea-122">Negli argomenti seguenti, in questa sezione vengono illustrate le funzionalità del linguaggio MIDL che applicano la tipizzazione dei dati avanzata:</span><span class="sxs-lookup"><span data-stu-id="b83ea-122">In the following topics, this section discusses the MIDL language features that enforce strong data typing:</span></span>

-   [<span data-ttu-id="b83ea-123">Tipi di base</span><span class="sxs-lookup"><span data-stu-id="b83ea-123">Base Types</span></span>](base-types.md)
-   [<span data-ttu-id="b83ea-124">Tipi firmati e non firmati</span><span class="sxs-lookup"><span data-stu-id="b83ea-124">Signed and Unsigned Types</span></span>](signed-and-unsigned-types.md)
-   [<span data-ttu-id="b83ea-125">Tipi di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="b83ea-125">Wide-Character Types</span></span>](wide-character-types.md)
-   [<span data-ttu-id="b83ea-126">Strutture</span><span class="sxs-lookup"><span data-stu-id="b83ea-126">Structures</span></span>](structures.md)
-   [<span data-ttu-id="b83ea-127">Unioni</span><span class="sxs-lookup"><span data-stu-id="b83ea-127">Unions</span></span>](unions.md)
-   [<span data-ttu-id="b83ea-128">Tipi enumerati</span><span class="sxs-lookup"><span data-stu-id="b83ea-128">Enumerated Types</span></span>](enumerated-types.md)
-   [<span data-ttu-id="b83ea-129">Matrici</span><span class="sxs-lookup"><span data-stu-id="b83ea-129">Arrays</span></span>](arrays.md)
-   [<span data-ttu-id="b83ea-130">Attributi di funzione</span><span class="sxs-lookup"><span data-stu-id="b83ea-130">Function Attributes</span></span>](function-attributes.md)
-   [<span data-ttu-id="b83ea-131">Attributi di campo</span><span class="sxs-lookup"><span data-stu-id="b83ea-131">Field Attributes</span></span>](field-attributes.md)
-   [<span data-ttu-id="b83ea-132">Tre tipi di puntatore</span><span class="sxs-lookup"><span data-stu-id="b83ea-132">Three Pointer Types</span></span>](three-pointer-types.md)
-   [<span data-ttu-id="b83ea-133">Attributi di tipo</span><span class="sxs-lookup"><span data-stu-id="b83ea-133">Type Attributes</span></span>](type-attributes.md)

 

 




