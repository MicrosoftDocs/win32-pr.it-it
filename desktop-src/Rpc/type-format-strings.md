---
title: Stringhe di formato del tipo
description: I caratteri di formato denotano gli oggetti di interesse per il motore NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045078"
---
# <a name="type-format-strings"></a><span data-ttu-id="33ead-103">Stringhe di formato del tipo</span><span class="sxs-lookup"><span data-stu-id="33ead-103">Type Format Strings</span></span>

<span data-ttu-id="33ead-104">I caratteri di formato denotano gli oggetti di interesse per il motore NDR.</span><span class="sxs-lookup"><span data-stu-id="33ead-104">Format characters denote objects of interest to the NDR engine.</span></span> <span data-ttu-id="33ead-105">È presente un carattere di formato per ogni tipo di base, per vari tipi complessi e per le descrizioni di puntatori, compressione, allineamento e altri oggetti esterni.</span><span class="sxs-lookup"><span data-stu-id="33ead-105">There is a format character for each basic type, for various complex types, and for descriptions of pointers, packing, alignment, and other miscellaneous objects.</span></span> <span data-ttu-id="33ead-106">Per i tipi composti, vengono riconosciute diverse categorie di strutture e matrici in base alle rispettive proprietà delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="33ead-106">For compound types, several categories of structures and arrays are recognized based on their performance properties.</span></span> <span data-ttu-id="33ead-107">Una stringa di formato per ogni categoria inizia con un token FC che identifica la stringa di formato particolare.</span><span class="sxs-lookup"><span data-stu-id="33ead-107">A format string for each category starts with an FC token identifying the particular format string.</span></span> <span data-ttu-id="33ead-108">I caratteri di formato per le categorie di strutture e matrici possono condividere le correzioni in nel nome del token FC principale mostrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="33ead-108">Format characters for structures and arrays categories may share the in-fixes in the name of the leading FC token shown in the following table.</span></span>



| <span data-ttu-id="33ead-109">Formato carattere</span><span class="sxs-lookup"><span data-stu-id="33ead-109">Format character</span></span> | <span data-ttu-id="33ead-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33ead-110">Description</span></span>                                    |
|------------------|------------------------------------------------|
| <span data-ttu-id="33ead-111">C</span><span class="sxs-lookup"><span data-stu-id="33ead-111">C</span></span>                | <span data-ttu-id="33ead-112">Indica le informazioni di conformità nel tipo.</span><span class="sxs-lookup"><span data-stu-id="33ead-112">Indicates conformance information in the type.</span></span> |
| <span data-ttu-id="33ead-113">V</span><span class="sxs-lookup"><span data-stu-id="33ead-113">V</span></span>                | <span data-ttu-id="33ead-114">Indica le informazioni sulla varianza nel tipo.</span><span class="sxs-lookup"><span data-stu-id="33ead-114">Indicates variance information in the type.</span></span>    |
| <span data-ttu-id="33ead-115">P</span><span class="sxs-lookup"><span data-stu-id="33ead-115">P</span></span>                | <span data-ttu-id="33ead-116">Indica che i puntatori fanno parte del tipo.</span><span class="sxs-lookup"><span data-stu-id="33ead-116">Indicates pointers are a part of the type.</span></span>     |



 

<span data-ttu-id="33ead-117">Ad esempio, FC \_ CSTRUCT e FC \_ CArray identificano rispettivamente la struttura conforme e i descrittori di matrici conformi.</span><span class="sxs-lookup"><span data-stu-id="33ead-117">For example, FC\_CSTRUCT and FC\_CARRAY identify the conformant structure and conformant array descriptors, respectively.</span></span>

<span data-ttu-id="33ead-118">Di seguito sono riportati i caratteri di formato con significati speciali.</span><span class="sxs-lookup"><span data-stu-id="33ead-118">The following are format characters with special meanings.</span></span>



| <span data-ttu-id="33ead-119">Formato carattere</span><span class="sxs-lookup"><span data-stu-id="33ead-119">Format character</span></span> | <span data-ttu-id="33ead-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33ead-120">Description</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33ead-121">\_PP FC</span><span class="sxs-lookup"><span data-stu-id="33ead-121">FC\_PP</span></span>           | <span data-ttu-id="33ead-122">Indica l'inizio della sezione della descrizione del puntatore di una struttura o di una matrice.</span><span class="sxs-lookup"><span data-stu-id="33ead-122">Indicates the beginning of the pointer description section of a structure or array.</span></span> |



 

<span data-ttu-id="33ead-123">Le stringhe di formato di tipo NDR RPC sono descritte in modo più dettagliato negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="33ead-123">RPC NDR type format strings are described in more detail in the following topics:</span></span>

-   [<span data-ttu-id="33ead-124">Tipi semplici</span><span class="sxs-lookup"><span data-stu-id="33ead-124">Simple Types</span></span>](simple-types-tfs.md)
-   [<span data-ttu-id="33ead-125">Pointers</span><span class="sxs-lookup"><span data-stu-id="33ead-125">Pointers</span></span>](pointers-tfs.md)
-   [<span data-ttu-id="33ead-126">Matrici</span><span class="sxs-lookup"><span data-stu-id="33ead-126">Arrays</span></span>](arrays-tfs.md)
-   [<span data-ttu-id="33ead-127">Stringhe</span><span class="sxs-lookup"><span data-stu-id="33ead-127">Strings</span></span>](strings-tfs.md)
-   [<span data-ttu-id="33ead-128">Descrittori di correlazione</span><span class="sxs-lookup"><span data-stu-id="33ead-128">Correlation Descriptors</span></span>](correlation-descriptors-tfs.md)
-   [<span data-ttu-id="33ead-129">Strutture</span><span class="sxs-lookup"><span data-stu-id="33ead-129">Structures</span></span>](structures-tfs.md)
-   [<span data-ttu-id="33ead-130">Layout puntatore</span><span class="sxs-lookup"><span data-stu-id="33ead-130">Pointer Layout</span></span>](pointer-layout-tfs.md)
-   [<span data-ttu-id="33ead-131">Unioni</span><span class="sxs-lookup"><span data-stu-id="33ead-131">Unions</span></span>](unions-tfs.md)
-   [<span data-ttu-id="33ead-132">Trasmettere \_ come e rappresentare \_ come</span><span class="sxs-lookup"><span data-stu-id="33ead-132">Transmit\_as and Represent\_as</span></span>](transmit-as-and-represent-as-tfs.md)
-   [<span data-ttu-id="33ead-133">Marshalling utente</span><span class="sxs-lookup"><span data-stu-id="33ead-133">User-marshal</span></span>](user-marshal-tfs.md)

 

 




