---
title: Matrici multidimensionali
description: Gli attributi di matrice possono essere usati anche con matrici multidimensionali.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963301"
---
# <a name="multidimensional-arrays"></a><span data-ttu-id="a7460-103">Matrici multidimensionali</span><span class="sxs-lookup"><span data-stu-id="a7460-103">Multidimensional Arrays</span></span>

<span data-ttu-id="a7460-104">Gli attributi di matrice possono essere usati anche con matrici multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="a7460-104">Array attributes can also be used with multidimensional arrays.</span></span> <span data-ttu-id="a7460-105">Tuttavia, prestare attenzione a garantire che ogni dimensione della matrice disponga di un attributo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a7460-105">However, be careful to ensure that every dimension of the array has a corresponding attribute.</span></span> <span data-ttu-id="a7460-106">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a7460-106">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

<span data-ttu-id="a7460-107">La matrice precedente è una matrice conforme (di dimensioni d1size) di 30 matrici di elementi (con gli elementi D2LEN spediti per ogni).</span><span class="sxs-lookup"><span data-stu-id="a7460-107">The preceding array is a conformant array (of size d1size ) of 30 element arrays (with d2len elements shipped for each).</span></span> <span data-ttu-id="a7460-108">La virgola tra le parentesi della \[ [**dimensione \_ è**](/windows/desktop/Midl/size-is) \] attribute specifica che il valore in d1size viene applicato alla prima dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="a7460-108">The comma in the parentheses of the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute specifies that value in d1size is applied to the first dimension of the array.</span></span> <span data-ttu-id="a7460-109">Analogamente, il comando tra le parentesi della \[ [**lunghezza \_ è**](/windows/desktop/Midl/length-is) \] attributo indica che il valore in D2LEN viene applicato alla seconda dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="a7460-109">Likewise, the command in the parentheses of the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute indicates that the value in d2len is applied to the second dimension of the array.</span></span>

<span data-ttu-id="a7460-110">Il compilatore MIDL 2,0 fornisce due metodi per il marshalling dei parametri: modalità mista (/**OS**) e completamente interpretato (/**OIF** o/**Oicf**).</span><span class="sxs-lookup"><span data-stu-id="a7460-110">The MIDL 2.0 compiler provides two methods for marshaling parameters: mixed-mode (/**Os**) and fully-interpreted (/**Oif** or /**Oicf**).</span></span> <span data-ttu-id="a7460-111">Per impostazione predefinita, il compilatore MIDL compila le interfacce in modalità mista.</span><span class="sxs-lookup"><span data-stu-id="a7460-111">By default, the MIDL compiler compiles interfaces in mixed mode.</span></span> <span data-ttu-id="a7460-112">Non è necessario specificare in modo esplicito l'opzione [**/OS**](/windows/desktop/Midl/-os) per ottenere il marshalling in modalità mista.</span><span class="sxs-lookup"><span data-stu-id="a7460-112">You do not need to explicitly specify the [**/Os**](/windows/desktop/Midl/-os) switch to get mixed-mode marshaling.</span></span>

<span data-ttu-id="a7460-113">Il metodo completamente interpretato esegue il marshalling dei dati completamente offline.</span><span class="sxs-lookup"><span data-stu-id="a7460-113">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="a7460-114">In questo modo si riduce considerevolmente le dimensioni del codice dello stub, ma si riducono anche le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a7460-114">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span> <span data-ttu-id="a7460-115">Nel marshalling in modalità mista, gli stub eseguono il marshalling di alcuni parametri online.</span><span class="sxs-lookup"><span data-stu-id="a7460-115">In mixed-mode marshaling, the stubs marshals some parameters online.</span></span> <span data-ttu-id="a7460-116">Sebbene il risultato sia un numero maggiore di dimensioni dello stub, offre prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="a7460-116">While this results in a larger stub size, it also offers increased performance.</span></span>

> [!Caution]  
> <span data-ttu-id="a7460-117">Prestare attenzione quando si compilano file IDL in questa modalità.</span><span class="sxs-lookup"><span data-stu-id="a7460-117">Exercise caution when compiling IDL files in this mode.</span></span> <span data-ttu-id="a7460-118">L'utilizzo di matrici multidimensionali in modalità mista può causare la mancata corretta marshalling dei parametri.</span><span class="sxs-lookup"><span data-stu-id="a7460-118">Using multidimensional arrays in mixed mode can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="a7460-119">L'opzione della riga di comando [**/Oicf**](/windows/desktop/Midl/-oi) è consigliata quando l'interfaccia definisce parametri che sono matrici multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="a7460-119">The [**/Oicf**](/windows/desktop/Midl/-oi) command line switch is recommended when your interface defines parameters that are multidimensional arrays.</span></span>

 

<span data-ttu-id="a7460-120">L' \[ attributo [**stringa**](/windows/desktop/Midl/string) \] può essere utilizzato anche con matrici multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="a7460-120">The \[[**string**](/windows/desktop/Midl/string)\] attribute can also be used with multidimensional arrays.</span></span> <span data-ttu-id="a7460-121">L'attributo si applica alla dimensione meno significativa, ad esempio una matrice di stringhe conforme.</span><span class="sxs-lookup"><span data-stu-id="a7460-121">The attribute applies to the least significant dimension, such as a conformant array of strings.</span></span> <span data-ttu-id="a7460-122">È inoltre possibile utilizzare gli attributi del puntatore multidimensionale.</span><span class="sxs-lookup"><span data-stu-id="a7460-122">You can also use multidimensional pointer attributes.</span></span> <span data-ttu-id="a7460-123">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a7460-123">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

<span data-ttu-id="a7460-124">Nell'esempio precedente, la variabile ptr2d è un puntatore a un blocco di puntatori di dimensioni d1len, ognuno dei quali punta a D2LEN puntatori a **Long**.</span><span class="sxs-lookup"><span data-stu-id="a7460-124">In the preceding example, the variable ptr2d is a pointer to a d1len-sized block of pointers, each of which points to d2len pointers to **long**.</span></span>

<span data-ttu-id="a7460-125">Le matrici multidimensionali non sono equivalenti a matrici di puntatori.</span><span class="sxs-lookup"><span data-stu-id="a7460-125">Multidimensional arrays are not equivalent to arrays of pointers.</span></span> <span data-ttu-id="a7460-126">Una matrice multidimensionale è un singolo blocco di dati di grandi dimensioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="a7460-126">A multidimensional array is a single, large block of data in memory.</span></span> <span data-ttu-id="a7460-127">Una matrice di puntatori contiene solo un blocco di puntatori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a7460-127">An array of pointers only contains a block of pointers in the array.</span></span> <span data-ttu-id="a7460-128">I dati a cui puntano i puntatori possono trovarsi in qualsiasi punto della memoria.</span><span class="sxs-lookup"><span data-stu-id="a7460-128">The data that the pointers point to can be anywhere in memory.</span></span> <span data-ttu-id="a7460-129">Inoltre, la sintassi ANSI C consente di non specificare in una matrice multidimensionale solo la dimensione di matrice più significativa (più a sinistra).</span><span class="sxs-lookup"><span data-stu-id="a7460-129">Also, ANSI C syntax allows only the most significant (leftmost) array dimension to be unspecified in a multidimensional array.</span></span> <span data-ttu-id="a7460-130">Di conseguenza, di seguito è riportata un'istruzione valida:</span><span class="sxs-lookup"><span data-stu-id="a7460-130">Therefore, the following is a valid statement:</span></span>

`long a1[] [20]`

<span data-ttu-id="a7460-131">Confrontare questa operazione con l'istruzione non valida seguente:</span><span class="sxs-lookup"><span data-stu-id="a7460-131">Compare this to the following invalid statement:</span></span>

`long a1[20] []`

 

 