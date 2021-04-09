---
title: Recupero di informazioni su una risorsa di rete
description: Per identificare il provider di rete che possiede una risorsa, un'applicazione può chiamare la funzione WNetGetResourceInformation, come illustrato nell'esempio di codice seguente.
ms.assetid: 4bddb55c-181d-4c6f-bd92-9c27d6b894bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf21e48be540f5307fc1ebd2359aea7ff03cbe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118078"
---
# <a name="retrieving-information-about-a-network-resource"></a><span data-ttu-id="c0f2d-103">Recupero di informazioni su una risorsa di rete</span><span class="sxs-lookup"><span data-stu-id="c0f2d-103">Retrieving Information About a Network Resource</span></span>

<span data-ttu-id="c0f2d-104">Per identificare il provider di rete che possiede una risorsa, un'applicazione può chiamare la funzione [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="c0f2d-104">To identify the network provider that owns a resource, an application can call the [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) function, as illustrated in the following code sample.</span></span>

<span data-ttu-id="c0f2d-105">L'esempio seguente è una funzione (CheckServer) che accetta un nome di server come parametro e restituisce informazioni su tale server.</span><span class="sxs-lookup"><span data-stu-id="c0f2d-105">The following sample is a function (CheckServer) that takes a server name as a parameter and returns information about that server.</span></span> <span data-ttu-id="c0f2d-106">Per prima cosa la funzione chiama la funzione [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) per inizializzare il contenuto di un blocco di memoria su zero.</span><span class="sxs-lookup"><span data-stu-id="c0f2d-106">First the function calls the [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) function to initialize the contents of a block of memory to zero.</span></span> <span data-ttu-id="c0f2d-107">Nell'esempio viene quindi chiamata la funzione [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , specificando un buffer sufficientemente grande da poter essere contenuta solo una struttura [**netresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) .</span><span class="sxs-lookup"><span data-stu-id="c0f2d-107">Then the sample calls the [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) function, specifying a buffer large enough to hold only a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure.</span></span> <span data-ttu-id="c0f2d-108">La routine include l'elaborazione degli errori per gestire il caso in cui un buffer di queste dimensioni non è sufficiente per includere le stringhe a lunghezza variabile a cui appartengono i membri del punto della struttura **netresource** .</span><span class="sxs-lookup"><span data-stu-id="c0f2d-108">The routine includes error processing to handle the case when a buffer of this size is insufficient to hold the variable-length strings to which members of the **NETRESOURCE** structure point.</span></span> <span data-ttu-id="c0f2d-109">Se si verifica questo errore, l'esempio alloca memoria sufficiente e chiama di nuovo **WNetGetResourceInformation** .</span><span class="sxs-lookup"><span data-stu-id="c0f2d-109">If this error occurs, the sample allocates sufficient memory and calls **WNetGetResourceInformation** again.</span></span> <span data-ttu-id="c0f2d-110">Infine, l'esempio libera la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="c0f2d-110">Finally, the sample frees the allocated memory.</span></span>

<span data-ttu-id="c0f2d-111">Si noti che nell'esempio si presuppone che il parametro *pszServer* punti al nome di un server riconosciuto da uno dei provider di rete nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="c0f2d-111">Note that the sample assumes that the *pszServer* parameter points to a server name that one of the network providers on the local computer recognizes.</span></span>


```C++
#include <Windows.h>
#include <Winnetwk.h >

// Need to link with Mpr.lib
#pragma comment(lib, "Mpr.lib")
//
// Verify a server on the network. 
//
DWORD
CheckServer( LPTSTR pszServer )
{  
    DWORD dwBufferSize = sizeof(NETRESOURCE);
    LPBYTE lpBuffer;                  // buffer
    NETRESOURCE nr;
    LPTSTR pszSystem = NULL;          // variable-length strings

    //
    // Set the block of memory to zero; then initialize
    // the NETRESOURCE structure. 
    //
    ZeroMemory(&nr, sizeof(nr));

    nr.dwScope       = RESOURCE_GLOBALNET;
    nr.dwType        = RESOURCETYPE_ANY;
    nr.lpRemoteName  = pszServer;

    //
    // First call the WNetGetResourceInformation function with 
    // memory allocated to hold only a NETRESOURCE structure. This 
    // method can succeed if all the NETRESOURCE pointers are NULL.
    // If the call fails because the buffer is too small, allocate
    // a larger buffer.
    //
    lpBuffer = (LPBYTE) malloc( dwBufferSize );
    if (lpBuffer == NULL) 
        return FALSE;

    while ( WNetGetResourceInformation(&nr, lpBuffer, &dwBufferSize, 
                &pszSystem) == ERROR_MORE_DATA)
    {
        lpBuffer = (LPBYTE) realloc(lpBuffer, dwBufferSize);
    }

    // Process the contents of the NETRESOURCE structure and the
    // variable-length strings in lpBuffer and set dwValue. When
    // finished, free the memory.

    free(lpBuffer);

    return TRUE;
}
```



 

 