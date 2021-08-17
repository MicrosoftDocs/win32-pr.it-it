---
title: Funzioni comuni (Windows Internet)
description: I diversi protocolli Internet, ad esempio ftp e http, usano diverse funzioni WinINet per gestire le informazioni su Internet.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7b6a68c2633175eca793f48b2180b7212905762ca0f58290436aa17ae9a728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132894"
---
# <a name="common-functions-windows-internet"></a>Funzioni comuni (Windows Internet)

I diversi protocolli Internet, ad esempio ftp e http, usano diverse funzioni WinINet per gestire le informazioni su Internet. Queste funzioni comuni gestiscono le attività in modo coerente, indipendentemente dal protocollo specifico a cui vengono applicate. Le applicazioni possono usare queste funzioni per creare funzioni generiche che gestiscono le attività nei diversi protocolli, ad esempio la lettura di file per ftp e http.

Le funzioni comuni gestiscono le attività seguenti:

-   Download di risorse da Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)e [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).
-   Configurazione di operazioni asincrone ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).
-   Visualizzazione e modifica delle opzioni ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).
-   Chiusura di tutti i tipi di handle [**HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).
-   Inserimento e rimozione di blocchi sulle risorse ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) e [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).

## <a name="using-common-functions"></a>Uso di funzioni comuni

La tabella seguente elenca le funzioni comuni incluse nelle funzioni WinINet. Le funzioni comuni possono essere usate in tipi diversi di [**handle HINTERNET**](appendix-a-hinternet-handles.md) o durante diversi tipi di sessioni.



| Funzione                                                         | Descrizione                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | Continua l'enumerazione o la ricerca di file. Richiede un handle creato dalla [**funzione FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                                                                            |
| [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | Consente all'utente di inserire un blocco sul file in uso. Questa funzione richiede un handle [**restituito dalla funzione FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)o [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) |
| [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | Recupera la quantità di dati disponibili. Richiede un handle creato dalla [**funzione FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)                                                                                    |
| [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | Recupera l'impostazione di un'opzione Internet.                                                                                                                                                                                                            |
| [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | Legge i dati dell'URL. Richiede un handle creato dalla [**funzione InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)                                                                |
| [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | Imposta la posizione per la lettura successiva in un file. Richiede un handle creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo su un URL HTTP) o un handle creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usando il verbo HTTP GET.                 |
| [**Internetsetoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | Imposta un'opzione Internet.                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | Imposta una funzione di callback che riceve informazioni sullo stato. Assegna una funzione di callback all'handle [**HINTERNET**](appendix-a-hinternet-handles.md) designato e a tutti gli handle derivati da esso.                                                      |
| [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | Sblocca un file bloccato usando la [**funzione InternetLockRequestFile.**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)                                                                                                                                           |



 

La lettura dei file, la ricerca del file successivo, la modifica delle opzioni e la configurazione di operazioni asincrone sono comuni alle funzioni che supportano vari protocolli e tipi di handle [**HINTERNET.**](appendix-a-hinternet-handles.md)

### <a name="reading-files"></a>Lettura di file

La [**funzione InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) viene usata per scaricare risorse da un handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituito dalla [**funzione InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)

[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accetta una variabile puntatore void che contiene l'indirizzo di un buffer e un puntatore a una variabile che contiene la lunghezza del buffer. La funzione restituisce i dati nel buffer e la quantità di dati scaricati nel buffer.

Le funzioni WinINet offrono due tecniche per scaricare un'intera risorsa:

-   Funzione [**InternetQueryDataAvailable.**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)
-   Valori restituiti di [**InternetReadFile.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) accetta l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (dopo che [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) è stato chiamato sull'handle) e restituisce il numero di byte disponibili. L'applicazione deve allocare un buffer uguale al numero di byte disponibili, più 1 per il carattere **Null** di terminazione e usare tale buffer con [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Questo metodo non sempre funziona perché [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) controlla le dimensioni del file elencate nell'intestazione e non il file effettivo. Le informazioni nel file di intestazione potrebbero non essere aggiornate o il file di intestazione potrebbe non essere presente, perché non è attualmente richiesto in tutti gli standard.

L'esempio seguente legge il contenuto della risorsa a cui accede l'handle hResource e viene visualizzato nella casella di modifica indicata da intCtrlID.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
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

    // Return.
    return TRUE;
}
```



[**InternetReadFile restituisce**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) zero byte letti e viene completato correttamente dopo la lettura di tutti i dati disponibili. In questo modo un'applicazione può usare [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in un ciclo per scaricare i dati e uscire quando restituisce zero byte letti e viene completato correttamente.

Nell'esempio seguente la risorsa viene letta da Internet e visualizzata nella casella di modifica indicata da intCtrlID. [**L'handle HINTERNET,**](appendix-a-hinternet-handles.md) hInternet, è stato restituito da [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (dopo l'invio da [**HttpSendRequest).**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a>Ricerca del file successivo

La [**funzione InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) viene usata per trovare il file successivo in una ricerca di file, usando i parametri di ricerca e l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)

Per completare una ricerca di file, continuare a chiamare [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usando l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituito da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) finché la funzione non ha esito negativo con il messaggio di errore esteso [ERROR NO MORE \_ \_ \_ FILES](wininet-errors.md). Per ottenere le informazioni sull'errore esteso, chiamare [**la funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Nell'esempio seguente viene visualizzato il contenuto di una directory FTP nella casella di riepilogo indicata da lstDirectory. [**L'handle HINTERNET,**](appendix-a-hinternet-handles.md) hConnect, è un handle restituito dalla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a>Modifica delle opzioni

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) vengono usati per modificare le opzioni di WinINet.

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accetta una variabile che indica l'opzione da impostare, un buffer per contenere l'impostazione dell'opzione e un puntatore che contiene l'indirizzo della variabile che contiene la lunghezza del buffer.

[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accetta una variabile che indica l'opzione da recuperare, un buffer per contenere l'impostazione dell'opzione e un puntatore che contiene l'indirizzo della variabile che contiene la lunghezza del buffer.

### <a name="setting-up-asynchronous-operations"></a>Configurazione di operazioni asincrone

Per impostazione predefinita, le funzioni WinINet funzionano in modo sincrono. Un'applicazione può richiedere un'operazione asincrona impostando il flag [ \_ INTERNET FLAG \_ ASYNC](api-flags.md) nella chiamata alla [**funzione InternetOpen.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) Tutte le chiamate future effettuate su handle derivati dall'handle restituito da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) vengono effettuate in modo asincrono.

La logica per le operazioni asincrone e sincrone è consentire a un'applicazione a thread singolo di ottimizzare l'utilizzo della CPU senza dover attendere il completamento dell'I/O di rete. Pertanto, a seconda della richiesta, l'operazione potrebbe essere completata in modo sincrono o asincrono. L'applicazione deve controllare il codice restituito. Se una funzione restituisce **FALSE** o **NULL** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR IO PENDING, la richiesta è stata effettuata in modo asincrono e l'applicazione viene richiamata con INTERNET STATUS REQUEST COMPLETE al termine della \_ \_ \_ \_ \_ funzione.

Per avviare l'operazione asincrona, l'applicazione deve impostare il flag [ \_ INTERNET FLAG \_ ASYNC](api-flags.md) nella chiamata a [**InternetApri**](/windows/desktop/api/Wininet/nf-wininet-internetopena). L'applicazione deve quindi registrare una funzione di callback valida, [**usando InternetSetStatusCallback.**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Dopo la registrazione di una funzione di callback per un handle, tutte le operazioni su tale handle possono generare indicazioni di stato, a condizione che il valore di contesto fornito al momento della creazione dell'handle sia diverso da zero. Se si specifica un valore di contesto zero, un'operazione viene completata in modo sincrono, anche se è stato specificato [INTERNET \_ FLAG \_ ASYNC](api-flags.md) in [**InternetApri**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

Le indicazioni sullo stato forniscono all'applicazione commenti e suggerimenti sullo stato delle operazioni di rete, ad esempio la risoluzione di un nome host, la connessione a un server e la ricezione di dati. È possibile creare tre indicazioni di stato per scopi speciali per un handle:

-   INTERNET \_ STATUS HANDLE CLOSING è \_ \_ l'ultima indicazione di stato effettuata per un handle.
-   INTERNET \_ STATUS HANDLE CREATED indica quando \_ \_ l'handle viene creato inizialmente.
-   INTERNET \_ STATUS REQUEST COMPLETE indica che \_ \_ un'operazione asincrona è stata completata.

L'applicazione deve controllare la [**struttura \_ INTERNET ASYNC \_ RESULT**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) per determinare se l'operazione ha avuto esito positivo o negativo dopo aver ricevuto un'indicazione INTERNET \_ STATUS REQUEST \_ \_ COMPLETE.

L'esempio seguente illustra un esempio di funzione di callback e una chiamata a [**InternetSetStatusCallback per**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) registrare la funzione come funzione di callback.


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a>Chiusura di handle HINTERNET

Tutti gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) possono essere chiusi tramite la [**funzione InternetCloseHandle.**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) Le applicazioni client devono chiudere tutti gli handle **HINTERNET** derivati dall'handle **HINTERNET** che tentano di chiudere prima di chiamare [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) sull'handle.

Nell'esempio seguente viene illustrata la gerarchia degli handle.


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a>Blocco e sblocco delle risorse

La [**funzione InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) consente a un'applicazione di assicurarsi che la risorsa memorizzata nella cache associata all'handle [**HINTERNET**](appendix-a-hinternet-handles.md) passato non scompaia dalla cache. Se un altro download tenta di eseguire il commit di una risorsa con lo stesso URL del file bloccato, la cache evita di rimuovere il file eseguendo un'eliminazione sicura. Dopo che l'applicazione [**ha chiamato la funzione InternetUnlockRequestFile,**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) alla cache viene concessa l'autorizzazione per eliminare il file.

Se è stato impostato il flag [INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE](api-flags.md) o [INTERNET FLAG \_ \_ DONT \_ CACHE,](api-flags.md) [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) crea un file temporaneo con estensione TMP, a meno che l'handle non sia connesso a una risorsa https. Se la funzione accede a una risorsa https ed è stato impostato IL FLAG INTERNET \_ \_ NO CACHE WRITE \_ \_ (o INTERNET FLAG \_ \_ DONT \_ CACHE), [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) ha esito negativo.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
