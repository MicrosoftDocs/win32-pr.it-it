---
description: Individuazione delle partizioni durante l'attivazione
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Individuazione delle partizioni durante l'attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561163"
---
# <a name="locating-partitions-during-activation"></a><span data-ttu-id="ba02d-103">Individuazione delle partizioni durante l'attivazione</span><span class="sxs-lookup"><span data-stu-id="ba02d-103">Locating Partitions During Activation</span></span>

<span data-ttu-id="ba02d-104">Individuare la partizione corretta in cui attivare un componente dipende da quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ba02d-104">Locating the correct partition in which to activate a component depends on the following:</span></span>

-   <span data-ttu-id="ba02d-105">La chiamata di funzione e i parametri usati nel programma chiamante per attivare il componente</span><span class="sxs-lookup"><span data-stu-id="ba02d-105">The function call and parameters used in the calling program to activate the component</span></span>
-   <span data-ttu-id="ba02d-106">Indica se il componente attivato è locale o remoto</span><span class="sxs-lookup"><span data-stu-id="ba02d-106">Whether the component being activated is local or remote</span></span>
-   <span data-ttu-id="ba02d-107">Uso interno della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="ba02d-107">The internal use of the partition cache</span></span>

## <a name="the-calling-program"></a><span data-ttu-id="ba02d-108">Programma chiamante</span><span class="sxs-lookup"><span data-stu-id="ba02d-108">The Calling Program</span></span>

<span data-ttu-id="ba02d-109">COM+ seleziona la partizione per l'attivazione dei componenti in base alla modalità di attivazione del componente da parte del programma chiamante.</span><span class="sxs-lookup"><span data-stu-id="ba02d-109">COM+ selects the partition for component activation based on how the calling program activates the component.</span></span>

<span data-ttu-id="ba02d-110">Sono disponibili tre diverse azioni che possono essere eseguite da COM+ quando si seleziona una partizione per l'attivazione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="ba02d-110">There are three different actions that COM+ can take when selecting a partition for component activation.</span></span> <span data-ttu-id="ba02d-111">L'azione eseguita dipende dalla modalità con cui il programma chiamante crea un'istanza dell'oggetto, ovvero se la chiamata di funzione include un moniker della partizione, costituito da un ID di partizione e un CLSID, oppure include solo un CLSID.</span><span class="sxs-lookup"><span data-stu-id="ba02d-111">The action taken depends on how the calling program instantiates the object that is, whether the function call includes a partition moniker, which consists of a partition ID and a CLSID, or includes a CLSID only.</span></span>

<span data-ttu-id="ba02d-112">Nella tabella seguente vengono illustrate le varie azioni che COM+ può intraprendere, in ordine di precedenza, per individuare una partizione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-112">The following table shows the various actions that COM+ can take, in order of precedence, to locate a partition.</span></span>



| <span data-ttu-id="ba02d-113">Chiamata di funzione</span><span class="sxs-lookup"><span data-stu-id="ba02d-113">Function call</span></span>                                                  | <span data-ttu-id="ba02d-114">Parametro</span><span class="sxs-lookup"><span data-stu-id="ba02d-114">Parameter</span></span>                                                      | <span data-ttu-id="ba02d-115">Azione COM+</span><span class="sxs-lookup"><span data-stu-id="ba02d-115">COM+ action</span></span>                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba02d-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) o **GetObject**</span><span class="sxs-lookup"><span data-stu-id="ba02d-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) or **GetObject**</span></span><br/> | <span data-ttu-id="ba02d-117">Moniker partizione (include ID partizione e CLSID)</span><span class="sxs-lookup"><span data-stu-id="ba02d-117">Partition moniker (includes partition ID and CLSID)</span></span><br/> | <span data-ttu-id="ba02d-118">Usa l'ID di partizione specificato nel moniker della partizione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-118">Uses the partition ID specified in the partition moniker.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="ba02d-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ba02d-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | <span data-ttu-id="ba02d-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="ba02d-120">CLSID</span></span><br/>                                               | <span data-ttu-id="ba02d-121">Usa l'ID di partizione della partizione predefinita dell'identità utente o l'ID di partizione aggiunto al contesto durante un'attivazione del componente precedente nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="ba02d-121">Uses either the partition ID of the user identity's default partition or the partition ID that was added to the context during a previous component activation in the same process.</span></span><br/> |



 

<span data-ttu-id="ba02d-122">Nelle sezioni seguenti vengono descritte le azioni COM+ elencate nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="ba02d-122">The COM+ actions listed in the preceding table are explained in the following sections.</span></span>

## <a name="use-of-partition-monikers"></a><span data-ttu-id="ba02d-123">Uso dei moniker della partizione</span><span class="sxs-lookup"><span data-stu-id="ba02d-123">Use of Partition Monikers</span></span>

<span data-ttu-id="ba02d-124">Una partizione può essere selezionata in modo esplicito all'interno di una chiamata di funzione usando un *moniker della partizione*.</span><span class="sxs-lookup"><span data-stu-id="ba02d-124">A partition can be selected explicitly within a function call by using a *partition moniker*.</span></span> <span data-ttu-id="ba02d-125">Un moniker di partizione viene usato all'interno del codice per specificare in modo esplicito la partizione del componente attivato.</span><span class="sxs-lookup"><span data-stu-id="ba02d-125">A partition moniker is used within code to explicitly specify the partition of the activated component.</span></span> <span data-ttu-id="ba02d-126">Se per individuare la partizione viene utilizzato un moniker della partizione, l'attivazione viene eseguita da tale partizione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-126">If a partition moniker is used to locate the partition, the activation occurs from that partition.</span></span> <span data-ttu-id="ba02d-127">Ovvero, l'ID partizione incluso nel moniker ha la precedenza sulla partizione predefinita dell'utente o su un ID di partizione esistente nel contesto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="ba02d-127">That is, the partition ID included in the moniker takes precedence over the user's default partition or over a partition ID that exists in the caller's context.</span></span>

<span data-ttu-id="ba02d-128">Nel codice C++, la sintassi per l'uso di un moniker di partizione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="ba02d-128">In C++ code, the syntax for the use of a partition moniker is as follows:</span></span>


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



<span data-ttu-id="ba02d-129">Nell'esempio seguente viene illustrato un frammento di codice C++, in cui un moniker di partizione viene usato come argomento per la funzione [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :</span><span class="sxs-lookup"><span data-stu-id="ba02d-129">The following example shows a snippet of C++ code, in which a partition moniker is being used as an argument to the [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function:</span></span>


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



<span data-ttu-id="ba02d-130">Nel codice Visual Basic la sintassi per un moniker di partizione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="ba02d-130">In Visual Basic code, the syntax for a partition moniker is as follows:</span></span>


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



<span data-ttu-id="ba02d-131">Nell'esempio seguente viene illustrato un frammento di codice di Visual Basic, in cui un moniker della partizione viene usato come argomento della funzione **GetObject** :</span><span class="sxs-lookup"><span data-stu-id="ba02d-131">The following example shows a snippet of Visual Basic code, in which a partition moniker is being used as an argument to the **GetObject** function:</span></span>


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a><span data-ttu-id="ba02d-132">Utilizzo del mapping predefinito</span><span class="sxs-lookup"><span data-stu-id="ba02d-132">Use of Default Mapping</span></span>

<span data-ttu-id="ba02d-133">Quando la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) viene utilizzata per attivare un componente, utilizzando il CLSID del componente, com+ utilizza il mapping dell'identità utente predefinito, ovvero il set di partizioni a cui l'utente è mappato all'interno Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ba02d-133">When the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function is used to activate a component, using the component's CLSID, COM+ uses the default user-identity mapping that is, the partition set that the user is mapped to within Active Directory.</span></span> <span data-ttu-id="ba02d-134">Tuttavia, se l'utente non è mappato a un set di partizioni all'interno Active Directory, viene selezionata la partizione globale.</span><span class="sxs-lookup"><span data-stu-id="ba02d-134">However, if the user is not mapped to a partition set within Active Directory, the Global Partition is selected.</span></span>

## <a name="use-of-partition-ids-and-object-context"></a><span data-ttu-id="ba02d-135">Uso degli ID di partizione e del contesto dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="ba02d-135">Use of Partition IDs and Object Context</span></span>

<span data-ttu-id="ba02d-136">Una delle cinque proprietà assegnate a una nuova partizione è l'ID della partizione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-136">One of the five properties assigned to a new partition is the partition ID.</span></span> <span data-ttu-id="ba02d-137">Quando il programma client chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza di un oggetto, l'ID partizione viene aggiunto al contesto.</span><span class="sxs-lookup"><span data-stu-id="ba02d-137">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to instantiate an object, the partition ID is added to the context.</span></span> <span data-ttu-id="ba02d-138">L'uso dell'ID partizione dal contesto per individuare la partizione è importante perché garantisce che dopo l'avvio di una catena di attivazioni l'ID di partizione rimanga invariato, a meno che non venga modificato in modo esplicito tramite un moniker della partizione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-138">Using the partition ID from the context to locate the partition is important because it ensures that after a chain of activations has begun, the partition ID remains the same unless it is changed explicitly through a partition moniker.</span></span>

<span data-ttu-id="ba02d-139">Per ulteriori informazioni sull'individuazione delle partizioni durante l'attivazione, vedere [componenti e partizioni in coda com+](com--queued-components-and-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="ba02d-139">For additional information on locating partitions during activation, see [COM+ Queued Components and Partitions](com--queued-components-and-partitions.md).</span></span>

## <a name="local-and-remote-activation"></a><span data-ttu-id="ba02d-140">Attivazione locale e remota</span><span class="sxs-lookup"><span data-stu-id="ba02d-140">Local and Remote Activation</span></span>

-   <span data-ttu-id="ba02d-141">Se il componente chiamato è presente in un altro computer, viene effettuato il marshalling delle proprietà della partizione (incluso l'ID partizione) nell'altro computer e il componente viene attivato dalla partizione sottoposta a marshalling.</span><span class="sxs-lookup"><span data-stu-id="ba02d-141">If the component being called exists on another computer, the partition properties (including the partition ID) are marshaled to the other computer and the component is activated from the marshaled partition.</span></span> <span data-ttu-id="ba02d-142">Se non è stato eseguito il marshalling di un ID di partizione, COM+ utilizza il set di partizioni predefinito mappato all'identità utente all'interno Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ba02d-142">If no partition ID was marshaled, COM+ uses the default partition set mapped to the user identity within Active Directory.</span></span>

## <a name="the-partition-cache"></a><span data-ttu-id="ba02d-143">Cache della partizione</span><span class="sxs-lookup"><span data-stu-id="ba02d-143">The Partition Cache</span></span>

<span data-ttu-id="ba02d-144">In un ambiente di dominio, COM+ utilizza i mapping in Active Directory per individuare la partizione corretta per l'attivazione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="ba02d-144">In a domain environment, COM+ uses the mappings in Active Directory to locate the correct partition for component activation.</span></span> <span data-ttu-id="ba02d-145">Tuttavia, le ricerche frequenti in Active Directory possono causare un traffico di rete eccessivo.</span><span class="sxs-lookup"><span data-stu-id="ba02d-145">However, frequent lookups in Active Directory can result in excessive network traffic.</span></span> <span data-ttu-id="ba02d-146">Per ridurre al minimo il traffico di rete risultante da ricerche frequenti di mapping di set da utente a partizione in Active Directory, COM+ usa una *cache di partizione*.</span><span class="sxs-lookup"><span data-stu-id="ba02d-146">To minimize network traffic resulting from frequent lookups of user-to-partition-set mapping in Active Directory, COM+ uses a *partition cache*.</span></span>

<span data-ttu-id="ba02d-147">La cache di partizione contiene i mapping eseguiti in Active Directory tra identità utente o unità organizzative e i relativi set di partizioni.</span><span class="sxs-lookup"><span data-stu-id="ba02d-147">The partition cache contains the mappings that were made in Active Directory between user identities or OUs and their partition sets.</span></span> <span data-ttu-id="ba02d-148">Questa cache di partizione si trova nel server applicazioni in cui risiedono le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="ba02d-148">This partition cache is located on the application server on which the COM+ applications reside.</span></span>

<span data-ttu-id="ba02d-149">Quando COM+ deve determinare la partizione predefinita di un utente o convalidare i diritti di accesso di un utente per una partizione, controlla la cache della partizione in locale per cercare il mapping dell'utente, invece di controllare Active Directory in remoto.</span><span class="sxs-lookup"><span data-stu-id="ba02d-149">When COM+ needs to determine a user's default partition or validate a user's access rights to a partition, it checks the partition cache locally to look up the user's mapping, instead of checking Active Directory remotely.</span></span>

<span data-ttu-id="ba02d-150">Se la ricerca nella cache della partizione ha esito negativo, COM+ controlla Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ba02d-150">If the lookup in the partition cache fails, COM+ then checks Active Directory.</span></span> <span data-ttu-id="ba02d-151">Se la ricerca ha esito positivo in Active Directory, COM+ archivia tale mapping nella cache della partizione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-151">If the lookup is successful in Active Directory, COM+ stores that mapping in the partition cache.</span></span> <span data-ttu-id="ba02d-152">La volta successiva che viene eseguita una ricerca per il mapping da utente a partizione, COM+ lo troverà nella cache della partizione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-152">The next time a lookup is done for that user-to-partition mapping, COM+ will find it in the partition cache.</span></span>

<span data-ttu-id="ba02d-153">Nella figura seguente viene illustrato il processo utilizzato da COM+ per individuare una partizione per l'attivazione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="ba02d-153">The following illustration shows the process that COM+ uses to locate a partition for component activation.</span></span>

![Diagramma che mostra un albero per la risoluzione dei problemi per il processo utilizzato da COM+ per individuare una partizione per l'attivazione dei componenti.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

<span data-ttu-id="ba02d-155">Le dimensioni della cache e l'ora di scadenza per le voci della cache vengono impostate tramite le chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ba02d-155">The size of the cache and the expiration time for the cache entries are set via registry keys.</span></span> <span data-ttu-id="ba02d-156">Per informazioni sulla configurazione di queste chiavi del registro di sistema, vedere [creazione e configurazione di partizioni com+](creating-and-configuring-com--partitions.md).</span><span class="sxs-lookup"><span data-stu-id="ba02d-156">For information on configuring these registry keys, see [Creating and Configuring COM+ Partitions](creating-and-configuring-com--partitions.md).</span></span>

> [!Note]  
> <span data-ttu-id="ba02d-157">Se un computer server è disconnesso dalla rete e il mapping tra utente e partizione viene modificato mentre il server è disconnesso, la cache della partizione potrebbe contenere un mapping da utente a partizione obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ba02d-157">If a server computer is disconnected from the network and the user-to-partition mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition mapping.</span></span> <span data-ttu-id="ba02d-158">Questo potrebbe causare un errore di attivazione se il mapping da utente a partizione è il meccanismo usato per attivare un componente.</span><span class="sxs-lookup"><span data-stu-id="ba02d-158">This could result in an activation error if user-to-partition mapping is the mechanism used to activate a component.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ba02d-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba02d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba02d-160">Individuazione di un componente per l'attivazione</span><span class="sxs-lookup"><span data-stu-id="ba02d-160">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)
</dt> </dl>

 

