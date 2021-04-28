---
title: Gestione degli errori in COM (Introduzione a Win32 e C++)
description: Gestione degli errori in COM (Introduzione a Win32 e C++)
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103919"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a><span data-ttu-id="7b607-103">Gestione degli errori in COM (Introduzione a Win32 e C++)</span><span class="sxs-lookup"><span data-stu-id="7b607-103">Error Handling in COM (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="7b607-104">COM usa **i valori HRESULT** per indicare l'esito positivo o negativo di una chiamata di metodo o funzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-104">COM uses **HRESULT** values to indicate the success or failure of a method or function call.</span></span> <span data-ttu-id="7b607-105">Varie intestazioni SDK definiscono diverse **costanti HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7b607-105">Various SDK headers define various **HRESULT** constants.</span></span> <span data-ttu-id="7b607-106">Un set comune di codici a livello di sistema è definito in WinError.h.</span><span class="sxs-lookup"><span data-stu-id="7b607-106">A common set of system-wide codes is defined in WinError.h.</span></span> <span data-ttu-id="7b607-107">La tabella seguente illustra alcuni di questi codici restituiti a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="7b607-107">The following table shows some of those system-wide return codes.</span></span>



| <span data-ttu-id="7b607-108">Costante</span><span class="sxs-lookup"><span data-stu-id="7b607-108">Constant</span></span>            | <span data-ttu-id="7b607-109">Valore numerico</span><span class="sxs-lookup"><span data-stu-id="7b607-109">Numeric value</span></span> | <span data-ttu-id="7b607-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b607-110">Description</span></span>                                          |
|---------------------|---------------|------------------------------------------------------|
| <span data-ttu-id="7b607-111">**E \_ ACCESSO NEGATO**</span><span class="sxs-lookup"><span data-stu-id="7b607-111">**E\_ACCESSDENIED**</span></span> | <span data-ttu-id="7b607-112">0x80070005</span><span class="sxs-lookup"><span data-stu-id="7b607-112">0x80070005</span></span>    | <span data-ttu-id="7b607-113">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7b607-113">Access denied.</span></span>                                       |
| <span data-ttu-id="7b607-114">**E \_ FAIL**</span><span class="sxs-lookup"><span data-stu-id="7b607-114">**E\_FAIL**</span></span>         | <span data-ttu-id="7b607-115">0x80004005</span><span class="sxs-lookup"><span data-stu-id="7b607-115">0x80004005</span></span>    | <span data-ttu-id="7b607-116">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7b607-116">Unspecified error.</span></span>                                   |
| <span data-ttu-id="7b607-117">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="7b607-117">**E\_INVALIDARG**</span></span>   | <span data-ttu-id="7b607-118">0x80070057</span><span class="sxs-lookup"><span data-stu-id="7b607-118">0x80070057</span></span>    | <span data-ttu-id="7b607-119">Valore del parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="7b607-119">Invalid parameter value.</span></span>                             |
| <span data-ttu-id="7b607-120">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="7b607-120">**E\_OUTOFMEMORY**</span></span>  | <span data-ttu-id="7b607-121">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="7b607-121">0x8007000E</span></span>    | <span data-ttu-id="7b607-122">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="7b607-122">Out of memory.</span></span>                                       |
| <span data-ttu-id="7b607-123">**PUNTATORE \_ E**</span><span class="sxs-lookup"><span data-stu-id="7b607-123">**E\_POINTER**</span></span>      | <span data-ttu-id="7b607-124">0x80004003</span><span class="sxs-lookup"><span data-stu-id="7b607-124">0x80004003</span></span>    | <span data-ttu-id="7b607-125">**Null è** stato passato in modo non corretto per un valore del puntatore.</span><span class="sxs-lookup"><span data-stu-id="7b607-125">**NULL** was passed incorrectly for a pointer value.</span></span> |
| <span data-ttu-id="7b607-126">**E \_ UNEXPECTED**</span><span class="sxs-lookup"><span data-stu-id="7b607-126">**E\_UNEXPECTED**</span></span>   | <span data-ttu-id="7b607-127">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="7b607-127">0x8000FFFF</span></span>    | <span data-ttu-id="7b607-128">Condizione imprevista.</span><span class="sxs-lookup"><span data-stu-id="7b607-128">Unexpected condition.</span></span>                                |
| <span data-ttu-id="7b607-129">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="7b607-129">**S\_OK**</span></span>           | <span data-ttu-id="7b607-130">0x0</span><span class="sxs-lookup"><span data-stu-id="7b607-130">0x0</span></span>           | <span data-ttu-id="7b607-131">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="7b607-131">Success.</span></span>                                             |
| <span data-ttu-id="7b607-132">**S \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="7b607-132">**S\_FALSE**</span></span>        | <span data-ttu-id="7b607-133">0x1</span><span class="sxs-lookup"><span data-stu-id="7b607-133">0x1</span></span>           | <span data-ttu-id="7b607-134">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="7b607-134">Success.</span></span>                                             |



 

<span data-ttu-id="7b607-135">Tutte le costanti con il prefisso \_ "E" sono codici di errore.</span><span class="sxs-lookup"><span data-stu-id="7b607-135">All of the constants with the prefix "E\_" are error codes.</span></span> <span data-ttu-id="7b607-136">Le costanti **S \_ OK e** S **\_ FALSE** sono entrambe codici di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7b607-136">The constants **S\_OK** and **S\_FALSE** are both success codes.</span></span> <span data-ttu-id="7b607-137">Probabilmente il 99% dei metodi COM restituisce **S \_ OK** quando hanno esito positivo, ma non lasciare che questo fatto sia un errore.</span><span class="sxs-lookup"><span data-stu-id="7b607-137">Probably 99% of COM methods return **S\_OK** when they succeed; but do not let this fact mislead you.</span></span> <span data-ttu-id="7b607-138">Un metodo potrebbe restituire altri codici di esito positivo, quindi verificare sempre la presenza di errori usando la macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) [**o FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed)</span><span class="sxs-lookup"><span data-stu-id="7b607-138">A method might return other success codes, so always test for errors by using the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) or [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="7b607-139">Il codice di esempio seguente illustra il modo errato e il modo corretto per testare l'esito positivo di una chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-139">The following example code shows the wrong way and the right way to test for the success of a function call.</span></span>


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



<span data-ttu-id="7b607-140">Il codice di **esito positivo S \_ FALSE** merita menzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-140">The success code **S\_FALSE** deserves mention.</span></span> <span data-ttu-id="7b607-141">Alcuni metodi usano **S \_ FALSE** per indicare approssimativamente una condizione negativa che non è un errore.</span><span class="sxs-lookup"><span data-stu-id="7b607-141">Some methods use **S\_FALSE** to mean, roughly, a negative condition that is not a failure.</span></span> <span data-ttu-id="7b607-142">Può anche indicare una "no-op", ovvero il metodo ha avuto esito positivo, ma non ha avuto alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="7b607-142">It can also indicate a "no-op"—the method succeeded, but had no effect.</span></span> <span data-ttu-id="7b607-143">Ad esempio, la [**funzione CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) restituisce **S \_ FALSE** se viene chiamata una seconda volta dallo stesso thread.</span><span class="sxs-lookup"><span data-stu-id="7b607-143">For example, the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function returns **S\_FALSE** if you call it a second time from the same thread.</span></span> <span data-ttu-id="7b607-144">Se è necessario distinguere **tra S \_ OK** e **S \_ FALSE** nel codice, è necessario testare direttamente il valore, ma usare [**ANCORA FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) o [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) per gestire i case rimanenti, come illustrato nel codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="7b607-144">If you need to differentiate between **S\_OK** and **S\_FALSE** in your code, you should test the value directly, but still use [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) or [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) to handle the remaining cases, as shown in the following example code.</span></span>


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



<span data-ttu-id="7b607-145">Alcuni **valori HRESULT** sono specifici di una particolare funzionalità o sottosistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="7b607-145">Some **HRESULT** values are specific to a particular feature or subsystem of Windows.</span></span> <span data-ttu-id="7b607-146">Ad esempio, l'API grafica Direct2D definisce il codice di errore **D2DERR \_ UNSUPPORTED \_ PIXEL \_ FORMAT**, il che significa che il programma ha usato un formato pixel non supportato.</span><span class="sxs-lookup"><span data-stu-id="7b607-146">For example, the Direct2D graphics API defines the error code **D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**, which means that the program used an unsupported pixel format.</span></span> <span data-ttu-id="7b607-147">La documentazione MSDN fornisce spesso un elenco di codici di errore specifici che un metodo potrebbe restituire.</span><span class="sxs-lookup"><span data-stu-id="7b607-147">MSDN documentation often gives a list of specific error codes that a method might return.</span></span> <span data-ttu-id="7b607-148">Tuttavia, non è consigliabile considerare questi elenchi come definitivi.</span><span class="sxs-lookup"><span data-stu-id="7b607-148">However, you should not consider these lists to be definitive.</span></span> <span data-ttu-id="7b607-149">Un metodo può sempre restituire un **valore HRESULT** non elencato nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="7b607-149">A method can always return an **HRESULT** value that is not listed in the documentation.</span></span> <span data-ttu-id="7b607-150">Anche in questo caso, usare le macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) [**e FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed)</span><span class="sxs-lookup"><span data-stu-id="7b607-150">Again, use the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macros.</span></span> <span data-ttu-id="7b607-151">Se si verifica un codice di errore specifico, includere anche un case predefinito.</span><span class="sxs-lookup"><span data-stu-id="7b607-151">If you test for a specific error code, include a default case as well.</span></span>


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a><span data-ttu-id="7b607-152">Modelli per la gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="7b607-152">Patterns for Error Handling</span></span>

<span data-ttu-id="7b607-153">Questa sezione esamina alcuni modelli per la gestione degli errori COM in modo strutturato.</span><span class="sxs-lookup"><span data-stu-id="7b607-153">This section looks at some patterns for handling COM errors in a structured way.</span></span> <span data-ttu-id="7b607-154">Ogni modello presenta vantaggi e svantaggi.</span><span class="sxs-lookup"><span data-stu-id="7b607-154">Each pattern has advantages and disadvantages.</span></span> <span data-ttu-id="7b607-155">In una certa misura, la scelta è una questione di assaggio.</span><span class="sxs-lookup"><span data-stu-id="7b607-155">To some extent, the choice is a matter of taste.</span></span> <span data-ttu-id="7b607-156">Se si lavora a un progetto esistente, è possibile che le linee guida per la scrittura del codice procrivano uno stile specifico.</span><span class="sxs-lookup"><span data-stu-id="7b607-156">If you work on an existing project, it might already have coding guidelines that proscribe a particular style.</span></span> <span data-ttu-id="7b607-157">Indipendentemente dal modello adottato, un codice affidabile rispetta le regole seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b607-157">Regardless of which pattern you adopt, robust code will obey the following rules.</span></span>

-   <span data-ttu-id="7b607-158">Per ogni metodo o funzione che restituisce **un HRESULT,** controllare il valore restituito prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="7b607-158">For every method or function that returns an **HRESULT**, check the return value before proceeding.</span></span>
-   <span data-ttu-id="7b607-159">Rilasciare le risorse dopo che sono state usate.</span><span class="sxs-lookup"><span data-stu-id="7b607-159">Release resources after they are used.</span></span>
-   <span data-ttu-id="7b607-160">Non tentare di accedere a risorse non valide o non inizializzate, ad esempio **puntatori NULL.**</span><span class="sxs-lookup"><span data-stu-id="7b607-160">Do not attempt to access invalid or uninitialized resources, such as **NULL** pointers.</span></span>
-   <span data-ttu-id="7b607-161">Non provare a usare una risorsa dopo il rilascio.</span><span class="sxs-lookup"><span data-stu-id="7b607-161">Do not try to use a resource after you release it.</span></span>

<span data-ttu-id="7b607-162">Tenere presenti queste regole, ecco quattro modelli per la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="7b607-162">With these rules in mind, here are four patterns for handling errors.</span></span>

-   [<span data-ttu-id="7b607-163">If annidati</span><span class="sxs-lookup"><span data-stu-id="7b607-163">Nested ifs</span></span>](#nested-ifs)
-   [<span data-ttu-id="7b607-164">If a catena</span><span class="sxs-lookup"><span data-stu-id="7b607-164">Cascading ifs</span></span>](#cascading-ifs)
-   [<span data-ttu-id="7b607-165">Jump on Fail</span><span class="sxs-lookup"><span data-stu-id="7b607-165">Jump on Fail</span></span>](#jump-on-fail)
-   [<span data-ttu-id="7b607-166">Genera in caso di errore</span><span class="sxs-lookup"><span data-stu-id="7b607-166">Throw on Fail</span></span>](#throw-on-fail)

### <a name="nested-ifs"></a><span data-ttu-id="7b607-167">If annidati</span><span class="sxs-lookup"><span data-stu-id="7b607-167">Nested ifs</span></span>

<span data-ttu-id="7b607-168">Dopo ogni chiamata che restituisce un **valore HRESULT,** usare un'istruzione **if** per verificare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7b607-168">After every call that returns an **HRESULT**, use an **if** statement to test for success.</span></span> <span data-ttu-id="7b607-169">Inserire quindi la chiamata al metodo successiva nell'ambito **dell'istruzione if.**</span><span class="sxs-lookup"><span data-stu-id="7b607-169">Then, put the next method call within the scope of the **if** statement.</span></span> <span data-ttu-id="7b607-170">Più **istruzioni if** possono essere annidate in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="7b607-170">More **if** statements can be nested as deeply as needed.</span></span> <span data-ttu-id="7b607-171">Gli esempi di codice precedenti in questo modulo hanno usato tutti questo modello, ma eccolo di nuovo:</span><span class="sxs-lookup"><span data-stu-id="7b607-171">The previous code examples in this module have all used this pattern, but here it is again:</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



<span data-ttu-id="7b607-172">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="7b607-172">Advantages</span></span>

-   <span data-ttu-id="7b607-173">Le variabili possono essere dichiarate con ambito minimo.</span><span class="sxs-lookup"><span data-stu-id="7b607-173">Variables can be declared with minimal scope.</span></span> <span data-ttu-id="7b607-174">Ad esempio, *pItem non* viene dichiarato fino a quando non viene usato.</span><span class="sxs-lookup"><span data-stu-id="7b607-174">For example, *pItem* is not declared until it is used.</span></span>
-   <span data-ttu-id="7b607-175">All'interno di ogni istruzione **if,** alcune invarianti sono vere: tutte le chiamate precedenti hanno avuto esito positivo e tutte le risorse acquisite sono ancora valide.</span><span class="sxs-lookup"><span data-stu-id="7b607-175">Within each **if** statement, certain invariants are true: All previous calls have succeeded, and all acquired resources are still valid.</span></span> <span data-ttu-id="7b607-176">Nell'esempio precedente, quando il programma raggiunge l'istruzione **if** più interna, sia *pItem* che *pFileOpen* sono noti come validi.</span><span class="sxs-lookup"><span data-stu-id="7b607-176">In the previous example, when the program reaches the innermost **if** statement, both *pItem* and *pFileOpen* are known to be valid.</span></span>
-   <span data-ttu-id="7b607-177">È chiaro quando rilasciare puntatori a interfaccia e altre risorse.</span><span class="sxs-lookup"><span data-stu-id="7b607-177">It is clear when to release interface pointers and other resources.</span></span> <span data-ttu-id="7b607-178">Si rilascia una risorsa alla fine dell'istruzione **if** che segue immediatamente la chiamata che ha acquisito la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b607-178">You release a resource at the end of the **if** statement that immediately follows the call that acquired the resource.</span></span>

<span data-ttu-id="7b607-179">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="7b607-179">Disadvantages</span></span>

-   <span data-ttu-id="7b607-180">Alcuni utenti trovano difficile leggere l'annidamento profondo.</span><span class="sxs-lookup"><span data-stu-id="7b607-180">Some people find deep nesting hard to read.</span></span>
-   <span data-ttu-id="7b607-181">La gestione degli errori è mista ad altre istruzioni di diramazione e ciclo.</span><span class="sxs-lookup"><span data-stu-id="7b607-181">Error handling is mixed in with other branching and looping statements.</span></span> <span data-ttu-id="7b607-182">Ciò può rendere la logica complessiva del programma più difficile da seguire.</span><span class="sxs-lookup"><span data-stu-id="7b607-182">This can make the overall program logic harder to follow.</span></span>

### <a name="cascading-ifs"></a><span data-ttu-id="7b607-183">If a catena</span><span class="sxs-lookup"><span data-stu-id="7b607-183">Cascading ifs</span></span>

<span data-ttu-id="7b607-184">Dopo ogni chiamata al metodo, usare **un'istruzione if** per verificare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7b607-184">After each method call, use an **if** statement to test for success.</span></span> <span data-ttu-id="7b607-185">Se il metodo ha esito positivo, inserire la chiamata al metodo successiva all'interno del **blocco if.**</span><span class="sxs-lookup"><span data-stu-id="7b607-185">If the method succeeds, place the next method call inside the **if** block.</span></span> <span data-ttu-id="7b607-186">Invece di annidare ulteriormente le **istruzioni if,** inserire ogni test [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) successivo dopo il blocco **if** precedente.</span><span class="sxs-lookup"><span data-stu-id="7b607-186">But instead of nesting further **if** statements, place each subsequent [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) test after the previous **if** block.</span></span> <span data-ttu-id="7b607-187">Se un metodo ha esito negativo, tutti i test **SUCCEEDED** rimanenti hanno semplicemente esito negativo fino a quando non viene raggiunta la parte inferiore della funzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-187">If any method fails, all the remaining **SUCCEEDED** tests simply fail until the bottom of the function is reached.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="7b607-188">In questo modello le risorse vengono rilasciate alla fine della funzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-188">In this pattern, you release resources at the very end of the function.</span></span> <span data-ttu-id="7b607-189">Se si verifica un errore, alcuni puntatori potrebbero non essere validi quando la funzione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="7b607-189">If an error occurs, some pointers might be invalid when the function exits.</span></span> <span data-ttu-id="7b607-190">La [**chiamata di Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su un puntatore non valido arresterà il programma in modo anomalo (o peggiore), quindi è necessario inizializzare tutti i puntatori su **NULL** e verificare se sono **NULL** prima di rilasciarli.</span><span class="sxs-lookup"><span data-stu-id="7b607-190">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on an invalid pointer will crash the program (or worse), so you must initialize all pointers to **NULL** and check whether they are **NULL** before releasing them.</span></span> <span data-ttu-id="7b607-191">In questo esempio viene utilizzata la funzione . Anche i puntatori intelligenti `SafeRelease` sono una buona scelta.</span><span class="sxs-lookup"><span data-stu-id="7b607-191">This example uses the `SafeRelease` function; smart pointers are also a good choice.</span></span>

<span data-ttu-id="7b607-192">Se si usa questo modello, è necessario prestare attenzione ai costrutti di ciclo.</span><span class="sxs-lookup"><span data-stu-id="7b607-192">If you use this pattern, you must be careful with loop constructs.</span></span> <span data-ttu-id="7b607-193">All'interno di un ciclo interrompere il ciclo se una chiamata ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7b607-193">Inside a loop, break from the loop if any call fails.</span></span>

<span data-ttu-id="7b607-194">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="7b607-194">Advantages</span></span>

-   <span data-ttu-id="7b607-195">Questo modello crea meno annidamento rispetto al modello "ifs annidato".</span><span class="sxs-lookup"><span data-stu-id="7b607-195">This pattern creates less nesting than the "nested ifs" pattern.</span></span>
-   <span data-ttu-id="7b607-196">Il flusso di controllo complessivo è più facile da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="7b607-196">Overall control flow is easier to see.</span></span>
-   <span data-ttu-id="7b607-197">Le risorse vengono rilasciate in un punto del codice.</span><span class="sxs-lookup"><span data-stu-id="7b607-197">Resources are released at one point in the code.</span></span>

<span data-ttu-id="7b607-198">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="7b607-198">Disadvantages</span></span>

-   <span data-ttu-id="7b607-199">Tutte le variabili devono essere dichiarate e inizializzate all'inizio della funzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-199">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="7b607-200">Se una chiamata non riesce, la funzione esegue più controlli degli errori non necessario, invece di uscire immediatamente dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-200">If a call fails, the function makes multiple unneeded error checks, instead of exiting the function immediately.</span></span>
-   <span data-ttu-id="7b607-201">Poiché il flusso di controllo continua attraverso la funzione dopo un errore, è necessario prestare attenzione in tutto il corpo della funzione a non accedere alle risorse non valide.</span><span class="sxs-lookup"><span data-stu-id="7b607-201">Because the flow of control continues through the function after a failure, you must be careful throughout the body of the function not to access invalid resources.</span></span>
-   <span data-ttu-id="7b607-202">Gli errori all'interno di un ciclo richiedono un caso speciale.</span><span class="sxs-lookup"><span data-stu-id="7b607-202">Errors inside a loop require a special case.</span></span>

### <a name="jump-on-fail"></a><span data-ttu-id="7b607-203">Jump on Fail</span><span class="sxs-lookup"><span data-stu-id="7b607-203">Jump on Fail</span></span>

<span data-ttu-id="7b607-204">Dopo ogni chiamata al metodo, verificare l'esito negativo (operazione non riuscita).</span><span class="sxs-lookup"><span data-stu-id="7b607-204">After each method call, test for failure (not success).</span></span> <span data-ttu-id="7b607-205">In caso di errore, passare a un'etichetta nella parte inferiore della funzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-205">On failure, jump to a label near the bottom of the function.</span></span> <span data-ttu-id="7b607-206">Dopo l'etichetta, ma prima di uscire dalla funzione, rilasciare le risorse.</span><span class="sxs-lookup"><span data-stu-id="7b607-206">After the label, but before exiting the function, release resources.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="7b607-207">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="7b607-207">Advantages</span></span>

-   <span data-ttu-id="7b607-208">Il flusso di controllo complessivo è facile da vedere.</span><span class="sxs-lookup"><span data-stu-id="7b607-208">The overall control flow is easy to see.</span></span>
-   <span data-ttu-id="7b607-209">In ogni punto del codice dopo un controllo [**FAILED,**](/windows/desktop/api/winerror/nf-winerror-failed) se non è stato possibile passare all'etichetta, è garantito che tutte le chiamate precedenti hanno avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7b607-209">At every point in the code after a [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) check, if you have not jumped to the label, it is guaranteed that all the previous calls have succeeded.</span></span>
-   <span data-ttu-id="7b607-210">Le risorse vengono rilasciate in un'unica posizione nel codice.</span><span class="sxs-lookup"><span data-stu-id="7b607-210">Resources are released at one place in the code.</span></span>

<span data-ttu-id="7b607-211">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="7b607-211">Disadvantages</span></span>

-   <span data-ttu-id="7b607-212">Tutte le variabili devono essere dichiarate e inizializzate all'inizio della funzione.</span><span class="sxs-lookup"><span data-stu-id="7b607-212">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="7b607-213">Alcuni programmatori non desiderano usare **goto** nel codice.</span><span class="sxs-lookup"><span data-stu-id="7b607-213">Some programmers do not like to use **goto** in their code.</span></span> <span data-ttu-id="7b607-214">Si noti tuttavia che questo uso di **goto** è altamente strutturato. Il codice non passa mai al di fuori della chiamata di funzione corrente.</span><span class="sxs-lookup"><span data-stu-id="7b607-214">(However, it should be noted that this use of **goto** is highly structured; the code never jumps outside the current function call.)</span></span>
-   <span data-ttu-id="7b607-215">**Le istruzioni goto** ignorano gli inizializzatori.</span><span class="sxs-lookup"><span data-stu-id="7b607-215">**goto** statements skip initializers.</span></span>

### <a name="throw-on-fail"></a><span data-ttu-id="7b607-216">Genera in caso di errore</span><span class="sxs-lookup"><span data-stu-id="7b607-216">Throw on Fail</span></span>

<span data-ttu-id="7b607-217">Anziché passare a un'etichetta, è possibile generare un'eccezione quando un metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7b607-217">Rather than jump to a label, you can throw an exception when a method fails.</span></span> <span data-ttu-id="7b607-218">Questo può produrre uno stile più idiomatico di C++ se si è usati per scrivere codice indipendente da eccezioni.</span><span class="sxs-lookup"><span data-stu-id="7b607-218">This can produce a more idiomatic style of C++ if you are used to writing exception-safe code.</span></span>


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



<span data-ttu-id="7b607-219">Si noti che questo esempio usa la **classe CComPtr** per gestire i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7b607-219">Notice that this example uses the **CComPtr** class to manage interface pointers.</span></span> <span data-ttu-id="7b607-220">In genere, se il codice genera eccezioni, è necessario seguire il modello RAII (Resource Acquisition is Initialization).</span><span class="sxs-lookup"><span data-stu-id="7b607-220">Generally, if your code throws exceptions, you should follow the RAII (Resource Acquisition is Initialization) pattern.</span></span> <span data-ttu-id="7b607-221">Ciò significa che ogni risorsa deve essere gestita da un oggetto il cui distruttore garantisce che la risorsa venga rilasciata correttamente.</span><span class="sxs-lookup"><span data-stu-id="7b607-221">That is, every resource should be managed by an object whose destructor guarantees that the resource is correctly released.</span></span> <span data-ttu-id="7b607-222">Se viene generata un'eccezione, viene garantito che il distruttore sia richiamato.</span><span class="sxs-lookup"><span data-stu-id="7b607-222">If an exception is thrown, the destructor is guaranteed to be invoked.</span></span> <span data-ttu-id="7b607-223">In caso contrario, il programma potrebbe perdere risorse.</span><span class="sxs-lookup"><span data-stu-id="7b607-223">Otherwise, your program might leak resources.</span></span>

<span data-ttu-id="7b607-224">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="7b607-224">Advantages</span></span>

-   <span data-ttu-id="7b607-225">Compatibile con il codice esistente che usa la gestione delle eccezioni.</span><span class="sxs-lookup"><span data-stu-id="7b607-225">Compatible with existing code that uses exception handling.</span></span>
-   <span data-ttu-id="7b607-226">Compatibile con le librerie C++ che generano eccezioni, ad esempio la libreria STL (Standard Template Library).</span><span class="sxs-lookup"><span data-stu-id="7b607-226">Compatible with C++ libraries that throw exceptions, such as the Standard Template Library (STL).</span></span>

<span data-ttu-id="7b607-227">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="7b607-227">Disadvantages</span></span>

-   <span data-ttu-id="7b607-228">Richiede oggetti C++ per gestire risorse come la memoria o gli handle di file.</span><span class="sxs-lookup"><span data-stu-id="7b607-228">Requires C++ objects to manage resources such as memory or file handles.</span></span>
-   <span data-ttu-id="7b607-229">Richiede una buona conoscenza di come scrivere codice indipendente da eccezioni.</span><span class="sxs-lookup"><span data-stu-id="7b607-229">Requires a good understanding of how to write exception-safe code.</span></span>

## <a name="next"></a><span data-ttu-id="7b607-230">Prossima</span><span class="sxs-lookup"><span data-stu-id="7b607-230">Next</span></span>

[<span data-ttu-id="7b607-231">Modulo 3. Grafica Di Windows</span><span class="sxs-lookup"><span data-stu-id="7b607-231">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)

 

 
