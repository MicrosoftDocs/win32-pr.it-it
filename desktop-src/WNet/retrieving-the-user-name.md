---
title: Recupero del nome utente
description: Per recuperare il nome dell'utente associato a una periferica locale connessa a una risorsa di rete o con il nome di una rete, un'applicazione può chiamare la funzione WNetGetUser.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0aeb8df11187828be0865d6b73e08325f2e0e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223969"
---
# <a name="retrieving-the-user-name"></a><span data-ttu-id="3c7b9-103">Recupero del nome utente</span><span class="sxs-lookup"><span data-stu-id="3c7b9-103">Retrieving the User Name</span></span>

<span data-ttu-id="3c7b9-104">Per recuperare il nome dell'utente associato a una periferica locale connessa a una risorsa di rete o con il nome di una rete, un'applicazione può chiamare la funzione [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="3c7b9-104">To retrieve the name of the user associated either with a local device connected to a network resource or with the name of a network, an application can call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="3c7b9-105">Nell'esempio seguente viene usato il nome del dispositivo per recuperare il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-105">The following example uses the device name to retrieve the name of the user.</span></span> <span data-ttu-id="3c7b9-106">Nell'esempio viene chiamato un gestore degli errori definito dall'applicazione per elaborare gli errori e la funzione di [**testo**](/windows/desktop/api/wingdi/nf-wingdi-textouta) per la stampa.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



<span data-ttu-id="3c7b9-107">Per ulteriori informazioni sull'utilizzo di un gestore degli errori definito dall'applicazione, vedere [recupero degli errori di rete](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3c7b9-107">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 