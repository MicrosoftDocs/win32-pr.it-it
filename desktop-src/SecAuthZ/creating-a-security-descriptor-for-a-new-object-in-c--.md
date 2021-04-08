---
description: Nell'esempio seguente viene creato un descrittore di sicurezza per una nuova chiave del registro di sistema utilizzando il processo seguente. È possibile utilizzare codice simile per creare un descrittore di sicurezza per altri tipi di oggetto.
ms.assetid: 866992a7-95c4-4094-87bb-e6d8eeb24317
title: Creazione di un descrittore di sicurezza per un nuovo oggetto in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17687b60999bc4e6828c9769eec32ec4ce5afb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879897"
---
# <a name="creating-a-security-descriptor-for-a-new-object-in-c"></a><span data-ttu-id="fd517-104">Creazione di un descrittore di sicurezza per un nuovo oggetto in C++</span><span class="sxs-lookup"><span data-stu-id="fd517-104">Creating a Security Descriptor for a New Object in C++</span></span>

<span data-ttu-id="fd517-105">Nell'esempio seguente viene creato un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) per una nuova chiave del registro di sistema utilizzando il processo seguente.</span><span class="sxs-lookup"><span data-stu-id="fd517-105">The following example creates a [*security descriptor*](/windows/desktop/SecGloss/s-gly) for a new registry key using the following process.</span></span> <span data-ttu-id="fd517-106">È possibile utilizzare codice simile per creare un descrittore di sicurezza per altri tipi di oggetto.</span><span class="sxs-lookup"><span data-stu-id="fd517-106">Similar code can be used to create a security descriptor for other object types.</span></span>

-   <span data-ttu-id="fd517-107">Nell'esempio viene riempita una matrice di strutture di [**\_ accesso esplicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con le informazioni per due voci ACE.</span><span class="sxs-lookup"><span data-stu-id="fd517-107">The example fills an array of [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structures with the information for two ACEs.</span></span> <span data-ttu-id="fd517-108">Una voce ACE consente l'accesso in lettura a tutti gli utenti. l'altra voce ACE consente l'accesso completo agli amministratori.</span><span class="sxs-lookup"><span data-stu-id="fd517-108">One ACE allows read access to everyone; the other ACE allows full access to administrators.</span></span>
-   <span data-ttu-id="fd517-109">La matrice di [**\_ accesso esplicita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) viene passata alla funzione [**SETENTRIESINACL**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per creare un DACL per il descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fd517-109">The [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) array is passed to the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to create a DACL for the security descriptor.</span></span>
-   <span data-ttu-id="fd517-110">Dopo l'allocazione della memoria per il descrittore di sicurezza, nell'esempio vengono chiamate le funzioni [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) e [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) per inizializzare il descrittore di sicurezza e il relativo DACL.</span><span class="sxs-lookup"><span data-stu-id="fd517-110">After allocating memory for the security descriptor, the example calls the [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) and [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) functions to initialize the security descriptor and attach the DACL.</span></span>
-   <span data-ttu-id="fd517-111">Il descrittore di sicurezza viene quindi archiviato in una struttura di attributi di sicurezza \_ e passato alla funzione [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa) , che connette il descrittore di sicurezza alla chiave appena creata.</span><span class="sxs-lookup"><span data-stu-id="fd517-111">The security descriptor is then stored in a SECURITY\_ATTRIBUTES structure and passed to the [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa) function, which attaches the security descriptor to the newly created key.</span></span>


```C++
#pragma comment(lib, "advapi32.lib")

#include <windows.h>
#include <stdio.h>
#include <aclapi.h>
#include <tchar.h>

void main()
{

    DWORD dwRes, dwDisposition;
    PSID pEveryoneSID = NULL, pAdminSID = NULL;
    PACL pACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea[2];
    SID_IDENTIFIER_AUTHORITY SIDAuthWorld =
            SECURITY_WORLD_SID_AUTHORITY;
    SID_IDENTIFIER_AUTHORITY SIDAuthNT = SECURITY_NT_AUTHORITY;
    SECURITY_ATTRIBUTES sa;
    LONG lRes;
    HKEY hkSub = NULL;

    // Create a well-known SID for the Everyone group.
    if(!AllocateAndInitializeSid(&SIDAuthWorld, 1,
                     SECURITY_WORLD_RID,
                     0, 0, 0, 0, 0, 0, 0,
                     &pEveryoneSID))
    {
        _tprintf(_T("AllocateAndInitializeSid Error %u\n"), GetLastError());
        goto Cleanup;
    }

    // Initialize an EXPLICIT_ACCESS structure for an ACE.
    // The ACE will allow Everyone read access to the key.
    ZeroMemory(&ea, 2 * sizeof(EXPLICIT_ACCESS));
    ea[0].grfAccessPermissions = KEY_READ;
    ea[0].grfAccessMode = SET_ACCESS;
    ea[0].grfInheritance= NO_INHERITANCE;
    ea[0].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[0].Trustee.TrusteeType = TRUSTEE_IS_WELL_KNOWN_GROUP;
    ea[0].Trustee.ptstrName  = (LPTSTR) pEveryoneSID;

    // Create a SID for the BUILTIN\Administrators group.
    if(! AllocateAndInitializeSid(&SIDAuthNT, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pAdminSID)) 
    {
        _tprintf(_T("AllocateAndInitializeSid Error %u\n"), GetLastError());
        goto Cleanup; 
    }

    // Initialize an EXPLICIT_ACCESS structure for an ACE.
    // The ACE will allow the Administrators group full access to
    // the key.
    ea[1].grfAccessPermissions = KEY_ALL_ACCESS;
    ea[1].grfAccessMode = SET_ACCESS;
    ea[1].grfInheritance= NO_INHERITANCE;
    ea[1].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[1].Trustee.TrusteeType = TRUSTEE_IS_GROUP;
    ea[1].Trustee.ptstrName  = (LPTSTR) pAdminSID;

    // Create a new ACL that contains the new ACEs.
    dwRes = SetEntriesInAcl(2, ea, NULL, &pACL);
    if (ERROR_SUCCESS != dwRes) 
    {
        _tprintf(_T("SetEntriesInAcl Error %u\n"), GetLastError());
        goto Cleanup;
    }

    // Initialize a security descriptor.  
    pSD = (PSECURITY_DESCRIPTOR) LocalAlloc(LPTR, 
                             SECURITY_DESCRIPTOR_MIN_LENGTH); 
    if (NULL == pSD) 
    { 
        _tprintf(_T("LocalAlloc Error %u\n"), GetLastError());
        goto Cleanup; 
    } 
 
    if (!InitializeSecurityDescriptor(pSD,
            SECURITY_DESCRIPTOR_REVISION)) 
    {  
        _tprintf(_T("InitializeSecurityDescriptor Error %u\n"),
                                GetLastError());
        goto Cleanup; 
    } 
 
    // Add the ACL to the security descriptor. 
    if (!SetSecurityDescriptorDacl(pSD, 
            TRUE,     // bDaclPresent flag   
            pACL, 
            FALSE))   // not a default DACL 
    {  
        _tprintf(_T("SetSecurityDescriptorDacl Error %u\n"),
                GetLastError());
        goto Cleanup; 
    } 

    // Initialize a security attributes structure.
    sa.nLength = sizeof (SECURITY_ATTRIBUTES);
    sa.lpSecurityDescriptor = pSD;
    sa.bInheritHandle = FALSE;

    // Use the security attributes to set the security descriptor 
    // when you create a key.
    lRes = RegCreateKeyEx(HKEY_CURRENT_USER, _T("mykey"), 0, _T(""), 0, 
            KEY_READ | KEY_WRITE, &sa, &hkSub, &dwDisposition); 
    _tprintf(_T("RegCreateKeyEx result %u\n"), lRes );

Cleanup:

    if (pEveryoneSID) 
        FreeSid(pEveryoneSID);
    if (pAdminSID) 
        FreeSid(pAdminSID);
    if (pACL) 
        LocalFree(pACL);
    if (pSD) 
        LocalFree(pSD);
    if (hkSub) 
        RegCloseKey(hkSub);

    return;

}
```



 

 
