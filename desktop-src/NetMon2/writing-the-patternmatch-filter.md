---
description: Il filtro di corrispondenza dei criteri di ricerca notifica al driver di accettare i frame con un modello specifico in corrispondenza di un offset specifico.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Scrittura del filtro PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310779"
---
# <a name="writing-the-patternmatch-filter"></a><span data-ttu-id="910b6-103">Scrittura del filtro PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="910b6-103">Writing the PATTERNMATCH Filter</span></span>

<span data-ttu-id="910b6-104">Il filtro di corrispondenza dei criteri di ricerca notifica al driver di accettare i frame con un modello specifico in corrispondenza di un offset specifico.</span><span class="sxs-lookup"><span data-stu-id="910b6-104">The pattern match filter notifies the driver to accept frames that have a specific pattern at a specific offset.</span></span> <span data-ttu-id="910b6-105">È possibile specificare un massimo di quattro corrispondenze dettagliate, che possono essere combinate in istruzioni AND o OR logiche per la valutazione del driver Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="910b6-105">You can specify a maximum of four detailed pattern matches, which can be combined in logical AND or OR statements for Network Monitor driver evaluation.</span></span>

<span data-ttu-id="910b6-106">Per implementare le corrispondenze dei criteri, usare le strutture di Network Monitor seguenti:</span><span class="sxs-lookup"><span data-stu-id="910b6-106">To implement pattern matches, use the following Network Monitor structures:</span></span>

-   [<span data-ttu-id="910b6-107">**ESPRESSIONE**</span><span class="sxs-lookup"><span data-stu-id="910b6-107">**EXPRESSION**</span></span>](expression.md)
-   [<span data-ttu-id="910b6-108">**ANDEXP**</span><span class="sxs-lookup"><span data-stu-id="910b6-108">**ANDEXP**</span></span>](andexp.md)
-   [<span data-ttu-id="910b6-109">**PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="910b6-109">**PATTERNMATCH**</span></span>](patternmatch.md)

<span data-ttu-id="910b6-110">Per valutare un'istruzione **o** , combinare due a quattro criteri corrisponde a una struttura [**ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3).</span><span class="sxs-lookup"><span data-stu-id="910b6-110">To evaluate an **OR** statement, combine two to four pattern matches an [**ANDEXP**](andexp.md) structure (PatternMatch1 \|\| PatternMatch2 \|\| PatternMatch3).</span></span> <span data-ttu-id="910b6-111">Per valutare un'istruzione AND, combinare una o quattro strutture **ANDEXP** e una struttura di [**espressioni**](expression.md) (AndExp1 && AndExp2).</span><span class="sxs-lookup"><span data-stu-id="910b6-111">To evaluate an AND statement, combine one to four **ANDEXP** structures and an [**EXPRESSION**](expression.md) structure (AndExp1 && AndExp2).</span></span>

## <a name="pattern-match-definitions"></a><span data-ttu-id="910b6-112">Definizioni delle corrispondenze dei criteri</span><span class="sxs-lookup"><span data-stu-id="910b6-112">Pattern Match Definitions</span></span>

<span data-ttu-id="910b6-113">Una singola corrispondenza di criteri è definita dalla struttura [**PATTERNMATCH**](patternmatch.md) .</span><span class="sxs-lookup"><span data-stu-id="910b6-113">A single pattern match is defined by the [**PATTERNMATCH**](patternmatch.md) structure.</span></span> <span data-ttu-id="910b6-114">Una singola corrispondenza può funzionare in due modi.</span><span class="sxs-lookup"><span data-stu-id="910b6-114">An individual match can operate in one of two ways.</span></span>

<span data-ttu-id="910b6-115">In genere, il driver prenderà la base di offset, che può essere OFFSET di \_ base \_ rispetto \_ a \_ frame, offset di base \_ \_ rispetto \_ al \_ \_ protocollo effettivo, offset \_ \_ di base rispetto \_ a \_ IPX o offset \_ \_ rispetto \_ a IP, \_ e iniziare a contare in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="910b6-115">Normally, the driver will take the offset basis (which can be OFFSET\_BASIS\_RELATIVE\_TO\_FRAME, OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL, OFFSET\_BASIS\_RELATIVE\_TO\_IPX, or OFFSET\_BASIS\_RELATIVE\_TO\_IP) and start counting there.</span></span> <span data-ttu-id="910b6-116">Il driver conteggia i byte di offset da tale posizione e quindi corrisponde ai dati trovati con i primi byte di lunghezza in **PatternToMatch**.</span><span class="sxs-lookup"><span data-stu-id="910b6-116">The driver will count offset bytes from there and then match the data it finds with the first length bytes in **PatternToMatch**.</span></span> <span data-ttu-id="910b6-117">Se sono uguali e i flag di corrispondenza criterio \_ \_ non sono \_ impostati, questo modello viene passato.</span><span class="sxs-lookup"><span data-stu-id="910b6-117">If they are the same, and the PATTERN\_MATCH\_FLAGS\_NOT flag is not set, then this pattern passes.</span></span> <span data-ttu-id="910b6-118">Se sono diversi e i flag di \_ corrispondenza dei criteri \_ non sono \_ stati impostati, il modello viene passato.</span><span class="sxs-lookup"><span data-stu-id="910b6-118">If they are different and the PATTERN\_MATCH\_FLAGS\_NOT has been set, the pattern passes.</span></span> <span data-ttu-id="910b6-119">In caso contrario, questo modello ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="910b6-119">Otherwise this pattern fails.</span></span>

<span data-ttu-id="910b6-120">Oppure:</span><span class="sxs-lookup"><span data-stu-id="910b6-120">Or:</span></span>

<span data-ttu-id="910b6-121">Se \_ \_ viene impostata la porta flag di corrispondenza dei flag \_ \_ specificata e la base è impostata su offset \_ rispetto \_ a \_ \_ IPX o offset \_ \_ rispetto \_ a \_ IP, il confronto è più complesso.</span><span class="sxs-lookup"><span data-stu-id="910b6-121">If the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag is set, and the basis is set to OFFSET\_BASIS\_RELATIVE\_TO\_IPX or OFFSET\_BASIS\_RELATIVE\_TO\_IP, the comparison is more complex.</span></span> <span data-ttu-id="910b6-122">Innanzitutto, il driver garantisce che il protocollo di base dell'offset sia presente, quindi il driver verifica che la porta specificata corrisponda alla porta nel frame.</span><span class="sxs-lookup"><span data-stu-id="910b6-122">First, the driver ensures that the offset basis protocol is there, then the driver verifies that the specified port matches the port in the frame.</span></span> <span data-ttu-id="910b6-123">Infine, il driver garantisce che il membro **PatternToMatch** corrisponda a quello precedente, con l'eccezione che l'offset è dalla fine di IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="910b6-123">Finally the driver ensures that the **PatternToMatch** member matches as before, with the exception that the offset is from the end of IP or IPX.</span></span> <span data-ttu-id="910b6-124">Si noti che se la base non è una di queste due, il \_ flag di corrispondenza dei flag della \_ \_ porta \_ specificata verrà ignorato e il modello verrà valutato come sopra.</span><span class="sxs-lookup"><span data-stu-id="910b6-124">Note that if the basis is not one of these two, then the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag will be ignored, and the pattern will be evaluated as above.</span></span>

<span data-ttu-id="910b6-125">Per valutare una corrispondenza con un solo criterio, una struttura di [**espressioni**](expression.md) deve avere un solo membro **AndExp** contenente un singolo criterio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="910b6-125">To evaluate a single pattern match, an [**EXPRESSION**](expression.md) structure must have one **AndExp** member containing a single pattern match.</span></span>

<span data-ttu-id="910b6-126">La creazione del filtro di corrispondenza dei criteri prevede la creazione di strutture [**PATTERNMATCH**](patternmatch.md) e la loro combinazione logica con le strutture [**Expression**](expression.md) e [**ANDEXP**](andexp.md) .</span><span class="sxs-lookup"><span data-stu-id="910b6-126">Building the pattern match filter involves creating [**PATTERNMATCH**](patternmatch.md) structures and logically combining them with [**EXPRESSION**](expression.md) and [**ANDEXP**](andexp.md) structures.</span></span>

<span data-ttu-id="910b6-127">**Per scrivere un filtro PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="910b6-127">**To write a PATTERNMATCH filter**</span></span>

1.  <span data-ttu-id="910b6-128">Nella struttura [**ANDEXP**](andexp.md) compilare la matrice con le corrispondenze dei criteri.</span><span class="sxs-lookup"><span data-stu-id="910b6-128">In the [**ANDEXP**](andexp.md) structure, populate the array with pattern matches.</span></span>
2.  <span data-ttu-id="910b6-129">Popola la struttura dell' [**espressione**](expression.md) con una matrice di membri **AndExp** .</span><span class="sxs-lookup"><span data-stu-id="910b6-129">Populate the [**EXPRESSION**](expression.md) structure with an array of **AndExp** members.</span></span>
3.  <span data-ttu-id="910b6-130">Non superare un totale di quattro corrispondenze del criterio per il filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="910b6-130">Do not exceed a total of four pattern matches for the capture filter.</span></span>
4.  <span data-ttu-id="910b6-131">Nella struttura [**PATTERNMATCH**](patternmatch.md) selezionare un tipo di flag.</span><span class="sxs-lookup"><span data-stu-id="910b6-131">In the [**PATTERNMATCH**](patternmatch.md) structure, select a flag type.</span></span>
5.  <span data-ttu-id="910b6-132">Selezionare una base di offset.</span><span class="sxs-lookup"><span data-stu-id="910b6-132">Select an offset basis.</span></span>
6.  <span data-ttu-id="910b6-133">Enumerare un valore di porta.</span><span class="sxs-lookup"><span data-stu-id="910b6-133">Enumerate a port value.</span></span>
7.  <span data-ttu-id="910b6-134">Definire il valore di offset.</span><span class="sxs-lookup"><span data-stu-id="910b6-134">Define offset value.</span></span>
8.  <span data-ttu-id="910b6-135">Definire la lunghezza del modello.</span><span class="sxs-lookup"><span data-stu-id="910b6-135">Define the pattern length.</span></span>
9.  <span data-ttu-id="910b6-136">Enumerare il valore del modello.</span><span class="sxs-lookup"><span data-stu-id="910b6-136">Enumerate the pattern value.</span></span>

## <a name="patternmatch-examples"></a><span data-ttu-id="910b6-137">Esempi di PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="910b6-137">PATTERNMATCH Examples</span></span>

<span data-ttu-id="910b6-138">Questo frame rappresenta un offset standard.</span><span class="sxs-lookup"><span data-stu-id="910b6-138">This frame represents a standard offset.</span></span>

![frame offset standard](images/offs-pat.png)

<span data-ttu-id="910b6-140">Il frammento di codice viene implementato come segue:</span><span class="sxs-lookup"><span data-stu-id="910b6-140">The code fragment is implemented as:</span></span>

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

<span data-ttu-id="910b6-141">Questo frame raffigura un offset specificato dalla porta (rispetto a IPX).</span><span class="sxs-lookup"><span data-stu-id="910b6-141">This frame depicts a port-specified offset (against IPX).</span></span>

![frame offset specificato dalla porta](images/stan-pat.png)

<span data-ttu-id="910b6-143">Il codice di esempio viene implementato come segue:</span><span class="sxs-lookup"><span data-stu-id="910b6-143">The example code is implemented as:</span></span>

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



