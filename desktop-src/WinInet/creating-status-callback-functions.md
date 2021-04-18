---
title: Creazione di funzioni di callback di stato
description: In questa esercitazione viene descritto come creare una funzione di callback di stato utilizzata per monitorare lo stato di una richiesta Internet.
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300698"
---
# <a name="creating-status-callback-functions"></a><span data-ttu-id="c3469-103">Creazione di funzioni di callback di stato</span><span class="sxs-lookup"><span data-stu-id="c3469-103">Creating Status Callback Functions</span></span>

<span data-ttu-id="c3469-104">In questa esercitazione viene descritto come creare una funzione di callback di stato utilizzata per monitorare lo stato di una richiesta Internet.</span><span class="sxs-lookup"><span data-stu-id="c3469-104">This tutorial describes how to create a status callback function used to monitor the status of an Internet request.</span></span>

<span data-ttu-id="c3469-105">Le funzioni di callback di stato ricevono callback di stato in qualsiasi richiesta Internet originata da qualsiasi funzione WinINet a cui è stato passato un valore di contesto diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c3469-105">Status callback functions receive status callbacks on any Internet requests that originated from any WinINet function that was passed a nonzero context value.</span></span>


<span data-ttu-id="c3469-106">I passaggi seguenti sono necessari per la creazione di una funzione di callback dello stato:</span><span class="sxs-lookup"><span data-stu-id="c3469-106">The following steps are necessary for creating a status callback function:</span></span>

1.  [<span data-ttu-id="c3469-107">Definire il valore di contesto.</span><span class="sxs-lookup"><span data-stu-id="c3469-107">Define the context value.</span></span>](#defining-the-context-value)
2.  [<span data-ttu-id="c3469-108">Creare la funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-108">Create the status callback function.</span></span>](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a><span data-ttu-id="c3469-109">Definizione del valore di contesto</span><span class="sxs-lookup"><span data-stu-id="c3469-109">Defining the Context Value</span></span>

<span data-ttu-id="c3469-110">Il valore di contesto può essere qualsiasi valore unsigned long integer.</span><span class="sxs-lookup"><span data-stu-id="c3469-110">The context value can be any unsigned long integer value.</span></span> <span data-ttu-id="c3469-111">Idealmente, il valore del contesto dovrebbe identificare la richiesta appena completata e la posizione di tutte le risorse associate, se necessario.</span><span class="sxs-lookup"><span data-stu-id="c3469-111">Ideally, the context value should identify what request has just been completed and the location of any associated resources, if needed.</span></span>

<span data-ttu-id="c3469-112">Uno dei modi più utili per usare il valore di contesto è passare l'indirizzo di una struttura ed eseguirne il cast a **un \_ ptr DWORD**.</span><span class="sxs-lookup"><span data-stu-id="c3469-112">One of the most useful ways to use the context value is to pass the address of a structure and cast it to a **DWORD\_PTR**.</span></span> <span data-ttu-id="c3469-113">La struttura può essere usata per archiviare le informazioni sulla richiesta, in modo che vengano passate alla funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-113">The structure can be used to store information about the request, so that it is passed to the status callback function.</span></span>

<span data-ttu-id="c3469-114">La struttura seguente è un esempio di un possibile valore di contesto.</span><span class="sxs-lookup"><span data-stu-id="c3469-114">The following structure is an example of a possible context value.</span></span> <span data-ttu-id="c3469-115">I membri della struttura vengono scelti tenendo presente la funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="c3469-115">The members of the structure are chosen with the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function in mind.</span></span>


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



<span data-ttu-id="c3469-116">In questo esempio, la funzione di callback dello stato può accedere all'handle della finestra, in modo da consentire la visualizzazione di un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c3469-116">In this example, the status callback function would have access to the window handle, which would allow it to display a user interface.</span></span> <span data-ttu-id="c3469-117">L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) può essere passato a un'altra funzione che può scaricare la risorsa e una matrice di caratteri che possono essere usati per passare informazioni sulla richiesta.</span><span class="sxs-lookup"><span data-stu-id="c3469-117">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) could be passed to another function that can download the resource and an array of characters that can be used to pass information about the request.</span></span>

<span data-ttu-id="c3469-118">I membri della struttura possono essere modificati in base alle esigenze di una particolare applicazione, quindi non si ritiene vincolati da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="c3469-118">The members of the structure can be changed to fit the needs of a particular application, so do not feel constrained by this example.</span></span>

### <a name="creating-the-status-callback-function"></a><span data-ttu-id="c3469-119">Creazione della funzione di callback dello stato</span><span class="sxs-lookup"><span data-stu-id="c3469-119">Creating the Status Callback Function</span></span>

<span data-ttu-id="c3469-120">La funzione di callback dello stato deve seguire il formato di [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span><span class="sxs-lookup"><span data-stu-id="c3469-120">The status callback function must follow the format of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span> <span data-ttu-id="c3469-121">Per eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="c3469-121">To do this:</span></span>

1.  <span data-ttu-id="c3469-122">Scrivere una dichiarazione di funzione per la funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-122">Write a function declaration for your status callback function.</span></span>

    <span data-ttu-id="c3469-123">Nell'esempio seguente viene illustrata una dichiarazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="c3469-123">The following example shows a sample declaration.</span></span>

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  <span data-ttu-id="c3469-124">Determinare la funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-124">Determine what your status callback function will do.</span></span> <span data-ttu-id="c3469-125">Per le applicazioni che eseguono chiamate asincrone, la funzione di callback dello stato deve gestire il \_ valore di completamento della richiesta di stato Internet \_ \_ , che indica che una richiesta asincrona è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c3469-125">For applications that are making asynchronous calls, the status callback function must handle the INTERNET\_STATUS\_REQUEST\_COMPLETE value, which indicates an asynchronous request is complete.</span></span> <span data-ttu-id="c3469-126">La funzione di callback dello stato può essere usata anche per tenere traccia dello stato di una richiesta Internet.</span><span class="sxs-lookup"><span data-stu-id="c3469-126">The status callback function can also be used to track the progress of an Internet request.</span></span>

    <span data-ttu-id="c3469-127">In generale, è consigliabile usare un'istruzione switch con *dwInternetStatus* come valore di opzione e i valori di stato per le istruzioni case.</span><span class="sxs-lookup"><span data-stu-id="c3469-127">In general, it works best to use a switch statement with *dwInternetStatus* as the switch value and the status values for the case statements.</span></span> <span data-ttu-id="c3469-128">A seconda dei tipi di funzioni che l'applicazione chiama, è possibile ignorare alcuni valori di stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-128">Depending on the types of functions your application is calling, you can ignore some of the status values.</span></span> <span data-ttu-id="c3469-129">Per una definizione dei diversi valori di stato, vedere l'elenco nel parametro *dwInternetStatus* di [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span><span class="sxs-lookup"><span data-stu-id="c3469-129">For a definition of the different status values, see the listing under the *dwInternetStatus* parameter of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span>

    <span data-ttu-id="c3469-130">L'istruzione switch seguente è un esempio di come gestire i callback di stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-130">The following switch statement is an example of how to handle status callbacks.</span></span>

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  <span data-ttu-id="c3469-131">Creare il codice per gestire i valori di stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-131">Create the code to handle the status values.</span></span>

    <span data-ttu-id="c3469-132">Il codice per gestire ognuno dei valori di stato dipende in larga misura dall'uso previsto della funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-132">The code to handle each of the status values depends heavily on your intended use of the status callback function.</span></span> <span data-ttu-id="c3469-133">Per le applicazioni che si limitano a tenere traccia dello stato di avanzamento di una richiesta, è possibile che la scrittura di una stringa in una casella di riepilogo sia sufficiente.</span><span class="sxs-lookup"><span data-stu-id="c3469-133">For applications that are just tracking the progress of a request, writing a string to a list box might be all you need.</span></span> <span data-ttu-id="c3469-134">Per le operazioni asincrone, il codice deve gestire alcuni dati restituiti nel callback.</span><span class="sxs-lookup"><span data-stu-id="c3469-134">For asynchronous operations, the code must handle some of the data returned in the callback.</span></span>

    <span data-ttu-id="c3469-135">La funzione di callback di stato seguente usa una funzione switch per determinare il valore di stato e crea una stringa che include il nome del valore di stato e la funzione precedente chiamata, che viene archiviata nel membro szMemo della struttura del contesto della richiesta \_ .</span><span class="sxs-lookup"><span data-stu-id="c3469-135">The following status callback function uses a switch function to determine what the status value is and creates a string that includes the name of the status value and the previous function called, which is stored in the szMemo member of the REQUEST\_CONTEXT structure.</span></span>

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  <span data-ttu-id="c3469-136">Utilizzare la funzione [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) per impostare la funzione di callback dello stato sull'handle [**HINTERNET**](appendix-a-hinternet-handles.md) per il quale si desidera ricevere i callback di stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-136">Use the [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) function to set the status callback function on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle for which you want to receive status callbacks.</span></span>

    <span data-ttu-id="c3469-137">Nell'esempio seguente viene illustrato come impostare una funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="c3469-137">The following example demonstrates how to set a status callback function.</span></span>

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> <span data-ttu-id="c3469-138">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="c3469-138">WinINet does not support server implementations.</span></span> <span data-ttu-id="c3469-139">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="c3469-139">In addition, it should not be used from a service.</span></span> <span data-ttu-id="c3469-140">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="c3469-140">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c3469-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3469-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3469-142">Creazione di funzioni di callback di stato</span><span class="sxs-lookup"><span data-stu-id="c3469-142">Creating Status Callback Functions</span></span>](creating-status-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="c3469-143">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="c3469-143">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[<span data-ttu-id="c3469-144">*InternetStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="c3469-144">*InternetStatusCallback*</span></span>](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 