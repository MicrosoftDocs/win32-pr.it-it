---
title: Sessioni FTP
description: WinINet consente alle applicazioni di esplorare e modificare directory e file in un server ftp. Poiché i proxy CERN non supportano FTP, le applicazioni che usano esclusivamente un proxy CERN devono usare la funzione InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70942fea5865fa96c9ee81ab996238e3f382471a701ac44969d1ff8797c8780d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113976"
---
# <a name="ftp-sessions"></a>Sessioni FTP

WinINet consente alle applicazioni di esplorare e modificare directory e file in un server ftp. Poiché i proxy CERN non supportano FTP, le applicazioni che usano esclusivamente un proxy CERN devono usare la [**funzione InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Per altre informazioni su come usare [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)vedere [Accesso diretto agli URL](handling-uniform-resource-locators.md).

Per avviare una sessione FTP, usare [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per creare l'handle di sessione.

WinINet consente di eseguire le azioni seguenti in un server FTP:

-   Spostarsi tra le directory.
-   Enumerare, creare, rimuovere e rinominare le directory.
-   Rinominare, caricare, scaricare ed eliminare file.

La navigazione viene fornita [**dalle funzioni FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**e FtpSetCurrentDirectory.**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) Queste funzioni utilizzano l'handle di sessione creato da una chiamata precedente a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per determinare la directory in cui si trova attualmente l'applicazione o per passare a una sottodirectory diversa.

L'enumerazione della directory viene eseguita [**tramite le funzioni FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**e InternetFindNextFile.**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) usa l'handle di sessione creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per trovare il primo file che corrisponde ai criteri di ricerca specificati e restituisce un handle per continuare l'enumerazione della directory. [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usa l'handle restituito da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) per restituire il file successivo che corrisponde ai criteri di ricerca originali. L'applicazione deve continuare a chiamare [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) finché non sono rimasti altri file nella directory.

Usare la [**funzione FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) per creare nuove directory. Questa funzione usa l'handle di sessione creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e crea la directory specificata dalla stringa passata alla funzione. La stringa può contenere un nome di directory relativo alla directory corrente o un percorso di directory completo.

Per rinominare file o directory, l'applicazione può chiamare [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea). Questa funzione sostituisce il nome originale con il nuovo nome passato alla funzione. Il nome del file o della directory può essere relativo alla directory corrente o a un nome completo.

Per caricare o inserire file in un server FTP, l'applicazione può usare [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (insieme a [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)). [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) può essere usato se il file esiste già in locale, mentre [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) possono essere usati se i dati devono essere scritti in un file nel server FTP.

Per scaricare o ottenere file, l'applicazione può usare [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (con [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)). [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) viene usato per recuperare un file da un server FTP e archiviarlo in locale, mentre [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) possono essere usati per controllare dove stanno andando le informazioni scaricate (ad esempio, l'applicazione potrebbe visualizzare le informazioni in una casella di modifica).

Eliminare i file in un server FTP usando la [**funzione FtpDeleteFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) Questa funzione rimuove un nome di file relativo alla directory corrente o a un nome file completo dal server FTP. [**FtpDeleteFile richiede**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) un handle di sessione restituito da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

## <a name="ftp-function-handles"></a>Handle di funzione FTP

Per il corretto funzionamento, le funzioni FTP richiedono determinati tipi di [**handle HINTERNET.**](appendix-a-hinternet-handles.md) Questi handle devono essere creati in un ordine specifico, a partire dall'handle radice creato da [**InternetApri**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect può**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) quindi creare un handle di sessione FTP.

Il diagramma seguente illustra le funzioni che dipendono dall'handle di sessione FTP restituito da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Le caselle ombreggiate rappresentano funzioni che restituiscono handle [**HINTERNET,**](appendix-a-hinternet-handles.md) mentre le caselle semplici rappresentano le funzioni che usano l'handle HINTERNET creato dalla funzione da cui dipendono.

![Funzioni ftp dipendenti dall'handle di sessione ftp restituito da internetconnect](images/ax-wnt06.png)

Il diagramma seguente illustra le due funzioni che restituiscono handle [HINTERNET](appendix-a-hinternet-handles.md) e le funzioni che dipendono da essi. Le caselle ombreggiate rappresentano funzioni che restituiscono handle **HINTERNET,** mentre le caselle semplici rappresentano le funzioni che usano l'handle **HINTERNET** creato dalla funzione da cui dipendono.

![Funzioni ftp che restituiscono handle hinternet](images/ax-wnt03.png)

Per altre informazioni, vedere [Handle HINTERNET](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>Uso delle funzioni WinINet per le sessioni FTP

Le funzioni seguenti vengono usate durante le sessioni FTP. Queste funzioni non sono riconosciute dai proxy CERN. Le applicazioni che devono funzionare tramite proxy CERN devono usare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e accedere direttamente alle risorse. Per altre informazioni sull'accesso diretto alle risorse, vedere [Accesso diretto agli URL](handling-uniform-resource-locators.md).



| Funzione                                                 | Descrizione                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | Crea una nuova directory nel server. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                  |
| [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | Elimina un file dal server. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                         |
| [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | Avvia l'enumerazione dei file o la ricerca di file nella directory corrente. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)        |
| [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | Restituisce la directory corrente del client nel server. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                   |
| [**Ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | Recupera un file dal server. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                       |
| [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | Avvia l'accesso a un file nel server per la lettura o la scrittura. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) |
| [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | Scrive un file nel server. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                            |
| [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | Elimina una directory nel server. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                      |
| [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | Rinomina un file nel server. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                           |
| [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | Modifica la directory corrente del client nel server. Questa funzione richiede un handle creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                   |
| [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | Scrive dati in un file aperto nel server. Questa funzione richiede un handle creato da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).                                      |



 

### <a name="starting-an-ftp-session"></a>Avvio di una sessione FTP

L'applicazione stabilisce una sessione FTP chiamando [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) su un handle creato da [**InternetApri**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect richiede**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) il nome del server, il numero di porta, il nome utente, la password e il tipo di servizio (che deve essere impostato su \_ INTERNET SERVICE \_ FTP). Per la semantica FTP passiva, l'applicazione deve impostare anche il flag [ \_ PASSIVO DEL FLAG \_ INTERNET.](api-flags.md)

I valori INTERNET DEFAULT FTP PORT e INTERNET INVALID PORT NUMBER possono \_ essere usati per il numero di \_ \_ \_ \_ \_ porta. INTERNET \_ DEFAULT FTP PORT usa la porta FTP predefinita, ma il tipo di servizio deve comunque essere \_ \_ impostato. INTERNET \_ INVALID PORT NUMBER usa il valore predefinito per il tipo di servizio \_ \_ indicato.

I valori per il nome utente e la password possono essere impostati su **NULL.** Se entrambi i valori sono impostati su **NULL,** [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa "anonymous" per il nome utente e l'indirizzo di posta elettronica dell'utente per la password. Se solo la password è impostata su **NULL,** per il nome utente viene usato il nome utente passato a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e per la password viene usata una stringa vuota. Se nessuno dei due valori **è NULL,** vengono usati il nome utente e la password dati a [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

### <a name="enumerating-directories"></a>Enumerazione delle directory

L'enumerazione di una directory in un server FTP richiede la creazione di un handle [**da parte di FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Questo handle è un ramo dell'handle di sessione creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) individua il primo file o directory nel server e lo restituisce in una struttura [**\_ WIN32 FIND \_ DATA.**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) Usare [**InternetFindNextFile finché**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) non restituisce [**ERROR NO MORE \_ \_ \_ FILES**](wininet-errors.md). Questo metodo trova tutti i file e le directory successivi nel server. Per altre informazioni su [**InternetFindNextFile,**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)vedere [Ricerca del file successivo](common-functions.md).

Per determinare se il file recuperato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) o [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) è una directory, controllare il **membro dwFileAttributes** della struttura [**FIND \_ \_ DATA WIN32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) per verificare se è uguale a FILE \_ ATTRIBUTE \_ DIRECTORY.

Se l'applicazione apporta modifiche al server FTP o se il server FTP cambia di frequente, i flag [INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE](api-flags.md) e [INTERNET FLAG \_ \_ RELOAD](api-flags.md) devono essere impostati in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Questi flag assicurano che le informazioni della directory recuperate dal server FTP siano aggiornate.

Dopo che l'applicazione ha completato l'enumerazione della directory, l'applicazione deve effettuare una chiamata a [**InternetCloseHandle sull'handle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) creato da [**FtpFindFirstFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) Finché tale handle non viene chiuso, l'applicazione non può chiamare [**nuovamente FtpFindFirstFile sull'handle**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) di sessione creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Se viene effettuata una chiamata a [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) sullo stesso handle di sessione prima della chiusura della chiamata precedente alla stessa funzione, la funzione ha esito negativo e restituisce [ERROR FTP TRANSFER IN \_ \_ \_ \_ PROGRESS](wininet-errors.md).

Nell'esempio seguente viene enumerato il contenuto di una directory FTP in un controllo casella di riepilogo. Il *parametro hConnection* è un handle restituito dalla [**funzione InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP. Il codice sorgente di esempio per la funzione InternetErrorOut a cui si fa riferimento in questo esempio è disponibile [nell'argomento Gestione degli](appendix-c-handling-errors.md)errori.


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a>Esplorazione delle directory

Le [**funzioni FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) gestiscono la navigazione nella directory.

[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) restituisce la directory corrente dell'applicazione nel server FTP. È incluso il percorso della directory radice nel server FTP.

[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) modifica la directory di lavoro nel server. Le informazioni sulla directory passate [**a FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) possono essere un nome di percorso parziale o completo relativo alla directory corrente. Ad esempio, se l'applicazione si trova attualmente nella directory "public/info" e il percorso è "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) modifica la directory corrente in "public/info/ftp/example".

Nell'esempio seguente viene utilizzato l'handle di sessione FTP hConnection, restituito da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Il nuovo nome di directory deriva dalla casella di modifica della finestra di dialogo padre il cui IDC viene passato nel *parametro nDirNameId.* Prima di apportare la modifica alla directory, la funzione recupera la directory corrente e la archivia nella stessa casella di modifica. Il codice souce per la funzione DisplayFtpDir chiamata alla fine è elencato in precedenza.


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a>Modifica di directory in un server FTP

WinINet consente di creare e rimuovere directory in un server FTP a cui l'applicazione dispone dei privilegi necessari. Se l'applicazione deve accedere a un server con un nome utente e una password specifici, i valori possono essere usati in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) durante la creazione dell'handle di sessione FTP.

La [**funzione FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) accetta un handle di sessione FTP valido e una stringa con terminazione **Null** che contiene un percorso completo o un nome relativo alla directory corrente e crea una directory nel server FTP.

Nell'esempio seguente vengono illustrate due chiamate separate [**a FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya). In entrambi gli esempi, hFtpSession è l'handle di sessione creato dalla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e la directory radice è la directory corrente.

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

La [**funzione FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) accetta un handle di sessione e una stringa con terminazione **Null** che contiene un percorso completo o un nome relativo alla directory corrente e rimuove tale directory dal server FTP.

Nell'esempio seguente vengono illustrate due chiamate di esempio [**a FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya). In entrambe le chiamate, hFtpSession è l'handle di sessione creato dalla [**funzione InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e la directory radice è la directory corrente. Nella directory radice è presente una directory denominata "test" e una directory denominata "example" nella directory "test".

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



Nell'esempio seguente viene creata una nuova directory nel server FTP. Il nuovo nome di directory deriva dalla casella di modifica della finestra di dialogo padre il cui IDC viene passato nel *parametro nDirNameId.* *L'handle hConnection* è stato creato [**da InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP. Il codice sorgente per la funzione DisplayFtpDir chiamata alla fine è elencato in precedenza.


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



Nell'esempio seguente viene eliminata una directory dal server FTP. Il nome della directory da eliminare viene preso dalla casella di modifica nella finestra di dialogo padre il cui IDC viene passato al *parametro nDirNameId.* *L'handle hConnection* è stato creato [**da InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP. Il codice sorgente per la funzione DisplayFtpDir chiamata alla fine è elencato in precedenza.


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a>Recupero di file in un server FTP

Esistono tre metodi per recuperare i file da un server FTP:

-   Usare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Usare [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Usare [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).

Per altre informazioni sull'uso della [**funzione InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) vedere [Lettura di file.](common-functions.md)

Se l'URL del file è disponibile, l'applicazione può chiamare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) per connettersi a tale URL, quindi usare [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) per controllare il download del file. Ciò consente all'applicazione un controllo più stretto sul download ed è ideale nelle situazioni in cui non è necessario eseguire altre operazioni sul server FTP. Per altre informazioni su come accedere direttamente alle risorse, vedere [Accesso diretto agli URL.](handling-uniform-resource-locators.md)

Se l'applicazione ha stabilito un handle di sessione FTP per il server con [**InternetConnect,**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)l'applicazione può chiamare [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con il nome del file esistente e con un nuovo nome per il file archiviato in locale. L'applicazione può quindi [**usare InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) per scaricare il file. In questo modo l'applicazione ha un controllo più stretto sul download e mantiene la connessione al server FTP, in modo da poter eseguire altri comandi.

Se l'applicazione non richiede un controllo stretto sul download, l'applicazione può usare [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) con l'handle di sessione FTP, il nome del file remoto e il nome del file locale per recuperare il file. [**FtpGetFile esegue**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) tutta la gestione e il sovraccarico associati alla lettura di un file da un server FTP e all'archiviazione locale.

L'esempio seguente recupera un file da un server FTP e lo salva in locale. Il nome del file nel server FTP deriva dalla casella di modifica della finestra di dialogo padre il cui IDC viene passato nel parametro *nFtpFileNameId* e il nome locale in cui viene salvato il file viene prelevato dalla casella di modifica il cui IDC viene passato nel *parametro nLocalFileNameId* . *L'handle hConnection* è stato creato [**da InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a>Inserimento di file in un server FTP

Esistono due metodi per inserire un file in un server FTP:

-   Usare [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).
-   Usare [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).

Un'applicazione che deve inviare dati a un server FTP, ma non dispone di un file locale che contiene tutti i dati, deve utilizzare [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) per creare e aprire un file nel server FTP. L'applicazione può quindi [**usare InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) per caricare le informazioni nel file.

Se il file esiste già in locale, l'applicazione può usare [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) per caricare il file nel server FTP. [**FtpPutFile esegue**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) tutto il sovraccarico associato al caricamento di un file locale in un server FTP remoto.

Nell'esempio seguente viene copiato un file locale nel server FTP. Il nome locale del file viene derivato dalla casella di modifica nella finestra di dialogo padre il cui IDC viene passato nel parametro *nLocalFileNameId* e il nome con cui il file viene salvato nel server FTP deriva dalla casella di modifica il cui IDC viene passato nel *parametro nFtpFileNameId* . *L'handle hConnection* è stato creato [**da InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a>Eliminazione di file da un server FTP

Per eliminare un file da un server FTP, usare la [**funzione FtpDeleteFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) L'applicazione chiamante deve disporre dei privilegi necessari per eliminare un file dal server FTP.

Nell'esempio seguente viene eliminato un file dal server FTP. Il nome del file da eliminare viene preso dalla casella di modifica della finestra di dialogo padre il cui IDC viene passato come int al parametro *nFtpFileNameId.* *L'handle hConnection* è stato creato [**da InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP. Poiché questa funzione non aggiorna gli elenchi di file o la visualizzazione della directory, il processo chiamante deve eseguire questa operazione al completamento dell'eliminazione.


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a>Ridenominazione di file e directory in un server FTP

I file e le directory in un server FTP possono essere rinominati usando la [**funzione FtpRenameFile.**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accetta due **stringhe con** terminazione Null che contengono nomi completi o parzialmente relativi alla directory corrente. La funzione modifica il nome del file designato dalla prima stringa con il nome designato dalla seconda stringa.

Nell'esempio seguente viene rinominato un file o una directory nel server FTP. Il nome corrente del file o della directory deriva dalla casella di modifica nella finestra di dialogo padre il cui IDC viene passato nel parametro *nOldFileNameId* e il nuovo nome viene derivato dalla casella di modifica il cui IDC viene passato nel parametro *nNewFileNameId.* *L'handle hConnection* è stato creato [**da InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP. Poiché questa funzione non aggiorna gli elenchi di file o la visualizzazione della directory, il processo chiamante deve eseguire questa operazione al completamento della ridenominazione.


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows servizi HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 