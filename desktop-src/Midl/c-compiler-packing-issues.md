---
title: Problemi di compressione del compilatore C
description: I livelli di compressione influiscono sul layout di memoria dei tipi sia per MIDL che per il compilatore Microsoft C/C++ nello stesso modo.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL compilatore MIDL, problemi di compressione del compilatore C
- creazione di pacchetti MIDL
- MIDL layout di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872453"
---
# <a name="c-compiler-packing-issues"></a><span data-ttu-id="81bf8-106">Problemi di compressione del compilatore C</span><span class="sxs-lookup"><span data-stu-id="81bf8-106">C-Compiler Packing Issues</span></span>

<span data-ttu-id="81bf8-107">I livelli di compressione influiscono sul layout di memoria dei tipi sia per MIDL che per il compilatore Microsoft C/C++ nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="81bf8-107">Packing levels affect the memory layout of types for both MIDL and the Microsoft C/C++ compiler in the same way.</span></span> <span data-ttu-id="81bf8-108">Negli ambienti di compilazione Microsoft, ad esempio l'ambiente di compilazione definito da VC + + o Platform Software Development Kit (SDK), il livello di compressione predefinito per i compilatori MIDL e C/C++ è lo stesso. il livello di compressione predefinito per gli ambienti di compilazione Windows a 32 bit e a 64 bit è 8.</span><span class="sxs-lookup"><span data-stu-id="81bf8-108">In Microsoft build environments, such as the build environment defined by VC++ or the Platform Software Development Kit (SDK), the default packing level for MIDL and C/C++ compilers is the same; the default packing level for the 32-bit and 64-bit Windows build environments is 8.</span></span>

## <a name="natural-alignment"></a><span data-ttu-id="81bf8-109">Allineamento naturale</span><span class="sxs-lookup"><span data-stu-id="81bf8-109">Natural Alignment</span></span>

<span data-ttu-id="81bf8-110">Per i tipi in memoria, l'allineamento predefinito corrisponde al relativo allineamento naturale.</span><span class="sxs-lookup"><span data-stu-id="81bf8-110">For types in memory, the default alignment is the same as its natural alignment.</span></span>

-   <span data-ttu-id="81bf8-111">Un tipo di base, ad esempio short, float e \_ \_ Int64, e un puntatore è allineato naturalmente se la relativa rappresentazione inizia in corrispondenza di un indirizzo di modulo di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="81bf8-111">A base type, such as short, float and \_\_int64, and a pointer is aligned naturally if its representation starts at an address that is modulo its size.</span></span> <span data-ttu-id="81bf8-112">Tutti i tipi di base attualmente supportati hanno dimensioni pari a 1, 2, 4 o 8.</span><span class="sxs-lookup"><span data-stu-id="81bf8-112">All the currently supported base types have sizes of 1, 2, 4 or 8.</span></span> <span data-ttu-id="81bf8-113">I puntatori hanno una dimensione di 4 negli ambienti a 32 bit e 8 negli ambienti a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="81bf8-113">Pointers have a size of 4 in 32-bit environments and 8 in 64-bit environments.</span></span>
-   <span data-ttu-id="81bf8-114">Un tipo composto viene allineato naturalmente se ogni componente è allineato in modo naturale rispetto all'inizio del tipo e se non sono presenti gap superflui (riempimento) tra i componenti.</span><span class="sxs-lookup"><span data-stu-id="81bf8-114">A compound type is aligned naturally if each of its components is aligned naturally relative to the beginning of the type, and if there are no unnecessary gaps (padding) between components.</span></span> <span data-ttu-id="81bf8-115">I componenti composti, ad esempio i campi o gli elementi, vengono ricorsi al puntatore o ai componenti del tipo di base.</span><span class="sxs-lookup"><span data-stu-id="81bf8-115">Compound components, such as fields or elements, are recursed to pointer or base type components.</span></span>

<span data-ttu-id="81bf8-116">Una regola semplice che consente di ricordare questo comportamento è che l'allineamento naturale di un tipo è uguale agli allineamenti principali dei relativi componenti.</span><span class="sxs-lookup"><span data-stu-id="81bf8-116">A simple rule to help remember this behavior is that the natural alignment of a type is equal to the biggest alignments of its components.</span></span>

<span data-ttu-id="81bf8-117">Esiste una connessione tra l'allineamento e le dimensioni della memoria di un tipo in linguaggi come C o C++ e IDL come espresso dall'operatore **sizeof ()**.</span><span class="sxs-lookup"><span data-stu-id="81bf8-117">There is a connection between alignment and memory size of a type in languages like C or C++ and IDL as expressed by the operator **sizeof()**.</span></span> <span data-ttu-id="81bf8-118">La dimensione è un multiplo dell'allineamento (il multiplo minimo si estende sul tipo).</span><span class="sxs-lookup"><span data-stu-id="81bf8-118">The size is a multiple of the alignment (the minimal multiple spanning the type).</span></span> <span data-ttu-id="81bf8-119">Segue la rappresentazione di una matrice in memoria.</span><span class="sxs-lookup"><span data-stu-id="81bf8-119">This follows from an array representation in memory.</span></span>

<span data-ttu-id="81bf8-120">L'allineamento naturale è importante perché l'accesso a dati non allineati può causare un'eccezione in alcuni sistemi.</span><span class="sxs-lookup"><span data-stu-id="81bf8-120">Natural alignment is important because accessing misaligned data may cause an exception on some systems.</span></span> <span data-ttu-id="81bf8-121">I dati possono essere contrassegnati per una manipolazione sicura se non allineati, ma in genere comportano una riduzione della velocità che può essere sostanziale su alcune piattaforme.</span><span class="sxs-lookup"><span data-stu-id="81bf8-121">Data can be marked for a safe manipulation when misaligned, but typically that involves a speed penalty that may be substantial on some platforms.</span></span>

> [!Note]  
> <span data-ttu-id="81bf8-122">In memoria, gli oggetti di tipo con un allineamento naturale di *n* sono sicuramente allineati correttamente quando vengono posizionati su indirizzi che sono un multiplo di *n*.</span><span class="sxs-lookup"><span data-stu-id="81bf8-122">In memory, objects of types with a natural alignment of *n* are guaranteed to be aligned properly when placed at addresses that are a multiple of *n*.</span></span>

 

## <a name="packing-versus-alignment"></a><span data-ttu-id="81bf8-123">Compressione rispetto all'allineamento</span><span class="sxs-lookup"><span data-stu-id="81bf8-123">Packing versus Alignment</span></span>

<span data-ttu-id="81bf8-124">Se si specifica un livello di compressione maggiore di quello naturale di un tipo, l'allineamento del tipo non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="81bf8-124">Specifying a packing level larger than the natural alignment of a type does not change the type alignment.</span></span> <span data-ttu-id="81bf8-125">Se si specifica un livello di compressione inferiore a quello naturale, viene ridotto l'allineamento del tipo al livello di compressione.</span><span class="sxs-lookup"><span data-stu-id="81bf8-125">Specifying a packing level smaller than the natural alignment reduces the type alignment to the packing level.</span></span> <span data-ttu-id="81bf8-126">Di conseguenza, i tipi compressi possono essere inseriti in memoria negli indirizzi che sono un multiplo del livello di compressione, ovvero l'allineamento ridotto, senza causare errori di allineamento.</span><span class="sxs-lookup"><span data-stu-id="81bf8-126">As a result, the packed types may be placed in memory at addresses that are a multiple of the packing level (the reduced alignment) without causing a misalignment.</span></span> <span data-ttu-id="81bf8-127">Questa operazione ha effetto sia sui tipi semplici che sui tipi di componenti.</span><span class="sxs-lookup"><span data-stu-id="81bf8-127">This affects both simple types and component types.</span></span> <span data-ttu-id="81bf8-128">Per i tipi composti, il layout interno del tipo potrebbe essere influenzato, in quanto l'allineamento ridotto dei componenti potrebbe modificare la dimensione della spaziatura interna necessaria per l'allineamento corretto dei componenti, riducendo così le dimensioni del tipo.</span><span class="sxs-lookup"><span data-stu-id="81bf8-128">For compound types, the internal layout of the type may be affected, because the reduced alignment of the components may change the size of padding necessary for the proper alignment of the components, thus reducing the size of the type.</span></span>

<span data-ttu-id="81bf8-129">Una regola semplice che consente di ricordare questo comportamento è che il nuovo allineamento di un tipo compresso è il più piccolo del livello di compressione e il relativo allineamento naturale.</span><span class="sxs-lookup"><span data-stu-id="81bf8-129">A simple rule to help remember this behavior is that the new alignment of a packed type is the smaller of the packing level and its natural alignment.</span></span> <span data-ttu-id="81bf8-130">Le dimensioni del tipo sono un multiplo del nuovo allineamento.</span><span class="sxs-lookup"><span data-stu-id="81bf8-130">The size of the type is a multiple of the new alignment.</span></span> <span data-ttu-id="81bf8-131">L'operatore **sizeof ()** restituisce le dimensioni ridotte per i tipi compressi.</span><span class="sxs-lookup"><span data-stu-id="81bf8-131">The **sizeof()** operator returns the reduced size for packed types.</span></span>

<span data-ttu-id="81bf8-132">Ad esempio, con il livello di compressione 2 un Long viene allineato a 2 e pertanto può essere inserito in qualsiasi indirizzo, non solo negli indirizzi che sono un multiplo di 4 come nel caso dell'allineamento naturale.</span><span class="sxs-lookup"><span data-stu-id="81bf8-132">For example, with packing level 2 a long becomes aligned at 2, and therefore may be placed at any even address, not only at the addresses that are a multiple of 4 as would be the case with natural alignment.</span></span> <span data-ttu-id="81bf8-133">Una struttura con un valore short e Long, compresso su 2, non necessita del gap interno tra la breve e la lunghezza seguente necessaria per l'allineamento naturale; di conseguenza, non solo la struttura è ora allineata a 2, ma anche la sua dimensione è ridotta da 8 a 6.</span><span class="sxs-lookup"><span data-stu-id="81bf8-133">A structure with a short and a long, packed at 2, does not need the internal gap between the short and the following long that was necessary for the natural alignment; hence, not only is the structure now aligned at 2, it also has its size reduced from 8 to 6.</span></span>

<span data-ttu-id="81bf8-134">Si consideri ad esempio un tipo composto costituito da un carattere a 1 byte, un numero intero di 4 byte e un carattere a 1 byte:</span><span class="sxs-lookup"><span data-stu-id="81bf8-134">As an example, consider a compound type consisting of a 1-byte character, an integer 4 bytes long, and a 1-byte character:</span></span>

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

<span data-ttu-id="81bf8-135">Questa struttura è naturalmente allineata a 4 e ha una dimensione naturale di 12.</span><span class="sxs-lookup"><span data-stu-id="81bf8-135">This structure is naturally aligned at 4 and has the natural size of 12.</span></span>

<span data-ttu-id="81bf8-136">Per il livello di compressione 4 o superiore, la struttura **struct** è allineata a 4 ed `sizeof(struct mystructtype)` è uguale a 12.</span><span class="sxs-lookup"><span data-stu-id="81bf8-136">For packing level 4 or greater, the structure **mystruct** is aligned at 4 and `sizeof(struct mystructtype)` is equal to 12.</span></span> <span data-ttu-id="81bf8-137">La struttura verrà allineata in modo non corretto se si trova in memoria in un indirizzo che non è un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="81bf8-137">The structure will be misaligned if located in memory at an address that is not a multiple of 4.</span></span>

<span data-ttu-id="81bf8-138">Per il livello di compressione 2, la struttura è allineata a 2 e la relativa dimensione è 8.</span><span class="sxs-lookup"><span data-stu-id="81bf8-138">For packing level 2, the structure is aligned at 2 and its size is 8.</span></span> <span data-ttu-id="81bf8-139">La struttura compressa con livello 2 sarà allineata in modo non corretto se si trova in memoria in un indirizzo che non è un multiplo di 2.</span><span class="sxs-lookup"><span data-stu-id="81bf8-139">The structure packed with level 2 will be misaligned if located in memory at an address that is not a multiple of 2.</span></span>

<span data-ttu-id="81bf8-140">Per il livello di compressione 1, la struttura è allineata a 1 e la relativa dimensione è 6.</span><span class="sxs-lookup"><span data-stu-id="81bf8-140">For packing level 1, the structure is aligned at 1 and its size is 6.</span></span> <span data-ttu-id="81bf8-141">La struttura compressa con livello 1 può essere posizionata ovunque senza causare un errore di allineamento.</span><span class="sxs-lookup"><span data-stu-id="81bf8-141">The structure packed with level 1 can be placed anywhere without causing a misalignment fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81bf8-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81bf8-142">Related topics</span></span>

<dl> <span data-ttu-id="81bf8-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="81bf8-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="81bf8-144">/ZP</span><span class="sxs-lookup"><span data-stu-id="81bf8-144">/Zp</span></span>](./-zp.md)
</dt> <dt>

[<span data-ttu-id="81bf8-145">/Pack</span><span class="sxs-lookup"><span data-stu-id="81bf8-145">/pack</span></span>](./-pack.md)
</dt> </dl>

 

 