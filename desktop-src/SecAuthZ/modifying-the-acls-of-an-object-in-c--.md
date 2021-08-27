---
description: Nell'esempio seguente viene aggiunta una voce di controllo di accesso (ACE) all'elenco di controllo di accesso discrezionale (DACL) di un oggetto .
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Modifica degli ACL di un oggetto in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42681a22e6b5f4b478d55d21f9b0b71dbe3f9c081ef5d18ba3da7a33f8709d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912461"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a>Modifica degli ACL di un oggetto in C++

Nell'esempio seguente viene aggiunta [*una voce*](/windows/desktop/SecGloss/a-gly) di controllo di accesso (ACE) all'elenco di controllo di accesso discrezionale (DACL) di un oggetto . [](/windows/desktop/SecGloss/d-gly)

Il *parametro AccessMode* determina il tipo di nuova ACE e il modo in cui la nuova ACE viene combinata con qualsiasi ACE esistente per il fiduciare specificato. Usare i flag GRANT \_ ACCESS, SET ACCESS, DENY ACCESS o \_ REVOKE ACCESS nel parametro \_ \_ *AccessMode.* Per informazioni su questi flag, vedere [**MODALITÀ \_ DI ACCESSO**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Codice simile può essere usato per usare un elenco [*di controllo di accesso*](/windows/desktop/SecGloss/s-gly) di sistema (SACL). Specificare SACL \_ SECURITY INFORMATION nelle funzioni \_ [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per ottenere e impostare il SACL per l'oggetto. Usare i flag SET AUDIT SUCCESS, SET AUDIT FAILURE e \_ REVOKE ACCESS nel parametro \_ \_ \_ \_ *AccessMode.* Per informazioni su questi flag, vedere [**MODALITÀ \_ DI ACCESSO**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Usare questo codice per aggiungere una [ACE specifica dell'oggetto](object-specific-aces.md) all'elenco DACL di un oggetto del servizio directory. Per specificare i GUID in una ACE specifica dell'oggetto, impostare il parametro *TrusteeForm* su TRUSTEE IS OBJECTS AND NAME o TRUSTEE IS OBJECTS AND SID e impostare il parametro \_ \_ \_ \_ \_ \_ \_ \_ *pszTrustee* [**\_ \_**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) [**\_ \_**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) come puntatore a una struttura OBJECTS AND NAME o OBJECTS AND SID.

In questo esempio viene utilizzata [**la funzione GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per ottenere l'elenco DACL esistente. Quindi riempie una struttura [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con informazioni su una voce ACE e usa la [**funzione SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per unire la nuova voce ACE con tutte le voci ACE esistenti nell'elenco DACL. Infine, nell'esempio viene chiamata la [**funzione SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per collegare il nuovo elenco DACL al [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) dell'oggetto .


```C++
#include <windows.h>
#include <stdio.h>

DWORD AddAceToObjectsSecurityDescriptor (
    LPTSTR pszObjName,          // name of object
    SE_OBJECT_TYPE ObjectType,  // type of object
    LPTSTR pszTrustee,          // trustee for new ACE
    TRUSTEE_FORM TrusteeForm,   // format of trustee structure
    DWORD dwAccessRights,       // access mask for new ACE
    ACCESS_MODE AccessMode,     // type of ACE
    DWORD dwInheritance         // inheritance flags for new ACE
) 
{
    DWORD dwRes = 0;
    PACL pOldDACL = NULL, pNewDACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea;

    if (NULL == pszObjName) 
        return ERROR_INVALID_PARAMETER;

    // Get a pointer to the existing DACL.

    dwRes = GetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, &pOldDACL, NULL, &pSD);
    if (ERROR_SUCCESS != dwRes) {
        printf( "GetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Initialize an EXPLICIT_ACCESS structure for the new ACE. 

    ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
    ea.grfAccessPermissions = dwAccessRights;
    ea.grfAccessMode = AccessMode;
    ea.grfInheritance= dwInheritance;
    ea.Trustee.TrusteeForm = TrusteeForm;
    ea.Trustee.ptstrName = pszTrustee;

    // Create a new ACL that merges the new ACE
    // into the existing DACL.

    dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetEntriesInAcl Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Attach the new ACL as the object's DACL.

    dwRes = SetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, pNewDACL, NULL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    Cleanup:

        if(pSD != NULL) 
            LocalFree((HLOCAL) pSD); 
        if(pNewDACL != NULL) 
            LocalFree((HLOCAL) pNewDACL); 

        return dwRes;
}

```



 

 
