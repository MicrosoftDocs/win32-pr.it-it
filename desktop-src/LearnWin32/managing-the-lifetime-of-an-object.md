---
title: Gestione della durata di un oggetto
description: Informazioni su come gestire i metodi AddRef e Release per controllare la durata di un oggetto.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104557212"
---
# <a name="managing-the-lifetime-of-an-object"></a><span data-ttu-id="27f8c-103">Gestione della durata di un oggetto</span><span class="sxs-lookup"><span data-stu-id="27f8c-103">Managing the Lifetime of an Object</span></span>

<span data-ttu-id="27f8c-104">Esiste una regola per le interfacce COM che non sono ancora state citate.</span><span class="sxs-lookup"><span data-stu-id="27f8c-104">There is a rule for COM interfaces that we have not yet mentioned.</span></span> <span data-ttu-id="27f8c-105">Ogni interfaccia COM deve ereditare, direttamente o indirettamente, da un'interfaccia denominata [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="27f8c-105">Every COM interface must inherit, directly or indirectly, from an interface named [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="27f8c-106">Questa interfaccia fornisce alcune funzionalità di base che tutti gli oggetti COM devono supportare.</span><span class="sxs-lookup"><span data-stu-id="27f8c-106">This interface provides some baseline capabilities that all COM objects must support.</span></span>

<span data-ttu-id="27f8c-107">L'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) definisce tre metodi:</span><span class="sxs-lookup"><span data-stu-id="27f8c-107">The [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface defines three methods:</span></span>

-   <span data-ttu-id="27f8c-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="27f8c-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
-   [<span data-ttu-id="27f8c-109">**AddRef**</span><span class="sxs-lookup"><span data-stu-id="27f8c-109">**AddRef**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [<span data-ttu-id="27f8c-110">**Versione**</span><span class="sxs-lookup"><span data-stu-id="27f8c-110">**Release**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

<span data-ttu-id="27f8c-111">Il metodo [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) consente a un programma di eseguire query sulle funzionalità dell'oggetto in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="27f8c-111">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method enables a program to query the capabilities of the object at run time.</span></span> <span data-ttu-id="27f8c-112">Nell'argomento successivo verrà richiesto di aggiungere [un oggetto per un'interfaccia](asking-an-object-for-an-interface.md).</span><span class="sxs-lookup"><span data-stu-id="27f8c-112">We'll say more about that in the next topic, [Asking an Object for an Interface](asking-an-object-for-an-interface.md).</span></span> <span data-ttu-id="27f8c-113">I metodi [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) vengono usati per controllare la durata di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="27f8c-113">The [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are used to control the lifetime of an object.</span></span> <span data-ttu-id="27f8c-114">Questo argomento è soggetto a questo argomento.</span><span class="sxs-lookup"><span data-stu-id="27f8c-114">This is the subject of this topic.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="27f8c-115">Conteggio dei riferimenti</span><span class="sxs-lookup"><span data-stu-id="27f8c-115">Reference Counting</span></span>

<span data-ttu-id="27f8c-116">Qualsiasi altra operazione eseguita da un programma, a un certo punto le risorse vengono allocate e gratuite.</span><span class="sxs-lookup"><span data-stu-id="27f8c-116">Whatever else a program might do, at some point it will allocate and free resources.</span></span> <span data-ttu-id="27f8c-117">L'allocazione di una risorsa è facile.</span><span class="sxs-lookup"><span data-stu-id="27f8c-117">Allocating a resource is easy.</span></span> <span data-ttu-id="27f8c-118">Sapere quando liberare la risorsa è difficile, soprattutto se la durata della risorsa si estende oltre l'ambito corrente.</span><span class="sxs-lookup"><span data-stu-id="27f8c-118">Knowing when to free the resource is hard, especially if the lifetime of the resource extends beyond the current scope.</span></span> <span data-ttu-id="27f8c-119">Questo problema non è univoco per COM.</span><span class="sxs-lookup"><span data-stu-id="27f8c-119">This problem is not unique to COM.</span></span> <span data-ttu-id="27f8c-120">Qualsiasi programma che alloca memoria heap deve risolvere lo stesso problema.</span><span class="sxs-lookup"><span data-stu-id="27f8c-120">Any program that allocates heap memory must solve the same problem.</span></span> <span data-ttu-id="27f8c-121">Ad esempio, C++ usa i distruttori automatici, mentre C# e Java usano Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="27f8c-121">For example, C++ uses automatic destructors, while C# and Java use garbage collection.</span></span> <span data-ttu-id="27f8c-122">COM usa un approccio denominato *conteggio dei riferimenti*.</span><span class="sxs-lookup"><span data-stu-id="27f8c-122">COM uses an approach called *reference counting*.</span></span>

<span data-ttu-id="27f8c-123">Ogni oggetto COM mantiene un conteggio interno.</span><span class="sxs-lookup"><span data-stu-id="27f8c-123">Every COM object maintains an internal count.</span></span> <span data-ttu-id="27f8c-124">Questa operazione è nota come conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="27f8c-124">This is known as the reference count.</span></span> <span data-ttu-id="27f8c-125">Il conteggio dei riferimenti tiene traccia del numero di riferimenti all'oggetto attualmente attivi.</span><span class="sxs-lookup"><span data-stu-id="27f8c-125">The reference count tracks how many references to the object are currently active.</span></span> <span data-ttu-id="27f8c-126">Quando il numero di riferimenti scende a zero, l'oggetto viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="27f8c-126">When the number of references drops to zero, the object deletes itself.</span></span> <span data-ttu-id="27f8c-127">L'ultima parte vale la pena di ripetere: l'oggetto Elimina se stesso.</span><span class="sxs-lookup"><span data-stu-id="27f8c-127">The last part is worth repeating: The object deletes itself.</span></span> <span data-ttu-id="27f8c-128">L'oggetto non viene mai eliminato in modo esplicito dal programma.</span><span class="sxs-lookup"><span data-stu-id="27f8c-128">The program never explicitly deletes the object.</span></span>

<span data-ttu-id="27f8c-129">Di seguito sono riportate le regole per il conteggio dei riferimenti:</span><span class="sxs-lookup"><span data-stu-id="27f8c-129">Here are the rules for reference counting:</span></span>

-   <span data-ttu-id="27f8c-130">Quando l'oggetto viene creato per la prima volta, il conteggio dei riferimenti è 1.</span><span class="sxs-lookup"><span data-stu-id="27f8c-130">When the object is first created, its reference count is 1.</span></span> <span data-ttu-id="27f8c-131">A questo punto, il programma ha un solo puntatore all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="27f8c-131">At this point, the program has a single pointer to the object.</span></span>
-   <span data-ttu-id="27f8c-132">Il programma può creare un nuovo riferimento duplicando (copiando) il puntatore.</span><span class="sxs-lookup"><span data-stu-id="27f8c-132">The program can create a new reference by duplicating (copying) the pointer.</span></span> <span data-ttu-id="27f8c-133">Quando si copia il puntatore, è necessario chiamare il metodo [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="27f8c-133">When you copy the pointer, you must call the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method of the object.</span></span> <span data-ttu-id="27f8c-134">Questo metodo incrementa di uno il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="27f8c-134">This method increments the reference count by one.</span></span>
-   <span data-ttu-id="27f8c-135">Al termine dell'utilizzo di un puntatore all'oggetto, è necessario chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="27f8c-135">When you are finished using a pointer to the object, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="27f8c-136">Il metodo di **rilascio** decrementa il conteggio dei riferimenti di uno.</span><span class="sxs-lookup"><span data-stu-id="27f8c-136">The **Release** method decrements the reference count by one.</span></span> <span data-ttu-id="27f8c-137">Invalida anche il puntatore.</span><span class="sxs-lookup"><span data-stu-id="27f8c-137">It also invalidates the pointer.</span></span> <span data-ttu-id="27f8c-138">Non usare di nuovo il puntatore dopo la chiamata a **Release**.</span><span class="sxs-lookup"><span data-stu-id="27f8c-138">Do not use the pointer again after you call **Release**.</span></span> <span data-ttu-id="27f8c-139">Se si dispone di altri puntatori allo stesso oggetto, è possibile continuare a usare tali puntatori.</span><span class="sxs-lookup"><span data-stu-id="27f8c-139">(If you have other pointers to the same object, you can continue to use those pointers.)</span></span>
-   <span data-ttu-id="27f8c-140">Quando è stato chiamato [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con ogni puntatore, il conteggio dei riferimenti all'oggetto dell'oggetto raggiunge zero e l'oggetto viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="27f8c-140">When you have called [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with every pointer, the object reference count of the object reaches zero, and the object deletes itself.</span></span>

<span data-ttu-id="27f8c-141">Il diagramma seguente mostra un caso semplice, ma tipico.</span><span class="sxs-lookup"><span data-stu-id="27f8c-141">The following diagram shows a simple but typical case.</span></span>

![Diagramma che mostra un caso semplice di conteggio dei riferimenti.](images/com04.png)

<span data-ttu-id="27f8c-143">Il programma crea un oggetto e archivia un puntatore (*p*) all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="27f8c-143">The program creates an object and stores a pointer (*p*) to the object.</span></span> <span data-ttu-id="27f8c-144">A questo punto, il conteggio dei riferimenti è 1.</span><span class="sxs-lookup"><span data-stu-id="27f8c-144">At this point, the reference count is 1.</span></span> <span data-ttu-id="27f8c-145">Al termine dell'uso del puntatore, il programma chiama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="27f8c-145">When the program is finished using the pointer, it calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="27f8c-146">Il conteggio dei riferimenti viene decrementato a zero e l'oggetto viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="27f8c-146">The reference count is decremented to zero, and the object deletes itself.</span></span> <span data-ttu-id="27f8c-147">Ora *p* non è valido.</span><span class="sxs-lookup"><span data-stu-id="27f8c-147">Now *p* is invalid.</span></span> <span data-ttu-id="27f8c-148">Non è possibile utilizzare *p* per altre chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="27f8c-148">It is an error to use *p* for any further method calls.</span></span>

<span data-ttu-id="27f8c-149">Il diagramma seguente mostra un esempio più complesso.</span><span class="sxs-lookup"><span data-stu-id="27f8c-149">The next diagram shows a more complex example.</span></span>

![illustrazione che mostra il conteggio dei riferimenti](images/com05.png)

<span data-ttu-id="27f8c-151">In questo caso, il programma crea un oggetto e archivia il puntatore *p*, come prima.</span><span class="sxs-lookup"><span data-stu-id="27f8c-151">Here, the program creates an object and stores the pointer *p*, as before.</span></span> <span data-ttu-id="27f8c-152">Successivamente, il programma copia *p* in una nuova variabile, *d*.</span><span class="sxs-lookup"><span data-stu-id="27f8c-152">Next, the program copies *p* to a new variable, *q*.</span></span> <span data-ttu-id="27f8c-153">A questo punto, il programma deve chiamare [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) per incrementare il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="27f8c-153">At this point, the program must call [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) to increment the reference count.</span></span> <span data-ttu-id="27f8c-154">Il conteggio dei riferimenti è ora 2 e sono presenti due puntatori validi per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="27f8c-154">The reference count is now 2, and there are two valid pointers to the object.</span></span> <span data-ttu-id="27f8c-155">Si supponga ora che il programma sia terminato con *p*.</span><span class="sxs-lookup"><span data-stu-id="27f8c-155">Now suppose that the program is finished using *p*.</span></span> <span data-ttu-id="27f8c-156">Il programma chiama il [**rilascio**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), il conteggio dei riferimenti va a 1 e *p* non è più valido.</span><span class="sxs-lookup"><span data-stu-id="27f8c-156">The program calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), the reference count goes to 1, and *p* is no longer valid.</span></span> <span data-ttu-id="27f8c-157">Tuttavia, *q* è ancora valido.</span><span class="sxs-lookup"><span data-stu-id="27f8c-157">However, *q* is still valid.</span></span> <span data-ttu-id="27f8c-158">Successivamente, il programma termina con *q*.</span><span class="sxs-lookup"><span data-stu-id="27f8c-158">Later, the program finishes using *q*.</span></span> <span data-ttu-id="27f8c-159">Quindi chiama di nuovo **Release** .</span><span class="sxs-lookup"><span data-stu-id="27f8c-159">Therefore, it calls **Release** again.</span></span> <span data-ttu-id="27f8c-160">Il conteggio dei riferimenti va a zero e l'oggetto viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="27f8c-160">The reference count goes to zero, and the object deletes itself.</span></span>

<span data-ttu-id="27f8c-161">Ci si potrebbe chiedere perché il programma copia *p*.</span><span class="sxs-lookup"><span data-stu-id="27f8c-161">You might wonder why the program would copy *p*.</span></span> <span data-ttu-id="27f8c-162">Esistono due motivi principali: prima di tutto, è consigliabile archiviare il puntatore in una struttura di dati, ad esempio un elenco.</span><span class="sxs-lookup"><span data-stu-id="27f8c-162">There are two main reasons: First, you might want to store the pointer in a data structure, such as a list.</span></span> <span data-ttu-id="27f8c-163">In secondo luogo, è consigliabile lasciare il puntatore oltre l'ambito corrente della variabile originale.</span><span class="sxs-lookup"><span data-stu-id="27f8c-163">Second, you might want to keep the pointer beyond the current scope of the original variable.</span></span> <span data-ttu-id="27f8c-164">Pertanto, è necessario copiarlo in una nuova variabile con ambito più ampio.</span><span class="sxs-lookup"><span data-stu-id="27f8c-164">Therefore, you would copy it to a new variable with wider scope.</span></span>

<span data-ttu-id="27f8c-165">Un vantaggio del conteggio dei riferimenti è che è possibile condividere i puntatori in diverse sezioni di codice, senza che i vari percorsi di codice coordinano per eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="27f8c-165">One advantage of reference counting is that you can share pointers across different sections of code, without the various code paths coordinating to delete the object.</span></span> <span data-ttu-id="27f8c-166">Al contrario, ogni percorso del codice chiama semplicemente [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando il percorso del codice viene eseguito utilizzando l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="27f8c-166">Instead, each code path merely calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when that code path is done using the object.</span></span> <span data-ttu-id="27f8c-167">L'oggetto gestisce l'eliminazione di se stesso all'ora corretta.</span><span class="sxs-lookup"><span data-stu-id="27f8c-167">The object handles deleting itself at the correct time.</span></span>

## <a name="example"></a><span data-ttu-id="27f8c-168">Esempio</span><span class="sxs-lookup"><span data-stu-id="27f8c-168">Example</span></span>

<span data-ttu-id="27f8c-169">Di seguito è riportato il codice dall'esempio di finestra di [dialogo Apri](example--the-open-dialog-box.md) .</span><span class="sxs-lookup"><span data-stu-id="27f8c-169">Here is the code from the [Open dialog box example](example--the-open-dialog-box.md) again.</span></span>

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

<span data-ttu-id="27f8c-170">Il conteggio dei riferimenti viene eseguito in due posizioni in questo codice.</span><span class="sxs-lookup"><span data-stu-id="27f8c-170">Reference counting occurs in two places in this code.</span></span> <span data-ttu-id="27f8c-171">Innanzitutto, se il programma crea correttamente l'oggetto finestra di dialogo elemento comune, deve chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sul puntatore *pFileOpen* .</span><span class="sxs-lookup"><span data-stu-id="27f8c-171">First, if program successfully creates the Common Item Dialog object, it must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pFileOpen* pointer.</span></span>

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

<span data-ttu-id="27f8c-172">In secondo luogo, quando il metodo [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) restituisce un puntatore all'interfaccia [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , il programma deve chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sul puntatore *pItem* .</span><span class="sxs-lookup"><span data-stu-id="27f8c-172">Second, when the [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method returns a pointer to the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, the program must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pItem* pointer.</span></span>

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

<span data-ttu-id="27f8c-173">Si noti che in entrambi i casi, la chiamata di [**versione**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) è l'ultima cosa che si verifica prima che il puntatore esca dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="27f8c-173">Notice that in both cases, the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call is the last thing that happens before the pointer goes out of scope.</span></span> <span data-ttu-id="27f8c-174">Si noti inoltre che la **versione** viene chiamata solo dopo aver testato **HRESULT** per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="27f8c-174">Also notice that **Release** is called only after you test the **HRESULT** for success.</span></span> <span data-ttu-id="27f8c-175">Se, ad esempio, la chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha esito negativo, il puntatore *pFileOpen* non è valido.</span><span class="sxs-lookup"><span data-stu-id="27f8c-175">For example, if the call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails, the *pFileOpen* pointer is not valid.</span></span> <span data-ttu-id="27f8c-176">Quindi, sarebbe un errore chiamare **Release** sul puntatore.</span><span class="sxs-lookup"><span data-stu-id="27f8c-176">Therefore, it would be an error to call **Release** on the pointer.</span></span>

## <a name="next"></a><span data-ttu-id="27f8c-177">Prossima</span><span class="sxs-lookup"><span data-stu-id="27f8c-177">Next</span></span>

[<span data-ttu-id="27f8c-178">Richiesta di un oggetto per un'interfaccia</span><span class="sxs-lookup"><span data-stu-id="27f8c-178">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)