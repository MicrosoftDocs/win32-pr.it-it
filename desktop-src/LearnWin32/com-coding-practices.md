---
title: Procedure di codifica COM
description: Questo argomento descrive i modi per rendere il codice COM più efficace e affidabile.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104118587"
---
# <a name="com-coding-practices"></a><span data-ttu-id="2b83f-103">Procedure di codifica COM</span><span class="sxs-lookup"><span data-stu-id="2b83f-103">COM Coding Practices</span></span>

<span data-ttu-id="2b83f-104">Questo argomento descrive i modi per rendere il codice COM più efficace e affidabile.</span><span class="sxs-lookup"><span data-stu-id="2b83f-104">This topic describes ways to make your COM code more effective and robust.</span></span>

-   [<span data-ttu-id="2b83f-105">\_ \_ Operatore uuidof</span><span class="sxs-lookup"><span data-stu-id="2b83f-105">The \_\_uuidof Operator</span></span>](/windows)
-   [<span data-ttu-id="2b83f-106">La macro degli argomenti di IID \_ PPV \_</span><span class="sxs-lookup"><span data-stu-id="2b83f-106">The IID\_PPV\_ARGS Macro</span></span>](/windows)
-   [<span data-ttu-id="2b83f-107">Modello SafeRelease</span><span class="sxs-lookup"><span data-stu-id="2b83f-107">The SafeRelease Pattern</span></span>](#the-saferelease-pattern)
-   [<span data-ttu-id="2b83f-108">Puntatori intelligenti COM</span><span class="sxs-lookup"><span data-stu-id="2b83f-108">COM Smart Pointers</span></span>](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a><span data-ttu-id="2b83f-109">\_ \_ Operatore uuidof</span><span class="sxs-lookup"><span data-stu-id="2b83f-109">The \_\_uuidof Operator</span></span>

<span data-ttu-id="2b83f-110">Quando si compila il programma, è possibile che vengano visualizzati errori del linker simili ai seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b83f-110">When you build your program, you might get linker errors similar to the following:</span></span>

`unresolved external symbol "struct _GUID const IID_IDrawable"`

<span data-ttu-id="2b83f-111">Questo errore indica che è stata dichiarata una costante GUID con collegamento esterno (**extern**) e che il linker non è riuscito a trovare la definizione della costante.</span><span class="sxs-lookup"><span data-stu-id="2b83f-111">This error means that a GUID constant was declared with external linkage (**extern**), and the linker could not find the definition of the constant.</span></span> <span data-ttu-id="2b83f-112">Il valore di una costante GUID viene in genere esportato da un file di libreria statica.</span><span class="sxs-lookup"><span data-stu-id="2b83f-112">The value of a GUID constant is usually exported from a static library file.</span></span> <span data-ttu-id="2b83f-113">Se si usa Microsoft Visual C++, è possibile evitare di dover collegare una libreria statica usando l'operatore **\_ \_ uuidof** .</span><span class="sxs-lookup"><span data-stu-id="2b83f-113">If you are using Microsoft Visual C++, you can avoid the need to link a static library by using the **\_\_uuidof** operator.</span></span> <span data-ttu-id="2b83f-114">Questo operatore è un'estensione del linguaggio Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2b83f-114">This operator is a Microsoft language extension.</span></span> <span data-ttu-id="2b83f-115">Restituisce un valore GUID da un'espressione.</span><span class="sxs-lookup"><span data-stu-id="2b83f-115">It returns a GUID value from an expression.</span></span> <span data-ttu-id="2b83f-116">L'espressione può essere un nome di tipo interfaccia, un nome di classe o un puntatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2b83f-116">The expression can be an interface type name, a class name, or an interface pointer.</span></span> <span data-ttu-id="2b83f-117">Utilizzando **\_ \_ uuidof**, è possibile creare l'oggetto finestra di dialogo elemento comune come segue:</span><span class="sxs-lookup"><span data-stu-id="2b83f-117">Using **\_\_uuidof**, you can create the Common Item Dialog object as follows:</span></span>


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



<span data-ttu-id="2b83f-118">Il compilatore estrae il valore GUID dall'intestazione, pertanto non è necessaria alcuna esportazione della libreria.</span><span class="sxs-lookup"><span data-stu-id="2b83f-118">The compiler extracts the GUID value from the header, so no library export is necessary.</span></span>

> [!Note]  
> <span data-ttu-id="2b83f-119">Il valore GUID è associato al nome del tipo dichiarando `__declspec(uuid( ... ))` nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="2b83f-119">The GUID value is associated with the type name by declaring `__declspec(uuid( ... ))` in the header.</span></span> <span data-ttu-id="2b83f-120">Per ulteriori informazioni, vedere la documentazione relativa a **\_ \_ declspec** nella documentazione di Visual C++.</span><span class="sxs-lookup"><span data-stu-id="2b83f-120">For more information, see the documentation for **\_\_declspec** in the Visual C++ documentation.</span></span>

 

## <a name="the-iid_ppv_args-macro"></a><span data-ttu-id="2b83f-121">La macro degli argomenti di IID \_ PPV \_</span><span class="sxs-lookup"><span data-stu-id="2b83f-121">The IID\_PPV\_ARGS Macro</span></span>

<span data-ttu-id="2b83f-122">È stato rilevato che per [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) è necessario assegnare il parametro finale a un tipo **void \* \*** .</span><span class="sxs-lookup"><span data-stu-id="2b83f-122">We saw that both [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) require coercing the final parameter to a **void\*\*** type.</span></span> <span data-ttu-id="2b83f-123">Ciò crea il rischio di mancata corrispondenza del tipo.</span><span class="sxs-lookup"><span data-stu-id="2b83f-123">This creates the potential for a type mismatch.</span></span> <span data-ttu-id="2b83f-124">Si consideri il frammento di codice riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2b83f-124">Consider the following code fragment:</span></span>


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



<span data-ttu-id="2b83f-125">Questo codice richiede l'interfaccia [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , ma passa un puntatore [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="2b83f-125">This code asks for the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface, but passes in an [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer.</span></span> <span data-ttu-id="2b83f-126">L'espressione **\_ cast reinterpretate** elude il sistema di tipi C++, pertanto il compilatore non rileverà questo errore.</span><span class="sxs-lookup"><span data-stu-id="2b83f-126">The **reinterpret\_cast** expression circumvents the C++ type system, so the compiler will not catch this error.</span></span> <span data-ttu-id="2b83f-127">Nel migliore dei casi, se l'oggetto non implementa l'interfaccia richiesta, la chiamata ha semplicemente esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2b83f-127">In the best case, if the object does not implement the requested interface, the call simply fails.</span></span> <span data-ttu-id="2b83f-128">Nel peggiore dei casi, la funzione ha esito positivo e si dispone di un puntatore non corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2b83f-128">In the worst case, the function succeeds and you have a mismatched pointer.</span></span> <span data-ttu-id="2b83f-129">In altre parole, il tipo di puntatore non corrisponde alla vtable effettiva in memoria.</span><span class="sxs-lookup"><span data-stu-id="2b83f-129">In other words, the pointer type does not match the actual vtable in memory.</span></span> <span data-ttu-id="2b83f-130">Come si può immaginare, a questo punto non è possibile che si verifichino elementi validi.</span><span class="sxs-lookup"><span data-stu-id="2b83f-130">As you can imagine, nothing good can happen at that point.</span></span>

> [!Note]  
> <span data-ttu-id="2b83f-131">Un oggetto *vtable* (tabella dei metodi virtuali) è una tabella di puntatori a funzione.</span><span class="sxs-lookup"><span data-stu-id="2b83f-131">A *vtable* (virtual method table) is a table of function pointers.</span></span> <span data-ttu-id="2b83f-132">Vtable è il modo in cui COM associa una chiamata al metodo alla relativa implementazione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2b83f-132">The vtable is how COM binds a method call to its implementation at run time.</span></span> <span data-ttu-id="2b83f-133">Per la maggior parte dei compilatori C++ implementano i metodi virtuali, vtable.</span><span class="sxs-lookup"><span data-stu-id="2b83f-133">Not coincidentally, vtables are how most C++ compilers implement virtual methods.</span></span>

 

<span data-ttu-id="2b83f-134">La macro [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) consente di evitare questa classe di errore.</span><span class="sxs-lookup"><span data-stu-id="2b83f-134">The [**IID\_PPV\_ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) macro helps to avoid this class of error.</span></span> <span data-ttu-id="2b83f-135">Per usare questa macro, sostituire il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="2b83f-135">To use this macro, replace the following code:</span></span>


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



<span data-ttu-id="2b83f-136">con il seguente:</span><span class="sxs-lookup"><span data-stu-id="2b83f-136">with this:</span></span>


```C++
IID_PPV_ARGS(&pFileOpen)
```



<span data-ttu-id="2b83f-137">La macro inserisce automaticamente `__uuidof(IFileOpenDialog)` per l'identificatore di interfaccia, quindi è garantita la corrispondenza con il tipo di puntatore.</span><span class="sxs-lookup"><span data-stu-id="2b83f-137">The macro automatically inserts `__uuidof(IFileOpenDialog)` for the interface identifier, so it is guaranteed to match the pointer type.</span></span> <span data-ttu-id="2b83f-138">Ecco il codice modificato (e corretto):</span><span class="sxs-lookup"><span data-stu-id="2b83f-138">Here is the modified (and correct) code:</span></span>


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



<span data-ttu-id="2b83f-139">È possibile usare la stessa macro con [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="2b83f-139">You can use the same macro with [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a><span data-ttu-id="2b83f-140">Modello SafeRelease</span><span class="sxs-lookup"><span data-stu-id="2b83f-140">The SafeRelease Pattern</span></span>

<span data-ttu-id="2b83f-141">Il conteggio dei riferimenti è uno degli elementi della programmazione che è sostanzialmente semplice, ma è anche noioso, il che rende più semplice l'errore.</span><span class="sxs-lookup"><span data-stu-id="2b83f-141">Reference counting is one of those things in programming that is basically easy, but is also tedious, which makes it easy to get wrong.</span></span> <span data-ttu-id="2b83f-142">Gli errori tipici comprendono:</span><span class="sxs-lookup"><span data-stu-id="2b83f-142">Typical errors include:</span></span>

-   <span data-ttu-id="2b83f-143">Errore di rilascio di un puntatore a interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="2b83f-143">Failing to release an interface pointer when you are done using it.</span></span> <span data-ttu-id="2b83f-144">Questa classe di bug provocherà la perdita di memoria e di altre risorse da un programma, perché gli oggetti non vengono eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="2b83f-144">This class of bug will cause your program to leak memory and other resources, because objects are not destroyed.</span></span>
-   <span data-ttu-id="2b83f-145">Chiamata della [**versione**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="2b83f-145">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with an invalid pointer.</span></span> <span data-ttu-id="2b83f-146">Questo errore può verificarsi, ad esempio, se l'oggetto non è mai stato creato.</span><span class="sxs-lookup"><span data-stu-id="2b83f-146">For example, this error can happen if the object was never created.</span></span> <span data-ttu-id="2b83f-147">Questa categoria di bug provocherà probabilmente un arresto anomalo del programma.</span><span class="sxs-lookup"><span data-stu-id="2b83f-147">This category of bug will probably cause your program to crash.</span></span>
-   <span data-ttu-id="2b83f-148">Dereferenziazione di un puntatore a interfaccia dopo la chiamata di [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="2b83f-148">Dereferencing an interface pointer after [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) is called.</span></span> <span data-ttu-id="2b83f-149">Questo bug può causare l'arresto anomalo del programma.</span><span class="sxs-lookup"><span data-stu-id="2b83f-149">This bug may cause your program to crash.</span></span> <span data-ttu-id="2b83f-150">Peggiori, potrebbe causare l'arresto anomalo del programma in un momento successivo, rendendo difficile l'individuazione dell'errore originale.</span><span class="sxs-lookup"><span data-stu-id="2b83f-150">Worse, it may cause your program to crash at a random later time, making it hard to track down the original error.</span></span>

<span data-ttu-id="2b83f-151">Un modo per evitare questi bug consiste nel chiamare il metodo [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) tramite una funzione che rilascia in modo sicuro il puntatore.</span><span class="sxs-lookup"><span data-stu-id="2b83f-151">One way to avoid these bugs is to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) through a function that safely releases the pointer.</span></span> <span data-ttu-id="2b83f-152">Nel codice seguente viene illustrata una funzione che esegue questa operazione:</span><span class="sxs-lookup"><span data-stu-id="2b83f-152">The following code shows a function that does this:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



<span data-ttu-id="2b83f-153">Questa funzione accetta un puntatore a interfaccia COM come parametro ed esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b83f-153">This function takes a COM interface pointer as a parameter and does the following:</span></span>

1.  <span data-ttu-id="2b83f-154">Controlla se il puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="2b83f-154">Checks whether the pointer is **NULL**.</span></span>
2.  <span data-ttu-id="2b83f-155">Chiama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se il puntatore non è **null**.</span><span class="sxs-lookup"><span data-stu-id="2b83f-155">Calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) if the pointer is not **NULL**.</span></span>
3.  <span data-ttu-id="2b83f-156">Imposta il puntatore su **null**.</span><span class="sxs-lookup"><span data-stu-id="2b83f-156">Sets the pointer to **NULL**.</span></span>

<span data-ttu-id="2b83f-157">Di seguito è riportato un esempio di come usare `SafeRelease` :</span><span class="sxs-lookup"><span data-stu-id="2b83f-157">Here is an example of how to use `SafeRelease`:</span></span>


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



<span data-ttu-id="2b83f-158">Se [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha esito positivo, la chiamata a `SafeRelease` rilascia il puntatore.</span><span class="sxs-lookup"><span data-stu-id="2b83f-158">If [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) succeeds, the call to `SafeRelease` releases the pointer.</span></span> <span data-ttu-id="2b83f-159">Se **CoCreateInstance** ha esito negativo, *pFileOpen* rimane **null**.</span><span class="sxs-lookup"><span data-stu-id="2b83f-159">If **CoCreateInstance** fails, *pFileOpen* remains **NULL**.</span></span> <span data-ttu-id="2b83f-160">La `SafeRelease` funzione verifica l'oggetto e ignora la chiamata a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="2b83f-160">The `SafeRelease` function checks for this and skips the call to [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span>

<span data-ttu-id="2b83f-161">È anche possibile chiamare `SafeRelease` più volte nello stesso puntatore, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2b83f-161">It is also safe to call `SafeRelease` more than once on the same pointer, as shown here:</span></span>


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a><span data-ttu-id="2b83f-162">Puntatori intelligenti COM</span><span class="sxs-lookup"><span data-stu-id="2b83f-162">COM Smart Pointers</span></span>

<span data-ttu-id="2b83f-163">La `SafeRelease` funzione è utile, ma è necessario ricordare due elementi:</span><span class="sxs-lookup"><span data-stu-id="2b83f-163">The `SafeRelease` function is useful, but it requires you to remember two things:</span></span>

-   <span data-ttu-id="2b83f-164">Inizializzare ogni puntatore di interfaccia su **null**.</span><span class="sxs-lookup"><span data-stu-id="2b83f-164">Initialize every interface pointer to **NULL**.</span></span>
-   <span data-ttu-id="2b83f-165">Chiamare `SafeRelease` prima che ogni puntatore esca dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="2b83f-165">Call `SafeRelease` before each pointer goes out of scope.</span></span>

<span data-ttu-id="2b83f-166">In qualità di programmatore C++, è probabile che si stia pensando di non dover ricordare uno di questi aspetti.</span><span class="sxs-lookup"><span data-stu-id="2b83f-166">As a C++ programmer, you are probably thinking that you shouldn't have to remember either of these things.</span></span> <span data-ttu-id="2b83f-167">Per questo motivo, C++ dispone di costruttori e distruttori.</span><span class="sxs-lookup"><span data-stu-id="2b83f-167">After all, that's why C++ has constructors and destructors.</span></span> <span data-ttu-id="2b83f-168">Sarebbe bello avere una classe che esegue il wrapping del puntatore a interfaccia sottostante e Inizializza e rilascia automaticamente il puntatore.</span><span class="sxs-lookup"><span data-stu-id="2b83f-168">It would be nice to have a class that wraps the underlying interface pointer and automatically initializes and releases the pointer.</span></span> <span data-ttu-id="2b83f-169">In altre parole, è necessario avere un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="2b83f-169">In other words, we want something like this:</span></span>


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



<span data-ttu-id="2b83f-170">La definizione della classe riportata di seguito è incompleta e non è utilizzabile come illustrato.</span><span class="sxs-lookup"><span data-stu-id="2b83f-170">The class definition shown here is incomplete, and is not usable as shown.</span></span> <span data-ttu-id="2b83f-171">Come minimo, è necessario definire un costruttore di copia, un operatore di assegnazione e un modo per accedere al puntatore COM sottostante.</span><span class="sxs-lookup"><span data-stu-id="2b83f-171">At a minimum, you would need to define a copy constructor, an assignment operator, and a way to access the underlying COM pointer.</span></span> <span data-ttu-id="2b83f-172">Fortunatamente, non è necessario eseguire alcuna operazione, perché Microsoft Visual Studio fornisce già una classe di puntatore intelligente come parte del Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="2b83f-172">Fortunately, you don't need to do any of this work, because Microsoft Visual Studio already provides a smart pointer class as part of the Active Template Library (ATL).</span></span>

<span data-ttu-id="2b83f-173">La classe del puntatore intelligente ATL è denominata **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="2b83f-173">The ATL smart pointer class is named **CComPtr**.</span></span> <span data-ttu-id="2b83f-174">(Esiste anche una classe **CComQIPtr** , che non viene discussa qui). Ecco l'esempio di finestra di [dialogo Apri](example--the-open-dialog-box.md) riscritta per usare **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="2b83f-174">(There is also a **CComQIPtr** class, which is not discussed here.) Here is the [Open Dialog Box](example--the-open-dialog-box.md) example rewritten to use **CComPtr**.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="2b83f-175">La differenza principale tra questo codice e l'esempio originale è che questa versione non chiama in modo esplicito [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="2b83f-175">The main difference between this code and the original example is that this version does not explicitly call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="2b83f-176">Quando l'istanza di **CComPtr** esce dall'ambito, il distruttore chiama **Release** sul puntatore sottostante.</span><span class="sxs-lookup"><span data-stu-id="2b83f-176">When the **CComPtr** instance goes out of scope, the destructor calls **Release** on the underlying pointer.</span></span>

<span data-ttu-id="2b83f-177">**CComPtr** è un modello di classe.</span><span class="sxs-lookup"><span data-stu-id="2b83f-177">**CComPtr** is a class template.</span></span> <span data-ttu-id="2b83f-178">L'argomento di modello è il tipo di interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="2b83f-178">The template argument is the COM interface type.</span></span> <span data-ttu-id="2b83f-179">Internamente, **CComPtr** include un puntatore di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="2b83f-179">Internally, **CComPtr** holds a pointer of that type.</span></span> <span data-ttu-id="2b83f-180">**CComPtr** esegue l'override di **operator-> ()** e dell' **operatore& ()** in modo che la classe funga da puntatore sottostante.</span><span class="sxs-lookup"><span data-stu-id="2b83f-180">**CComPtr** overrides **operator->()** and **operator&()** so that the class acts like the underlying pointer.</span></span> <span data-ttu-id="2b83f-181">Ad esempio, il codice seguente equivale a chiamare direttamente il metodo **IFileOpenDialog:: Show** :</span><span class="sxs-lookup"><span data-stu-id="2b83f-181">For example, the following code is equivalent to calling the **IFileOpenDialog::Show** method directly:</span></span>


```C++
hr = pFileOpen->Show(NULL);
```



<span data-ttu-id="2b83f-182">**CComPtr** definisce anche un metodo **CComPtr:: CoCreateInstance** , che chiama la funzione com [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con alcuni valori di parametro predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2b83f-182">**CComPtr** also defines a **CComPtr::CoCreateInstance** method, which calls the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function with some default parameter values.</span></span> <span data-ttu-id="2b83f-183">L'unico parametro obbligatorio è l'identificatore della classe, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="2b83f-183">The only required parameter is the class identifier, as the next example shows:</span></span>


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



<span data-ttu-id="2b83f-184">Il metodo **CComPtr:: CoCreateInstance** viene fornito esclusivamente come praticità. Se lo si preferisce, è comunque possibile chiamare la funzione COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="2b83f-184">The **CComPtr::CoCreateInstance** method is provided purely as a convenience; you can still call the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, if you prefer.</span></span>

## <a name="next"></a><span data-ttu-id="2b83f-185">Prossima</span><span class="sxs-lookup"><span data-stu-id="2b83f-185">Next</span></span>

[<span data-ttu-id="2b83f-186">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="2b83f-186">Error Handling in COM</span></span>](error-handling-in-com.md)

 

 