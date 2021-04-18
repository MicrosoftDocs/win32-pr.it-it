---
title: Inizializzazione della libreria COM
description: Inizializzazione della libreria COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299782"
---
# <a name="initializing-the-com-library"></a><span data-ttu-id="6aa9d-103">Inizializzazione della libreria COM</span><span class="sxs-lookup"><span data-stu-id="6aa9d-103">Initializing the COM Library</span></span>

<span data-ttu-id="6aa9d-104">Qualsiasi programma Windows che usa COM deve inizializzare la libreria COM chiamando la funzione [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="6aa9d-104">Any Windows program that uses COM must initialize the COM library by calling the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> <span data-ttu-id="6aa9d-105">Ogni thread che usa un'interfaccia COM deve effettuare una chiamata separata a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-105">Each thread that uses a COM interface must make a separate call to this function.</span></span> <span data-ttu-id="6aa9d-106">**CoInitializeEx** ha la firma seguente:</span><span class="sxs-lookup"><span data-stu-id="6aa9d-106">**CoInitializeEx** has the following signature:</span></span>


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



<span data-ttu-id="6aa9d-107">Il primo parametro è riservato e deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-107">The first parameter is reserved and must be **NULL**.</span></span> <span data-ttu-id="6aa9d-108">Il secondo parametro specifica il modello di threading che il programma utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-108">The second parameter specifies the threading model that your program will use.</span></span> <span data-ttu-id="6aa9d-109">COM supporta due modelli di threading diversi, con *Threading di Apartment* e *multithreading*.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-109">COM supports two different threading models, *apartment threaded* and *multithreaded*.</span></span> <span data-ttu-id="6aa9d-110">Se si specifica il threading dell'Apartment, si apportano le garanzie seguenti:</span><span class="sxs-lookup"><span data-stu-id="6aa9d-110">If you specify apartment threading, you are making the following guarantees:</span></span>

-   <span data-ttu-id="6aa9d-111">Ogni oggetto COM sarà accessibile da un singolo thread. i puntatori di interfaccia COM non vengono condivisi tra più thread.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-111">You will access each COM object from a single thread; you will not share COM interface pointers between multiple threads.</span></span>
-   <span data-ttu-id="6aa9d-112">Il thread avrà un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-112">The thread will have a message loop.</span></span> <span data-ttu-id="6aa9d-113">(Vedere [messaggi della finestra](window-messages.md) nel modulo 1).</span><span class="sxs-lookup"><span data-stu-id="6aa9d-113">(See [Window Messages](window-messages.md) in Module 1.)</span></span>

<span data-ttu-id="6aa9d-114">Se uno di questi vincoli non è true, utilizzare il modello multithread.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-114">If either of these constraints is not true, use the multithreaded model.</span></span> <span data-ttu-id="6aa9d-115">Per specificare il modello di threading, impostare uno dei flag seguenti nel parametro *dwCoInit* .</span><span class="sxs-lookup"><span data-stu-id="6aa9d-115">To specify the threading model, set one of the following flags in the *dwCoInit* parameter.</span></span>



| <span data-ttu-id="6aa9d-116">Flag</span><span class="sxs-lookup"><span data-stu-id="6aa9d-116">Flag</span></span>                          | <span data-ttu-id="6aa9d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6aa9d-117">Description</span></span>         |
|-------------------------------|---------------------|
| <span data-ttu-id="6aa9d-118">**CoInit \_ ApartmentThreaded**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-118">**COINIT\_APARTMENTTHREADED**</span></span> | <span data-ttu-id="6aa9d-119">Threading Apartment.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-119">Apartment threaded.</span></span> |
| <span data-ttu-id="6aa9d-120">**CoInit \_ MULTIthreading**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-120">**COINIT\_MULTITHREADED**</span></span>     | <span data-ttu-id="6aa9d-121">Multithreading.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-121">Multithreaded.</span></span>      |



 

<span data-ttu-id="6aa9d-122">È necessario impostare esattamente uno di questi flag.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-122">You must set exactly one of these flags.</span></span> <span data-ttu-id="6aa9d-123">In genere, un thread che crea una finestra deve usare il flag **CoInit \_ ApartmentThreaded** e gli altri thread usano il **\_ multithreading di CoInit**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-123">Generally, a thread that creates a window should use the **COINIT\_APARTMENTTHREADED** flag, and other threads should use **COINIT\_MULTITHREADED**.</span></span> <span data-ttu-id="6aa9d-124">Tuttavia, alcuni componenti COM richiedono un particolare modello di Threading.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-124">However, some COM components require a particular threading model.</span></span> <span data-ttu-id="6aa9d-125">La documentazione di MSDN dovrebbe indicare quando questo è il caso.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-125">The MSDN documentation should tell you when that is the case.</span></span>

> [!Note]  
> <span data-ttu-id="6aa9d-126">In realtà, anche se si specifica il threading dell'Apartment, è comunque possibile condividere le interfacce tra i thread, usando una tecnica chiamata *marshalling*.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-126">Actually, even if you specify apartment threading, it is still possible to share interfaces between threads, by using a technique called *marshaling*.</span></span> <span data-ttu-id="6aa9d-127">Il marshalling esula dall'ambito di questo modulo.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-127">Marshaling is beyond the scope of this module.</span></span> <span data-ttu-id="6aa9d-128">Il punto importante è che, con il threading dell'Apartment, non è mai sufficiente copiare un puntatore di interfaccia in un altro thread.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-128">The important point is that with apartment threading, you must never simply copy an interface pointer to another thread.</span></span> <span data-ttu-id="6aa9d-129">Per ulteriori informazioni sui modelli di threading COM, vedere [processi, thread e Apartment](/windows/desktop/com/processes--threads--and-apartments).</span><span class="sxs-lookup"><span data-stu-id="6aa9d-129">For more information about the COM threading models, see [Processes, Threads, and Apartments](/windows/desktop/com/processes--threads--and-apartments).</span></span>

 

<span data-ttu-id="6aa9d-130">Oltre ai flag già citati, è consigliabile impostare il flag **CoInit \_ Disable \_ OLE1DDE** nel parametro *dwCoInit* .</span><span class="sxs-lookup"><span data-stu-id="6aa9d-130">In addition to the flags already mentioned, it is a good idea to set the **COINIT\_DISABLE\_OLE1DDE** flag in the *dwCoInit* parameter.</span></span> <span data-ttu-id="6aa9d-131">L'impostazione di questo flag evita un sovraccarico associato a Object Linking and Embedding (OLE) 1,0, una tecnologia obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-131">Setting this flag avoids some overhead associated with Object Linking and Embedding (OLE) 1.0, an obsolete technology.</span></span>

<span data-ttu-id="6aa9d-132">Di seguito viene illustrato come inizializzare COM per il threading di Apartment:</span><span class="sxs-lookup"><span data-stu-id="6aa9d-132">Here is how you would initialize COM for apartment threading:</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



<span data-ttu-id="6aa9d-133">Il tipo restituito **HRESULT** contiene un errore o un codice di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-133">The **HRESULT** return type contains an error or success code.</span></span> <span data-ttu-id="6aa9d-134">Nella sezione successiva verrà esaminata la gestione degli errori COM.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-134">We'll look at COM error handling in the next section.</span></span>

## <a name="uninitializing-the-com-library"></a><span data-ttu-id="6aa9d-135">Annullamento dell'inizializzazione della libreria COM</span><span class="sxs-lookup"><span data-stu-id="6aa9d-135">Uninitializing the COM Library</span></span>

<span data-ttu-id="6aa9d-136">Per ogni chiamata riuscita a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), è necessario chiamare [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) prima che il thread venga chiuso.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-136">For every successful call to [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), you must call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) before the thread exits.</span></span> <span data-ttu-id="6aa9d-137">Questa funzione non accetta parametri e non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-137">This function takes no parameters and has no return value.</span></span>


```C++
CoUninitialize();
```



## <a name="next"></a><span data-ttu-id="6aa9d-138">Prossima</span><span class="sxs-lookup"><span data-stu-id="6aa9d-138">Next</span></span>

[<span data-ttu-id="6aa9d-139">Codici di errore in COM</span><span class="sxs-lookup"><span data-stu-id="6aa9d-139">Error Codes in COM</span></span>](error-codes-in-com.md)

 

 