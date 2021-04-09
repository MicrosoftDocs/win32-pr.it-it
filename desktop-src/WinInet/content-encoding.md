---
title: Codifica contenuto
description: A partire da Windows Server 2008 e Windows Vista, l'applicazione può indirizzare WinINet per eseguire la decodifica del contenuto per gli schemi di codifica del contenuto gzip e Deflate.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Codifica contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b089ae2aa4cbacdfc9b6ebefe5cbdfc1bfc10e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047228"
---
# <a name="content-encoding"></a>Codifica contenuto

Come specificato nel protocollo HTTP (RFC 2616), le applicazioni possono richiedere che il server restituisca risposte HTTP in formato codificato. Prima di Windows Server 2008 e Windows Vista, le richieste con codifica del contenuto venivano inviate all'applicazione per l'elaborazione a livello di livello. A partire da Windows Server 2008 e Windows Vista, l'applicazione può indirizzare WinINet per eseguire la decodifica del contenuto per gli schemi di codifica del contenuto gzip e Deflate.

Per abilitare la decodifica del contenuto, l'applicazione imposta l'opzione di decodifica che richiede che WinINet esegua la decodifica per conto dell'utente. Tuttavia, l'abilitazione della decodifica non garantisce che WinINet esegua la decodifica del contenuto e l'applicazione deve essere preparata per la gestione della decodifica. WinINet rimuove l'intestazione Content-Encoding dalla risposta quando la decodifica del contenuto viene eseguita correttamente. Si prevede che le applicazioni gestiscano la decodifica del contenuto, indipendentemente dal fatto che l'opzione di decodifica sia abilitata o disabilitata quando l'intestazione Content-Encoding è presente nella risposta.

Quando è abilitata la decodifica, l'applicazione deve specificare l'elenco di codifiche supportate nell'intestazione Accept-Encoding della richiesta. L'intestazione Accept-Encoding, tuttavia, non obbliga il server a inviare una risposta codificata. WinINet invierà risposte che non corrispondono all'elenco di codifiche accettabili all'applicazione.

Nell'elenco seguente vengono descritte le condizioni in base alle quali WinINet eseguirà la decodifica del contenuto quando l'opzione è abilitata:

-   L'intestazione Accept-Encoding deve essere presente nella richiesta ed è necessario specificare gli schemi di codifica gzip, deflate o gzip e Deflate.
-   Lo schema di codifica specificato nell'intestazione Content-Encoding deve corrispondere a uno degli schemi di codifica specificati nell'intestazione Accept-Encoding.
-   L'intestazione Content-Encoding nella risposta specifica un solo schema di codifica.
-   La risposta deve contenere solo un'intestazione Content-Encoding. WinINet decodifica il contenuto codificato con un solo schema di codifica.
-   L'intestazione Cache-Control non deve contenere la direttiva no-transform.
-   L'intestazione Content-Range non deve essere presente nella risposta.

## <a name="setting-the-decompression-option"></a>Impostazione dell'opzione di decompressione

È possibile impostare l'opzione decodifica nell'handle di sessione, nell'handle della richiesta o nell'handle di connessione. L'handle su cui è impostata l'opzione di decodifica definisce l'ambito dell'opzione di decodifica. Se, ad esempio, si imposta la decodifica nella sessione, la decodifica di tutte le connessioni e richieste create con tale handle.

Per impostare l'opzione di decodifica, l'applicazione chiama [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con l'handle restituito da [**internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena), [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). L' **opzione \_ Internet \_ \_ decodifica http** è specificata nel parametro *dwOption* e il parametro *lpBuffer* punta a una variabile booleana impostata su true. Per disabilitare la decodifica, l'applicazione chiama **InternetSetOption** con l' **opzione \_ Internet \_ \_ decodifica http** e la variabile booleana impostata su false.

Quando viene impostata l'opzione decodifica, WinINet esegue la decodifica sulla richiesta quando l'applicazione chiama [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Se WinINet rileva un errore durante l'esecuzione della decodifica del contenuto, la chiamata a **InternetReadFile** ha esito negativo e si verifica un **errore di \_ \_ decodifica \_ Internet**. Quando la decodifica ha esito negativo, l'applicazione ha due opzioni: può rimuovere l'intestazione Accept-Encoding e inviare di nuovo la richiesta oppure impostare l' **opzione \_ Internet \_ \_ decodifica http** per la richiesta su false e quindi inviare nuovamente la richiesta. Se l'opzione decodifica è impostata su false, l'applicazione deve controllare l'intestazione Content-Encoding ed eseguire qualsiasi decodifica a livello di applicazione.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 