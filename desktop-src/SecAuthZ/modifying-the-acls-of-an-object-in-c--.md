---
description: Nell'esempio seguente viene aggiunta una voce di controllo di accesso (ACE) all'elenco di controllo di accesso discrezionale (DACL) di un oggetto.
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Modifica degli ACL di un oggetto in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21195b1164ce949d1305f0c1748d24b0dbb7525b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968288"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a>Modifica degli ACL di un oggetto in C++

Nell'esempio seguente viene aggiunta una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) all'elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di un oggetto.

Il parametro *AccessMode* determina il tipo di nuova voce ACE e il modo in cui la nuova voce ACE viene combinata con le voci ACE esistenti per il trustee specificato. Usare i \_ flag Concedi accesso, imposta \_ accesso, Nega \_ accesso o revoca accesso \_ nel parametro *AccessMode* . Per informazioni su questi flag, vedere [**\_ modalità di accesso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

È possibile usare codice simile per lavorare con un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Specificare le \_ informazioni di sicurezza SACL \_ nelle funzioni [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per ottenere e impostare il SACL per l'oggetto. Usare i \_ flag set audit \_ Success, set \_ Audit \_ Failure e REVOKE \_ Access nel parametro *AccessMode* . Per informazioni su questi flag, vedere [**\_ modalità di accesso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Utilizzare questo codice per aggiungere una [voce ACE specifica dell'oggetto](object-specific-aces.md) all'elenco DACL di un oggetto servizio di directory. Per specificare i GUID in una voce ACE specifica dell'oggetto, impostare il parametro *TrusteeForm* su trustee \_ è \_ Objects \_ e \_ Name o trustee \_ è \_ Objects \_ e \_ SID e impostare il parametro *pszTrustee* in modo che sia un puntatore a [**oggetti, \_ \_ nome**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) o [**oggetti e struttura \_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) .

In questo esempio viene utilizzata la funzione [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per ottenere l'elenco DACL esistente. Quindi compila una struttura di [**\_ accesso esplicita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con le informazioni su una voce ACE e usa la funzione [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per unire la nuova voce ACE con le voci ACE esistenti nell'elenco DACL. Infine, nell'esempio viene chiamata la funzione [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per alleghi il nuovo DACL al [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) dell'oggetto.


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



 

 
