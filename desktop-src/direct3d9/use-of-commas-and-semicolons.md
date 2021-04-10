---
description: L'uso di virgole e punti e virgola può essere il problema di sintassi più complesso nel formato di file e questo utilizzo è molto limitato. Le virgole vengono usate per separare i membri della matrice; i punti e virgola terminano ogni elemento di dati.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Uso di virgole e punti e virgola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125571"
---
# <a name="use-of-commas-and-semicolons"></a><span data-ttu-id="a91d5-104">Uso di virgole e punti e virgola</span><span class="sxs-lookup"><span data-stu-id="a91d5-104">Use of Commas and Semicolons</span></span>

<span data-ttu-id="a91d5-105">L'uso di virgole e punti e virgola può essere il problema di sintassi più complesso nel formato di file e questo utilizzo è molto limitato.</span><span class="sxs-lookup"><span data-stu-id="a91d5-105">Using commas and semicolons can be the most complex syntax issue in the file format, and this usage is very strict.</span></span> <span data-ttu-id="a91d5-106">Le virgole vengono usate per separare i membri della matrice; i punti e virgola terminano ogni elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="a91d5-106">Commas are used to separate array members; semicolons terminate each data item.</span></span>

<span data-ttu-id="a91d5-107">Se, ad esempio, un modello viene definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="a91d5-107">For example, if a template is defined in the following manner:</span></span>


```
template mytemp {
DWORD myvar;
}
```



<span data-ttu-id="a91d5-108">Quindi, un'istanza di questo modello è simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="a91d5-108">Then an instance of this template looks like the following:</span></span>


```
mytemp dataTemp {
1;
}
```



<span data-ttu-id="a91d5-109">Se un modello contenente un altro modello viene definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="a91d5-109">If a template containing another template is defined in the following manner;</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



<span data-ttu-id="a91d5-110">Quindi, un'istanza di questo modello è simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="a91d5-110">Then an instance of this template looks like the following:</span></span>


```
container dataContainer {
1.1;
2; 
3;;
}
```



<span data-ttu-id="a91d5-111">Si noti che la seconda riga che rappresenta il contenitore Temp interno presenta due punti e virgola alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="a91d5-111">Note that the second line that represents the mytemp inside container has two semicolons at the end of the line.</span></span> <span data-ttu-id="a91d5-112">Il primo punto e virgola indica la fine dell'elemento di dati, aTemp (all'interno del contenitore) e il secondo punto e virgola indica la fine del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a91d5-112">The first semicolon indicates the end of the data item, aTemp (inside container), and the second semicolon indicates the end of the container.</span></span>

<span data-ttu-id="a91d5-113">Se una matrice viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="a91d5-113">If an array is defined in the following manner:</span></span>


```
Template mytemp {

array DWORD myvar[3];

}
```



<span data-ttu-id="a91d5-114">Quindi, un'istanza di questo aspetto è simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="a91d5-114">Then an instance of this looks like the following:</span></span>


```
mytemp aTemp {
1, 2, 3;
}
```



<span data-ttu-id="a91d5-115">Nell'esempio di matrice non è necessario che gli elementi dati siano separati da punti e virgola perché sono delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="a91d5-115">In the array example, there is no need for the data items to be separated by semicolons because they are delineated by commas.</span></span> <span data-ttu-id="a91d5-116">Il punto e virgola alla fine contrassegna la fine della matrice.</span><span class="sxs-lookup"><span data-stu-id="a91d5-116">The semicolon at the end marks the end of the array.</span></span>

<span data-ttu-id="a91d5-117">Si consideri un modello che contiene una matrice di elementi di dati definiti da un modello.</span><span class="sxs-lookup"><span data-stu-id="a91d5-117">Consider a template that contains an array of data items defined by a template.</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



<span data-ttu-id="a91d5-118">Un'istanza di questo aspetto sarà simile all'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="a91d5-118">An instance of this would look like the following example.</span></span>


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a><span data-ttu-id="a91d5-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a91d5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a91d5-120">Codifica testo</span><span class="sxs-lookup"><span data-stu-id="a91d5-120">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



