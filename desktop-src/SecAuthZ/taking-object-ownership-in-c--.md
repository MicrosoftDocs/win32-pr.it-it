---
description: Nell'esempio seguente si tenta di modificare l'elenco DACL di un oggetto file assumendo la proprietà di tale oggetto.
ms.assetid: 0b309ac9-177d-425f-8b78-71fe73e41979
title: Proprietà degli oggetti in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fba581c449309dcfbfaeba6ca207b58f26f966088e43b99717bbd4fb89323f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413301"
---
# <a name="taking-object-ownership-in-c"></a>Proprietà degli oggetti in C++

Nell'esempio seguente si tenta di modificare l'elenco DACL di un oggetto file assumendo la proprietà di tale oggetto. Questa operazione avrà esito positivo solo se il chiamante dispone dell'accesso DAC WRITE all'oggetto o \_ è il proprietario dell'oggetto. Se il tentativo iniziale di modificare l'elenco DACL ha esito negativo, un amministratore può assumere la proprietà dell'oggetto. Per assegnare la proprietà all'amministratore, l'esempio abilita il privilegio edizione Standard TAKE OWNERSHIP NAME nel token di accesso del chiamante e imposta il gruppo Administrators del sistema locale come proprietario \_ \_ \_ dell'oggetto. [](/windows/desktop/SecGloss/a-gly) Se il chiamante è membro del gruppo Administrators, il codice sarà in grado di modificare l'elenco DACL dell'oggetto.

Per abilitare e disabilitare i privilegi, in questo esempio viene utilizzata la funzione di esempio SetPrivilege descritta in Abilitazione e disabilitazione [dei privilegi in C++.](enabling-and-disabling-privileges-in-c--.md)


```C++
#include <windows.h>
#include <stdio.h>
#include <accctrl.h>
#include <aclapi.h>

//Forward declaration of SetPrivilege
BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) ;


BOOL TakeOwnership(LPTSTR lpszOwnFile) 
{

    BOOL bRetval = FALSE;

    HANDLE hToken = NULL; 
    PSID pSIDAdmin = NULL;
    PSID pSIDEveryone = NULL;
    PACL pACL = NULL;
    SID_IDENTIFIER_AUTHORITY SIDAuthWorld =
            SECURITY_WORLD_SID_AUTHORITY;
    SID_IDENTIFIER_AUTHORITY SIDAuthNT = SECURITY_NT_AUTHORITY;
    const int NUM_ACES  = 2;
    EXPLICIT_ACCESS ea[NUM_ACES];
    DWORD dwRes;

    // Specify the DACL to use.
    // Create a SID for the Everyone group.
    if (!AllocateAndInitializeSid(&SIDAuthWorld, 1,
                     SECURITY_WORLD_RID,
                     0,
                     0, 0, 0, 0, 0, 0,
                     &pSIDEveryone)) 
    {
        printf("AllocateAndInitializeSid (Everyone) error %u\n",
                GetLastError());
        goto Cleanup;
    }

    // Create a SID for the BUILTIN\Administrators group.
    if (!AllocateAndInitializeSid(&SIDAuthNT, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pSIDAdmin)) 
    {
        printf("AllocateAndInitializeSid (Admin) error %u\n",
                GetLastError());
        goto Cleanup;
    }

    ZeroMemory(&ea, NUM_ACES * sizeof(EXPLICIT_ACCESS));

    // Set read access for Everyone.
    ea[0].grfAccessPermissions = GENERIC_READ;
    ea[0].grfAccessMode = SET_ACCESS;
    ea[0].grfInheritance = NO_INHERITANCE;
    ea[0].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[0].Trustee.TrusteeType = TRUSTEE_IS_WELL_KNOWN_GROUP;
    ea[0].Trustee.ptstrName = (LPTSTR) pSIDEveryone;

    // Set full control for Administrators.
    ea[1].grfAccessPermissions = GENERIC_ALL;
    ea[1].grfAccessMode = SET_ACCESS;
    ea[1].grfInheritance = NO_INHERITANCE;
    ea[1].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[1].Trustee.TrusteeType = TRUSTEE_IS_GROUP;
    ea[1].Trustee.ptstrName = (LPTSTR) pSIDAdmin;

    if (ERROR_SUCCESS != SetEntriesInAcl(NUM_ACES,
                                         ea,
                                         NULL,
                                         &pACL))
    {
        printf("Failed SetEntriesInAcl\n");
        goto Cleanup;
    }

    // Try to modify the object's DACL.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        DACL_SECURITY_INFORMATION,   // change only the object's DACL
        NULL, NULL,                  // do not change owner or group
        pACL,                        // DACL specified
        NULL);                       // do not change SACL

    if (ERROR_SUCCESS == dwRes) 
    {
        printf("Successfully changed DACL\n");
        bRetval = TRUE;
        // No more processing needed.
        goto Cleanup;
    }
    if (dwRes != ERROR_ACCESS_DENIED)
    {
        printf("First SetNamedSecurityInfo call failed: %u\n",
                dwRes); 
        goto Cleanup;
    }

    // If the preceding call failed because access was denied, 
    // enable the SE_TAKE_OWNERSHIP_NAME privilege, create a SID for 
    // the Administrators group, take ownership of the object, and 
    // disable the privilege. Then try again to set the object's DACL.

    // Open a handle to the access token for the calling process.
    if (!OpenProcessToken(GetCurrentProcess(), 
                          TOKEN_ADJUST_PRIVILEGES, 
                          &hToken)) 
       {
          printf("OpenProcessToken failed: %u\n", GetLastError()); 
          goto Cleanup; 
       } 

    // Enable the SE_TAKE_OWNERSHIP_NAME privilege.
    if (!SetPrivilege(hToken, SE_TAKE_OWNERSHIP_NAME, TRUE)) 
    {
        printf("You must be logged on as Administrator.\n");
        goto Cleanup; 
    }

    // Set the owner in the object's security descriptor.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        OWNER_SECURITY_INFORMATION,  // change only the object's owner
        pSIDAdmin,                   // SID of Administrator group
        NULL,
        NULL,
        NULL); 

    if (dwRes != ERROR_SUCCESS) 
    {
        printf("Could not set owner. Error: %u\n", dwRes); 
        goto Cleanup;
    }
        
    // Disable the SE_TAKE_OWNERSHIP_NAME privilege.
    if (!SetPrivilege(hToken, SE_TAKE_OWNERSHIP_NAME, FALSE)) 
    {
        printf("Failed SetPrivilege call unexpectedly.\n");
        goto Cleanup;
    }

    // Try again to modify the object's DACL,
    // now that we are the owner.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        DACL_SECURITY_INFORMATION,   // change only the object's DACL
        NULL, NULL,                  // do not change owner or group
        pACL,                        // DACL specified
        NULL);                       // do not change SACL

    if (dwRes == ERROR_SUCCESS)
    {
        printf("Successfully changed DACL\n");
        bRetval = TRUE; 
    }
    else
    {
        printf("Second SetNamedSecurityInfo call failed: %u\n",
                dwRes); 
    }

Cleanup:

    if (pSIDAdmin)
        FreeSid(pSIDAdmin); 

    if (pSIDEveryone)
        FreeSid(pSIDEveryone); 

    if (pACL)
       LocalFree(pACL);

    if (hToken)
       CloseHandle(hToken);

    return bRetval;

}
```



 

 
