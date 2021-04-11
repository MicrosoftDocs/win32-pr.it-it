---
title: Attributo represent_as
description: L'attributo \ rappresenta \_ come \ consente di specificare la modalità di rappresentazione di un particolare tipo di dati transmittable nell'applicazione.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- RPC, attributi, represent_as di procedura remota
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118334"
---
# <a name="the-represent_as-attribute"></a><span data-ttu-id="cb392-105">Rappresenta \_ come attributo</span><span class="sxs-lookup"><span data-stu-id="cb392-105">The represent\_as Attribute</span></span>

<span data-ttu-id="cb392-106">L' \[ attributo [rappresenta \_ come](/windows/desktop/Midl/represent-as) \] consente di specificare il modo in cui un particolare tipo di dati transmittable viene rappresentato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb392-106">The \[ [represent\_as](/windows/desktop/Midl/represent-as)\] attribute lets you specify how a particular transmittable data type is represented to the application.</span></span> <span data-ttu-id="cb392-107">Questa operazione viene eseguita specificando il nome del tipo rappresentato per un tipo transmittable noto e fornendo le routine di conversione.</span><span class="sxs-lookup"><span data-stu-id="cb392-107">This is done by specifying the name of the represented type for a known transmittable type and supplying the conversion routines.</span></span> <span data-ttu-id="cb392-108">È inoltre necessario specificare le routine per liberare la memoria utilizzata dagli oggetti del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="cb392-108">You must also supply the routines to free the memory used by the data type objects.</span></span>

<span data-ttu-id="cb392-109">Utilizzare l'attributo **\[ rappresenta \_ come \]** per presentare un'applicazione con un tipo di dati diverso, possibilmente untransmittable, anziché il tipo effettivamente trasmesso tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="cb392-109">Use the **\[represent\_as\]** attribute to present an application with a different, possibly untransmittable, data type rather than the type that is actually transmitted between the client and server.</span></span> <span data-ttu-id="cb392-110">È anche possibile che il tipo modificato dall'applicazione possa essere sconosciuto al momento della compilazione MIDL.</span><span class="sxs-lookup"><span data-stu-id="cb392-110">It is also possible that the type the application manipulates can be unknown at the time of MIDL compilation.</span></span> <span data-ttu-id="cb392-111">Quando si sceglie un tipo transmittable ben definito, non è necessario preoccuparsi della rappresentazione dei dati nell'ambiente eterogeneo.</span><span class="sxs-lookup"><span data-stu-id="cb392-111">When you choose a well-defined transmittable type, you need not be concerned about data representation in the heterogeneous environment.</span></span> <span data-ttu-id="cb392-112">L'attributo **\[ rappresenta \_ come \]** può migliorare l'efficienza dell'applicazione riducendo la quantità di dati trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="cb392-112">The **\[represent\_as\]** attribute can make your application more efficient by reducing the amount of data transmitted over the network.</span></span>

<span data-ttu-id="cb392-113">L'attributo **\[ rappresenta \_ \] come** è simile all'attributo \[ [trasmissione \_ come](/windows/desktop/Midl/transmit-as) \] .</span><span class="sxs-lookup"><span data-stu-id="cb392-113">The **\[represent\_as\]** attribute is similar to the \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\] attribute.</span></span> <span data-ttu-id="cb392-114">Tuttavia, mentre **\[ trasmette \_ come \]** consente di specificare un tipo di dati che verrà usato per la trasmissione, **\[ rappresenta \_ come \]** consente di specificare la modalità di rappresentazione di un tipo di dati per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb392-114">However, while **\[transmit\_as\]** lets you specify a data type that will be used for transmission, **\[represent\_as\]** lets you specify how a data type is represented for the application.</span></span> <span data-ttu-id="cb392-115">Non è necessario definire il tipo rappresentato nei file elaborati MIDL; può essere definito nel momento in cui gli stub vengono compilati con il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="cb392-115">The represented type need not be defined in the MIDL processed files; it can be defined at the time the stubs are compiled with the C compiler.</span></span> <span data-ttu-id="cb392-116">A tale scopo, usare la direttiva include nel [file di configurazione dell'applicazione (ACF)](the-application-configuration-file-acf-.md) per compilare il file di intestazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="cb392-116">To do this, use the include directive in the [application configuration file (ACF)](the-application-configuration-file-acf-.md) to compile the appropriate header file.</span></span> <span data-ttu-id="cb392-117">Ad esempio, l'ACF seguente definisce un tipo locale per l'applicazione, **repr \_ Type**, per il tipo transmittable Type **denominato \_ :**</span><span class="sxs-lookup"><span data-stu-id="cb392-117">For example, the following ACF defines a type local to the application, **repr\_type**, for the transmittable type **named\_type:**</span></span>

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

<span data-ttu-id="cb392-118">Nella tabella seguente vengono descritte le quattro routine fornite dal programmatore.</span><span class="sxs-lookup"><span data-stu-id="cb392-118">The following table describes the four programmer-supplied routines.</span></span>



| <span data-ttu-id="cb392-119">Routine</span><span class="sxs-lookup"><span data-stu-id="cb392-119">Routine</span></span>                      | <span data-ttu-id="cb392-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb392-120">Description</span></span>                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb392-121">**\_tipo denominato \_ da \_ local**</span><span class="sxs-lookup"><span data-stu-id="cb392-121">**named\_type\_from\_local**</span></span> | <span data-ttu-id="cb392-122">Alloca un'istanza del tipo di rete e la converte dal tipo locale al tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="cb392-122">Allocates an instance of the network type and converts from the local type to the network type.</span></span>      |
| <span data-ttu-id="cb392-123">**\_tipo denominato \_ in \_ locale**</span><span class="sxs-lookup"><span data-stu-id="cb392-123">**named\_type\_to\_local**</span></span>   | <span data-ttu-id="cb392-124">Esegue la conversione dal tipo di rete al tipo locale.</span><span class="sxs-lookup"><span data-stu-id="cb392-124">Converts from the network type to the local type.</span></span>                                                    |
| <span data-ttu-id="cb392-125">**\_tipo denominato \_ Free \_ local**</span><span class="sxs-lookup"><span data-stu-id="cb392-125">**named\_type\_free\_local**</span></span> | <span data-ttu-id="cb392-126">Libera la memoria allocata da una chiamata al **\_ tipo denominato \_ alla routine \_ locale** , ma non al tipo stesso.</span><span class="sxs-lookup"><span data-stu-id="cb392-126">Frees memory allocated by a call to the **named\_type\_to\_local** routine, but not the type itself.</span></span> |
| <span data-ttu-id="cb392-127">**\_ \_ inst libero del tipo denominato \_**</span><span class="sxs-lookup"><span data-stu-id="cb392-127">**named\_type\_free\_inst**</span></span>  | <span data-ttu-id="cb392-128">Libera lo spazio di archiviazione per il tipo di rete (entrambi i lati).</span><span class="sxs-lookup"><span data-stu-id="cb392-128">Frees storage for the network type (both sides).</span></span>                                                     |



 

<span data-ttu-id="cb392-129">Ad eccezione di queste quattro routine fornite dal programmatore, il tipo denominato non viene modificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb392-129">Other than by these four programmer-supplied routines, the named type is not manipulated by the application.</span></span> <span data-ttu-id="cb392-130">L'unico tipo visibile all'applicazione è il tipo rappresentato.</span><span class="sxs-lookup"><span data-stu-id="cb392-130">The only type visible to the application is the represented type.</span></span> <span data-ttu-id="cb392-131">L'applicazione usa il nome del tipo rappresentato anziché il nome del tipo trasmesso nei prototipi e negli stub generati dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="cb392-131">The application uses the represented type name instead of the transmitted type name in the prototypes and stubs generated by the compiler.</span></span> <span data-ttu-id="cb392-132">È necessario fornire il set di routine per entrambi i lati.</span><span class="sxs-lookup"><span data-stu-id="cb392-132">You must supply the set of routines for both sides.</span></span>

<span data-ttu-id="cb392-133">Per gli oggetti di **\_ tipo denominato** temporaneo, lo stub chiamerà il **\_ tipo denominato \_ \_ inst Free** per liberare la memoria allocata da una chiamata al **\_ tipo denominato \_ da \_ local**.</span><span class="sxs-lookup"><span data-stu-id="cb392-133">For temporary **named\_type** objects, the stub will call **named\_type\_free\_inst** to free any memory allocated by a call to **named\_type\_from\_local**.</span></span>

<span data-ttu-id="cb392-134">Se il tipo rappresentato è un puntatore o contiene un puntatore, il **\_ tipo denominato \_ alla routine \_ locale** deve allocare memoria per i dati a cui puntatori (l'oggetto di tipo rappresentato stesso viene modificato dallo stub nel modo consueto).</span><span class="sxs-lookup"><span data-stu-id="cb392-134">If the represented type is a pointer or contains a pointer, the **named\_type\_to\_local** routine must allocate memory for the data to which the pointers point (the represented type object itself is manipulated by the stub in the usual way).</span></span> <span data-ttu-id="cb392-135">Per \[ [out](/windows/desktop/Midl/out-idl) \] e \[ [in](/windows/desktop/Midl/in), \] i parametri out di un tipo che contengono **\[ rappresentano \_ come** o uno dei suoi componenti, **il \_ tipo denominato \_ Free \_ local** routine viene chiamato automaticamente per gli oggetti dati che contengono l'attributo.</span><span class="sxs-lookup"><span data-stu-id="cb392-135">For \[ [out](/windows/desktop/Midl/out-idl)\] and \[ [in](/windows/desktop/Midl/in), out\] parameters of a type that contain **\[represent\_as** or one of its components, the **named\_type\_free\_local** routine is automatically called for the data objects that contain the attribute.</span></span> <span data-ttu-id="cb392-136">Per i parametri **\[ in \]** , **il \_ tipo denominato \_ Free \_ local** routine viene chiamato solo se l'attributo **\[ rappresenta \_ come \]** è stato applicato al parametro.</span><span class="sxs-lookup"><span data-stu-id="cb392-136">For **\[in\]** parameters, the **named\_type\_free\_local** routine is called only if the **\[represent\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="cb392-137">Se l'attributo è stato applicato ai componenti del parametro, la routine *\* \*\*\* \_ \_ locale gratuita*\* non viene chiamata.</span><span class="sxs-lookup"><span data-stu-id="cb392-137">If the attribute has been applied to the components of the parameter, the *\*\*\*\*\_free\_local*\* routine is not called.</span></span> <span data-ttu-id="cb392-138">Le routine di liberazione non vengono chiamate per i dati incorporati e la chiamata at-most-once (correlata all'attributo di primo livello) **\[ \] per un solo** parametro.</span><span class="sxs-lookup"><span data-stu-id="cb392-138">Freeing routines are not called for the embedded data and at-most-once call (related to the top-level attribute) for an **\[in\]** only parameter.</span></span>

> [!Note]  
> <span data-ttu-id="cb392-139">È possibile applicare sia la **\[ trasmissione \_ che \]** la **\[ rappresentazione \_ come \]** attributi allo stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="cb392-139">It is possible to apply both the **\[transmit\_as\]** and **\[represent\_as\]** attributes to the same type.</span></span> <span data-ttu-id="cb392-140">Quando si effettua il marshalling dei dati, l'oggetto **\[ rappresenta \_ come \]** conversione del tipo viene applicato per primo e quindi viene applicata la **\[ trasmissione \_ come \]** conversione.</span><span class="sxs-lookup"><span data-stu-id="cb392-140">When marshaling data, the **\[represent\_as\]** type conversion is applied first and then the **\[transmit\_as\]** conversion is applied.</span></span> <span data-ttu-id="cb392-141">L'ordine viene invertito durante l'annullamento del marshalling dei dati.</span><span class="sxs-lookup"><span data-stu-id="cb392-141">The order is reversed when unmarshaling data.</span></span> <span data-ttu-id="cb392-142">Pertanto, quando si effettua il marshalling, \* **\_ da \_ local** alloca un'istanza di un tipo denominato e la converte da un oggetto di tipo locale all'oggetto di tipo denominato temporaneo.</span><span class="sxs-lookup"><span data-stu-id="cb392-142">Thus, when marshaling, \***\_from\_local** allocates an instance of a named type and translates it from a local type object to the temporary named type object.</span></span> <span data-ttu-id="cb392-143">Questo oggetto è l'oggetto tipo presentato usato per la \* routine **\_ to \_ Xmit** .</span><span class="sxs-lookup"><span data-stu-id="cb392-143">This object is the presented type object used for the \***\_to\_xmit** routine.</span></span> <span data-ttu-id="cb392-144">La \* routine **\_ to \_ Xmit** quindi alloca un oggetto tipo trasmesso e lo converte dall'oggetto presentato (denominato) all'oggetto trasmesso.</span><span class="sxs-lookup"><span data-stu-id="cb392-144">The \***\_to\_xmit** routine then allocates a transmitted type object and translates it from the presented (named) object to the transmitted object.</span></span>

 

<span data-ttu-id="cb392-145">Una matrice di valori long integer può essere usata per rappresentare un elenco collegato.</span><span class="sxs-lookup"><span data-stu-id="cb392-145">An array of long integers can be used to represent a linked list.</span></span> <span data-ttu-id="cb392-146">In questo modo, l'applicazione modifica l'elenco e la trasmissione usa una matrice di valori long integer quando viene trasmesso un elenco di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="cb392-146">In this way, the application manipulates the list, and the transmission uses an array of long integers when a list of this type is transmitted.</span></span> <span data-ttu-id="cb392-147">È possibile iniziare con una matrice, ma è più facile usare un costrutto con una matrice aperta di valori long integer.</span><span class="sxs-lookup"><span data-stu-id="cb392-147">You can begin with an array, but using a construct with an open array of long integers is more convenient.</span></span> <span data-ttu-id="cb392-148">L'esempio seguente illustra come farlo.</span><span class="sxs-lookup"><span data-stu-id="cb392-148">The following example shows how to do this.</span></span>

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

<span data-ttu-id="cb392-149">Si noti che i prototipi delle routine che usano il tipo **LONGARR** vengono effettivamente visualizzati nei file stub. h come **ploc \_ Box** al posto del tipo **LONGARR** .</span><span class="sxs-lookup"><span data-stu-id="cb392-149">Note that the prototypes of the routines that use the **LONGARR** type are actually displayed in the Stub.h files as **PLOC\_BOX** in place of the **LONGARR** type.</span></span> <span data-ttu-id="cb392-150">Lo stesso vale per gli stub appropriati nel \_ file c. c dello stub.</span><span class="sxs-lookup"><span data-stu-id="cb392-150">The same is true of the appropriate stubs in the Stub\_c.c file.</span></span>

<span data-ttu-id="cb392-151">È necessario fornire le quattro funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb392-151">You must supply the following four functions:</span></span>

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

<span data-ttu-id="cb392-152">Le routine illustrate in precedenza eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb392-152">The routines shown above do the following:</span></span>

-   <span data-ttu-id="cb392-153">**LONGARR \_ dalla routine \_ locale** conta i nodi dell'elenco, alloca un oggetto LONGARR con le dimensioni **sizeof**(**LONGARR**) + Count \* **sizeof**(**Long**), imposta il campo delle **dimensioni** su Count e copia i dati nel campo **DataArr** .</span><span class="sxs-lookup"><span data-stu-id="cb392-153">The **LONGARR\_from\_local** routine counts the nodes of the list, allocates a LONGARR object with the size **sizeof**(**LONGARR**) + Count\***sizeof**(**long**), sets the **Size** field to Count, and copies the data to the **DataArr** field.</span></span>
-   <span data-ttu-id="cb392-154">La routine **LONGARR \_ to \_ local** crea un elenco con nodi di dimensioni e trasferisce la matrice ai nodi appropriati.</span><span class="sxs-lookup"><span data-stu-id="cb392-154">The **LONGARR\_to\_local** routine creates a list with Size nodes and transfers the array to the appropriate nodes.</span></span>
-   <span data-ttu-id="cb392-155">In questo caso la routine **\_ \_ inst Free di LONGARR** non consente di liberare nulla.</span><span class="sxs-lookup"><span data-stu-id="cb392-155">The **LONGARR\_free\_inst** routine frees nothing in this case.</span></span>
-   <span data-ttu-id="cb392-156">La **routine \_ \_ locale gratuita LONGARR** libera tutti i nodi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="cb392-156">The **LONGARR\_free\_local** routine frees all the nodes of the list.</span></span>

 

 