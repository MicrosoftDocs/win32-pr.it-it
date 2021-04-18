---
title: Attributo transmit_as
description: L'attributo \ trasmette \_ come \ consente di controllare il marshalling dei dati senza doversi preoccupare del marshalling dei dati a un livello basso, ovvero senza doversi preoccupare delle dimensioni dei dati o dello scambio di byte in un ambiente eterogeneo.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- RPC, attributi, transmit_as di procedura remota
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399421"
---
# <a name="the-transmit_as-attribute"></a><span data-ttu-id="4c7c9-105">Attributo trasmissione \_ As</span><span class="sxs-lookup"><span data-stu-id="4c7c9-105">The transmit\_as Attribute</span></span>

<span data-ttu-id="4c7c9-106">L' **\[** attributo [**trasmissione \_ As**](/windows/desktop/Midl/transmit-as) **\]** offre un modo per controllare il marshalling dei dati senza doversi preoccupare del marshalling dei dati a un livello basso, ovvero senza preoccuparsi delle dimensioni dei dati o dello scambio di byte in un ambiente eterogeneo.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-106">The **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute offers a way to control data marshaling without worrying about marshaling data at a low level—that is, without worrying about data sizes or byte swapping in a heterogeneous environment.</span></span> <span data-ttu-id="4c7c9-107">Consentendo di ridurre la quantità di dati trasmessi in rete, l'attributo **\[ trasmissione \_ come \]** può rendere più efficiente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-107">By letting you reduce the amount of data transmitted over the network, the **\[transmit\_as\]** attribute can make your application more efficient.</span></span>

<span data-ttu-id="4c7c9-108">Utilizzare l'attributo **\[ trasmissione \_ As \]** per specificare un tipo di dati che gli stub RPC trasmetteranno sulla rete anziché utilizzare il tipo di dati fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-108">You use the **\[transmit\_as\]** attribute to specify a data type that the RPC stubs will transmit over the network instead of using the data type provided by the application.</span></span> <span data-ttu-id="4c7c9-109">Vengono fornite routine che convertono il tipo di dati da e verso il tipo utilizzato per la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-109">You supply routines that convert the data type to and from the type that is used for transmission.</span></span> <span data-ttu-id="4c7c9-110">È inoltre necessario specificare routine per liberare la memoria utilizzata per il tipo di dati e il tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-110">You must also supply routines to free the memory used for the data type and the transmitted type.</span></span> <span data-ttu-id="4c7c9-111">Ad esempio, di seguito viene definito il **\_ tipo Xmit** come tipo di dati trasmesso per tutti i dati dell'applicazione specificati come tipo **\_ spec**:</span><span class="sxs-lookup"><span data-stu-id="4c7c9-111">For example, the following defines **xmit\_type** as the data type transmitted for all application data specified as being of type **type\_spec**:</span></span>

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

<span data-ttu-id="4c7c9-112">Nella tabella seguente vengono descritti i quattro nomi di routine forniti dal programmatore.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-112">The following table describes the four programmer-supplied routine names.</span></span> <span data-ttu-id="4c7c9-113">Il **tipo è il** tipo di dati noto all'applicazione e **Xmit \_ tipo** è il tipo di dati utilizzato per la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-113">**Type** is the data type known to the application, and **xmit\_type** is the data type used for transmission.</span></span>



| <span data-ttu-id="4c7c9-114">Routine</span><span class="sxs-lookup"><span data-stu-id="4c7c9-114">Routine</span></span>                                                 | <span data-ttu-id="4c7c9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c7c9-115">Description</span></span>                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c7c9-116">**Digitare \_ per \_ Xmit**</span><span class="sxs-lookup"><span data-stu-id="4c7c9-116">**type\_to\_xmit**</span></span>](the-type-to-xmit-function.md)     | <span data-ttu-id="4c7c9-117">Alloca un oggetto del tipo trasmesso e viene convertito dal tipo di applicazione al tipo trasmesso sulla rete (chiamante e oggetto chiamato).</span><span class="sxs-lookup"><span data-stu-id="4c7c9-117">Allocates an object of the transmitted type and converts from application type to type transmitted over the network (caller and object called).</span></span> |
| [<span data-ttu-id="4c7c9-118">**Digitare \_ da \_ Xmit**</span><span class="sxs-lookup"><span data-stu-id="4c7c9-118">**Type\_from\_xmit**</span></span>](the-type-from-xmit-function.md) | <span data-ttu-id="4c7c9-119">Esegue la conversione dal tipo trasmesso al tipo di applicazione (chiamante e oggetto denominato).</span><span class="sxs-lookup"><span data-stu-id="4c7c9-119">Converts from transmitted type to application type (caller and object called).</span></span>                                                                  |
| [<span data-ttu-id="4c7c9-120">**Digitare \_ Free \_ inst**</span><span class="sxs-lookup"><span data-stu-id="4c7c9-120">**Type\_free\_inst**</span></span>](the-type-free-inst-function.md) | <span data-ttu-id="4c7c9-121">Libera le risorse utilizzate dal tipo di applicazione (solo oggetto chiamato).</span><span class="sxs-lookup"><span data-stu-id="4c7c9-121">Frees resources used by the application type (object called only).</span></span>                                                                              |
| [<span data-ttu-id="4c7c9-122">**Digitare \_ Free \_ Xmit**</span><span class="sxs-lookup"><span data-stu-id="4c7c9-122">**Type\_free\_xmit**</span></span>](the-type-free-xmit-function.md) | <span data-ttu-id="4c7c9-123">Libera lo spazio di archiviazione restituito dal **tipo ***\_*** alla routine \_ Xmit** (chiamante e oggetto chiamato).</span><span class="sxs-lookup"><span data-stu-id="4c7c9-123">Frees storage returned by the **type ***\_*** to\_xmit** routine (caller and object called).</span></span>                                                      |



 

<span data-ttu-id="4c7c9-124">Oltre a queste quattro funzioni fornite dal programmatore, il tipo trasmesso non viene modificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-124">Other than by these four programmer-supplied functions, the transmitted type is not manipulated by the application.</span></span> <span data-ttu-id="4c7c9-125">Il tipo trasmesso viene definito solo per lo spostamento dei dati sulla rete.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-125">The transmitted type is defined only to move data over the network.</span></span> <span data-ttu-id="4c7c9-126">Dopo la conversione dei dati nel tipo utilizzato dall'applicazione, la memoria utilizzata dal tipo trasmesso viene liberata.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-126">After the data is converted to the type used by the application, the memory used by the transmitted type is freed.</span></span>

<span data-ttu-id="4c7c9-127">Queste routine fornite dal programmatore vengono fornite dal client o dall'applicazione server basata sugli attributi direzionali.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span> <span data-ttu-id="4c7c9-128">Se il parametro è **\[** solo [**in**](/windows/desktop/Midl/in) **\]** , il client trasmette al server.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-128">If the parameter is **\[**[**in**](/windows/desktop/Midl/in)**\]** only, the client transmits to the server.</span></span> <span data-ttu-id="4c7c9-129">Il client richiede **che il \_ tipo \_ Xmit** e **digiti le funzioni \_ \_ Xmit gratuite** .</span><span class="sxs-lookup"><span data-stu-id="4c7c9-129">The client needs the **type\_to\_xmit** and **type\_free\_xmit** functions.</span></span> <span data-ttu-id="4c7c9-130">Il server richiede il **tipo \_ di \_ Xmit** e **digita le funzioni \_ \_ inst gratuite** .</span><span class="sxs-lookup"><span data-stu-id="4c7c9-130">The server needs the **type\_from\_xmit** and **type\_free\_inst** functions.</span></span> <span data-ttu-id="4c7c9-131">Per un **\[** [](/windows/desktop/Midl/out-idl) **\]** parametro di sola uscita, il server trasmette al client.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-131">For an **\[**[**out**](/windows/desktop/Midl/out-idl)**\]**-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="4c7c9-132">L'applicazione server deve implementare il **tipo \_ in \_ Xmit** e **digitare \_ funzioni \_ Xmit gratuite** , mentre il programma client deve fornire il **tipo \_ dalla funzione \_ Xmit** .</span><span class="sxs-lookup"><span data-stu-id="4c7c9-132">The server application must implement the **type\_to\_xmit** and **type\_free\_xmit** functions, while the client program must supply the **type\_from\_xmit** function.</span></span> <span data-ttu-id="4c7c9-133">Per gli oggetti **di \_ tipo Xmit** temporaneo, lo stub chiamerà **il ***\_*** tipo Free \_ Xmit** per liberare la memoria allocata da una chiamata al **tipo \_ a \_ Xmit**.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-133">For the temporary **xmit\_type** objects, the stub will call **type ***\_*** free\_xmit** to free any memory allocated by a call to **type\_to\_xmit**.</span></span>

<span data-ttu-id="4c7c9-134">Alcune linee guida si applicano all'istanza del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-134">Certain guidelines apply to the application type instance.</span></span> <span data-ttu-id="4c7c9-135">Se il tipo di applicazione è un puntatore o contiene un puntatore, il **tipo** \_ **dalla routine \_ Xmit** deve allocare memoria per i dati a cui puntano i puntatori (l'oggetto del tipo di applicazione stesso viene modificato dallo stub nel modo consueto).</span><span class="sxs-lookup"><span data-stu-id="4c7c9-135">If the application type is a pointer or contains a pointer, then the **type**\_**from\_xmit** routine must allocate memory for the data that the pointers point to (the application type object itself is manipulated by the stub in the usual way).</span></span>

<span data-ttu-id="4c7c9-136">Per **\[ out \]** e **\[ in, parametri \] out \]** out o uno dei rispettivi componenti di un tipo che contiene l'attributo **\[ trasmissione \_ As \]** , la routine  \_ **\_ inst gratuita** del tipo viene chiamata automaticamente per gli oggetti dati che hanno l'attributo.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-136">For **\[out\]** and **\[in, out\] out\]** parameters, or one of their components, of a type that contains the **\[transmit\_as\]** attribute, the **type**\_**free\_inst** routine is automatically called for the data objects that have the attribute.</span></span> <span data-ttu-id="4c7c9-137">Per i parametri **in** , la \_ **routine \_ inst Free** del tipo viene chiamata solo se l'attributo **\[ trasmissione \_ \] As** è stato applicato al parametro.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-137">For **in** parameters, the **type**\_**free\_inst** routine is called only if the **\[transmit\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="4c7c9-138">Se l'attributo è stato applicato ai componenti del parametro, la  \_ routine **\_ inst Free** del tipo non viene chiamata.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-138">If the attribute has been applied to the components of the parameter, the **type**\_**free\_inst** routine is not called.</span></span> <span data-ttu-id="4c7c9-139">Non sono disponibili chiamate gratuite per i dati incorporati e una chiamata al massimo uno (correlato all'attributo di primo livello) **per un solo** parametro.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-139">There are no freeing calls for the embedded data and at-most-one call (related to the top-level attribute) for an **in** only parameter.</span></span>

<span data-ttu-id="4c7c9-140">A partire da MIDL 2,0, sia il client che il server devono fornire tutte e quattro le funzioni.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-140">Effective with MIDL 2.0, both client and server must supply all four functions.</span></span> <span data-ttu-id="4c7c9-141">Un elenco collegato, ad esempio, può essere trasmesso come matrice di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-141">For example, a linked list can be transmitted as a sized array.</span></span> <span data-ttu-id="4c7c9-142">Il **tipo \_ per \_** la routine Xmit esamina l'elenco collegato e copia i dati ordinati in una matrice.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-142">The **type\_to\_xmit** routine walks the linked list and copies the ordered data into an array.</span></span> <span data-ttu-id="4c7c9-143">Gli elementi della matrice vengono ordinati in modo che i molti puntatori associati alla struttura elenco non debbano essere trasmessi.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-143">The array elements are ordered so that the many pointers associated with the list structure do not have to be transmitted.</span></span> <span data-ttu-id="4c7c9-144">Il **tipo \_ dalla routine \_ Xmit** legge la matrice e inserisce i relativi elementi in una struttura di elenco collegato.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-144">The **type\_from\_xmit** routine reads the array and puts its elements into a linked-list structure.</span></span>

<span data-ttu-id="4c7c9-145">L'elenco \_ a collegamento doppio ( \_ elenco di collegamenti doppi) include i dati e i puntatori agli elementi elenco precedente e successivo:</span><span class="sxs-lookup"><span data-stu-id="4c7c9-145">The double-linked list (DOUBLE\_LINK\_LIST) includes data and pointers to the previous and next list elements:</span></span>

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

<span data-ttu-id="4c7c9-146">Anziché spedire la struttura complessa, l' **\[** attributo [**trasmissione \_ As**](/windows/desktop/Midl/transmit-as) **\]** può essere usato per inviarlo tramite la rete come matrice.</span><span class="sxs-lookup"><span data-stu-id="4c7c9-146">Rather than shipping the complex structure, the **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute can be used to send it over the network as an array.</span></span> <span data-ttu-id="4c7c9-147">La sequenza di elementi nella matrice mantiene l'ordine degli elementi nell'elenco a un costo inferiore:</span><span class="sxs-lookup"><span data-stu-id="4c7c9-147">The sequence of items in the array retains the ordering of the elements in the list at a lower cost:</span></span>

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

<span data-ttu-id="4c7c9-148">L'attributo **\[ trasmissione \_ come \]** viene visualizzato nel file IDL:</span><span class="sxs-lookup"><span data-stu-id="4c7c9-148">The **\[transmit\_as\]** attribute appears in the IDL file:</span></span>

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

<span data-ttu-id="4c7c9-149">Nell'esempio seguente **ModifyListProc** definisce il parametro di tipo Double \_ link \_ come parametro **\[ in, out \]** :</span><span class="sxs-lookup"><span data-stu-id="4c7c9-149">In the following example, **ModifyListProc** defines the parameter of type DOUBLE\_LINK\_TYPE as an **\[in, out\]** parameter:</span></span>

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

<span data-ttu-id="4c7c9-150">Le quattro funzioni definite dal programmatore utilizzano il nome del tipo nei nomi di funzione e utilizzano i tipi presentati e trasmessi come tipi di parametro, come richiesto:</span><span class="sxs-lookup"><span data-stu-id="4c7c9-150">The four programmer-defined functions use the name of the type in the function names, and use the presented and transmitted types as parameter types, as required:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 