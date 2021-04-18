---
title: Ricerca del nome completo di un utente
description: I computer possono essere organizzati in un dominio, ovvero una raccolta di rete di computer. L'amministratore di dominio mantiene le informazioni sugli account utente e di gruppo centralizzati.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2daa6bc2bc7d7255e961537c641a999d5a0bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298305"
---
# <a name="looking-up-a-users-full-name"></a><span data-ttu-id="dea7f-104">Ricerca del nome completo di un utente</span><span class="sxs-lookup"><span data-stu-id="dea7f-104">Looking Up a User's Full Name</span></span>

<span data-ttu-id="dea7f-105">I computer possono essere organizzati in un *dominio*, ovvero una raccolta di rete di computer.</span><span class="sxs-lookup"><span data-stu-id="dea7f-105">Computers can be organized into a *domain*, which is a collection of computers network.</span></span> <span data-ttu-id="dea7f-106">L'amministratore di dominio mantiene le informazioni sugli account utente e di gruppo centralizzati.</span><span class="sxs-lookup"><span data-stu-id="dea7f-106">The domain administrator maintains centralized user and group account information.</span></span>

<span data-ttu-id="dea7f-107">Per trovare il nome completo di un utente, in base al nome utente e al nome di dominio:</span><span class="sxs-lookup"><span data-stu-id="dea7f-107">To find the full name of a user, given the user name and domain name:</span></span>

-   <span data-ttu-id="dea7f-108">Convertire il nome utente e il nome di dominio in Unicode, se non sono già stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="dea7f-108">Convert the user name and domain name to Unicode, if they are not already Unicode strings.</span></span>
-   <span data-ttu-id="dea7f-109">Cercare il nome del computer del controller di dominio chiamando [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span><span class="sxs-lookup"><span data-stu-id="dea7f-109">Look up the computer name of the domain controller (DC) by calling [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span></span>
-   <span data-ttu-id="dea7f-110">Cercare il nome utente nel computer DC chiamando [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span><span class="sxs-lookup"><span data-stu-id="dea7f-110">Look up the user name on the DC computer by calling [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span></span>
-   <span data-ttu-id="dea7f-111">Convertire il nome utente completo in ANSI, a meno che il programma non sia in attesa di utilizzare stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="dea7f-111">Convert the full user name to ANSI, unless the program is expecting to work with Unicode strings.</span></span>

<span data-ttu-id="dea7f-112">Il codice di esempio seguente è una funzione (getcompletename) che accetta un nome utente e un nome di dominio nei primi due argomenti e restituisce il nome completo dell'utente nel terzo argomento.</span><span class="sxs-lookup"><span data-stu-id="dea7f-112">The following sample code is a function (GetFullName) that takes a user name and a domain name in the first two arguments and returns the user's full name in the third argument.</span></span>


```C++
#include <windows.h>
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

BOOL GetFullName( char *UserName, char *Domain, char *dest )
{
    WCHAR wszUserName[UNLEN+1];          // Unicode user name
    WCHAR wszDomain[256]; 
    LPBYTE ComputerName;
    
//    struct _SERVER_INFO_100 *si100;  // Server structure
    struct _USER_INFO_2 *ui;         // User structure

// Convert ANSI user name and domain to Unicode

    MultiByteToWideChar( CP_ACP, 0, UserName,
        (int) strlen(UserName)+1, wszUserName, 
        sizeof(wszUserName)/sizeof(WCHAR) );

    MultiByteToWideChar( CP_ACP, 0, Domain,
        (int) strlen(Domain)+1, wszDomain, 
        sizeof(wszDomain)/sizeof(WCHAR) );

// Get the computer name of a DC for the domain.

    NetGetDCName( NULL, wszDomain, &ComputerName );

// Look up the user on the DC.

    if( NetUserGetInfo( (LPWSTR) ComputerName,
        (LPWSTR) &wszUserName, 2, (LPBYTE *) &ui ) )
    {
        wprintf( L"Error getting user information.\n" );
        return( FALSE );
    }

// Convert the Unicode full name to ANSI.

    WideCharToMultiByte( CP_ACP, 0, ui->usri2_full_name, -1,
        dest, 256, NULL, NULL );

    return (TRUE);
}
```



 

 




