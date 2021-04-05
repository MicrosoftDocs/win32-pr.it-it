---
title: Sviluppo di interfacce con handle di contesto
description: In genere, si crea un handle di contesto specificando l' \_ attributo \ context handle \ in una definizione di tipo nel file IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729311"
---
# <a name="interface-development-using-context-handles"></a><span data-ttu-id="9afb2-103">Sviluppo di interfacce con handle di contesto</span><span class="sxs-lookup"><span data-stu-id="9afb2-103">Interface Development Using Context Handles</span></span>

<span data-ttu-id="9afb2-104">In genere, si crea un handle di contesto specificando l'attributo dell' \[ [**\_ handle di contesto**](/windows/desktop/Midl/context-handle) in \] una definizione di tipo nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="9afb2-104">Typically, you create a context handle by specifying the \[[**context\_handle**](/windows/desktop/Midl/context-handle)\] attribute on a type definition in the IDL file.</span></span> <span data-ttu-id="9afb2-105">La definizione del tipo specifica anche in modo implicito una routine di esecuzione del contesto, che è necessario fornire.</span><span class="sxs-lookup"><span data-stu-id="9afb2-105">The type definition also implicitly specifies a context run-down routine, which you must provide.</span></span> <span data-ttu-id="9afb2-106">Se la comunicazione tra il client e il server si interrompe, il tempo di esecuzione del server richiama questa routine per eseguire tutte le operazioni di pulizia necessarie.</span><span class="sxs-lookup"><span data-stu-id="9afb2-106">If communication between the client and server breaks down, the server run time invokes this routine to perform any needed cleanup.</span></span> <span data-ttu-id="9afb2-107">Per ulteriori informazioni sulle routine di esecuzione del contesto, vedere [routine di esecuzione del contesto del server](server-context-run-down-routine.md).</span><span class="sxs-lookup"><span data-stu-id="9afb2-107">For more information on context run-down routines, see [Server Context Run-down Routine](server-context-run-down-routine.md).</span></span>

<span data-ttu-id="9afb2-108">Un'interfaccia che utilizza un handle di contesto deve disporre di un handle di associazione per l'associazione iniziale, che deve essere eseguita prima che il server possa restituire un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="9afb2-108">An interface that uses a context handle must have a binding handle for the initial binding, which has to take place before the server can return a context handle.</span></span> <span data-ttu-id="9afb2-109">È possibile utilizzare un handle di binding automatico, implicito o esplicito per creare l'associazione e stabilire il contesto.</span><span class="sxs-lookup"><span data-stu-id="9afb2-109">You can use an automatic, implicit, or explicit binding handle to create the binding and establish the context.</span></span>

<span data-ttu-id="9afb2-110">Un handle di contesto deve essere del [**tipo \* void**](/windows/desktop/Midl/void) o un tipo che viene risolto in [**void \***](/windows/desktop/Midl/void).</span><span class="sxs-lookup"><span data-stu-id="9afb2-110">A context handle must be of the [**void \***](/windows/desktop/Midl/void) type, or a type that resolves to [**void \***](/windows/desktop/Midl/void).</span></span> <span data-ttu-id="9afb2-111">Il programma server ne esegue il cast al tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="9afb2-111">The server program casts it to the required type.</span></span>

> [!Note]  
> <span data-ttu-id="9afb2-112">L'uso di \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] per i parametri di handle di contesto è sconsigliato, ad eccezione delle routine che chiudono gli handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="9afb2-112">The use of \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] for context handle parameters is discouraged except for routines that close context handles.</span></span> <span data-ttu-id="9afb2-113">Se il contesto gestisce i parametri contrassegnati \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] vengono utilizzati, non passare un handle di contesto **null** o non inizializzato dal client al server.</span><span class="sxs-lookup"><span data-stu-id="9afb2-113">If context handles parameters marked \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] are used, do not pass a **NULL** or uninitialized context handle from the client to the server.</span></span> <span data-ttu-id="9afb2-114">È necessario passare invece un puntatore **null** a un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="9afb2-114">A **NULL** pointer to a context handle should be passed instead.</span></span> <span data-ttu-id="9afb2-115">Si noti che i parametri di handle \[ [**di**](/windows/desktop/Midl/in) contesto contrassegnati in non \] accettano puntatori **null** .</span><span class="sxs-lookup"><span data-stu-id="9afb2-115">Please note, context handle parameters marked \[[**in**](/windows/desktop/Midl/in)\] do not accept **NULL** pointers.</span></span>

 

<span data-ttu-id="9afb2-116">Il frammento di una definizione di interfaccia di esempio seguente mostra come un'applicazione distribuita può utilizzare un handle di contesto per aprire un server e aggiornare un file di dati per ogni client.</span><span class="sxs-lookup"><span data-stu-id="9afb2-116">The following fragment of a sample interface definition shows how a distributed application can use a context handle to have a server open and update a data file for each client.</span></span>

<span data-ttu-id="9afb2-117">L'interfaccia deve contenere una chiamata di procedura remota per inizializzare l'handle e impostarlo su un valore non **null** .</span><span class="sxs-lookup"><span data-stu-id="9afb2-117">The interface must contain a remote procedure call to initialize the handle and set it to a non-**null** value.</span></span> <span data-ttu-id="9afb2-118">In questo esempio, la funzione RemoteOpen esegue questa operazione.</span><span class="sxs-lookup"><span data-stu-id="9afb2-118">In this example, the RemoteOpen function performs this operation.</span></span> <span data-ttu-id="9afb2-119">Specifica l'handle di contesto con un \[ attributo [**out**](/windows/desktop/Midl/out-idl) \] Directional.</span><span class="sxs-lookup"><span data-stu-id="9afb2-119">It specifies the context handle with an \[[**out**](/windows/desktop/Midl/out-idl)\] directional attribute.</span></span> <span data-ttu-id="9afb2-120">In alternativa, è possibile restituire l'handle di contesto come valore restituito della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="9afb2-120">Alternatively, you could return the context handle as the procedure's return value.</span></span> <span data-ttu-id="9afb2-121">Tuttavia, in questo esempio, l'handle del contesto verrà passato tramite l'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="9afb2-121">However in this example, we'll pass the context handle out through the parameter list.</span></span>

<span data-ttu-id="9afb2-122">In questo esempio, le informazioni sul contesto sono un handle di file.</span><span class="sxs-lookup"><span data-stu-id="9afb2-122">In this example, the context information is a file handle.</span></span> <span data-ttu-id="9afb2-123">Tiene traccia della posizione corrente nel file.</span><span class="sxs-lookup"><span data-stu-id="9afb2-123">It keeps track of the current location in the file.</span></span> <span data-ttu-id="9afb2-124">L'interfaccia esegue il pacchetto dell'handle di file come handle di contesto e lo passa come parametro alle chiamate di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="9afb2-124">The interface packages the file handle as a context handle and passes it as a parameter to remote procedure calls.</span></span> <span data-ttu-id="9afb2-125">Una struttura contiene il nome file e l'handle di file.</span><span class="sxs-lookup"><span data-stu-id="9afb2-125">A structure contains the file name and the file handle.</span></span>

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

<span data-ttu-id="9afb2-126">La funzione RemoteOpen crea un handle di contesto non **null** valido.</span><span class="sxs-lookup"><span data-stu-id="9afb2-126">The RemoteOpen function creates a valid, non-**null** context handle.</span></span> <span data-ttu-id="9afb2-127">Passa l'handle di contesto al client.</span><span class="sxs-lookup"><span data-stu-id="9afb2-127">It passes the context handle to the client.</span></span> <span data-ttu-id="9afb2-128">Per le successive chiamate di procedure remote, ad esempio RemoteRead, viene utilizzato l'handle di contesto come puntatore in.</span><span class="sxs-lookup"><span data-stu-id="9afb2-128">Subsequent remote procedure calls, such as RemoteRead, use the context handle as an in pointer.</span></span>

<span data-ttu-id="9afb2-129">Oltre alla procedura remota che Inizializza l'handle del contesto, l'interfaccia deve contenere una procedura che libera il contesto del server e imposta l'handle del contesto su **null**.</span><span class="sxs-lookup"><span data-stu-id="9afb2-129">In addition to the remote procedure that initializes the context handle, the interface must contain a procedure that frees the server context and sets context handle to **NULL**.</span></span> <span data-ttu-id="9afb2-130">Nell'esempio precedente, la funzione RemoteClose esegue questa operazione.</span><span class="sxs-lookup"><span data-stu-id="9afb2-130">In the preceding example, the RemoteClose function performs this operation.</span></span>

 

 