---
title: Recupero di intestazioni HTTP
description: Questa esercitazione descrive come recuperare le informazioni di intestazione dalle richieste HTTP.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b31043940b8c2127d1cfa1696d2821641d0784
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300263"
---
# <a name="retrieving-http-headers"></a>Recupero di intestazioni HTTP

Questa esercitazione descrive come recuperare le informazioni di intestazione dalle richieste HTTP.

## <a name="implementation-steps"></a>Passaggi di implementazione

Esistono due modi per recuperare le informazioni di intestazione:

-   Usare una delle costanti [**flag di informazioni di query**](query-info-flags.md) associate all'intestazione HTTP richiesta dall'applicazione.
-   Usare il \_ \_ flag di attributo personalizzato della query http e passare il nome dell'intestazione HTTP.

L'uso della costante associata all'intestazione HTTP richiesta dall'applicazione è più veloce internamente, ma è possibile che esistano intestazioni HTTP a cui non è associata una costante. In questi casi, è disponibile il metodo che usa il \_ flag di attributo personalizzato della query http \_ .

Entrambi i metodi usano la funzione [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) . [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) accetta l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) in cui è stata effettuata la richiesta HTTP, un attributo, un buffer, un valore DWORD che contiene la dimensione del buffer e un valore di indice. Un modificatore può anche essere aggiunto all'attributo passato a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per indicare il formato in cui devono essere restituiti i dati.

### <a name="retrieving-headers-using-a-constant"></a>Recupero di intestazioni mediante una costante

Per utilizzare la funzione [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per recuperare un'intestazione HTTP utilizzando una costante, attenersi alla seguente procedura:

1.  Chiamare [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con una costante dall'elenco degli [**attributi**](query-info-flags.md) , un buffer **null** e la variabile che include le dimensioni del buffer impostate su zero. Inoltre, se l'applicazione richiede i dati in un formato particolare, è possibile aggiungere una costante dall'elenco dei [**modificatori**](query-info-flags.md) .
2.  Se l'intestazione HTTP richiesta esiste, la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) dovrebbe avere esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) deve restituire \_ l'errore buffer insufficiente \_ e la variabile passata per il parametro *lpdwBufferLength* deve essere impostata sul numero di byte richiesti.
3.  Allocare un buffer con il numero di byte richiesto.
4.  Ripetere la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

Nell'esempio seguente viene illustrata una chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando \_ la \_ costante CRLF delle intestazioni RAW della query http \_ \_ , che è un valore speciale che richiede tutte le intestazioni HTTP restituite.


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



### <a name="retrieving-headers-using-http_query_custom"></a>Recupero di intestazioni utilizzando una \_ query http \_ personalizzata

Per utilizzare la funzione [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per recuperare un'intestazione HTTP utilizzando una \_ query http \_ personalizzata, attenersi alla seguente procedura:

1.  Allocare un buffer sufficientemente grande da mantenere il nome della stringa dell'intestazione HTTP.
2.  Scrivere il nome di stringa dell'intestazione HTTP nel buffer.
3.  Chiamare [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con la \_ query http \_ Custom, il buffer che contiene il nome di stringa dell'intestazione HTTP e la variabile che contiene la dimensione del buffer. Inoltre, se l'applicazione richiede i dati in un formato particolare, è possibile aggiungere una costante dall'elenco dei [**modificatori**](query-info-flags.md) .
4.  Se la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) ha esito negativo e [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce \_ un errore \_ di buffer insufficiente, riallocare un buffer con il numero di byte richiesto.
5.  Scrivere di nuovo il nome di stringa dell'intestazione HTTP nel buffer.
6.  Ripetere la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

Nell'esempio seguente viene illustrata una chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando la \_ costante personalizzata della query http \_ per richiedere l'intestazione HTTP Content-Type.


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
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 