---
title: Ricerca del nome completo di un utente
description: I computer possono essere organizzati in un dominio, ovvero una raccolta di computer di rete. L'amministratore di dominio gestisce informazioni centralizzate sugli account utente e di gruppo.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdff00483b38ef12355af4dcda4a48d60bf849a8fd5d6829640ae8907e426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012519"
---
# <a name="looking-up-a-users-full-name"></a>Ricerca del nome completo di un utente

I computer possono essere organizzati in *un dominio*, ovvero una raccolta di computer di rete. L'amministratore di dominio gestisce informazioni centralizzate sugli account utente e di gruppo.

Per trovare il nome completo di un utente, in base al nome utente e al nome di dominio:

-   Convertire il nome utente e il nome di dominio in Unicode, se non sono già stringhe Unicode.
-   Cercare il nome del computer del controller di dominio chiamando [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).
-   Cercare il nome utente nel computer del controller di dominio chiamando [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).
-   Convertire il nome utente completo in ANSI, a meno che il programma non si aspetti di usare stringhe Unicode.

Il codice di esempio seguente è una funzione (GetFullName) che accetta un nome utente e un nome di dominio nei primi due argomenti e restituisce il nome completo dell'utente nel terzo argomento.


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



 

 




