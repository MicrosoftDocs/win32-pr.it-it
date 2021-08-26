---
title: Recupero di intestazioni HTTP
description: Questa esercitazione descrive come recuperare informazioni sull'intestazione dalle richieste HTTP.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9c1dbae3447d5ae44c8d348394f2dc802ed9d7b4af7d99fde19d0b5d2c3d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955511"
---
# <a name="retrieving-http-headers"></a>Recupero di intestazioni HTTP

Questa esercitazione descrive come recuperare informazioni sull'intestazione dalle richieste HTTP.

## <a name="implementation-steps"></a>Passaggi di implementazione

Esistono due modi per recuperare le informazioni sull'intestazione:

-   Usare una delle costanti [**Query Info Flag**](query-info-flags.md) associate all'intestazione HTTP richiesta dall'applicazione.
-   Usare il \_ flag di attributo HTTP QUERY CUSTOM e passare il nome \_ dell'intestazione HTTP.

L'uso della costante associata all'intestazione HTTP richiesta dall'applicazione è più veloce internamente, ma potrebbero esserci intestazioni HTTP a cui non è associata una costante. In questi casi, è disponibile il metodo che usa il flag di attributo HTTP \_ QUERY \_ CUSTOM.

Entrambi i metodi usano [**la funzione HttpQueryInfo.**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) accetta l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) in cui è stata effettuata la richiesta HTTP, un attributo, un buffer, un valore DWORD che contiene le dimensioni del buffer e un valore di indice. È anche possibile aggiungere un modificatore all'attributo passato a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per indicare in quale formato devono essere restituiti i dati.

### <a name="retrieving-headers-using-a-constant"></a>Recupero di intestazioni tramite una costante

Per usare la [**funzione HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per recuperare un'intestazione HTTP usando una costante, seguire questa procedura:

1.  Chiamare [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con una costante dall'elenco [**Attributi,**](query-info-flags.md) un buffer **NULL** e la variabile che contiene le dimensioni del buffer impostate su zero. Inoltre, se l'applicazione necessita dei dati in un formato specifico, è possibile aggiungere una costante [**dall'elenco Modificatori.**](query-info-flags.md)
2.  Se l'intestazione HTTP richiesta esiste, la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) avrà esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà ERROR INSUFFICIENT BUFFER e la variabile passata per il parametro \_ \_ *lpdwBufferLength* deve essere impostata sul numero di byte necessari.
3.  Allocare un buffer con il numero di byte necessari.
4.  Ripetere la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

L'esempio seguente illustra una chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando la costante \_ HTTP QUERY RAW HEADERS \_ \_ CRLF, che è un valore speciale che richiede tutte le \_ intestazioni HTTP restituite.


```C++
// Retrieving Headers Using a Constant
BOOL SampleCodeOne(HINTERNET hHttp)
{
   LPVOID lpOutBuffer=NULL;
   DWORD dwSize = 0;

retry:

   // This call will fail on the first pass, because
   // no buffer is allocated.
   if(!HttpQueryInfo(hHttp,HTTP_QUERY_RAW_HEADERS_CRLF,
      (LPVOID)lpOutBuffer,&dwSize,NULL))
   {
      if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
      {
         // Code to handle the case where the header isn't available.
         return TRUE;
      }
      else
      {
        // Check for an insufficient buffer.
        if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
        {
            // Allocate the necessary buffer.
            lpOutBuffer = new char[dwSize];

            // Retry the call.
            goto retry;
        }
        else
        {
            // Error handling code.
            if (lpOutBuffer)
            {
               delete [] lpOutBuffer;
            }
            return FALSE;
        }
      }
   }

   if (lpOutBuffer)
   {
      delete [] lpOutBuffer;
   }

   return TRUE;
}
```



### <a name="retrieving-headers-using-http_query_custom"></a>Recupero di intestazioni tramite HTTP \_ QUERY \_ CUSTOM

Per usare la [**funzione HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per recuperare un'intestazione HTTP usando HTTP \_ QUERY \_ CUSTOM, seguire questa procedura:

1.  Allocare un buffer sufficientemente grande da contenere il nome della stringa dell'intestazione HTTP.
2.  Scrivere il nome della stringa dell'intestazione HTTP nel buffer.
3.  Chiamare [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con HTTP QUERY CUSTOM, il buffer che contiene il nome della stringa dell'intestazione HTTP e la variabile \_ che contiene le dimensioni del \_ buffer. Inoltre, se l'applicazione necessita dei dati in un formato specifico, è possibile aggiungere una costante [**dall'elenco Modificatori.**](query-info-flags.md)
4.  Se la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ INSUFFICIENT \_ BUFFER, riallocare un buffer con il numero di byte necessari.
5.  Scrivere di nuovo il nome della stringa dell'intestazione HTTP nel buffer.
6.  Ripetere la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

L'esempio seguente illustra una chiamata a [**HttpQueryInfo usando**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) la costante HTTP \_ QUERY CUSTOM per richiedere \_ l'intestazione HTTP Content-Type.


```C++
// Retrieving Headers Using HTTP_QUERY_CUSTOM
BOOL SampleCodeTwo(HINTERNET hHttp)
{
    DWORD dwSize = 20;
    LPVOID lpOutBuffer = new char[dwSize];

    StringCchPrintfA((LPSTR)lpOutBuffer,dwSize,"Content-Type");

retry:

    if(!HttpQueryInfo(hHttp,HTTP_QUERY_CUSTOM,
        (LPVOID)lpOutBuffer,&dwSize,NULL))
    {
        if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
        {
            // Code to handle the case where the header isn't available.
            delete [] lpOutBuffer;
            return TRUE;
        }
        else
        {
            // Check for an insufficient buffer.
            if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
            {
                // Allocate the necessary buffer.
                delete [] lpOutBuffer;
                lpOutBuffer = new char[dwSize];

                // Rewrite the header name in the buffer.
                StringCchPrintfA((LPSTR)lpOutBuffer,
                                 dwSize,"Content-Type");

                // Retry the call.
                goto retry;
            }
            else
            {
                // Error handling code.
                delete [] lpOutBuffer;
                return FALSE;
            }
        }
    }

   return TRUE;
}
```



> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 