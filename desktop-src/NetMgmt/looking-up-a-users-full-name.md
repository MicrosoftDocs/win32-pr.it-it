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
# <a name="looking-up-a-users-full-name"></a>Ricerca del nome completo di un utente

I computer possono essere organizzati in un *dominio*, ovvero una raccolta di rete di computer. L'amministratore di dominio mantiene le informazioni sugli account utente e di gruppo centralizzati.

Per trovare il nome completo di un utente, in base al nome utente e al nome di dominio:

-   Convertire il nome utente e il nome di dominio in Unicode, se non sono già stringhe Unicode.
-   Cercare il nome del computer del controller di dominio chiamando [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).
-   Cercare il nome utente nel computer DC chiamando [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).
-   Convertire il nome utente completo in ANSI, a meno che il programma non sia in attesa di utilizzare stringhe Unicode.

Il codice di esempio seguente è una funzione (getcompletename) che accetta un nome utente e un nome di dominio nei primi due argomenti e restituisce il nome completo dell'utente nel terzo argomento.


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



 

 




