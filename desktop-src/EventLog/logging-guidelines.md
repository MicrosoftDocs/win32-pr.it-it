---
description: I registri eventi archiviano i record degli eventi significativi per conto del sistema e delle applicazioni in esecuzione nel sistema.
ms.assetid: 58a6569a-2775-4687-bf99-579fa4153191
title: Linee guida per la registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1210757a7961d82d13d4887e40fbd3837b86138
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131315"
---
# <a name="logging-guidelines"></a>Linee guida per la registrazione

I registri eventi archiviano i record degli eventi significativi per conto del sistema e delle applicazioni in esecuzione nel sistema. Poiché le funzioni di registrazione sono a scopo generico, è necessario decidere quali informazioni sono appropriate per la registrazione. In genere, è consigliabile registrare solo le informazioni che potrebbero essere utili per la diagnosi di un problema hardware o software. La registrazione degli eventi non può essere utilizzata come strumento di traccia.

## <a name="choosing-events-to-log"></a>Scelta degli eventi da registrare

Di seguito sono riportati alcuni esempi di casi in cui la registrazione degli eventi può essere utile:

-   Problemi di risorse. La registrazione di un evento di avviso quando l'allocazione di memoria non riesce può aiutare a indicare la cause di una situazione di memoria insufficiente.
-   Problemi hardware. Se un driver di dispositivo rileva un timeout del controller del disco, un'interruzione dell'alimentazione in una porta parallela o un errore di dati da una rete o da una scheda seriale, il driver di dispositivo può registrare le informazioni relative a questi eventi per consentire all'amministratore di sistema di diagnosticare i problemi hardware.
-   Settori danneggiati. Se un driver del disco rileva un settore errato, è possibile che sia in grado di leggere o scrivere nel settore dopo aver ritentato l'operazione, ma il settore non andrà a buon fine. Se il driver del disco può continuare, deve registrare un evento di avviso. in caso contrario, dovrebbe registrare un evento di errore. Se un driver file system trova un numero elevato di settori danneggiati e li corregge, la registrazione degli eventi di avviso può aiutare un amministratore a determinare se il disco sta per avere esito negativo.
-   Eventi informativi. Un'applicazione server, ad esempio un server di database, registra un utente che esegue l'accesso, apre un database o avvia un trasferimento di file. Il server può inoltre registrare altri eventi, ad esempio errori (non può accedere al file, al processo host disconnesso e così via), al danneggiamento del database o se un trasferimento di file è stato eseguito correttamente.

## <a name="writing-messages"></a>Scrittura di messaggi

I messaggi devono avere senso per gli amministratori e gli utenti che tentano di risolvere un problema. Un messaggio deve contenere tutte le informazioni necessarie per capire cosa ha causato il problema e come correggerlo.

Evitare di scrivere un messaggio enigmatico, ad esempio "un pacchetto driver ricevuto dal sottosistema di I/O non è valido. I dati sono il pacchetto ". Un messaggio migliore indicherà che il driver in questione funziona correttamente, ma che registra pacchetti formattati in modo errato. Per risolvere il problema, è possibile che sia necessaria una versione Unicode del driver. Per ulteriori informazioni sulla scrittura di messaggi di errore validi, vedere [linee guida](/windows/desktop/Debug/error-message-guidelines)per i messaggi di errore.

Non utilizzare tabulazioni o virgole nel testo del messaggio, perché i registri eventi possono essere salvati come file di testo delimitati da virgole o tabulazioni. Molte organizzazioni importano questi file nei database e i caratteri di formattazione aggiuntivi richiedono la manipolazione manuale.

Quando si utilizzano nomi UNC o altri collegamenti contenenti spazi, racchiudere il nome tra parentesi angolari. Ad esempio, <\\ \\ *ShareName* \\ *ServerName*>. È possibile scrivere un URL alla fine del messaggio che indica all'utente il materiale della Guida correlato. L'URL deve essere un nome host DNS completo. Ad esempio, è possibile aggiungere il testo seguente ai messaggi: "per ulteriori informazioni su questo messaggio, visitare il sito del supporto tecnico all'indirizzo https://www.microsoft.com/Support/ProdRedirect/ContentSearch.asp ". Il collegamento porterebbe a una pagina ASP che reindirizza l'utente al contenuto relativo al messaggio di errore. Analizzerà i parametri aggiuntivi (passati quando si fa clic sull'URL) per determinare dove reindirizzare l'utente.

Gli argomenti passati alla funzione [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) vengono aggiunti all'URL come indicato di seguito:

``` syntax
strHTTPQuery += L"?EvtSrc=" + _strEscapedSource;
strHTTPQuery += L"&EvtCat=" + _strEscapedCategory;
strHTTPQuery += L"&EvtID=" + _strEscapedEventID;
strHTTPQuery += L"&EvtCatID=" + _strEscapedCategoryID;
strHTTPQuery += L"&EvtType=" + _strEscapedType;
strHTTPQuery += L"&EvtTypeID=" + _strEscapedTypeID;
strHTTPQuery += L"&EvtRptTime=" + _strEscapedDateAndTime;
strHTTPQuery += L"&EvtTZBias=" + _strEscapedTimeZoneBias;
```

Se il nome della società, il nome del prodotto, la versione del prodotto, il nome del file e la versione del file dall'intestazione DLL del messaggio per l'origine evento sono validi, vengono aggiunti anche all'URL:

``` syntax
ADD_VER_STR(L"CoName",   _strEscapedCompanyName);
ADD_VER_STR(L"ProdName", _strEscapedProductName);
ADD_VER_STR(L"ProdVer",  _strEscapedProductVersion);
ADD_VER_STR(L"FileName", _strEscapedFileName);
ADD_VER_STR(L"FileVer",  _strEscapedFileVersion);
```

## <a name="reducing-overhead"></a>Riduzione del sovraccarico

La registrazione degli eventi utilizza risorse quali lo spazio su disco e il tempo processore. La quantità di spazio su disco richiesta da un log eventi e l'overhead per un'applicazione che registra gli eventi dipendono dalla quantità di informazioni che si sceglie di registrare. Per questo motivo è importante registrare solo le informazioni essenziali. È anche opportuno inserire le chiamate di registrazione eventi in un percorso di errore nel codice anziché nel percorso del codice principale, riducendo così le prestazioni.

La quantità di spazio su disco necessaria per ogni record del registro eventi include i membri della struttura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . Si tratta di una struttura a lunghezza variabile. le stringhe e i dati binari vengono archiviati dopo la struttura.

 

 
