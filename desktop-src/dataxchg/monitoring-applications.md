---
title: Monitoraggio di applicazioni
description: In questo argomento viene illustrato come utilizzare gli elementi di Dynamic Data Exchange Management Library per creare un'applicazione che monitora l'attività di scambio dinamico dei dati nel sistema.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Windows Interfaccia utente,Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), monitoraggio delle applicazioni
- DDE (Dynamic Data Exchange),monitoraggio delle applicazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Windows Interfaccia utente,Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange Management Library (DDEML), monitoraggio delle applicazioni
- DDEML (Dynamic Data Exchange Management Library), monitoraggio delle applicazioni
- scambio di dati, Dynamic Data Exchange Management Library (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbf6db1faa765378ea2b22b1146de770e9c94b14cf7e9e511ab862be48369c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128553"
---
# <a name="monitoring-applications"></a>Monitoraggio di applicazioni

Gli elementi API di Dynamic Data Exchange Management Library (DDEML) possono essere usati per creare un'applicazione che monitora l'attività di Dynamic Data Exchange (DDE) nel sistema. Come qualsiasi applicazione DDEML, un'applicazione di monitoraggio DDE contiene una funzione di callback DDE. DDEML invia una notifica alla funzione di callback DDE di un'applicazione di monitoraggio ogni volta che si verifica un evento DDE, passando informazioni sull'evento alla funzione di callback. L'applicazione visualizza in genere le informazioni in una finestra o le scrive in un file.

Per ricevere notifiche da DDEML, un'applicazione deve essere registrata come monitoraggio DDE specificando il flag APPCLASS MONITOR in una chiamata alla \_ [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) In questa stessa chiamata, l'applicazione può specificare uno o più flag di monitoraggio per indicare i tipi di eventi per i quali DDEML deve notificare la funzione di callback dell'applicazione. Un'applicazione può specificare i flag di monitoraggio seguenti:



| Flag          | Descrizione                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALLBACK MF \_ | Notifica alla funzione di callback ogni volta che una transazione viene inviata a qualsiasi funzione di callback DDE nel sistema.                                                                                                                                           |
| MF \_ CONV      | Notifica alla funzione di callback ogni volta che viene stabilita o terminata una conversazione.                                                                                                                                                                |
| ERRORI \_ MF    | Notifica alla funzione di callback ogni volta che si verifica un errore DDEML.                                                                                                                                                                                       |
| MF \_ HSZ \_ INFO | Notifica alla funzione di callback ogni volta che un'applicazione DDEML crea, libera o incrementa il conteggio di utilizzo di un handle di stringa o ogni volta che un handle di stringa viene liberato in seguito a una chiamata alla [**funzione DdeUninitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) |
| COLLEGAMENTI \_ MF     | Notifica alla funzione di callback ogni volta che viene avviato o terminato un ciclo di consulenza.                                                                                                                                                                         |
| MF \_ POSTMSGS  | Notifica alla funzione di callback ogni volta che il sistema o un'applicazione invia un messaggio DDE.                                                                                                                                                           |
| MF \_ SENDMSGS  | Notifica alla funzione di callback ogni volta che il sistema o un'applicazione invia un messaggio DDE.                                                                                                                                                           |



 

Nell'esempio seguente viene illustrato come registrare un'applicazione di monitoraggio DDE in modo che la relativa funzione di callback DDE riceva le notifiche di tutti gli eventi DDE.


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



DDEML informa un'applicazione di monitoraggio di un evento DDE inviando una transazione [**\_ MONITOR XTYP**](xtyp-monitor.md) alla funzione di callback DDE dell'applicazione. Durante questa transazione, DDEML passa un flag di monitoraggio che specifica il tipo di evento DDE che si è verificato e un handle a un oggetto DDE che contiene informazioni dettagliate sull'evento. DDEML fornisce un set di strutture che l'applicazione può usare per estrarre le informazioni dall'oggetto DDE. Esiste una struttura corrispondente per ogni tipo di evento DDE.



| Struttura                                  | Descrizione                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | Contiene informazioni su una transazione.                         |
| [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | Contiene informazioni su una conversazione.                        |
| [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | Contiene informazioni sull'errore DDE più recente.                  |
| [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | Contiene informazioni su un ciclo di consulenza.                        |
| [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | Contiene informazioni su un handle di stringa.                       |
| [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | Contiene informazioni su un messaggio DDE inviato o inviato. |



 

L'esempio seguente illustra la funzione di callback DDE di un'applicazione di monitoraggio DDE che formatta le informazioni su ogni evento di handle di stringa e quindi visualizza le informazioni in una finestra. La funzione usa la [**struttura MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) per estrarre le informazioni dall'oggetto DDE.


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




