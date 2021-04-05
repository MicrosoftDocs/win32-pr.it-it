---
title: Uso di buffer di stringa
description: Le funzioni che restituiscono stringhe contengono un parametro di input, lpszBuffer, e un parametro size, lpdwBufferLength. Sebbene lpszBuffer possa essere NULL, lpdwBufferLength deve essere un puntatore valido a una variabile DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728762"
---
# <a name="using-string-buffers"></a><span data-ttu-id="da0c7-104">Uso di buffer di stringa</span><span class="sxs-lookup"><span data-stu-id="da0c7-104">Using String Buffers</span></span>

<span data-ttu-id="da0c7-105">Le funzioni che restituiscono stringhe contengono un parametro di input, *lpszBuffer*, e un parametro size, *lpdwBufferLength*.</span><span class="sxs-lookup"><span data-stu-id="da0c7-105">Functions that return strings contain an input parameter, *lpszBuffer*, and a size parameter, *lpdwBufferLength*.</span></span> <span data-ttu-id="da0c7-106">Sebbene *lpszBuffer* possa essere **null**, *lpdwBufferLength* deve essere un puntatore valido a una variabile **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="da0c7-106">Although *lpszBuffer* can be **NULL**, *lpdwBufferLength* must be a valid pointer to a **DWORD** variable.</span></span> <span data-ttu-id="da0c7-107">Se il buffer di input a cui punta *lpszBuffer* è **null** o troppo piccolo per conservare la stringa di output, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore \_ \_ buffer insufficiente**.</span><span class="sxs-lookup"><span data-stu-id="da0c7-107">If the input buffer pointed to by *lpszBuffer* is **NULL** or too small to hold the output string, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="da0c7-108">La variabile a cui punta *lpdwBufferLength* contiene un numero che rappresenta il numero di byte che la funzione richiede per restituire la stringa richiesta, incluso il terminatore **null** .</span><span class="sxs-lookup"><span data-stu-id="da0c7-108">The variable pointed to by *lpdwBufferLength* contains a number that represents the number of bytes the function requires to return the requested string, including the **null** terminator.</span></span> <span data-ttu-id="da0c7-109">L'applicazione deve allocare un buffer di queste dimensioni, impostare la variabile a cui punta *lpdwBufferLength* su questo valore e inviare nuovamente la richiesta.</span><span class="sxs-lookup"><span data-stu-id="da0c7-109">The application should allocate a buffer of this size, set the variable pointed to by *lpdwBufferLength* to this value, and resubmit the request.</span></span> <span data-ttu-id="da0c7-110">Se la dimensione del buffer è sufficiente per ricevere la stringa richiesta, la stringa viene copiata nel buffer di output con un carattere di terminazione **null** e la funzione restituisce un'indicazione di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="da0c7-110">If the buffer size is sufficient to receive the requested string, the string is copied to the output buffer with a **null** terminator and the function returns a success indication.</span></span> <span data-ttu-id="da0c7-111">La variabile a cui punta *lpdwBufferLength* ora contiene il numero di caratteri archiviati nel buffer, escluso il terminatore **null** .</span><span class="sxs-lookup"><span data-stu-id="da0c7-111">The variable pointed to by *lpdwBufferLength* now contains the number of characters stored in the buffer, excluding the **null** terminator.</span></span>

> [!Note]  
> <span data-ttu-id="da0c7-112">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="da0c7-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="da0c7-113">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="da0c7-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="da0c7-114">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="da0c7-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 