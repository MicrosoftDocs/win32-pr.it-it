---
description: In questa sezione viene descritto come stampare da un programma desktop di Windows nativo.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Stampa di app desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317285"
---
# <a name="desktop-app-printing"></a><span data-ttu-id="f8a88-103">Stampa di app desktop</span><span class="sxs-lookup"><span data-stu-id="f8a88-103">Desktop App Printing</span></span>

<span data-ttu-id="f8a88-104">In questa sezione viene descritto come stampare da un programma desktop di Windows nativo.</span><span class="sxs-lookup"><span data-stu-id="f8a88-104">This section describes how to print from a native Windows desktop program.</span></span>

## <a name="overview"></a><span data-ttu-id="f8a88-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="f8a88-105">Overview</span></span>

<span data-ttu-id="f8a88-106">Per offrire la migliore esperienza utente quando si esegue la stampa da un programma Windows nativo, è necessario che il programma sia progettato per la stampa da un thread dedicato.</span><span class="sxs-lookup"><span data-stu-id="f8a88-106">To provide the best user experience when you print from a native Windows program, the program must be designed to print from a dedicated thread.</span></span> <span data-ttu-id="f8a88-107">In un programma Windows nativo il programma è responsabile della gestione degli eventi e dei messaggi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f8a88-107">In a native Windows program, the program is responsible for managing user interface events and messages.</span></span> <span data-ttu-id="f8a88-108">Le operazioni di stampa possono richiedere periodi di calcolo intensivo quando viene eseguito il rendering del contenuto dell'applicazione per la stampante, che può impedire che il programma risponda all'interazione dell'utente se questa elaborazione viene eseguita nello stesso thread dell'elaborazione di eventi dell'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f8a88-108">Printing operations can require periods of intense computation as the application content is rendered for the printer, which can prevent the program from responding to user interaction if this processing is performed in the same thread as event processing of the user interaction.</span></span>

<span data-ttu-id="f8a88-109">Se si ha già familiarità con la scrittura di un programma Windows nativo multithread, è possibile passare direttamente alla [modalità di stampa da un'applicazione Windows](how-to--print-from-a-windows-application.md) e apprendere come aggiungere funzionalità di stampa al programma.</span><span class="sxs-lookup"><span data-stu-id="f8a88-109">If you are already familiar with how to write a multi-threaded native Windows program, you go directly to [How to print from a Windows application](how-to--print-from-a-windows-application.md) and learn how to add printing functionality to your program.</span></span>

### <a name="basic-windows-program-requirements"></a><span data-ttu-id="f8a88-110">Requisiti del programma Windows di base</span><span class="sxs-lookup"><span data-stu-id="f8a88-110">Basic Windows Program Requirements</span></span>

<span data-ttu-id="f8a88-111">Per ottimizzare le prestazioni e la velocità di risposta del programma, non eseguire l'elaborazione del processo di stampa di un programma nel thread che elabora l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f8a88-111">For best performance and program responsiveness, do not perform a program's print job processing in the thread that processes user interaction.</span></span>

<span data-ttu-id="f8a88-112">Questa separazione della stampa dall'interazione dell'utente influirà sul modo in cui il programma gestisce i dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8a88-112">This separation of printing from user interaction will influence how the program manages the application data.</span></span> <span data-ttu-id="f8a88-113">Prima di iniziare a scrivere l'applicazione, è necessario comprendere attentamente queste implicazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a88-113">You should thoroughly understand these implications before you start writing the application.</span></span> <span data-ttu-id="f8a88-114">Negli argomenti seguenti vengono descritti i requisiti di base per la gestione della stampa in un thread separato di un programma.</span><span class="sxs-lookup"><span data-stu-id="f8a88-114">The following topics describe the basic requirements of handling printing in a separate thread of a program.</span></span>

### <a name="windows-program-basics"></a><span data-ttu-id="f8a88-115">Nozioni fondamentali sui programmi Windows</span><span class="sxs-lookup"><span data-stu-id="f8a88-115">Windows Program Basics</span></span>

<span data-ttu-id="f8a88-116">Un programma Windows nativo deve fornire la routine della finestra principale per elaborare i messaggi della finestra ricevuti dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f8a88-116">A native Windows program must provide the main window procedure to process the window messages that it receives from the operating system.</span></span> <span data-ttu-id="f8a88-117">Ogni finestra di un programma Windows ha una funzione **WndProc** corrispondente che elabora i messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="f8a88-117">Every window in a Windows program has a corresponding **WndProc** function that processes these window messages.</span></span> <span data-ttu-id="f8a88-118">Il thread in cui viene eseguita questa funzione è denominato interfaccia utente, o interfaccia utente, thread.</span><span class="sxs-lookup"><span data-stu-id="f8a88-118">The thread in which this function runs is called the user interface, or UI, thread.</span></span>

<span data-ttu-id="f8a88-119">**Usare le risorse per le stringhe.**</span><span class="sxs-lookup"><span data-stu-id="f8a88-119">**Use resources for strings.**</span></span>  
<span data-ttu-id="f8a88-120">Usare le risorse di stringa dal file di risorse del programma invece delle costanti stringa per le stringhe che potrebbero dover essere modificate quando si supporta un'altra lingua.</span><span class="sxs-lookup"><span data-stu-id="f8a88-120">Use string resources from the program's resource file instead of string constants for strings that might need to be changed when you support another language.</span></span> <span data-ttu-id="f8a88-121">Prima che un programma possa usare una risorsa di stringa come stringa, il programma deve recuperare la risorsa dal file di risorse e copiarla in un buffer di memoria locale.</span><span class="sxs-lookup"><span data-stu-id="f8a88-121">Before a program can use a string resource as a string, the program must retrieve the resource from the resource file and copy it to a local memory buffer.</span></span> <span data-ttu-id="f8a88-122">Questa operazione richiede una programmazione aggiuntiva all'inizio, ma consente di semplificare la modifica, la traduzione e la localizzazione del programma in futuro.</span><span class="sxs-lookup"><span data-stu-id="f8a88-122">This requires some additional programming in the beginning, but allows for easier modification, translation, and localization of the program in the future.</span></span>  
<span data-ttu-id="f8a88-123">**Elaborare i dati nei passaggi.**</span><span class="sxs-lookup"><span data-stu-id="f8a88-123">**Process data in steps.**</span></span>  
<span data-ttu-id="f8a88-124">Elaborare il processo di stampa nei passaggi che possono essere interrotti.</span><span class="sxs-lookup"><span data-stu-id="f8a88-124">Process the print job in steps that can be interrupted.</span></span> <span data-ttu-id="f8a88-125">Questa progettazione consente all'utente di annullare un'operazione di elaborazione lunga prima del completamento e impedisce al programma di bloccare altri programmi che potrebbero essere in esecuzione nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="f8a88-125">This design makes it possible for the user to cancel a long processing operation before it completes and prevents the program from blocking other programs that might be running at the same time.</span></span>  
<span data-ttu-id="f8a88-126">**Usare i dati utente della finestra.**</span><span class="sxs-lookup"><span data-stu-id="f8a88-126">**Use window user data.**</span></span>  
<span data-ttu-id="f8a88-127">Le applicazioni di stampa hanno spesso più finestre e thread.</span><span class="sxs-lookup"><span data-stu-id="f8a88-127">Printing applications often have several windows and threads.</span></span> <span data-ttu-id="f8a88-128">Per rendere disponibili i dati tra i thread e i passaggi di elaborazione senza utilizzare variabili globali statiche, fare riferimento alle strutture di dati mediante un puntatore ai dati che fa parte della finestra in cui vengono utilizzate.</span><span class="sxs-lookup"><span data-stu-id="f8a88-128">To keep the data available between threads and processing steps without using static, global variables, reference the data structures by a data pointer that is part of the window in which they are used.</span></span>  


<span data-ttu-id="f8a88-129">Nell'esempio di codice riportato di seguito viene illustrato un punto di ingresso principale per un'applicazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="f8a88-129">The following code example shows a main entry point for a printing application.</span></span> <span data-ttu-id="f8a88-130">Questo esempio illustra come usare le risorse di stringa anziché le costanti di stringa e Mostra anche il ciclo di messaggi principale che elabora i messaggi della finestra del programma.</span><span class="sxs-lookup"><span data-stu-id="f8a88-130">This example shows how to use string resources instead of string constants and also shows the main message loop that processes the program's window messages.</span></span>


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a><span data-ttu-id="f8a88-131">Informazioni sul documento</span><span class="sxs-lookup"><span data-stu-id="f8a88-131">Document Information</span></span>

<span data-ttu-id="f8a88-132">I programmi Windows nativi stampati devono essere progettati per l'elaborazione multithread.</span><span class="sxs-lookup"><span data-stu-id="f8a88-132">Native Windows programs that print should be designed for multi-threaded processing.</span></span> <span data-ttu-id="f8a88-133">Uno dei requisiti di una progettazione multithread consiste nel proteggere gli elementi dati del programma in modo che siano sicuri per l'uso di più thread contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="f8a88-133">One of the requirements of a multi-threaded design is to protect the program's data elements so that they are safe for multiple threads to use at the same time.</span></span> <span data-ttu-id="f8a88-134">È possibile proteggere gli elementi dati utilizzando gli oggetti di sincronizzazione e organizzando i dati per evitare conflitti tra i thread.</span><span class="sxs-lookup"><span data-stu-id="f8a88-134">You can protect data elements by using synchronization objects and organizing the data to avoid conflicts between the threads.</span></span> <span data-ttu-id="f8a88-135">Allo stesso tempo, il programma deve impedire modifiche ai dati del programma durante la stampa.</span><span class="sxs-lookup"><span data-stu-id="f8a88-135">At the same time, the program must prevent changes to the program data while it is being printed.</span></span> <span data-ttu-id="f8a88-136">Il programma di esempio usa diverse tecniche di programmazione multithread.</span><span class="sxs-lookup"><span data-stu-id="f8a88-136">The sample program uses several different multi-threaded programming techniques.</span></span>

 <span data-ttu-id="f8a88-137">**Eventi di sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="f8a88-137">**Synchronization Events**</span></span>  
<span data-ttu-id="f8a88-138">Il programma di esempio utilizza eventi, handle di thread e funzioni di attesa per sincronizzare l'elaborazione tra il thread di stampa e il programma principale e per indicare che i dati sono in uso.</span><span class="sxs-lookup"><span data-stu-id="f8a88-138">The sample program uses events, thread handles, and wait functions to synchronize the processing between the print thread and the main program and to indicate that the data is in use.</span></span>  
<span data-ttu-id="f8a88-139">**Messaggi di Windows specifici dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="f8a88-139">**Application-Specific Windows Messages**</span></span>  
<span data-ttu-id="f8a88-140">Il programma di esempio utilizza messaggi finestra specifici dell'applicazione per rendere il programma più compatibile con altri programmi Windows nativi.</span><span class="sxs-lookup"><span data-stu-id="f8a88-140">The sample program uses application-specific window messages to make the program more compatible with other native Windows programs.</span></span> <span data-ttu-id="f8a88-141">Suddividendo l'elaborazione in passaggi più piccoli e accodando tali passaggi nel ciclo di messaggi della finestra, è più semplice per Windows gestire l'elaborazione senza bloccare altre applicazioni che potrebbero essere in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="f8a88-141">Breaking the processing into smaller steps and queuing those steps in the window message loop makes it easier for Windows to manage the processing without blocking other applications that might also be running on the computer.</span></span>  
<span data-ttu-id="f8a88-142">**strutture di dati**</span><span class="sxs-lookup"><span data-stu-id="f8a88-142">**Data Structures**</span></span>  
<span data-ttu-id="f8a88-143">Il programma di esempio non viene scritto in uno stile orientato a oggetti utilizzando oggetti e classi, sebbene raggruppa gli elementi dati in strutture di dati.</span><span class="sxs-lookup"><span data-stu-id="f8a88-143">The sample program is not written in an object-oriented style using objects and classes, although it does group data elements into data structures.</span></span> <span data-ttu-id="f8a88-144">Nell'esempio non viene utilizzato un approccio orientato agli oggetti per evitare di implicare che un approccio è migliore o peggiore di un altro.</span><span class="sxs-lookup"><span data-stu-id="f8a88-144">The sample does not use an object-oriented approach to avoid implying that one approach is better or worse than another.</span></span>  
<span data-ttu-id="f8a88-145">È possibile utilizzare le funzioni e le strutture di dati del programma di esempio come punto di partenza quando si progetta il programma.</span><span class="sxs-lookup"><span data-stu-id="f8a88-145">You can use the functions and data structures of the sample program as a starting point when you design your program.</span></span> <span data-ttu-id="f8a88-146">Se si decide di progettare un programma orientato a oggetti o meno, è importante tenere presente che è necessario raggruppare gli elementi dati correlati in modo che sia possibile utilizzarli in modo sicuro in thread diversi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="f8a88-146">Whether you decide to design an object-oriented program or not, the important design consideration to remember is to group the related data elements so that you can use them safely in different threads as necessary.</span></span>  


### <a name="printer-device-context"></a><span data-ttu-id="f8a88-147">Contesto dispositivo stampante</span><span class="sxs-lookup"><span data-stu-id="f8a88-147">Printer Device Context</span></span>

<span data-ttu-id="f8a88-148">Durante la stampa, potrebbe essere necessario eseguire il rendering del contenuto da stampare in un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8a88-148">When printing, you might want to render the content to be printed to a device context.</span></span> <span data-ttu-id="f8a88-149">[Procedura: recuperare un contesto di dispositivo stampante](retrieving-a-printer-device-context.md) descrive i diversi modi in cui è possibile ottenere un contesto di dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="f8a88-149">[How To: Retrieve a Printer Device Context](retrieving-a-printer-device-context.md) describes the different ways that you can obtain a printer device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8a88-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8a88-150">Related topics</span></span>



[<span data-ttu-id="f8a88-151">Come stampare da un'applicazione Windows</span><span class="sxs-lookup"><span data-stu-id="f8a88-151">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)


 

 



