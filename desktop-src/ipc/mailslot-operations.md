---
description: Descrizioni delle funzioni da usare quando si usano mailslot, client e server.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operazioni di Mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fefce55c70971f5d611c41d473180897706bc04960509818cb0d092c7f83825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829501"
---
# <a name="mailslot-operations"></a>Operazioni di Mailslot

Quando si usano mailslot, i client e i server devono usare solo le funzioni descritte nelle tabelle seguenti. Non usare altre funzioni, anche se accettano handle di file o nomi di file come parametri, perché non sono progettati per funzionare con mailslot.

## <a name="mailslot-server-functions"></a>Funzioni del server Mailslot

I server Mailslot usano esclusivamente tre funzioni, come illustrato nella tabella seguente.



| Funzione                                   | Descrizione                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Crea un mailslot e restituisce un handle mailslot.                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Recupera le dimensioni massime dei messaggi, le dimensioni di mailslot, le dimensioni del messaggio successivo nel mailslot, il numero di messaggi nel mailslot e il tempo di attesa di un messaggio da parte di un'operazione di lettura. |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Modifica il timeout di lettura per un mailslot.                                                                                                                                                                    |



 

Le funzioni seguenti vengono usate anche dai server mailslot.



| Funzione                                                         | Descrizione                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Duplica l'handle mailslot.                     |
| [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Recupera i messaggi da un mailslot.                 |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera la data e l'ora di creazione di un mailslot. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Imposta la data e l'ora di creazione di un mailslot.      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Recupera le proprietà dell'handle di mailslot.        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Imposta le proprietà dell'handle di mailslot.             |



 

## <a name="mailslot-client-functions"></a>Funzioni client di Mailslot

Un processo client usa le funzioni seguenti quando interagisce con un mailslot.



| Funzione                                                             | Descrizione                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**Closehandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Chiude un handle mailslot per un processo client.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Crea un handle mailslot per un processo client. |
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Duplica un handle mailslot.                   |
| [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Scrive i dati in un mailslot.                      |



 

 

 
