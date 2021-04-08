---
title: Puntatori univoci
description: Nei programmi C, più di un puntatore può contenere l'indirizzo dei dati.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046780"
---
# <a name="unique-pointers"></a><span data-ttu-id="1066e-103">Puntatori univoci</span><span class="sxs-lookup"><span data-stu-id="1066e-103">Unique Pointers</span></span>

<span data-ttu-id="1066e-104">Nei programmi C, più di un puntatore può contenere l'indirizzo dei dati.</span><span class="sxs-lookup"><span data-stu-id="1066e-104">In C programs, more than one pointer can contain the address of data.</span></span> <span data-ttu-id="1066e-105">Ai puntatori viene detto di creare un [*alias*](a-glos.md) per i dati.</span><span class="sxs-lookup"><span data-stu-id="1066e-105">The pointers are said to create an [*alias*](a-glos.md) for the data.</span></span> <span data-ttu-id="1066e-106">Gli alias vengono creati anche quando i puntatori puntano a variabili dichiarate.</span><span class="sxs-lookup"><span data-stu-id="1066e-106">Aliases are also created when pointers point at declared variables.</span></span> <span data-ttu-id="1066e-107">Nel frammento di codice seguente vengono illustrati entrambi i metodi di aliasing:</span><span class="sxs-lookup"><span data-stu-id="1066e-107">The following code fragment illustrates both of these methods of aliasing:</span></span>


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



<span data-ttu-id="1066e-108">In un tipico programma C, è possibile specificare un albero binario usando la definizione seguente:</span><span class="sxs-lookup"><span data-stu-id="1066e-108">In a typical C program, you might specify a binary tree using the following definition:</span></span>


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



<span data-ttu-id="1066e-109">Più di un puntatore può accedere al contenuto di un nodo della struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="1066e-109">More than one pointer can access the contents of a tree node.</span></span> <span data-ttu-id="1066e-110">Questa operazione è in genere corretta per le applicazioni non distribuite.</span><span class="sxs-lookup"><span data-stu-id="1066e-110">This is generally fine for nondistributed applications.</span></span> <span data-ttu-id="1066e-111">Tuttavia, questo stile di programmazione genera un codice di supporto RPC più complesso.</span><span class="sxs-lookup"><span data-stu-id="1066e-111">However, this style of programming generates more complicated RPC support code.</span></span> <span data-ttu-id="1066e-112">Gli stub client e server richiedono il codice aggiuntivo per gestire i dati e i puntatori.</span><span class="sxs-lookup"><span data-stu-id="1066e-112">The client and server stubs require the additional code to manage the data and the pointers.</span></span> <span data-ttu-id="1066e-113">Il codice stub sottostante deve risolvere i diversi puntatori agli indirizzi e determinare la copia dei dati che rappresenta la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="1066e-113">The underlying stub code must resolve the various pointers to the addresses and determine which copy of the data represents the most recent version.</span></span>

<span data-ttu-id="1066e-114">La quantità di elaborazione può essere ridotta se si garantisce che il puntatore sia l'unico modo in cui l'applicazione può accedere a tale area di memoria.</span><span class="sxs-lookup"><span data-stu-id="1066e-114">The amount of processing can be reduced if you guarantee that your pointer is the only way the application can access that area of memory.</span></span> <span data-ttu-id="1066e-115">Il puntatore può ancora avere molte delle funzionalità di un puntatore C.</span><span class="sxs-lookup"><span data-stu-id="1066e-115">The pointer can still have many of the features of a C pointer.</span></span> <span data-ttu-id="1066e-116">Ad esempio, può variare tra valori **null** e non **null** o rimanere invariati.</span><span class="sxs-lookup"><span data-stu-id="1066e-116">For example, it can change between **null** and non-**null** values or stay the same.</span></span> <span data-ttu-id="1066e-117">Questa condizione è illustrata nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="1066e-117">The following example illustrates this.</span></span> <span data-ttu-id="1066e-118">Il puntatore è **null** prima della chiamata e punta a una stringa valida dopo la chiamata:</span><span class="sxs-lookup"><span data-stu-id="1066e-118">The pointer is **null** before the call and points to a valid string after the call:</span></span>

![puntatore che cambia tra valori null e non null](images/prog-a01.png)

<span data-ttu-id="1066e-120">Per impostazione predefinita, il compilatore MIDL applica l' \[ attributo [univoco](/windows/desktop/Midl/unique) del \] puntatore a tutti i puntatori che non sono parametri.</span><span class="sxs-lookup"><span data-stu-id="1066e-120">By default, the MIDL compiler applies the \[ [unique](/windows/desktop/Midl/unique)\] pointer attribute to all pointers that are not parameters.</span></span> <span data-ttu-id="1066e-121">Questa impostazione predefinita può essere modificata con l' \[ [attributo \_ default del puntatore](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="1066e-121">This default setting can be changed with the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] attribute.</span></span>

<span data-ttu-id="1066e-122">Un puntatore univoco presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="1066e-122">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="1066e-123">Il valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="1066e-123">It can have the value **null**.</span></span>
-   <span data-ttu-id="1066e-124">Può variare da **null** a non **null** durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="1066e-124">It can change from **null** to non-**null** during the call.</span></span> <span data-ttu-id="1066e-125">Quando il valore viene modificato in un valore diverso da **null**, la nuova memoria viene allocata al momento della restituzione.</span><span class="sxs-lookup"><span data-stu-id="1066e-125">When the value changes to non-**null**, new memory is allocated on return.</span></span>
-   <span data-ttu-id="1066e-126">È possibile passare da un valore diverso da **null** a **null** durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="1066e-126">It can change from non-**null** to **null** during the call.</span></span> <span data-ttu-id="1066e-127">Quando il valore viene modificato in **null**, l'applicazione è responsabile della liberazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="1066e-127">When the value changes to **NULL**, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="1066e-128">Il valore può variare da un valore non **null** a un altro.</span><span class="sxs-lookup"><span data-stu-id="1066e-128">The value can change from one non-**null** value to another.</span></span>
-   <span data-ttu-id="1066e-129">Non è possibile accedere alla risorsa di archiviazione a cui punta un puntatore univoco per qualsiasi altro puntatore o nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1066e-129">The storage that a unique pointer points to cannot be accessed by any other pointer or name in the operation.</span></span>
-   <span data-ttu-id="1066e-130">I dati restituiti vengono scritti nell'archiviazione esistente se il puntatore non ha il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="1066e-130">Return data is written into existing storage if the pointer does not have the value **null**.</span></span>

<span data-ttu-id="1066e-131">Nell'esempio seguente viene illustrato come definire un puntatore univoco.</span><span class="sxs-lookup"><span data-stu-id="1066e-131">The following example demonstrates how to define a unique pointer.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

<span data-ttu-id="1066e-132">In questo esempio il parametro *ACH* è un puntatore univoco ai dati di tipo carattere che vengono inviati a un server per l'elaborazione con la routine RemoteFn.</span><span class="sxs-lookup"><span data-stu-id="1066e-132">In this example, the parameter *ach* is a unique pointer to character data that is sent to a server to be processed with the RemoteFn routine.</span></span>

 

 