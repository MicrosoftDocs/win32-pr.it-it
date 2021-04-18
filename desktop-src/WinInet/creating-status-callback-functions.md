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
# <a name="creating-status-callback-functions"></a>Creazione di funzioni di callback di stato

In questa esercitazione viene descritto come creare una funzione di callback di stato utilizzata per monitorare lo stato di una richiesta Internet.

Le funzioni di callback di stato ricevono callback di stato in qualsiasi richiesta Internet originata da qualsiasi funzione WinINet a cui è stato passato un valore di contesto diverso da zero.


I passaggi seguenti sono necessari per la creazione di una funzione di callback dello stato:

1.  [Definire il valore di contesto.](#defining-the-context-value)
2.  [Creare la funzione di callback dello stato.](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a>Definizione del valore di contesto

Il valore di contesto può essere qualsiasi valore unsigned long integer. Idealmente, il valore del contesto dovrebbe identificare la richiesta appena completata e la posizione di tutte le risorse associate, se necessario.

Uno dei modi più utili per usare il valore di contesto è passare l'indirizzo di una struttura ed eseguirne il cast a **un \_ ptr DWORD**. La struttura può essere usata per archiviare le informazioni sulla richiesta, in modo che vengano passate alla funzione di callback dello stato.

La struttura seguente è un esempio di un possibile valore di contesto. I membri della struttura vengono scelti tenendo presente la funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



In questo esempio, la funzione di callback dello stato può accedere all'handle della finestra, in modo da consentire la visualizzazione di un'interfaccia utente. L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) può essere passato a un'altra funzione che può scaricare la risorsa e una matrice di caratteri che possono essere usati per passare informazioni sulla richiesta.

I membri della struttura possono essere modificati in base alle esigenze di una particolare applicazione, quindi non si ritiene vincolati da questo esempio.

### <a name="creating-the-status-callback-function"></a>Creazione della funzione di callback dello stato

La funzione di callback dello stato deve seguire il formato di [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback). Per eseguire questa operazione:

1.  Scrivere una dichiarazione di funzione per la funzione di callback dello stato.

    Nell'esempio seguente viene illustrata una dichiarazione di esempio.

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  Determinare la funzione di callback dello stato. Per le applicazioni che eseguono chiamate asincrone, la funzione di callback dello stato deve gestire il \_ valore di completamento della richiesta di stato Internet \_ \_ , che indica che una richiesta asincrona è stata completata. La funzione di callback dello stato può essere usata anche per tenere traccia dello stato di una richiesta Internet.

    In generale, è consigliabile usare un'istruzione switch con *dwInternetStatus* come valore di opzione e i valori di stato per le istruzioni case. A seconda dei tipi di funzioni che l'applicazione chiama, è possibile ignorare alcuni valori di stato. Per una definizione dei diversi valori di stato, vedere l'elenco nel parametro *dwInternetStatus* di [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).

    L'istruzione switch seguente è un esempio di come gestire i callback di stato.

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

3.  Creare il codice per gestire i valori di stato.

    Il codice per gestire ognuno dei valori di stato dipende in larga misura dall'uso previsto della funzione di callback dello stato. Per le applicazioni che si limitano a tenere traccia dello stato di avanzamento di una richiesta, è possibile che la scrittura di una stringa in una casella di riepilogo sia sufficiente. Per le operazioni asincrone, il codice deve gestire alcuni dati restituiti nel callback.

    La funzione di callback di stato seguente usa una funzione switch per determinare il valore di stato e crea una stringa che include il nome del valore di stato e la funzione precedente chiamata, che viene archiviata nel membro szMemo della struttura del contesto della richiesta \_ .

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

    

4.  Utilizzare la funzione [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) per impostare la funzione di callback dello stato sull'handle [**HINTERNET**](appendix-a-hinternet-handles.md) per il quale si desidera ricevere i callback di stato.

    Nell'esempio seguente viene illustrato come impostare una funzione di callback dello stato.

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
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di funzioni di callback di stato](creating-status-callback-functions.md)
</dt> <dt>

[**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 