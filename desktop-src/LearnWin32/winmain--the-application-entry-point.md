---
title: WinMain il punto di ingresso dell'applicazione
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223558"
---
# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="43a37-103">WinMain: punto di ingresso dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="43a37-103">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="43a37-104">Ogni programma Windows include una funzione del punto di ingresso denominata **WinMain** o **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="43a37-104">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="43a37-105">Di seguito è illustrata la firma di **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="43a37-105">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="43a37-106">I quattro parametri sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="43a37-106">The four parameters are:</span></span>

-   <span data-ttu-id="43a37-107">*HINSTANCE* è un elemento denominato "handle per un'istanza" o "handle per un modulo".</span><span class="sxs-lookup"><span data-stu-id="43a37-107">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="43a37-108">Il sistema operativo utilizza questo valore per identificare il file eseguibile (EXE) quando viene caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="43a37-108">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="43a37-109">L'handle dell'istanza è necessario per determinate funzioni di Windows, ad esempio per caricare icone o bitmap.</span><span class="sxs-lookup"><span data-stu-id="43a37-109">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="43a37-110">*hPrevInstance* non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="43a37-110">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="43a37-111">È stata usata in Windows a 16 bit, ma ora è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="43a37-111">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="43a37-112">*pCmdLine* contiene gli argomenti della riga di comando come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="43a37-112">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="43a37-113">*nCmdShow* è un flag che indica se la finestra principale dell'applicazione verrà ridotta a icona, ingrandita o visualizzata normalmente.</span><span class="sxs-lookup"><span data-stu-id="43a37-113">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="43a37-114">La funzione restituisce un valore **int** .</span><span class="sxs-lookup"><span data-stu-id="43a37-114">The function returns an **int** value.</span></span> <span data-ttu-id="43a37-115">Il valore restituito non viene utilizzato dal sistema operativo, ma è possibile utilizzare il valore restituito per fornire un codice di stato a un altro programma che viene scritto.</span><span class="sxs-lookup"><span data-stu-id="43a37-115">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="43a37-116">**WINAPI** è la convenzione di chiamata.</span><span class="sxs-lookup"><span data-stu-id="43a37-116">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="43a37-117">Una *convenzione di chiamata* definisce il modo in cui una funzione riceve parametri dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="43a37-117">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="43a37-118">Ad esempio, definisce l'ordine in cui i parametri vengono visualizzati nello stack.</span><span class="sxs-lookup"><span data-stu-id="43a37-118">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="43a37-119">È sufficiente assicurarsi di dichiarare la funzione **wWinMain** come illustrato.</span><span class="sxs-lookup"><span data-stu-id="43a37-119">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="43a37-120">La funzione **WinMain** è identica a **wWinMain**, con la differenza che gli argomenti della riga di comando vengono passati come stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="43a37-120">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="43a37-121">È preferibile la versione Unicode.</span><span class="sxs-lookup"><span data-stu-id="43a37-121">The Unicode version is preferred.</span></span> <span data-ttu-id="43a37-122">È possibile usare la funzione ANSI **WinMain** anche se si compila il programma come Unicode.</span><span class="sxs-lookup"><span data-stu-id="43a37-122">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="43a37-123">Per ottenere una copia Unicode degli argomenti della riga di comando, chiamare la funzione [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="43a37-123">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="43a37-124">Questa funzione restituisce tutti gli argomenti in una singola stringa.</span><span class="sxs-lookup"><span data-stu-id="43a37-124">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="43a37-125">Se si desidera che gli argomenti siano una matrice di tipo *argv*, passare questa stringa a [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="43a37-125">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="43a37-126">In che modo il compilatore sa richiamare **wWinMain** invece della funzione **Main** standard?</span><span class="sxs-lookup"><span data-stu-id="43a37-126">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="43a37-127">In realtà, la libreria di runtime di Microsoft C (CRT) fornisce un'implementazione del **principale** che chiama **WinMain** o **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="43a37-127">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="43a37-128">CRT esegue alcune operazioni aggiuntive all'interno di **Main**.</span><span class="sxs-lookup"><span data-stu-id="43a37-128">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="43a37-129">Ad esempio, tutti gli inizializzatori statici vengono chiamati prima di **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="43a37-129">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="43a37-130">Sebbene sia possibile indicare al linker di usare una funzione del punto di ingresso diversa, usare il valore predefinito se si collega a CRT.</span><span class="sxs-lookup"><span data-stu-id="43a37-130">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="43a37-131">In caso contrario, il codice di inizializzazione CRT verrà ignorato, con risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="43a37-131">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="43a37-132">Gli oggetti globali, ad esempio, non verranno inizializzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="43a37-132">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="43a37-133">Ecco una funzione **WinMain** vuota.</span><span class="sxs-lookup"><span data-stu-id="43a37-133">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="43a37-134">Ora che si dispone di un punto di ingresso e si comprendono alcune delle convenzioni di codifica e terminologia di base, si è pronti per creare un programma Windows completo.</span><span class="sxs-lookup"><span data-stu-id="43a37-134">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="43a37-135">Prossima</span><span class="sxs-lookup"><span data-stu-id="43a37-135">Next</span></span>

<span data-ttu-id="43a37-136">[Modulo 1. Il primo programma Windows](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="43a37-136">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 