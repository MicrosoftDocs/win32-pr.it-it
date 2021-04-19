---
title: Aggiunta di una connessione di rete
description: Per creare una connessione a una risorsa di rete descritta da una struttura NETRESOURCE, un'applicazione può chiamare WNetAddConnection2, WNetAddConnection3 o WNetUseConnection.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476e03193b919f17a2060e415db5e7ea60c8364e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300192"
---
# <a name="adding-a-network-connection"></a><span data-ttu-id="b1931-103">Aggiunta di una connessione di rete</span><span class="sxs-lookup"><span data-stu-id="b1931-103">Adding a Network Connection</span></span>

<span data-ttu-id="b1931-104">Per creare una connessione a una risorsa di rete descritta da una struttura [**netresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , un'applicazione può chiamare [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)o [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) .</span><span class="sxs-lookup"><span data-stu-id="b1931-104">To make a connection to a network resource described by a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure, an application can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a), or the [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) function.</span></span> <span data-ttu-id="b1931-105">Nell'esempio seguente viene illustrato l'utilizzo della funzione **WNetAddConnection2** .</span><span class="sxs-lookup"><span data-stu-id="b1931-105">The following example demonstrates use of the **WNetAddConnection2** function.</span></span>

<span data-ttu-id="b1931-106">Nell'esempio di codice viene chiamata la funzione **WNetAddConnection2** , specificando che il sistema deve aggiornare il profilo dell'utente con le informazioni, creando una connessione "memorizzata" o permanente.</span><span class="sxs-lookup"><span data-stu-id="b1931-106">The code sample calls the **WNetAddConnection2** function, specifying that the system should update the user's profile with the information, creating a "remembered" or persistent connection.</span></span> <span data-ttu-id="b1931-107">Nell'esempio viene chiamato un gestore degli errori definito dall'applicazione per elaborare gli errori e la funzione di [**testo**](/windows/desktop/api/wingdi/nf-wingdi-textouta) per la stampa.</span><span class="sxs-lookup"><span data-stu-id="b1931-107">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



<span data-ttu-id="b1931-108">La funzione [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) è supportata per la compatibilità con le versioni precedenti di Windows per gruppi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b1931-108">The [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="b1931-109">Le nuove applicazioni devono chiamare la funzione [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) o la funzione [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) .</span><span class="sxs-lookup"><span data-stu-id="b1931-109">New applications should call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function.</span></span>

<span data-ttu-id="b1931-110">Per ulteriori informazioni sull'utilizzo di un gestore degli errori definito dall'applicazione, vedere [recupero degli errori di rete](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b1931-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 