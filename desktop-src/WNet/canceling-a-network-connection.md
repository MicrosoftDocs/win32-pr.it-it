---
title: Annullamento di una connessione di rete
description: Per annullare una connessione a una risorsa di rete, un'applicazione può chiamare la funzione WNetCancelConnection2, come illustrato nell'esempio seguente.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cc5fb9536a5d073a6c99d8b49a00e3c2771546
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872806"
---
# <a name="canceling-a-network-connection"></a><span data-ttu-id="323d1-103">Annullamento di una connessione di rete</span><span class="sxs-lookup"><span data-stu-id="323d1-103">Canceling a Network Connection</span></span>

<span data-ttu-id="323d1-104">Per annullare una connessione a una risorsa di rete, un'applicazione può chiamare la funzione [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="323d1-104">To cancel a connection to a network resource, an application can call the [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) function, as shown in the following example.</span></span>

<span data-ttu-id="323d1-105">La chiamata a **WNetCancelConnection2** specifica che una connessione di rete non deve più essere persistente.</span><span class="sxs-lookup"><span data-stu-id="323d1-105">The call to **WNetCancelConnection2** specifies that a network connection should no longer be persistent.</span></span> <span data-ttu-id="323d1-106">Nell'esempio viene chiamato un gestore degli errori definito dall'applicazione per elaborare gli errori e la funzione di [**testo**](/windows/desktop/api/wingdi/nf-wingdi-textouta) per la stampa.</span><span class="sxs-lookup"><span data-stu-id="323d1-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
DWORD dwResult; 
 
// Call the WNetCancelConnection2 function, specifying
//  that the connection should no longer be a persistent one.
//
dwResult = WNetCancelConnection2("z:", 
    CONNECT_UPDATE_PROFILE, // remove connection from profile 
    FALSE);                 // fail if open files or jobs 
 
// Process errors.
//  The device is not a local redirected device.
//
if (dwResult == ERROR_NOT_CONNECTED) 
{ 
    printf("Drive z: not connected.\n"); 
    return dwResult; 
} 
 
// Call an application-defined error handler.
//
else if(dwResult != NO_ERROR) 
{ 
    printf("WNetCancelConnection2 failed.\n"); 
    return dwResult; 
}
//
// Otherwise, report canceling the connection.
//
printf("Connection closed for z: drive.\n"); 
```



<span data-ttu-id="323d1-107">La funzione [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) è supportata per la compatibilità con le versioni precedenti di Windows per gruppi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="323d1-107">The [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="323d1-108">Per le nuove applicazioni, usare [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span><span class="sxs-lookup"><span data-stu-id="323d1-108">For new applications, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span></span>

<span data-ttu-id="323d1-109">Per ulteriori informazioni sull'utilizzo di un gestore degli errori definito dall'applicazione, vedere [recupero degli errori di rete](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="323d1-109">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 