---
title: Combinazione di attributi di matrice
description: Gli attributi di campo possono essere forniti in diverse combinazioni, purché lo stub possa usare le informazioni per determinare le dimensioni della matrice e il numero di byte da trasmettere al server.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300251"
---
# <a name="combining-array-attributes"></a><span data-ttu-id="f79ca-103">Combinazione di attributi di matrice</span><span class="sxs-lookup"><span data-stu-id="f79ca-103">Combining Array Attributes</span></span>

<span data-ttu-id="f79ca-104">Gli attributi di campo possono essere forniti in diverse combinazioni, purché lo stub possa usare le informazioni per determinare le dimensioni della matrice e il numero di byte da trasmettere al server.</span><span class="sxs-lookup"><span data-stu-id="f79ca-104">Field attributes can be supplied in various combinations as long as the stub can use the information to determine the size of the array and the number of bytes to transmit to the server.</span></span> <span data-ttu-id="f79ca-105">Le relazioni tra gli attributi vengono definite utilizzando le formule seguenti:</span><span class="sxs-lookup"><span data-stu-id="f79ca-105">The relationships between the attributes are defined using the following formulas:</span></span>

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

<span data-ttu-id="f79ca-106">I valori associati agli attributi devono rispettare diverse regole comuni basate su tali formule.</span><span class="sxs-lookup"><span data-stu-id="f79ca-106">The values associated with the attributes must obey several common-sense rules based on those formulas.</span></span> <span data-ttu-id="f79ca-107">Queste regole sono:</span><span class="sxs-lookup"><span data-stu-id="f79ca-107">These rules are:</span></span>

-   <span data-ttu-id="f79ca-108">Non specificare un \[ [**primo \_**](/windows/desktop/Midl/first-is) \] valore di indice minore di zero o un valore \[ [**Last \_ è**](/windows/desktop/Midl/last-is) \] maggiore di \[ [**Max \_ è**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="f79ca-108">Do not specify a \[[**first\_is**](/windows/desktop/Midl/first-is)\] index value smaller than zero or a \[[**last\_is**](/windows/desktop/Midl/last-is)\] value greater than \[[**max\_is**](/windows/desktop/Midl/max-is)\].</span></span>
-   <span data-ttu-id="f79ca-109">Non specificare dimensioni negative per una matrice.</span><span class="sxs-lookup"><span data-stu-id="f79ca-109">Do not specify a negative size for an array.</span></span> <span data-ttu-id="f79ca-110">Definire il primo e l'ultimo elemento in modo da ottenere un valore di lunghezza pari a zero o superiore.</span><span class="sxs-lookup"><span data-stu-id="f79ca-110">Define the first and last elements so that they result in a length value of zero or greater.</span></span> <span data-ttu-id="f79ca-111">Definire il \[ [**valore \_ massimo**](/windows/desktop/Midl/max-is) in \] modo che le dimensioni siano pari a zero o superiori.</span><span class="sxs-lookup"><span data-stu-id="f79ca-111">Define the \[[**max\_is**](/windows/desktop/Midl/max-is)\] value so that the size is zero or greater.</span></span> <span data-ttu-id="f79ca-112">Se MIDL è stato richiamato con l'opzione di controllo dei limiti di [**/Error**](/windows/desktop/Midl/-error) \_ , lo stub genera un'eccezione quando la dimensione è minore di zero oppure la lunghezza trasmessa è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="f79ca-112">If MIDL was invoked with the [**/error**](/windows/desktop/Midl/-error) bounds\_check option, then the stub raises an exception when the size is less than zero, or the transmitted length is less than zero.</span></span>
-   <span data-ttu-id="f79ca-113">Non utilizzare la \[ [**lunghezza \_ è**](/windows/desktop/Midl/length-is) \] e l' \[ [**Ultima \_ è**](/windows/desktop/Midl/last-is) \] Attributes contemporaneamente, né la \[ **dimensione \_ è** \] e l' \[ **Ultima \_ è** \] attribuita allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="f79ca-113">Do not use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes at the same time, nor the \[**size\_is**\] and \[**last\_is**\] attributes at the same time.</span></span>

<span data-ttu-id="f79ca-114">A causa della relazione di chiusura in C tra matrici e puntatori, MIDL consente inoltre di dichiarare matrici negli elenchi di parametri utilizzando la notazione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f79ca-114">Because of the close relationship in C between arrays and pointers, MIDL also lets you declare arrays in parameter lists using pointer notation.</span></span> <span data-ttu-id="f79ca-115">MIDL considera un parametro che è un puntatore a un tipo come matrice di tale tipo se il parametro dispone di uno qualsiasi degli attributi associati comunemente alle matrici.</span><span class="sxs-lookup"><span data-stu-id="f79ca-115">MIDL treats a parameter that is a pointer to a type as an array of that type if the parameter has any of the attributes commonly associated with arrays.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

<span data-ttu-id="f79ca-116">Nell'esempio precedente, i parametri della matrice e del puntatore nelle funzioni fArray6 e fArray7 sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="f79ca-116">In the preceding example, the array and pointer parameters in the functions fArray6 and fArray7 are equivalent.</span></span>

 

 