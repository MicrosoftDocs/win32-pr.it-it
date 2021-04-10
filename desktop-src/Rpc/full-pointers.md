---
title: Puntatori completi
description: A differenza dei puntatori univoci, i puntatori completi supportano l'aliasing.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963187"
---
# <a name="full-pointers"></a><span data-ttu-id="2778b-103">Puntatori completi</span><span class="sxs-lookup"><span data-stu-id="2778b-103">Full Pointers</span></span>

<span data-ttu-id="2778b-104">A differenza dei puntatori [univoci](unique-pointers.md) , i puntatori completi supportano l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="2778b-104">Unlike [unique](unique-pointers.md) pointers, full pointers support aliasing.</span></span> <span data-ttu-id="2778b-105">Ciò significa che più puntatori possono fare riferimento agli stessi dati, come illustrato nella figura seguente:</span><span class="sxs-lookup"><span data-stu-id="2778b-105">This means that multiple pointers can refer to the same data, as shown in the following figure:</span></span>

![due puntatori che fanno riferimento agli stessi dati](images/prog-a02.png)

<span data-ttu-id="2778b-107">Un puntatore completo presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="2778b-107">A full pointer has the following characteristics:</span></span>

-   <span data-ttu-id="2778b-108">Il valore può essere null.</span><span class="sxs-lookup"><span data-stu-id="2778b-108">It can have the value null.</span></span>
-   <span data-ttu-id="2778b-109">Può variare da null a non null durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="2778b-109">It can change from null to non-null during the call.</span></span> <span data-ttu-id="2778b-110">Quando il valore viene modificato in un valore diverso da null, lo stub client alloca la nuova memoria allocata al momento della restituzione.</span><span class="sxs-lookup"><span data-stu-id="2778b-110">When the value changes to non-null, the client stub allocates new memory allocated on return.</span></span> <span data-ttu-id="2778b-111">Il programma client deve liberare questa memoria prima di terminare.</span><span class="sxs-lookup"><span data-stu-id="2778b-111">The client program should free this memory before it terminates.</span></span>
-   <span data-ttu-id="2778b-112">È possibile passare da un valore diverso da null a null durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="2778b-112">It can change from non-null to null during the call.</span></span> <span data-ttu-id="2778b-113">Quando il valore viene modificato in null, l'applicazione è responsabile della liberazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="2778b-113">When the value changes to null, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="2778b-114">Il valore può variare da un valore non null a un altro.</span><span class="sxs-lookup"><span data-stu-id="2778b-114">The value can change from one non-null value to another.</span></span>
-   <span data-ttu-id="2778b-115">È possibile accedere all'archiviazione a cui punta un puntatore completo tramite un altro puntatore o nome nell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2778b-115">The storage that a full pointer points to may be accessed by another pointer or name in the operation.</span></span>
-   <span data-ttu-id="2778b-116">I dati restituiti vengono scritti nell'archiviazione esistente se il puntatore non ha il valore null.</span><span class="sxs-lookup"><span data-stu-id="2778b-116">Return data is written into existing storage if the pointer does not have the value null.</span></span>

<span data-ttu-id="2778b-117">Usare l' \[ attributo [**ptr**](/windows/desktop/Midl/ptr) \] per specificare un puntatore completo, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="2778b-117">Use the \[ [**ptr**](/windows/desktop/Midl/ptr) \] attribute to specify a full pointer, as shown in the following example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

<span data-ttu-id="2778b-118">In questo esempio i parametri *ptrName1* e *ptrName2* sono definiti come puntatori completi a una stringa.</span><span class="sxs-lookup"><span data-stu-id="2778b-118">In this example the parameters *ptrName1* and *ptrName2* are defined as full pointers to a string.</span></span> <span data-ttu-id="2778b-119">È possibile che entrambi i puntatori puntino allo stesso indirizzo di memoria contenente una singola stringa.</span><span class="sxs-lookup"><span data-stu-id="2778b-119">It is possible for both pointers to point to the same memory address containing a single string.</span></span>

<span data-ttu-id="2778b-120">\[**ptr** \] è obbligatorio quando si fornisce supporto per l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="2778b-120">\[**ptr**\] is required when providing aliasing support.</span></span> <span data-ttu-id="2778b-121">Tuttavia, poiché richiede la maggior parte dell'elaborazione di tutti i puntatori disponibili in RPC, non è consigliabile per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2778b-121">However, since it requires the most processing of all the pointers available in RPC, it is not recommended for most applications.</span></span>

 

 