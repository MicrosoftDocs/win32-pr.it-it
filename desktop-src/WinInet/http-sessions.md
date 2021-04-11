---
title: Sessioni HTTP
description: È possibile accedere alle risorse nel sito Web tramite http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117975"
---
# <a name="http-sessions"></a>Sessioni HTTP

WinINet consente di accedere alle risorse nel World Wide Web (WWW). È possibile accedere a queste risorse direttamente usando [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . per altre informazioni, vedere [accesso diretto agli URL](handling-uniform-resource-locators.md).

È possibile accedere alle risorse nel sito Web tramite http. Le funzioni HTTP gestiscono i protocolli sottostanti, consentendo allo stesso tempo all'applicazione di accedere alle informazioni sul sito Web. Con l'evolversi del protocollo HTTP, i protocolli sottostanti vengono aggiornati per mantenere il comportamento della funzione.

Nel diagramma seguente vengono illustrate le relazioni delle funzioni utilizzate con il protocollo HTTP. Le caselle ombreggiate rappresentano funzioni che restituiscono handle [**HINTERNET**](appendix-a-hinternet-handles.md) , mentre le caselle semplici rappresentano funzioni che usano l'handle **HINTERNET** creato dalla funzione da cui dipendono.

![funzioni WinInet usate per http](images/ax-wnt05.png)

Per altre informazioni, vedere [handle hInternet](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-to-access-the-www"></a>Uso delle funzioni WinINet per accedere al sito Web

-   [Avvio di una connessione a WWW](#initiating-a-connection-to-the-www)
-   [Apertura di una richiesta](#opening-a-request)
-   [Aggiunta di intestazioni di richiesta](#adding-request-headers)
-   [Invio di una richiesta](#sending-a-request)
-   [Invio di dati al server](#posting-data-to-the-server)
-   [Ottenere informazioni su una richiesta](#getting-information-about-a-request)
-   [Download delle risorse dal sito Web](#downloading-resources-from-the-www)

Le funzioni seguenti vengono usate durante le sessioni HTTP per accedere a WWW.



| Funzione                                               | Descrizione                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | Aggiunge intestazioni di richiesta HTTP all'handle della richiesta HTTP. Questa funzione richiede un handle creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                 |
| [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | Apre un handle di richiesta HTTP. Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                                                         |
| [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | Esegue una query sulle informazioni relative a una richiesta HTTP. Questa funzione richiede un handle creato dalla funzione [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | Invia la richiesta HTTP specificata al server HTTP. Questa funzione richiede un handle creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                  |
| [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | Consente di visualizzare le finestre di dialogo predefinite per le condizioni di errore Internet comuni. Questa funzione richiede l'handle usato nella chiamata a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).                     |



 

### <a name="initiating-a-connection-to-the-www"></a>Avvio di una connessione a WWW

Per avviare una connessione a WWW, l'applicazione deve chiamare la funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) sulla [**HINTERNET**](appendix-a-hinternet-handles.md) radice restituita da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve stabilire una sessione HTTP dichiarando il \_ tipo di \_ servizio http del servizio Internet. Per altre informazioni sull'uso di [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), vedere [uso di InternetConnect](enabling-internet-functionality.md).

### <a name="opening-a-request"></a>Apertura di una richiesta

La funzione [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) apre una richiesta HTTP e restituisce un handle [**HINTERNET**](appendix-a-hinternet-handles.md) che può essere usato da altre funzioni http. Diversamente dalle altre funzioni aperte, ad esempio [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) non invia la richiesta a Internet quando viene chiamata. La funzione [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) Invia la richiesta e stabilisce una connessione sulla rete.

[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) accetta un handle di sessione HTTP creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e un verbo HTTP, un nome di oggetto, una stringa di versione, un referrer, i tipi Accept, i flag e il valore di contesto.

Il verbo HTTP è una stringa da utilizzare nella richiesta. I verbi HTTP comuni usati nelle richieste includono GET, PUT e POST. Se questo valore è impostato su **null**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usa il valore predefinito Get.

Il nome dell'oggetto è una stringa che contiene il nome dell'oggetto di destinazione del verbo HTTP specificato. Si tratta in genere di un nome file, un modulo eseguibile o un identificatore di ricerca. Se il nome dell'oggetto specificato è una stringa vuota, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) cerca la pagina predefinita.

La stringa di versione deve contenere la versione HTTP. Se questo parametro è **null**, la funzione userà "" http/1.1 "".

Il referrer specifica l'indirizzo del documento da cui è stato ottenuto il nome dell'oggetto. Se questo parametro è **null**, non viene specificato alcun referrer.

La stringa con terminazione **null** che contiene i tipi Accept indica i tipi di contenuto accettati dall'applicazione. L'impostazione di questo parametro su **null** indica che l'applicazione non accetta tipi di contenuto. Se viene fornita una stringa vuota, l'applicazione indica che accetta solo documenti di tipo "" Text/ \* "". Il valore "" Text/ \* "" indica solo i documenti di testo, non le immagini o altri file binari.

I valori dei flag controllano la memorizzazione nella cache, i cookie e i problemi di sicurezza. Per Microsoft Network (MSN), NTLM e altri tipi di autenticazione, impostare il contrassegno [Internet \_ flag \_ Keep \_ Connection](api-flags.md) .

Se il flag di [ \_ flag \_ asincrono Internet](api-flags.md) è stato impostato nella chiamata a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), è necessario impostare un valore di contesto diverso da zero per un'operazione asincrona corretta.

Nell'esempio seguente viene illustrata una chiamata di esempio a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a>Aggiunta di intestazioni di richiesta

La funzione [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) consente alle applicazioni di aggiungere una o più intestazioni di richiesta alla richiesta iniziale. Questa funzione consente a un'applicazione di aggiungere intestazioni di formato libero aggiuntive all'handle di richiesta HTTP; è progettato per l'uso da parte di applicazioni sofisticate che richiedono un controllo preciso sulla richiesta inviata al server HTTP.

[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) richiede un handle di richiesta HTTP creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), una stringa che contiene le intestazioni, la lunghezza delle intestazioni e i modificatori.

### <a name="sending-a-request"></a>Invio di una richiesta

[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) stabilisce una connessione a Internet e Invia la richiesta al sito specificato. Questa funzione richiede un handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) può anche inviare intestazioni aggiuntive o informazioni facoltative. Le informazioni facoltative vengono in genere usate per le operazioni che scrivono le informazioni sul server, ad esempio PUT e POST.

Dopo che [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) ha inviato la richiesta, l'applicazione può usare le funzioni [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) sull'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) per scaricare le risorse del server.

### <a name="posting-data-to-the-server"></a>Invio di dati al server

Per inserire i dati in un server, il verbo HTTP nella chiamata a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) deve essere post o put. L'indirizzo del buffer che contiene i dati POST deve quindi essere passato al parametro *lpOptional* in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Il parametro *dwOptionalLength* deve essere impostato sulla dimensione dei dati.

È anche possibile usare la funzione [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) per pubblicare dati in un handle [**HINTERNET**](appendix-a-hinternet-handles.md) inviato usando [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).

### <a name="getting-information-about-a-request"></a>Ottenere informazioni su una richiesta

[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) consente a un'applicazione di recuperare informazioni su una richiesta HTTP. La funzione richiede un handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), un valore a livello di informazioni e una lunghezza del buffer. [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) accetta anche un buffer che archivia le informazioni e un indice in base zero dell'intestazione che enumera più intestazioni con lo stesso nome.

### <a name="downloading-resources-from-the-www"></a>Download delle risorse dal sito Web

Dopo l'apertura di una richiesta con [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e l'invio al server con [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), l'applicazione può usare le funzioni [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) per scaricare la risorsa dal server http.

Nell'esempio seguente viene scaricata una risorsa. La funzione accetta l'handle per la finestra corrente, il numero di identificazione di una casella di modifica e un handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e inviato da [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). USA [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) per determinare le dimensioni della risorsa e quindi lo Scarica usando [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Il contenuto viene quindi visualizzato nella casella di modifica.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 