---
title: Attributi di matrice
description: Esiste una relazione di chiusura tra matrici e puntatori nel linguaggio C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729434"
---
# <a name="array-attributes"></a><span data-ttu-id="eb9d5-103">Attributi di matrice</span><span class="sxs-lookup"><span data-stu-id="eb9d5-103">Array Attributes</span></span>

<span data-ttu-id="eb9d5-104">Esiste una relazione di chiusura tra matrici e puntatori nel linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-104">There is a close relationship between arrays and pointers in the C language.</span></span> <span data-ttu-id="eb9d5-105">Quando viene passato come parametro a una funzione, un nome di matrice viene considerato come un puntatore al primo elemento della matrice, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="eb9d5-105">When passed as a parameter to a function, an array name is treated as a pointer to the first element of the array, as shown in the following example:</span></span>


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



<span data-ttu-id="eb9d5-106">In una chiamata locale è possibile usare il parametro pointer per procedere alla memoria ed esaminare il contenuto di altri indirizzi:</span><span class="sxs-lookup"><span data-stu-id="eb9d5-106">In a local call, you can use the pointer parameter to march through memory and examine the contents of other addresses:</span></span>


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



<span data-ttu-id="eb9d5-107">Quando un client passa un puntatore a una procedura remota, lo stub del client trasmette sia il puntatore che i dati a cui punta.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-107">When a client passes a pointer to a remote procedure, the client stub transmits both the pointer and the data it points to.</span></span> <span data-ttu-id="eb9d5-108">A meno che il puntatore non sia limitato ai dati corrispondenti, tutta la memoria del client deve essere trasmessa con ogni chiamata remota.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-108">Unless the pointer is restricted to its corresponding data, all the client's memory must be transmitted with every remote call.</span></span> <span data-ttu-id="eb9d5-109">Applicando la tipizzazione forte nella definizione di interfaccia, MIDL limita l'elaborazione del client-Stub ai dati che corrispondono al puntatore specificato.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-109">By enforcing strong typing in the interface definition, MIDL limits client-stub processing to the data that corresponds to the specified pointer.</span></span>

<span data-ttu-id="eb9d5-110">La dimensione della matrice e l'intervallo di elementi della matrice trasmessi al computer remoto possono essere costanti o variabili.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-110">The size of the array and the range of array elements transmitted to the remote computer can be constant or variable.</span></span> <span data-ttu-id="eb9d5-111">Quando questi valori sono variabili e pertanto determinati in fase di esecuzione, è necessario utilizzare gli attributi nel file IDL per specificare il numero di elementi di matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-111">When these values are variable, and thus determined at run time, you must use attributes in the IDL file to specify how many array elements to transmit.</span></span> <span data-ttu-id="eb9d5-112">Gli attributi MIDL seguenti supportano i limiti della matrice.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-112">The following MIDL attributes support array bounds.</span></span>



| <span data-ttu-id="eb9d5-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="eb9d5-113">Attribute</span></span>                             | <span data-ttu-id="eb9d5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb9d5-114">Description</span></span>                                             | <span data-ttu-id="eb9d5-115">Predefinito</span><span class="sxs-lookup"><span data-stu-id="eb9d5-115">Default</span></span> |
|---------------------------------------|---------------------------------------------------------|---------|
| <span data-ttu-id="eb9d5-116">\[il [ **primo \_ è**](/windows/desktop/Midl/first-is)\]</span><span class="sxs-lookup"><span data-stu-id="eb9d5-116">\[ [**first\_is**](/windows/desktop/Midl/first-is)\]</span></span>   | <span data-ttu-id="eb9d5-117">Indice del primo elemento della matrice trasmesso.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-117">Index of the first array element transmitted.</span></span>           | <span data-ttu-id="eb9d5-118">0</span><span class="sxs-lookup"><span data-stu-id="eb9d5-118">0</span></span>       |
| <span data-ttu-id="eb9d5-119">\[[ **ultimo \_ è**](/windows/desktop/Midl/last-is)\]</span><span class="sxs-lookup"><span data-stu-id="eb9d5-119">\[ [**last\_is**](/windows/desktop/Midl/last-is)\]</span></span>     | <span data-ttu-id="eb9d5-120">Indice dell'ultimo elemento della matrice trasmesso.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-120">Index of the last array element transmitted.</span></span>            | \-      |
| <span data-ttu-id="eb9d5-121">\[[ **lunghezza \_**](/windows/desktop/Midl/length-is)\]</span><span class="sxs-lookup"><span data-stu-id="eb9d5-121">\[ [**length\_is**](/windows/desktop/Midl/length-is)\]</span></span> | <span data-ttu-id="eb9d5-122">Numero totale di elementi della matrice trasmessi.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-122">Total number of array elements transmitted.</span></span>             | \-      |
| <span data-ttu-id="eb9d5-123">\[[ **Max \_ è**](/windows/desktop/Midl/max-is)\]</span><span class="sxs-lookup"><span data-stu-id="eb9d5-123">\[ [**max\_is**](/windows/desktop/Midl/max-is)\]</span></span>       | <span data-ttu-id="eb9d5-124">Valore di indice di matrice valido più alto.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-124">Highest valid array index value.</span></span>                        | \-      |
| <span data-ttu-id="eb9d5-125">\[[ **Min \_ è**](/windows/desktop/Midl/min-is)\]</span><span class="sxs-lookup"><span data-stu-id="eb9d5-125">\[ [**min\_is**](/windows/desktop/Midl/min-is)\]</span></span>       | <span data-ttu-id="eb9d5-126">Valore di indice di matrice valido più basso.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-126">Lowest valid array index value.</span></span>                         | <span data-ttu-id="eb9d5-127">0</span><span class="sxs-lookup"><span data-stu-id="eb9d5-127">0</span></span>       |
| <span data-ttu-id="eb9d5-128">\[[ **dimensioni \_**](/windows/desktop/Midl/size-is)\]</span><span class="sxs-lookup"><span data-stu-id="eb9d5-128">\[ [**size\_is**](/windows/desktop/Midl/size-is)\]</span></span>     | <span data-ttu-id="eb9d5-129">Numero totale di elementi della matrice allocati per la matrice.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-129">Total number of array elements allocated for the array.</span></span> | \-      |



 

> [!Note]  
> <span data-ttu-id="eb9d5-130">L'attributo **Min \_ is** non è implementato in RPC.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-130">The **min\_is** attribute is not implemented in RPC.</span></span> <span data-ttu-id="eb9d5-131">L'indice di matrice minimo viene sempre considerato come zero.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-131">The minimum array index is always treated as zero.</span></span>

 

 

 