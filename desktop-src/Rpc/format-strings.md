---
title: Stringhe di formato
description: Una stringa di formato è un token interpretato che il motore di rapporto di recapito riconosce. Le stringhe di formato sono spesso denominate MOPs; Questa documentazione usa il termine formato stringa in tutto.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711428"
---
# <a name="format-strings"></a><span data-ttu-id="2b3ec-104">Stringhe di formato</span><span class="sxs-lookup"><span data-stu-id="2b3ec-104">Format Strings</span></span>

<span data-ttu-id="2b3ec-105">Una stringa di formato è un token interpretato che il motore di rapporto di recapito riconosce.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-105">A format string is an interpreted token that the NDR engine understands.</span></span> <span data-ttu-id="2b3ec-106">Le stringhe di formato sono spesso denominate MOPs; Questa documentazione usa il termine formato stringa in tutto.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-106">Format strings are often referred to as MOPs; this documentation uses the term format string throughout.</span></span>

<span data-ttu-id="2b3ec-107">Per maggiore precisione, un carattere di formato è un singolo token interpretabile (Atomic).</span><span class="sxs-lookup"><span data-stu-id="2b3ec-107">To be more precise, a format character is an individual (atomic) interpretable token.</span></span> <span data-ttu-id="2b3ec-108">Ogni carattere di formato è di dimensioni pari a un byte.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-108">Each format character is one byte in size.</span></span> <span data-ttu-id="2b3ec-109">Una stringa di formato è una sequenza di caratteri di formato o caratteri di formato e dati numerici.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-109">A format string is a sequence of format characters or format characters and numerical data.</span></span> <span data-ttu-id="2b3ec-110">Il termine descrittore viene utilizzato anche per la denominazione di sequenze comuni; una stringa di formato di parametro o un descrittore di parametro è ad esempio una stringa di formato utilizzata per descrivere un parametro di una routine.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-110">The term descriptor is also used for naming common sequences; for example, a parameter format string or a parameter descriptor is a format string used to describe a parameter of a routine.</span></span>

<span data-ttu-id="2b3ec-111">I caratteri di formato presentano nomi simbolici suggestivi, ad esempio FC \_ Long o FC \_ struct.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-111">Format characters have suggestive symbolic names like FC\_LONG or FC\_STRUCT.</span></span> <span data-ttu-id="2b3ec-112">Tutti i caratteri stringa di formato usati da MIDL e dal motore NDR sono definiti nel file Ndrtypes. h.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-112">All format string characters used by MIDL and the NDR engine are defined in the Ndrtypes.h file.</span></span>

## <a name="format-string-tables"></a><span data-ttu-id="2b3ec-113">Formattare le tabelle di stringhe</span><span class="sxs-lookup"><span data-stu-id="2b3ec-113">Format String Tables</span></span>

<span data-ttu-id="2b3ec-114">Due tabelle di stringhe di formato primarie vengono usate dal motore: la tabella delle stringhe di formato della procedura, **\_ \_ MIDL \_ ProcFormatString**, che mantiene i descrittori di routine e la tabella di stringhe di formato del tipo, **\_ \_ MIDL \_ TypeFormatString**, che mantiene i descrittori del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-114">Two primary format string tables are used by the engine: the procedure format string table, **\_\_MIDL\_ProcFormatString**, that keeps the procedure descriptors; and the type format string table, **\_\_MIDL\_TypeFormatString**, that keeps the data type descriptors.</span></span> <span data-ttu-id="2b3ec-115">Il compilatore genera entrambi i file stub principali ( \* \_ c. c, \* \_ s. c, \* \_ p. c).</span><span class="sxs-lookup"><span data-stu-id="2b3ec-115">The compiler generates both into the main stub files (\*\_c.c, \*\_s.c, \*\_p.c).</span></span> <span data-ttu-id="2b3ec-116">La tabella delle stringhe di formato delle procedure viene utilizzata principalmente da diversi interpreti, ma viene utilizzata anche per la conversione del buffer indipendentemente dalla modalità del compilatore.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-116">The procedure format string table is used mostly by various interpreters but it is also used for the buffer conversion regardless of the compiler mode.</span></span> <span data-ttu-id="2b3ec-117">La tabella delle stringhe di formato del tipo viene utilizzata quando si chiama il motore di recapito di base per indicare tipi di dati specifici su cui lavorare.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-117">The type format string table is used when calling the core NDR engine to indicate specific data types to be worked on.</span></span>

## <a name="format-string-notation"></a><span data-ttu-id="2b3ec-118">Notazione stringa di formato</span><span class="sxs-lookup"><span data-stu-id="2b3ec-118">Format String Notation</span></span>

<span data-ttu-id="2b3ec-119">La notazione utilizzata in questo documento segue le linee guida comuni per la descrizione della programmazione, con una barra ( \| ) utilizzata per indicare costrutti alternativi e parentesi quadre ( \[ \] ) utilizzati per indicare gli elementi facoltativi.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-119">The notation used in this document follows common programming description guidelines, with a bar ( \| ) used to denote alternative constructs and square brackets ( \[ \] ) used to indicate optional elements.</span></span> <span data-ttu-id="2b3ec-120">Le stringhe di formato vengono spesso impilate per migliorare la leggibilità (responsabilità).</span><span class="sxs-lookup"><span data-stu-id="2b3ec-120">Format strings are frequently stacked up for readability (accountability).</span></span> <span data-ttu-id="2b3ec-121">In questo documento FC indica un singolo carattere di formato.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-121">Throughout this document, FC denotes a single format character.</span></span> <span data-ttu-id="2b3ec-122">I caratteri di formato vengono presentati in tutte le MAIUSCOLe, usando i nomi simbolici effettivi.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-122">Format characters are presented in all CAPS, using their actual symbolic names.</span></span> <span data-ttu-id="2b3ec-123">Altri campi arbitrari sono rappresentati da un nome e da una dimensione.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-123">Other arbitrary fields are represented by a name and a size.</span></span>

<span data-ttu-id="2b3ec-124">Le parentesi angolari ( <> ) vengono utilizzate per indicare le dimensioni dei descrittori.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-124">Angle brackets ( <> ) are used to denote sizes of the descriptors.</span></span> <span data-ttu-id="2b3ec-125">Vengono utilizzate le convenzioni illustrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-125">The conventions shown in the following table are employed.</span></span>



| <span data-ttu-id="2b3ec-126">Notation</span><span class="sxs-lookup"><span data-stu-id="2b3ec-126">Notation</span></span>     | <span data-ttu-id="2b3ec-127">Significato</span><span class="sxs-lookup"><span data-stu-id="2b3ec-127">Meaning</span></span>                                                   |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="2b3ec-128"><*n*></span><span class="sxs-lookup"><span data-stu-id="2b3ec-128"><*n*></span></span>  | <span data-ttu-id="2b3ec-129">Le dimensioni del descrittore sono pari a n byte.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-129">The size of descriptor is n bytes.</span></span>                        |
| <>     | <span data-ttu-id="2b3ec-130">Le dimensioni del descrittore variano.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-130">The size of descriptor varies.</span></span>                            |
| <span data-ttu-id="2b3ec-131">{<>}\*</span><span class="sxs-lookup"><span data-stu-id="2b3ec-131">{<>}\*</span></span> | <span data-ttu-id="2b3ec-132">Il descrittore viene ripetuto per un numero qualsiasi di volte (0, 1, 2...).</span><span class="sxs-lookup"><span data-stu-id="2b3ec-132">The descriptor is repeated any number of times (0,1,2 …).</span></span> |



 

<span data-ttu-id="2b3ec-133">I caratteri di formato seguenti hanno un significato speciale.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-133">The following format characters have a special meaning.</span></span>



| <span data-ttu-id="2b3ec-134">Carattere</span><span class="sxs-lookup"><span data-stu-id="2b3ec-134">Character</span></span> | <span data-ttu-id="2b3ec-135">Significato</span><span class="sxs-lookup"><span data-stu-id="2b3ec-135">Meaning</span></span>                                   |
|-----------|-------------------------------------------|
| <span data-ttu-id="2b3ec-136">\_fine FC</span><span class="sxs-lookup"><span data-stu-id="2b3ec-136">FC\_END</span></span>   | <span data-ttu-id="2b3ec-137">Indica la fine di alcune stringhe di formato.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-137">Indicates the end of some format strings.</span></span> |
| <span data-ttu-id="2b3ec-138">\_Pad FC</span><span class="sxs-lookup"><span data-stu-id="2b3ec-138">FC\_PAD</span></span>   | <span data-ttu-id="2b3ec-139">Carattere di riempimento non interpretato.</span><span class="sxs-lookup"><span data-stu-id="2b3ec-139">Uninterpreted pad character.</span></span>              |



 

 

 




