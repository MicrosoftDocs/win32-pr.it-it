---
title: Puntatori di riferimento
description: I puntatori di riferimento sono i puntatori più semplici e richiedono la quantità minima di elaborazione da parte dello stub client.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047244"
---
# <a name="reference-pointers"></a><span data-ttu-id="74c67-103">Puntatori di riferimento</span><span class="sxs-lookup"><span data-stu-id="74c67-103">Reference Pointers</span></span>

<span data-ttu-id="74c67-104">I puntatori di riferimento sono i puntatori più semplici e richiedono la quantità minima di elaborazione da parte dello stub client.</span><span class="sxs-lookup"><span data-stu-id="74c67-104">Reference pointers are the simplest pointers and require the least amount of processing by the client stub.</span></span> <span data-ttu-id="74c67-105">Quando un programma client passa un puntatore di riferimento a una procedura remota, il puntatore di riferimento contiene sempre l'indirizzo di un blocco di memoria valido.</span><span class="sxs-lookup"><span data-stu-id="74c67-105">When a client program passes a reference pointer to a remote procedure, the reference pointer always contains the address of a valid block of memory.</span></span> <span data-ttu-id="74c67-106">Il puntatore verrà ancora posizionato allo stesso blocco di memoria al termine della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="74c67-106">It will still be pointing to the same memory block when the remote procedure completes.</span></span> <span data-ttu-id="74c67-107">Questi puntatori vengono utilizzati principalmente per implementare la semantica di riferimento e per consentire \[ parametri [**out**](/windows/desktop/Midl/out-idl) \] in C.</span><span class="sxs-lookup"><span data-stu-id="74c67-107">These pointers are mainly used to implement reference semantics, and to allow for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters in C.</span></span>

<span data-ttu-id="74c67-108">Nell'esempio seguente, il valore del puntatore non cambia durante la chiamata, sebbene il contenuto dei dati all'indirizzo indicato dal puntatore possa cambiare.</span><span class="sxs-lookup"><span data-stu-id="74c67-108">In the following example, the value of the pointer does not change during the call, although the contents of the data at the address indicated by the pointer can change.</span></span>

![modifica dei dati in corrispondenza di un indirizzo puntatore di riferimento statico](images/prog-a07.png)

<span data-ttu-id="74c67-110">Un puntatore di riferimento presenta le seguenti caratteristiche:</span><span class="sxs-lookup"><span data-stu-id="74c67-110">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="74c67-111">Punta sempre a una risorsa di archiviazione valida e non ha mai il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="74c67-111">It always points to valid storage and never has the value **NULL**.</span></span>
-   <span data-ttu-id="74c67-112">Non viene mai modificato durante una chiamata e punta sempre alla stessa risorsa di archiviazione prima e dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="74c67-112">It never changes during a call and always points to the same storage before and after the call.</span></span>
-   <span data-ttu-id="74c67-113">I dati restituiti dalla procedura remota vengono scritti nella risorsa di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="74c67-113">Data returned from the remote procedure is written into the existing storage.</span></span>
-   <span data-ttu-id="74c67-114">Non è possibile accedere allo spazio di archiviazione a cui punta un puntatore di riferimento per nessun altro puntatore o altro nome nella funzione.</span><span class="sxs-lookup"><span data-stu-id="74c67-114">The storage pointed to by a reference pointer cannot be accessed by any other pointer or any other name in the function.</span></span>

<span data-ttu-id="74c67-115">Usare l' \[ attributo [**ref**](/windows/desktop/Midl/ref) \] per specificare i puntatori di riferimento nelle definizioni di interfaccia, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="74c67-115">Use the \[[**ref**](/windows/desktop/Midl/ref)\] attribute to specify reference pointers in interface definitions, as shown in the following example.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

<span data-ttu-id="74c67-116">Questo esempio definisce il parametro *PChar* come puntatore a un singolo carattere, non a una matrice di caratteri.</span><span class="sxs-lookup"><span data-stu-id="74c67-116">This example defines the parameter *pChar* as a pointer to a single character, not an array of characters.</span></span> <span data-ttu-id="74c67-117">Si tratta \[  \] di un parametro out e di un puntatore di riferimento che punta alla memoria che la routine del server RemoteFn riempirà con i dati.</span><span class="sxs-lookup"><span data-stu-id="74c67-117">It is an \[**out**\] parameter and a reference pointer that points to memory that the server routine RemoteFn will fill with data.</span></span>

 

 