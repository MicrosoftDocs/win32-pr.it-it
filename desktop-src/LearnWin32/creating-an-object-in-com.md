---
title: Creazione di un oggetto in COM
description: Per usare un'interfaccia COM, il programma crea prima un'istanza di un oggetto che implementa tale interfaccia.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398935"
---
# <a name="creating-an-object-in-com"></a><span data-ttu-id="44913-103">Creazione di un oggetto in COM</span><span class="sxs-lookup"><span data-stu-id="44913-103">Creating an Object in COM</span></span>

<span data-ttu-id="44913-104">Dopo l'inizializzazione della libreria COM da parte di un thread, è possibile che il thread utilizzi le interfacce COM in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="44913-104">After a thread has initialized the COM library, it is safe for the thread to use COM interfaces.</span></span> <span data-ttu-id="44913-105">Per usare un'interfaccia COM, il programma crea prima un'istanza di un oggetto che implementa tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="44913-105">To use a COM interface, your program first creates an instance of an object that implements that interface.</span></span>

<span data-ttu-id="44913-106">In generale, esistono due modi per creare un oggetto COM:</span><span class="sxs-lookup"><span data-stu-id="44913-106">In general, there are two ways to create a COM object:</span></span>

-   <span data-ttu-id="44913-107">Il modulo che implementa l'oggetto potrebbe fornire una funzione progettata in modo specifico per creare istanze di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="44913-107">The module that implements the object might provide a function specifically designed to create instances of that object.</span></span>
-   <span data-ttu-id="44913-108">In alternativa, COM fornisce una funzione di creazione generica denominata [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="44913-108">Alternatively, COM provides a generic creation function named [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="44913-109">Ad esempio, prendere l'oggetto ipotetico `Shape` dall'argomento [che cos'è un'interfaccia com?](what-is-a-com-interface-.md).</span><span class="sxs-lookup"><span data-stu-id="44913-109">For example, take the hypothetical `Shape` object from the topic [What Is a COM Interface?](what-is-a-com-interface-.md).</span></span> <span data-ttu-id="44913-110">In questo esempio, l' `Shape` oggetto implementa un'interfaccia denominata `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="44913-110">In that example, the `Shape` object implements an interface named `IDrawable`.</span></span> <span data-ttu-id="44913-111">La libreria grafica che implementa l' `Shape` oggetto potrebbe esportare una funzione con la firma seguente.</span><span class="sxs-lookup"><span data-stu-id="44913-111">The graphics library that implements the `Shape` object might export a function with the following signature.</span></span>


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



<span data-ttu-id="44913-112">Data questa funzione, è possibile creare un nuovo `Shape` oggetto come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="44913-112">Given this function, you could create a new `Shape` object as follows.</span></span>


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="44913-113">Il parametro *ppShape* è di tipo puntatore a puntatore a `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="44913-113">The *ppShape* parameter is of type pointer-to-pointer-to-`IDrawable`.</span></span> <span data-ttu-id="44913-114">Se questo modello non è stato visto in precedenza, il doppio riferimento indiretto può essere sconcertante.</span><span class="sxs-lookup"><span data-stu-id="44913-114">If you have not seen this pattern before, the double indirection might be puzzling.</span></span>

<span data-ttu-id="44913-115">Considerare i requisiti della `CreateShape` funzione.</span><span class="sxs-lookup"><span data-stu-id="44913-115">Consider the requirements of the `CreateShape` function.</span></span> <span data-ttu-id="44913-116">La funzione deve restituire un `IDrawable` puntatore al chiamante.</span><span class="sxs-lookup"><span data-stu-id="44913-116">The function must give an `IDrawable` pointer back to the caller.</span></span> <span data-ttu-id="44913-117">Tuttavia, il valore restituito della funzione è già usato per il codice di errore o di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="44913-117">But the function's return value is already used for the error/success code.</span></span> <span data-ttu-id="44913-118">Pertanto, il puntatore deve essere restituito tramite un argomento alla funzione.</span><span class="sxs-lookup"><span data-stu-id="44913-118">Therefore, the pointer must be returned through an argument to the function.</span></span> <span data-ttu-id="44913-119">Il chiamante passerà una variabile di tipo `IDrawable*` alla funzione e la funzione sovrascriverà questa variabile con un nuovo `IDrawable` puntatore.</span><span class="sxs-lookup"><span data-stu-id="44913-119">The caller will pass a variable of type `IDrawable*` to the function, and the function will overwrite this variable with a new `IDrawable` pointer.</span></span> <span data-ttu-id="44913-120">In C++ sono disponibili solo due modi per la sovrascrittura di un valore di parametro da una funzione: passa per riferimento o passa per indirizzo.</span><span class="sxs-lookup"><span data-stu-id="44913-120">In C++, there are only two ways for a function to overwrite a parameter value: pass by reference, or pass by address.</span></span> <span data-ttu-id="44913-121">COM utilizza la seconda opzione, pass-by-Address.</span><span class="sxs-lookup"><span data-stu-id="44913-121">COM uses the latter, pass-by-address.</span></span> <span data-ttu-id="44913-122">E l'indirizzo di un puntatore è un puntatore a puntatore, quindi il tipo di parametro deve essere `IDrawable**` .</span><span class="sxs-lookup"><span data-stu-id="44913-122">And the address of a pointer is a pointer-to-a-pointer, so the parameter type must be `IDrawable**`.</span></span>

<span data-ttu-id="44913-123">Ecco un diagramma che consente di visualizzare gli elementi in corso.</span><span class="sxs-lookup"><span data-stu-id="44913-123">Here is a diagram to help visualize what's going on.</span></span>

![diagramma che mostra un riferimento indiretto a doppio puntatore](images/com03.png)

<span data-ttu-id="44913-125">La `CreateShape` funzione usa l'indirizzo di *pShape* ( `&pShape` ) per scrivere un nuovo valore del puntatore in *pShape*.</span><span class="sxs-lookup"><span data-stu-id="44913-125">The `CreateShape` function uses the address of *pShape* (`&pShape`) to write a new pointer value to *pShape*.</span></span>

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a><span data-ttu-id="44913-126">CoCreateInstance: metodo generico per la creazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="44913-126">CoCreateInstance: A Generic Way to Create Objects</span></span>

<span data-ttu-id="44913-127">La funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fornisce un meccanismo generico per la creazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="44913-127">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function provides a generic mechanism for creating objects.</span></span> <span data-ttu-id="44913-128">Per comprendere **CoCreateInstance**, tenere presente che due oggetti com possono implementare la stessa interfaccia e un oggetto può implementare due o più interfacce.</span><span class="sxs-lookup"><span data-stu-id="44913-128">To understand **CoCreateInstance**, keep in mind that two COM objects can implement the same interface, and one object can implement two or more interfaces.</span></span> <span data-ttu-id="44913-129">Pertanto, una funzione generica che crea oggetti richiede due tipi di informazioni.</span><span class="sxs-lookup"><span data-stu-id="44913-129">Thus, a generic function that creates objects needs two pieces of information.</span></span>

-   <span data-ttu-id="44913-130">Oggetto da creare.</span><span class="sxs-lookup"><span data-stu-id="44913-130">Which object to create.</span></span>
-   <span data-ttu-id="44913-131">Interfaccia da ottenere dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="44913-131">Which interface to get from the object.</span></span>

<span data-ttu-id="44913-132">Ma come è possibile indicare queste informazioni quando si chiama la funzione?</span><span class="sxs-lookup"><span data-stu-id="44913-132">But how do we indicate this information when we call the function?</span></span> <span data-ttu-id="44913-133">In COM, un oggetto o un'interfaccia viene identificato tramite l'assegnazione di un numero a 128 bit, denominato *identificatore univoco globale* (Guid).</span><span class="sxs-lookup"><span data-stu-id="44913-133">In COM, an object or an interface is identified by assigning it a 128-bit number, called a *globally unique identifier* (GUID).</span></span> <span data-ttu-id="44913-134">I GUID vengono generati in modo da renderli effettivamente univoci.</span><span class="sxs-lookup"><span data-stu-id="44913-134">GUIDs are generated in a way that makes them effectively unique.</span></span> <span data-ttu-id="44913-135">I GUID rappresentano una soluzione al problema di come creare identificatori univoci senza un'autorità di registrazione centrale.</span><span class="sxs-lookup"><span data-stu-id="44913-135">GUIDs are a solution to the problem of how to create unique identifiers without a central registration authority.</span></span> <span data-ttu-id="44913-136">I GUID sono talvolta denominati *identificatori universalmente univoci* (UUID).</span><span class="sxs-lookup"><span data-stu-id="44913-136">GUIDs are sometimes called *universally unique identifiers* (UUIDs).</span></span> <span data-ttu-id="44913-137">Prima di COM, venivano usati in DCE/RPC (Distributed Computing Environment/Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="44913-137">Prior to COM, they were used in DCE/RPC (Distributed Computing Environment/Remote Procedure Call).</span></span> <span data-ttu-id="44913-138">Sono disponibili diversi algoritmi per la creazione di nuovi GUID.</span><span class="sxs-lookup"><span data-stu-id="44913-138">Several algorithms exist for creating new GUIDs.</span></span> <span data-ttu-id="44913-139">Non tutti questi algoritmi assicurano esclusivamente l'univocità, ma la probabilità di creare accidentalmente lo stesso valore GUID è molto ridotta, in effetti zero.</span><span class="sxs-lookup"><span data-stu-id="44913-139">Not all of these algorithms strictly guarantee uniqueness, but the probability of accidentally creating the same GUID value twice is extremely small—effectively zero.</span></span> <span data-ttu-id="44913-140">I GUID possono essere usati per identificare qualsiasi tipo di entità, non solo per oggetti e interfacce.</span><span class="sxs-lookup"><span data-stu-id="44913-140">GUIDs can be used to identify any sort of entity, not just objects and interfaces.</span></span> <span data-ttu-id="44913-141">Tuttavia, questo è l'unico utilizzo che ci interessa in questo modulo.</span><span class="sxs-lookup"><span data-stu-id="44913-141">However, that is the only use that concerns us in this module.</span></span>

<span data-ttu-id="44913-142">Ad esempio, la `Shapes` libreria può dichiarare due costanti GUID:</span><span class="sxs-lookup"><span data-stu-id="44913-142">For example, the `Shapes` library might declare two GUID constants:</span></span>


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



<span data-ttu-id="44913-143">Si può presupporre che i valori numerici a 128 bit effettivi per queste costanti siano definiti altrove. La **\_ forma** di costante CLSID identifica l' `Shape` oggetto, mentre la costante **IID \_ IDrawable** identifica l' `IDrawable` interfaccia.</span><span class="sxs-lookup"><span data-stu-id="44913-143">(You can assume that the actual 128-bit numeric values for these constants are defined elsewhere.) The constant **CLSID\_Shape** identifies the `Shape` object, while the constant **IID\_IDrawable** identifies the `IDrawable` interface.</span></span> <span data-ttu-id="44913-144">Il prefisso "CLSID" sta per l' *identificatore di classe* e l' *IID* di prefisso sta per l'identificatore di *interfaccia*.</span><span class="sxs-lookup"><span data-stu-id="44913-144">The prefix "CLSID" stands for *class identifier*, and the prefix *IID* stands for *interface identifier*.</span></span> <span data-ttu-id="44913-145">Si tratta di convenzioni di denominazione standard in COM.</span><span class="sxs-lookup"><span data-stu-id="44913-145">These are standard naming conventions in COM.</span></span>

<span data-ttu-id="44913-146">Dato questi valori, è necessario creare una nuova `Shape` istanza nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="44913-146">Given these values, you would create a new `Shape` instance as follows:</span></span>


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="44913-147">La funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha cinque parametri.</span><span class="sxs-lookup"><span data-stu-id="44913-147">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function has five parameters.</span></span> <span data-ttu-id="44913-148">Il primo e il quarto parametro sono l'identificatore di classe e l'identificatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="44913-148">The first and fourth parameters are the class identifier and interface identifier.</span></span> <span data-ttu-id="44913-149">Questi parametri indicano in effetti che la funzione "crea l'oggetto forma e fornisce un puntatore all'interfaccia IDrawable".</span><span class="sxs-lookup"><span data-stu-id="44913-149">In effect, these parameters tell the function, "Create the Shape object, and give me a pointer to the IDrawable interface."</span></span>

<span data-ttu-id="44913-150">Impostare il secondo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="44913-150">Set the second parameter to **NULL**.</span></span> <span data-ttu-id="44913-151">Per ulteriori informazioni sul significato di questo parametro, vedere l'argomento [aggregazione](/windows/desktop/com/aggregation) nella documentazione com. Il terzo parametro accetta un set di flag il cui scopo principale è quello di specificare il *contesto di esecuzione* per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="44913-151">(For more information about the meaning of this parameter, see the topic [Aggregation](/windows/desktop/com/aggregation) in the COM documentation.) The third parameter takes a set of flags whose main purpose is to specify the *execution context* for the object.</span></span> <span data-ttu-id="44913-152">Il contesto di esecuzione specifica se l'oggetto viene eseguito nello stesso processo dell'applicazione; in un processo diverso nello stesso computer; o in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="44913-152">The execution context specifies whether the object runs in the same process as the application; in a different process on the same computer; or on a remote computer.</span></span> <span data-ttu-id="44913-153">La tabella seguente mostra i valori più comuni per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44913-153">The following table shows the most common values for this parameter.</span></span>



| <span data-ttu-id="44913-154">Flag</span><span class="sxs-lookup"><span data-stu-id="44913-154">Flag</span></span>                       | <span data-ttu-id="44913-155">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44913-155">Description</span></span>                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44913-156">**\_server inproc \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="44913-156">**CLSCTX\_INPROC\_SERVER**</span></span> | <span data-ttu-id="44913-157">Stesso processo.</span><span class="sxs-lookup"><span data-stu-id="44913-157">Same process.</span></span>                                                                                                                                                      |
| <span data-ttu-id="44913-158">**\_server locale \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="44913-158">**CLSCTX\_LOCAL\_SERVER**</span></span>  | <span data-ttu-id="44913-159">Processo diverso, stesso computer.</span><span class="sxs-lookup"><span data-stu-id="44913-159">Different process, same computer.</span></span>                                                                                                                                  |
| <span data-ttu-id="44913-160">**\_server remoto \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="44913-160">**CLSCTX\_REMOTE\_SERVER**</span></span> | <span data-ttu-id="44913-161">Computer diverso.</span><span class="sxs-lookup"><span data-stu-id="44913-161">Different computer.</span></span>                                                                                                                                                |
| <span data-ttu-id="44913-162">**CLSCTX \_ tutto**</span><span class="sxs-lookup"><span data-stu-id="44913-162">**CLSCTX\_ALL**</span></span>            | <span data-ttu-id="44913-163">Utilizzare l'opzione più efficiente supportata dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="44913-163">Use the most efficient option that the object supports.</span></span> <span data-ttu-id="44913-164">(La classificazione, dal più efficiente al meno efficiente, è: in-process, out-of-process e tra computer).</span><span class="sxs-lookup"><span data-stu-id="44913-164">(The ranking, from most efficient to least efficient, is: in-process, out-of-process, and cross-computer.)</span></span> |



 

<span data-ttu-id="44913-165">La documentazione relativa a un particolare componente potrebbe indicare il contesto di esecuzione supportato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="44913-165">The documentation for a particular component might tell you which execution context the object supports.</span></span> <span data-ttu-id="44913-166">In caso contrario, utilizzare **CLSCTX \_ All**.</span><span class="sxs-lookup"><span data-stu-id="44913-166">If not, use **CLSCTX\_ALL**.</span></span> <span data-ttu-id="44913-167">Se si richiede un contesto di esecuzione non supportato dall'oggetto, la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) restituisce il codice di errore **REGDB \_ E \_ CLASSNOTREG**.</span><span class="sxs-lookup"><span data-stu-id="44913-167">If you request an execution context that the object does not support, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function returns the error code **REGDB\_E\_CLASSNOTREG**.</span></span> <span data-ttu-id="44913-168">Questo codice di errore può anche indicare che il CLSID non corrisponde ad alcun componente registrato nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="44913-168">This error code can also indicate that the CLSID does not correspond to any component registered on the user's computer.</span></span>

<span data-ttu-id="44913-169">Il quinto parametro per [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) riceve un puntatore all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="44913-169">The fifth parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) receives a pointer to the interface.</span></span> <span data-ttu-id="44913-170">Poiché **CoCreateInstance** è un meccanismo generico, questo parametro non può essere fortemente tipizzato.</span><span class="sxs-lookup"><span data-stu-id="44913-170">Because **CoCreateInstance** is a generic mechanism, this parameter cannot be strongly typed.</span></span> <span data-ttu-id="44913-171">Il tipo di dati è invece **void \* \*** e il chiamante deve forzare l'indirizzo del puntatore a un tipo **void \* \*** .</span><span class="sxs-lookup"><span data-stu-id="44913-171">Instead, the data type is **void\*\***, and the caller must coerce the address of the pointer to a **void\*\*** type.</span></span> <span data-ttu-id="44913-172">Questo è lo scopo del **\_ cast di reinterpretazione** nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="44913-172">That is the purpose of the **reinterpret\_cast** in the previous example.</span></span>

<span data-ttu-id="44913-173">È fondamentale controllare il valore restituito di [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="44913-173">It is crucial to check the return value of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="44913-174">Se la funzione restituisce un codice di errore, il puntatore all'interfaccia COM non è valido e il tentativo di dereferenziarlo può causare l'arresto anomalo del programma.</span><span class="sxs-lookup"><span data-stu-id="44913-174">If the function returns an error code, the COM interface pointer is invalid, and attempting to dereference it can cause your program to crash.</span></span>

<span data-ttu-id="44913-175">Internamente, la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilizza varie tecniche per creare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="44913-175">Internally, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function uses various techniques to create an object.</span></span> <span data-ttu-id="44913-176">Nel caso più semplice, Cerca l'identificatore di classe nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="44913-176">In the simplest case, it looks up the class identifier in the registry.</span></span> <span data-ttu-id="44913-177">La voce del registro di sistema punta a una DLL o a un file EXE che implementa l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="44913-177">The registry entry points to a DLL or EXE that implements the object.</span></span> <span data-ttu-id="44913-178">**CoCreateInstance** può inoltre utilizzare le informazioni di un catalogo com+ o di un manifesto side-by-Side (SxS).</span><span class="sxs-lookup"><span data-stu-id="44913-178">**CoCreateInstance** can also use information from a COM+ catalog or a side-by-side (SxS) manifest.</span></span> <span data-ttu-id="44913-179">Indipendentemente, i dettagli sono trasparenti per il chiamante.</span><span class="sxs-lookup"><span data-stu-id="44913-179">Regardless, the details are transparent to the caller.</span></span> <span data-ttu-id="44913-180">Per ulteriori informazioni sui dettagli interni di **CoCreateInstance**, vedere [client e server com](/windows/desktop/com/com-clients-and-servers).</span><span class="sxs-lookup"><span data-stu-id="44913-180">For more information about the internal details of **CoCreateInstance**, see [COM Clients and Servers](/windows/desktop/com/com-clients-and-servers).</span></span>

<span data-ttu-id="44913-181">L' `Shapes` esempio usato è stato escogitato in qualche modo, ora passiamo a un esempio reale di com in azione: la visualizzazione della finestra di dialogo **Apri** in cui l'utente può selezionare un file.</span><span class="sxs-lookup"><span data-stu-id="44913-181">The `Shapes` example that we have been using is somewhat contrived, so now let's turn to a real-world example of COM in action: displaying the **Open** dialog box for the user to select a file.</span></span>

## <a name="next"></a><span data-ttu-id="44913-182">Prossima</span><span class="sxs-lookup"><span data-stu-id="44913-182">Next</span></span>

[<span data-ttu-id="44913-183">Esempio: finestra di dialogo Apri</span><span class="sxs-lookup"><span data-stu-id="44913-183">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)

 

 