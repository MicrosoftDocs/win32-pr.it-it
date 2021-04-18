---
description: Di seguito sono riportati alcuni suggerimenti e suggerimenti da tenere in considerazione durante la scrittura di un'applicazione per TAPI 3
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Suggerimenti e suggerimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321172"
---
# <a name="hints-and-tips"></a><span data-ttu-id="51bee-103">Suggerimenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="51bee-103">Hints and Tips</span></span>

<span data-ttu-id="51bee-104">Di seguito sono riportati alcuni suggerimenti e suggerimenti da tenere in considerazione durante la scrittura di un'applicazione per TAPI 3:</span><span class="sxs-lookup"><span data-stu-id="51bee-104">The following are hints and tips to consider when writing an application for TAPI 3:</span></span>

1.  <span data-ttu-id="51bee-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) crea indirettamente Windows; Questa operazione è particolarmente importante per il threading dell'Apartment.</span><span class="sxs-lookup"><span data-stu-id="51bee-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) indirectly creates windows; this is especially important for apartment threading.</span></span> <span data-ttu-id="51bee-106">Se un thread crea qualsiasi finestra, deve elaborare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="51bee-106">If a thread creates any windows, it must process messages.</span></span> <span data-ttu-id="51bee-107">Se i thread chiamano **CoInitialize**, eseguire un message pump per evitare problemi.</span><span class="sxs-lookup"><span data-stu-id="51bee-107">If your threads call **CoInitialize**, run a message pump to prevent problems.</span></span> <span data-ttu-id="51bee-108">Ad esempio, COM potrebbe interrompere correttamente il marshalling oppure i metodi su interfacce COM, ad esempio **IGlobalInterfaceTable** , potrebbero bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="51bee-108">For example, COM might stop marshalling properly, or methods on COM interfaces, such as **IGlobalInterfaceTable** might hang.</span></span>

    <span data-ttu-id="51bee-109">Nel threading dell'Apartment è necessario disporre di un message pump indipendentemente dal fatto che si attendano gli oggetti di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="51bee-109">In apartment threading you must have a message pump regardless of whether you wait for synchronization objects.</span></span> <span data-ttu-id="51bee-110">Questa operazione è particolarmente importante se si dispone di un'applicazione console o si scrive un oggetto server locale/remoto COM con threading Apartment (in cui non è presente una console o un'interfaccia utente grafica, ma il controllo viene semplicemente "eseguito" nel sistema).</span><span class="sxs-lookup"><span data-stu-id="51bee-110">This is particularly important if you have a console application or you write a COM local/remote server object that is apartment threaded (where you do not have a console or a GUI, but the control just "runs" in the system).</span></span>

    > [!Caution]  
    > <span data-ttu-id="51bee-111">Quando si chiamano le funzioni di attesa e di sincronizzazione, ad esempio [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)e così via.</span><span class="sxs-lookup"><span data-stu-id="51bee-111">When calling the wait and synchronization functions, such as [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), and so on.</span></span> <span data-ttu-id="51bee-112">Usare invece [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ed elaborare i messaggi oppure usare [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), che rileverà automaticamente il tipo di Apartment in cui si trova il thread (sta o MTA) e aspetterà in un ciclo com (If sta) o in un blocco su **WaitForMultipleObjects** (se MTA).</span><span class="sxs-lookup"><span data-stu-id="51bee-112">Instead, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) and process the messages, or use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), which will automatically detect what type of apartment the thread is in (STA or MTA) and will wait either in a COM modal loop (if STA) or block on **WaitForMultipleObjects** (if MTA).</span></span> <span data-ttu-id="51bee-113">**MsgWaitForMultipleObjects** e **CoWaitForMultipleHandles** elaborano anche i messaggi di Windows in base alle regole com.</span><span class="sxs-lookup"><span data-stu-id="51bee-113">**MsgWaitForMultipleObjects** and **CoWaitForMultipleHandles** also process windows messages according to the COM rules.</span></span>

     

    <span data-ttu-id="51bee-114">Ad esempio, anziché:</span><span class="sxs-lookup"><span data-stu-id="51bee-114">For example, instead of:</span></span>

    `Sleep (5000);`

    <span data-ttu-id="51bee-115">Usare:</span><span class="sxs-lookup"><span data-stu-id="51bee-115">Use:</span></span>

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  <span data-ttu-id="51bee-116">**ITTAPIEventNotification:: Event** è la funzione di evento Apps chiamata in un thread di callback di TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="51bee-116">**ITTAPIEventNotification::Event** is the apps Event function called on a TAPI 3 callback thread.</span></span>

    <span data-ttu-id="51bee-117">Eseguire il minimo nella routine di evento; usare invece il proprio thread laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="51bee-117">Do the minimum in the Event routine; instead, use your own thread where possible.</span></span>

    <span data-ttu-id="51bee-118">Tenere presente che viene fornito l'esempio di codice seguente, ma non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="51bee-118">Be aware that the following code example is provided, but is not a requirement.</span></span>

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  <span data-ttu-id="51bee-119">Non modificare gli oggetti COM dopo aver chiamato [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="51bee-119">Do not manipulate COM objects after calling [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span></span> <span data-ttu-id="51bee-120">I risultati sono imprevedibili e dannosi a un'applicazione integra.</span><span class="sxs-lookup"><span data-stu-id="51bee-120">The results are unpredictable and detrimental to a healthy application.</span></span> <span data-ttu-id="51bee-121">Alcuni esempi in cui questo può verificarsi sono i thread di lavoro e i distruttori C++ che possono essere eseguiti dopo che un'applicazione chiama **CoUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="51bee-121">Some examples in which this can happen are worker threads and C++ destructors that may execute after an application calls **CoUninitialize**.</span></span>

 

 
