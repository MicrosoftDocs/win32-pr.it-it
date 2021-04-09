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
# <a name="modifying-the-acls-of-an-object-in-c"></a><span data-ttu-id="3e10b-103">Modifica degli ACL di un oggetto in C++</span><span class="sxs-lookup"><span data-stu-id="3e10b-103">Modifying the ACLs of an Object in C++</span></span>

<span data-ttu-id="3e10b-104">Nell'esempio seguente viene aggiunta una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) all'elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e10b-104">The following example adds an [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) to the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of an object.</span></span>

<span data-ttu-id="3e10b-105">Il parametro *AccessMode* determina il tipo di nuova voce ACE e il modo in cui la nuova voce ACE viene combinata con le voci ACE esistenti per il trustee specificato.</span><span class="sxs-lookup"><span data-stu-id="3e10b-105">The *AccessMode* parameter determines the type of new ACE and how the new ACE is combined with any existing ACEs for the specified trustee.</span></span> <span data-ttu-id="3e10b-106">Usare i \_ flag Concedi accesso, imposta \_ accesso, Nega \_ accesso o revoca accesso \_ nel parametro *AccessMode* .</span><span class="sxs-lookup"><span data-stu-id="3e10b-106">Use the GRANT\_ACCESS, SET\_ACCESS, DENY\_ACCESS, or REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="3e10b-107">Per informazioni su questi flag, vedere [**\_ modalità di accesso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span><span class="sxs-lookup"><span data-stu-id="3e10b-107">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="3e10b-108">È possibile usare codice simile per lavorare con un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="3e10b-108">Similar code can be used to work with a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="3e10b-109">Specificare le \_ informazioni di sicurezza SACL \_ nelle funzioni [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per ottenere e impostare il SACL per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e10b-109">Specify SACL\_SECURITY\_INFORMATION in the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) and [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions to get and set the SACL for the object.</span></span> <span data-ttu-id="3e10b-110">Usare i \_ flag set audit \_ Success, set \_ Audit \_ Failure e REVOKE \_ Access nel parametro *AccessMode* .</span><span class="sxs-lookup"><span data-stu-id="3e10b-110">Use the SET\_AUDIT\_SUCCESS, SET\_AUDIT\_FAILURE, and REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="3e10b-111">Per informazioni su questi flag, vedere [**\_ modalità di accesso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span><span class="sxs-lookup"><span data-stu-id="3e10b-111">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="3e10b-112">Utilizzare questo codice per aggiungere una [voce ACE specifica dell'oggetto](object-specific-aces.md) all'elenco DACL di un oggetto servizio di directory.</span><span class="sxs-lookup"><span data-stu-id="3e10b-112">Use this code to add an [object-specific ACE](object-specific-aces.md) to the DACL of a directory service object.</span></span> <span data-ttu-id="3e10b-113">Per specificare i GUID in una voce ACE specifica dell'oggetto, impostare il parametro *TrusteeForm* su trustee \_ è \_ Objects \_ e \_ Name o trustee \_ è \_ Objects \_ e \_ SID e impostare il parametro *pszTrustee* in modo che sia un puntatore a [**oggetti, \_ \_ nome**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) o [**oggetti e struttura \_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) .</span><span class="sxs-lookup"><span data-stu-id="3e10b-113">To specify the GUIDs in an object-specific ACE, set the *TrusteeForm* parameter to TRUSTEE\_IS\_OBJECTS\_AND\_NAME or TRUSTEE\_IS\_OBJECTS\_AND\_SID and set the *pszTrustee* parameter to be a pointer to an [**OBJECTS\_AND\_NAME**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) or [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure.</span></span>

<span data-ttu-id="3e10b-114">In questo esempio viene utilizzata la funzione [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per ottenere l'elenco DACL esistente.</span><span class="sxs-lookup"><span data-stu-id="3e10b-114">This example uses the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) function to get the existing DACL.</span></span> <span data-ttu-id="3e10b-115">Quindi compila una struttura di [**\_ accesso esplicita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con le informazioni su una voce ACE e usa la funzione [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per unire la nuova voce ACE con le voci ACE esistenti nell'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="3e10b-115">Then it fills an [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure with information about an ACE and uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to merge the new ACE with any existing ACEs in the DACL.</span></span> <span data-ttu-id="3e10b-116">Infine, nell'esempio viene chiamata la funzione [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per alleghi il nuovo DACL al [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e10b-116">Finally, the example calls the [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) function to attach the new DACL to the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the object.</span></span>


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



 

 
