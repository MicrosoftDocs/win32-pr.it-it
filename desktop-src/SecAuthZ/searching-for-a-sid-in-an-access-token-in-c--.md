---
description: Nell'esempio seguente vengono usate le funzioni OpenProcessToken e GetTokenInformation per ottenere l'appartenenza a un gruppo in un token di accesso.
ms.assetid: f895dfef-75ad-419c-95d0-6480bdf9c769
title: Ricerca di un SID in un token di accesso in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713f69511f780898641e65f22503e595706307ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308137"
---
# <a name="searching-for-a-sid-in-an-access-token-in-c"></a>Ricerca di un SID in un token di accesso in C++

Nell'esempio seguente vengono usate le funzioni [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) e [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) per ottenere l'appartenenza a un gruppo in un [*token di accesso*](/windows/desktop/SecGloss/a-gly). USA quindi la funzione [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) per creare un SID che identifichi il SID noto del gruppo Administrator per il computer locale. USA quindi la funzione [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) per confrontare il SID noto con i SID del gruppo dal token di accesso. Se il SID è presente nel token, la funzione controlla gli attributi del SID per determinare se è abilitato.

La funzione [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) deve essere utilizzata per determinare se un SID specificato è presente e abilitato in un token di accesso. Questa funzione Elimina le potenziali interpretazioni errate dell'appartenenza al gruppo attivo.


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "advapi32.lib")

#define MAX_NAME 256

BOOL SearchTokenGroupsForSID (VOID) 
{
    DWORD i, dwSize = 0, dwResult = 0;
    HANDLE hToken;
    PTOKEN_GROUPS pGroupInfo;
    SID_NAME_USE SidType;
    char lpName[MAX_NAME];
    char lpDomain[MAX_NAME];
    PSID pSID = NULL;
    SID_IDENTIFIER_AUTHORITY SIDAuth = SECURITY_NT_AUTHORITY;
       
    // Open a handle to the access token for the calling process.

    if (!OpenProcessToken( GetCurrentProcess(), TOKEN_QUERY, &hToken )) 
    {
        printf( "OpenProcessToken Error %u\n", GetLastError() );
        return FALSE;
    }

    // Call GetTokenInformation to get the buffer size.

    if(!GetTokenInformation(hToken, TokenGroups, NULL, dwSize, &dwSize)) 
    {
        dwResult = GetLastError();
        if( dwResult != ERROR_INSUFFICIENT_BUFFER ) {
            printf( "GetTokenInformation Error %u\n", dwResult );
            return FALSE;
        }
    }

    // Allocate the buffer.

    pGroupInfo = (PTOKEN_GROUPS) GlobalAlloc( GPTR, dwSize );

    // Call GetTokenInformation again to get the group information.

    if(! GetTokenInformation(hToken, TokenGroups, pGroupInfo, 
                            dwSize, &dwSize ) ) 
    {
        printf( "GetTokenInformation Error %u\n", GetLastError() );
        return FALSE;
    }

    // Create a SID for the BUILTIN\Administrators group.

    if(! AllocateAndInitializeSid( &SIDAuth, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pSID) ) 
    {
        printf( "AllocateAndInitializeSid Error %u\n", GetLastError() );
        return FALSE;
    }

    // Loop through the group SIDs looking for the administrator SID.

    for(i=0; i<pGroupInfo->GroupCount; i++) 
    {
        if ( EqualSid(pSID, pGroupInfo->Groups[i].Sid) ) 
        {

            // Lookup the account name and print it.

            dwSize = MAX_NAME;
            if( !LookupAccountSid( NULL, pGroupInfo->Groups[i].Sid,
                                  lpName, &dwSize, lpDomain, 
                                  &dwSize, &SidType ) ) 
            {
                dwResult = GetLastError();
                if( dwResult == ERROR_NONE_MAPPED )
                   strcpy_s (lpName, dwSize, "NONE_MAPPED" );
                else 
                {
                    printf("LookupAccountSid Error %u\n", GetLastError());
                    return FALSE;
                }
            }
            printf( "Current user is a member of the %s\\%s group\n", 
                    lpDomain, lpName );

            // Find out whether the SID is enabled in the token.
            if (pGroupInfo->Groups[i].Attributes & SE_GROUP_ENABLED)
                printf("The group SID is enabled.\n");
            else if (pGroupInfo->Groups[i].Attributes & 
                              SE_GROUP_USE_FOR_DENY_ONLY)
                printf("The group SID is a deny-only SID.\n");
            else 
                printf("The group SID is not enabled.\n");
        }
    }

    if (pSID)
        FreeSid(pSID);
    if ( pGroupInfo )
        GlobalFree( pGroupInfo );
    return TRUE;
}
```



 

 
