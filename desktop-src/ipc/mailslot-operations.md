---
description: Descrizioni delle funzioni da utilizzare quando si utilizzano mailslot, client e server.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operazioni inserimento/espulsione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313057"
---
# <a name="mailslot-operations"></a>Operazioni inserimento/espulsione

Quando si utilizza mailslot, i client e i server devono utilizzare solo le funzioni descritte nelle tabelle seguenti. Non usare altre funzioni, anche se accettano gli handle di file o i nomi di file come parametri, perché non sono progettati per funzionare con mailslot.

## <a name="mailslot-server-functions"></a>Funzioni del server inserimento/espulsione

I server inserimento/espulsione hanno un utilizzo esclusivo di tre funzioni, come illustrato nella tabella seguente.



| Funzione                                   | Descrizione                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Crea un inserimento/espulsione e restituisce un handle inserimento/espulsione.                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Recupera le dimensioni massime del messaggio, le dimensioni inserimento/espulsione, le dimensioni del messaggio successivo in inserimento/espulsione, il numero di messaggi nel inserimento/espulsione e l'intervallo di tempo durante il quale un'operazione di lettura può attendere un messaggio. |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Modifica il timeout di lettura per un inserimento/espulsione.                                                                                                                                                                    |



 

Le funzioni seguenti sono usate anche dai server inserimento/espulsione.



| Funzione                                                         | Descrizione                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Duplica l'handle inserimento/espulsione.                     |
| [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Recupera i messaggi da un inserimento/espulsione.                 |
| [**GetFileTime ha provocato**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera la data e l'ora di creazione di un inserimento/espulsione. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Imposta la data e l'ora di creazione di un inserimento/espulsione.      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Recupera le proprietà dell'handle inserimento/espulsione.        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Imposta le proprietà dell'handle inserimento/espulsione.             |



 

## <a name="mailslot-client-functions"></a>Funzioni client inserimento/espulsione

Un processo client usa le funzioni seguenti quando si interagisce con un inserimento/espulsione.



| Funzione                                                             | Descrizione                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Chiude un handle inserimento/espulsione per un processo client.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Crea un handle inserimento/espulsione per un processo client. |
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Duplica un handle inserimento/espulsione.                   |
| [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Scrive i dati in un inserimento/espulsione.                      |



 

 

 
