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
# <a name="retrieving-http-headers"></a><span data-ttu-id="7d7d0-103">Recupero di intestazioni HTTP</span><span class="sxs-lookup"><span data-stu-id="7d7d0-103">Retrieving HTTP Headers</span></span>

<span data-ttu-id="7d7d0-104">Questa esercitazione descrive come recuperare le informazioni di intestazione dalle richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-104">This tutorial describes how to retrieve header information from HTTP requests.</span></span>

## <a name="implementation-steps"></a><span data-ttu-id="7d7d0-105">Passaggi di implementazione</span><span class="sxs-lookup"><span data-stu-id="7d7d0-105">Implementation Steps</span></span>

<span data-ttu-id="7d7d0-106">Esistono due modi per recuperare le informazioni di intestazione:</span><span class="sxs-lookup"><span data-stu-id="7d7d0-106">There are two ways to retrieve the header information:</span></span>

-   <span data-ttu-id="7d7d0-107">Usare una delle costanti [**flag di informazioni di query**](query-info-flags.md) associate all'intestazione HTTP richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-107">Use one of the [**Query Info Flag**](query-info-flags.md) constants associated with the HTTP header that your application needs.</span></span>
-   <span data-ttu-id="7d7d0-108">Usare il \_ \_ flag di attributo personalizzato della query http e passare il nome dell'intestazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-108">Use the HTTP\_QUERY\_CUSTOM attribute flag and pass the name of the HTTP header.</span></span>

<span data-ttu-id="7d7d0-109">L'uso della costante associata all'intestazione HTTP richiesta dall'applicazione è più veloce internamente, ma è possibile che esistano intestazioni HTTP a cui non è associata una costante.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-109">Using the constant associated with the HTTP header that your application needs is faster internally, but there might be HTTP headers that do not have a constant associated with them.</span></span> <span data-ttu-id="7d7d0-110">In questi casi, è disponibile il metodo che usa il \_ flag di attributo personalizzato della query http \_ .</span><span class="sxs-lookup"><span data-stu-id="7d7d0-110">For those cases, the method using the HTTP\_QUERY\_CUSTOM attribute flag is available.</span></span>

<span data-ttu-id="7d7d0-111">Entrambi i metodi usano la funzione [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="7d7d0-111">Both methods use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function.</span></span> <span data-ttu-id="7d7d0-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) accetta l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) in cui è stata effettuata la richiesta HTTP, un attributo, un buffer, un valore DWORD che contiene la dimensione del buffer e un valore di indice.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle on which the HTTP request was made, one attribute, a buffer, a DWORD value that contains the buffer size, and an index value.</span></span> <span data-ttu-id="7d7d0-113">Un modificatore può anche essere aggiunto all'attributo passato a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per indicare il formato in cui devono essere restituiti i dati.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-113">A modifier can also be added to the attribute passed to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to indicate in what format the data should be returned.</span></span>

### <a name="retrieving-headers-using-a-constant"></a><span data-ttu-id="7d7d0-114">Recupero di intestazioni mediante una costante</span><span class="sxs-lookup"><span data-stu-id="7d7d0-114">Retrieving Headers Using a Constant</span></span>

<span data-ttu-id="7d7d0-115">Per utilizzare la funzione [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per recuperare un'intestazione HTTP utilizzando una costante, attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="7d7d0-115">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using a constant, follow these steps:</span></span>

1.  <span data-ttu-id="7d7d0-116">Chiamare [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con una costante dall'elenco degli [**attributi**](query-info-flags.md) , un buffer **null** e la variabile che include le dimensioni del buffer impostate su zero.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-116">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with a constant from the [**Attributes**](query-info-flags.md) list, a **NULL** buffer, and the variable that holds the buffer size set to zero.</span></span> <span data-ttu-id="7d7d0-117">Inoltre, se l'applicazione richiede i dati in un formato particolare, è possibile aggiungere una costante dall'elenco dei [**modificatori**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="7d7d0-117">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
2.  <span data-ttu-id="7d7d0-118">Se l'intestazione HTTP richiesta esiste, la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) dovrebbe avere esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) deve restituire \_ l'errore buffer insufficiente \_ e la variabile passata per il parametro *lpdwBufferLength* deve essere impostata sul numero di byte richiesti.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-118">If the requested HTTP header exists, the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) should fail, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) should return ERROR\_INSUFFICIENT\_BUFFER, and the variable passed for the *lpdwBufferLength* parameter should be set to the number of bytes required.</span></span>
3.  <span data-ttu-id="7d7d0-119">Allocare un buffer con il numero di byte richiesto.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-119">Allocate a buffer with the number of bytes required.</span></span>
4.  <span data-ttu-id="7d7d0-120">Ripetere la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="7d7d0-120">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="7d7d0-121">Nell'esempio seguente viene illustrata una chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando \_ la \_ costante CRLF delle intestazioni RAW della query http \_ \_ , che è un valore speciale che richiede tutte le intestazioni HTTP restituite.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-121">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_RAW\_HEADERS\_CRLF constant, which is a special value that requests all of the returned HTTP headers.</span></span>


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



### <a name="retrieving-headers-using-http_query_custom"></a><span data-ttu-id="7d7d0-122">Recupero di intestazioni utilizzando una \_ query http \_ personalizzata</span><span class="sxs-lookup"><span data-stu-id="7d7d0-122">Retrieving Headers Using HTTP\_QUERY\_CUSTOM</span></span>

<span data-ttu-id="7d7d0-123">Per utilizzare la funzione [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) per recuperare un'intestazione HTTP utilizzando una \_ query http \_ personalizzata, attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="7d7d0-123">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using HTTP\_QUERY\_CUSTOM, follow these steps:</span></span>

1.  <span data-ttu-id="7d7d0-124">Allocare un buffer sufficientemente grande da mantenere il nome della stringa dell'intestazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-124">Allocate a buffer that is large enough to hold the string name of the HTTP header.</span></span>
2.  <span data-ttu-id="7d7d0-125">Scrivere il nome di stringa dell'intestazione HTTP nel buffer.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-125">Write the string name of the HTTP header into the buffer.</span></span>
3.  <span data-ttu-id="7d7d0-126">Chiamare [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) con la \_ query http \_ Custom, il buffer che contiene il nome di stringa dell'intestazione HTTP e la variabile che contiene la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-126">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with HTTP\_QUERY\_CUSTOM, the buffer that contains the string name of the HTTP header, and the variable that holds the buffer size.</span></span> <span data-ttu-id="7d7d0-127">Inoltre, se l'applicazione richiede i dati in un formato particolare, è possibile aggiungere una costante dall'elenco dei [**modificatori**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="7d7d0-127">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
4.  <span data-ttu-id="7d7d0-128">Se la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) ha esito negativo e [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce \_ un errore \_ di buffer insufficiente, riallocare un buffer con il numero di byte richiesto.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-128">If the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, reallocate a buffer with the number of bytes required.</span></span>
5.  <span data-ttu-id="7d7d0-129">Scrivere di nuovo il nome di stringa dell'intestazione HTTP nel buffer.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-129">Write the string name of the HTTP header into the buffer again.</span></span>
6.  <span data-ttu-id="7d7d0-130">Ripetere la chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="7d7d0-130">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="7d7d0-131">Nell'esempio seguente viene illustrata una chiamata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando la \_ costante personalizzata della query http \_ per richiedere l'intestazione HTTP Content-Type.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-131">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_CUSTOM constant to request the Content-Type HTTP header.</span></span>


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
> <span data-ttu-id="7d7d0-132">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="7d7d0-133">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="7d7d0-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="7d7d0-134">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="7d7d0-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 