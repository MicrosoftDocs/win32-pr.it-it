---
<span data-ttu-id="27c9d-101">title: WinMain Descrizione del punto di ingresso dell'applicazione: WinMain: Punto di ingresso dell'applicazione ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="27c9d-101">title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="27c9d-102">WinMain: punto di ingresso dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="27c9d-102">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="27c9d-103">Ogni programma Windows include una funzione del punto di ingresso denominata **WinMain** o **wWinMain.**</span><span class="sxs-lookup"><span data-stu-id="27c9d-103">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="27c9d-104">Ecco la firma per **wWinMain.**</span><span class="sxs-lookup"><span data-stu-id="27c9d-104">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="27c9d-105">I quattro parametri sono:</span><span class="sxs-lookup"><span data-stu-id="27c9d-105">The four parameters are:</span></span>

-   <span data-ttu-id="27c9d-106">*hInstance* è un elemento denominato "handle per un'istanza" o "handle per un modulo".</span><span class="sxs-lookup"><span data-stu-id="27c9d-106">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="27c9d-107">Il sistema operativo usa questo valore per identificare il file eseguibile (EXE) quando viene caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="27c9d-107">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="27c9d-108">L'handle di istanza è necessario per alcune funzioni di Windows, ad esempio per caricare icone o bitmap.</span><span class="sxs-lookup"><span data-stu-id="27c9d-108">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="27c9d-109">*hPrevInstance* non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="27c9d-109">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="27c9d-110">È stato usato in Windows a 16 bit, ma ora è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="27c9d-110">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="27c9d-111">*pCmdLine contiene* gli argomenti della riga di comando come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="27c9d-111">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="27c9d-112">*nCmdShow è* un flag che indica se la finestra principale dell'applicazione verrà ridotta a icona, ingrandita o visualizzata normalmente.</span><span class="sxs-lookup"><span data-stu-id="27c9d-112">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="27c9d-113">La funzione restituisce un **valore int.**</span><span class="sxs-lookup"><span data-stu-id="27c9d-113">The function returns an **int** value.</span></span> <span data-ttu-id="27c9d-114">Il valore restituito non viene usato dal sistema operativo, ma è possibile usare il valore restituito per trasmettere un codice di stato a un altro programma scritto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="27c9d-114">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="27c9d-115">**WINAPI è** la convenzione di chiamata.</span><span class="sxs-lookup"><span data-stu-id="27c9d-115">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="27c9d-116">Una *convenzione di* chiamata definisce il modo in cui una funzione riceve i parametri dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="27c9d-116">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="27c9d-117">Ad esempio, definisce l'ordine in cui i parametri vengono visualizzati nello stack.</span><span class="sxs-lookup"><span data-stu-id="27c9d-117">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="27c9d-118">È sufficiente assicurarsi di dichiarare la **funzione wWinMain** come illustrato.</span><span class="sxs-lookup"><span data-stu-id="27c9d-118">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="27c9d-119">La **funzione WinMain** è identica a **wWinMain,** ad eccezione del fatto che gli argomenti della riga di comando vengono passati come stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="27c9d-119">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="27c9d-120">È preferibile la versione Unicode.</span><span class="sxs-lookup"><span data-stu-id="27c9d-120">The Unicode version is preferred.</span></span> <span data-ttu-id="27c9d-121">È possibile usare la funzione ANSI **WinMain** anche se si compila il programma come Unicode.</span><span class="sxs-lookup"><span data-stu-id="27c9d-121">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="27c9d-122">Per ottenere una copia Unicode degli argomenti della riga di comando, chiamare la [**funzione GetCommandLine.**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea)</span><span class="sxs-lookup"><span data-stu-id="27c9d-122">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="27c9d-123">Questa funzione restituisce tutti gli argomenti in una singola stringa.</span><span class="sxs-lookup"><span data-stu-id="27c9d-123">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="27c9d-124">Se si vogliono gli argomenti come matrice di tipo *argv,* passare questa stringa a [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="27c9d-124">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="27c9d-125">Come fa il compilatore a richiamare **wWinMain** anziché la funzione **main** standard?</span><span class="sxs-lookup"><span data-stu-id="27c9d-125">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="27c9d-126">Ciò che accade è che la libreria di runtime di Microsoft C (CRT) fornisce un'implementazione di **main** che chiama **WinMain** o **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="27c9d-126">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="27c9d-127">CRT esegue alcune operazioni aggiuntive all'interno **di main**.</span><span class="sxs-lookup"><span data-stu-id="27c9d-127">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="27c9d-128">Ad esempio, tutti gli inizializzatori statici vengono chiamati prima **di wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="27c9d-128">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="27c9d-129">Anche se è possibile indicare al linker di usare una funzione del punto di ingresso diversa, usare l'impostazione predefinita se ci si collega a CRT.</span><span class="sxs-lookup"><span data-stu-id="27c9d-129">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="27c9d-130">In caso contrario, il codice di inizializzazione CRT verrà ignorato, con risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="27c9d-130">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="27c9d-131">Ad esempio, gli oggetti globali non verranno inizializzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="27c9d-131">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="27c9d-132">Ecco una funzione **WinMain** vuota.</span><span class="sxs-lookup"><span data-stu-id="27c9d-132">Here is an empty **WinMain** function.</span></span>


```C++
INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="27c9d-133">Dopo aver creato il punto di ingresso e aver compreso alcune delle convenzioni di terminologia e codifica di base, si è pronti per creare un programma Window completo.</span><span class="sxs-lookup"><span data-stu-id="27c9d-133">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="27c9d-134">Prossima</span><span class="sxs-lookup"><span data-stu-id="27c9d-134">Next</span></span>

<span data-ttu-id="27c9d-135">[Modulo 1. Il primo programma windows](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="27c9d-135">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 
