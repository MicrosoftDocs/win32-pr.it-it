---
title: Forzare l'utente a modificare la password di accesso
description: Questo esempio di codice illustra come forzare un utente a modificare la password di accesso all'accesso successivo usando le funzioni NetUserGetInfo e NetUserSetInfo e la \_ struttura User info \_ 3.
ms.assetid: 828f5d72-3e19-4b65-a1db-ac702fd4cfde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3d0910f77c2553a55a53f1393aae5c9535982
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856318"
---
# <a name="forcing-a-user-to-change-the-logon-password"></a>Forzare l'utente a modificare la password di accesso

Questo esempio di codice illustra come forzare un utente a modificare la password di accesso all'accesso successivo usando le funzioni [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) e [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) e la struttura [**User \_ info \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3) . Si noti che a partire da Windows XP, è consigliabile usare invece la struttura [**User \_ info \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4) .

Impostare il membro **usri3 \_ password \_ scaduta** della struttura **User \_ info \_ 3** su un valore diverso da zero usando il frammento di codice seguente:


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <stdio.h>
#include <lm.h>

#pragma comment(lib, "netapi32.lib")

#define USERNAME L"your_user_name"
#define SERVER L"\\\\server"

void main( void )
{
    PUSER_INFO_3 pUsr = NULL;
    NET_API_STATUS netRet = 0;
    DWORD dwParmError = 0;
 //
 // First, retrieve the user information at level 3. This is 
 // necessary to prevent resetting other user information when 
 // the NetUserSetInfo call is made.
 //
   netRet = NetUserGetInfo( SERVER, USERNAME, 3, (LPBYTE *)&pUsr);

   if( netRet == NERR_Success )
   {
     //
     // The function was successful; set the usri3_password_expired value to 
     // a nonzero value. Call the NetUserSetInfo function.
     //
        pUsr->usri3_password_expired = TRUE;
        netRet = NetUserSetInfo( SERVER, USERNAME, 3, (LPBYTE)pUsr, &dwParmError);
    //
    // A zero return indicates success. 
    // If the return value is ERROR_INVALID_PARAMETER, 
    //  the dwParmError parameter will contain a value indicating the 
    //  invalid parameter within the user_info_3 structure. These values 
    //  are defined in the lmaccess.h file.
    //
        if( netRet == NERR_Success )
            printf("User %S will need to change password at next logon", USERNAME);
        else printf("Error %d occurred. Parm Error %d returned.\n", netRet, dwParmError);
    //
    // Must free the buffer returned by NetUserGetInfo.
    //
        NetApiBufferFree( pUsr);
    }
    else printf("NetUserGetInfo failed: %d\n", netRet);
}
```



 

 




