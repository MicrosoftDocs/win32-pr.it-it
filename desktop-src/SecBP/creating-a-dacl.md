---
description: Viene illustrato come creare correttamente un DACL.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Creazione di un DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf8213f6fbb4e2a885655b47437ec464337ea13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884862"
---
# <a name="creating-a-dacl"></a><span data-ttu-id="2f067-103">Creazione di un DACL</span><span class="sxs-lookup"><span data-stu-id="2f067-103">Creating a DACL</span></span>

<span data-ttu-id="2f067-104">La creazione di un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) appropriato è una parte essenziale e importante dello sviluppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2f067-104">Creating a proper [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) is a necessary and important part of application development.</span></span> <span data-ttu-id="2f067-105">Poiché un DACL **null** consente tutti i tipi di accesso a tutti gli utenti, non usare DACL **null** .</span><span class="sxs-lookup"><span data-stu-id="2f067-105">Because a **NULL** DACL permits all types of access to all users, do not use **NULL** DACLs.</span></span>

<span data-ttu-id="2f067-106">Nell'esempio seguente viene illustrato come creare correttamente un DACL.</span><span class="sxs-lookup"><span data-stu-id="2f067-106">The following example shows how to properly create a DACL.</span></span> <span data-ttu-id="2f067-107">Nell'esempio è inclusa una funzione, CreateMyDACL, che utilizza il linguaggio SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ) per definire il controllo di accesso concesso e negato in un DACL.</span><span class="sxs-lookup"><span data-stu-id="2f067-107">The example contains a function, CreateMyDACL, that uses the [security descriptor definition language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) to define the granted and denied access control in a DACL.</span></span> <span data-ttu-id="2f067-108">Per fornire accesso diverso per gli oggetti dell'applicazione, modificare la funzione CreateMyDACL in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2f067-108">To provide different access for your application's objects, modify the CreateMyDACL function as needed.</span></span>

<span data-ttu-id="2f067-109">Nell'esempio:</span><span class="sxs-lookup"><span data-stu-id="2f067-109">In the example:</span></span>

1.  <span data-ttu-id="2f067-110">La funzione Main passa un indirizzo di una struttura di [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) alla funzione CreateMyDACL.</span><span class="sxs-lookup"><span data-stu-id="2f067-110">The main function passes an address of a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to the CreateMyDACL function.</span></span>
2.  <span data-ttu-id="2f067-111">La funzione CreateMyDACL usa le stringhe SDDL per:</span><span class="sxs-lookup"><span data-stu-id="2f067-111">The CreateMyDACL function uses SDDL strings to:</span></span>
    -   <span data-ttu-id="2f067-112">Negare l'accesso agli utenti guest e accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="2f067-112">Deny access to guest and anonymous logon users.</span></span>
    -   <span data-ttu-id="2f067-113">Consente l'accesso in lettura/scrittura/esecuzione agli utenti autenticati.</span><span class="sxs-lookup"><span data-stu-id="2f067-113">Allow read/write/execute access to authenticated users.</span></span>
    -   <span data-ttu-id="2f067-114">Consentire il controllo completo agli amministratori.</span><span class="sxs-lookup"><span data-stu-id="2f067-114">Allow full control to administrators.</span></span>

    <span data-ttu-id="2f067-115">Per ulteriori informazioni sui formati di stringa SDDL, vedere il [formato della stringa del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="2f067-115">For more information about the SDDL string formats, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>
3.  <span data-ttu-id="2f067-116">La funzione CreateMyDACL chiama la funzione [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per convertire le stringhe SDDL in un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="2f067-116">The CreateMyDACL function calls the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL strings to a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="2f067-117">Il descrittore di sicurezza a cui fa riferimento il membro **lpSecurityDescriptor** della struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2f067-117">The security descriptor is pointed to by the **lpSecurityDescriptor** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="2f067-118">CreateMyDACL invia il valore restituito da **ConvertStringSecurityDescriptorToSecurityDescriptor ha** alla funzione Main.</span><span class="sxs-lookup"><span data-stu-id="2f067-118">CreateMyDACL sends the return value from **ConvertStringSecurityDescriptorToSecurityDescriptor** to the main function.</span></span>
4.  <span data-ttu-id="2f067-119">La funzione Main usa la struttura aggiornata degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) per specificare l'elenco DACL per una nuova cartella creata dalla funzione [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="2f067-119">The main function uses the updated [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to specify the DACL for a new folder that is created by the [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) function.</span></span>
5.  <span data-ttu-id="2f067-120">Quando la funzione Main viene terminata usando la struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , la funzione Main libera la memoria allocata per il membro **LpSecurityDescriptor** chiamando la funzione [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="2f067-120">When the main function is finished using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure, the main function frees the memory allocated for the **lpSecurityDescriptor** member by calling the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="2f067-121">Per compilare correttamente le funzioni SDDL, ad esempio [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), è necessario definire la \_ \_ costante WinNT Win32 come 0x0500 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="2f067-121">To successfully compile SDDL functions such as [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), you must define the \_WIN32\_WINNT constant as 0x0500 or greater.</span></span>

 


```C++
#define _WIN32_WINNT 0x0500

#include <windows.h>
#include <sddl.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

BOOL CreateMyDACL(SECURITY_ATTRIBUTES *);

void main()
{
     SECURITY_ATTRIBUTES  sa;
      
     sa.nLength = sizeof(SECURITY_ATTRIBUTES);
     sa.bInheritHandle = FALSE;  

     // Call function to set the DACL. The DACL
     // is set in the SECURITY_ATTRIBUTES 
     // lpSecurityDescriptor member.
     if (!CreateMyDACL(&sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateMyDACL\n");
         exit(1);
     }

     // Use the updated SECURITY_ATTRIBUTES to specify
     // security attributes for securable objects.
     // This example uses security attributes during
     // creation of a new directory.
     if (0 == CreateDirectory(TEXT("C:\\MyFolder"), &sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateDirectory\n");
         exit(1);
     }

     // Free the memory allocated for the SECURITY_DESCRIPTOR.
     if (NULL != LocalFree(sa.lpSecurityDescriptor))
     {
         // Error encountered; generate message and exit.
         printf("Failed LocalFree\n");
         exit(1);
     }
}


// CreateMyDACL.
//    Create a security descriptor that contains the DACL 
//    you want.
//    This function uses SDDL to make Deny and Allow ACEs.
//
// Parameter:
//    SECURITY_ATTRIBUTES * pSA
//    Pointer to a SECURITY_ATTRIBUTES structure. It is your
//    responsibility to properly initialize the 
//    structure and to free the structure's 
//    lpSecurityDescriptor member when you have
//    finished using it. To free the structure's 
//    lpSecurityDescriptor member, call the 
//    LocalFree function.
// 
// Return value:
//    FALSE if the address to the structure is NULL. 
//    Otherwise, this function returns the value from the
//    ConvertStringSecurityDescriptorToSecurityDescriptor 
//    function.
BOOL CreateMyDACL(SECURITY_ATTRIBUTES * pSA)
{
     // Define the SDDL for the DACL. This example sets 
     // the following access:
     //     Built-in guests are denied all access.
     //     Anonymous logon is denied all access.
     //     Authenticated users are allowed 
     //     read/write/execute access.
     //     Administrators are allowed full control.
     // Modify these values as needed to generate the proper
     // DACL for your application. 
     TCHAR * szSD = TEXT("D:")       // Discretionary ACL
        TEXT("(D;OICI;GA;;;BG)")     // Deny access to 
                                     // built-in guests
        TEXT("(D;OICI;GA;;;AN)")     // Deny access to 
                                     // anonymous logon
        TEXT("(A;OICI;GRGWGX;;;AU)") // Allow 
                                     // read/write/execute 
                                     // to authenticated 
                                     // users
        TEXT("(A;OICI;GA;;;BA)");    // Allow full control 
                                     // to administrators

    if (NULL == pSA)
        return FALSE;

     return ConvertStringSecurityDescriptorToSecurityDescriptor(
                szSD,
                SDDL_REVISION_1,
                &(pSA->lpSecurityDescriptor),
                NULL);
}
```



 

 
