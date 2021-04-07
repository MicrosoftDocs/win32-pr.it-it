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
# <a name="creating-a-dacl"></a>Creazione di un DACL

La creazione di un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) appropriato è una parte essenziale e importante dello sviluppo di applicazioni. Poiché un DACL **null** consente tutti i tipi di accesso a tutti gli utenti, non usare DACL **null** .

Nell'esempio seguente viene illustrato come creare correttamente un DACL. Nell'esempio è inclusa una funzione, CreateMyDACL, che utilizza il linguaggio SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ) per definire il controllo di accesso concesso e negato in un DACL. Per fornire accesso diverso per gli oggetti dell'applicazione, modificare la funzione CreateMyDACL in base alle esigenze.

Nell'esempio:

1.  La funzione Main passa un indirizzo di una struttura di [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) alla funzione CreateMyDACL.
2.  La funzione CreateMyDACL usa le stringhe SDDL per:
    -   Negare l'accesso agli utenti guest e accesso anonimo.
    -   Consente l'accesso in lettura/scrittura/esecuzione agli utenti autenticati.
    -   Consentire il controllo completo agli amministratori.

    Per ulteriori informazioni sui formati di stringa SDDL, vedere il [formato della stringa del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  La funzione CreateMyDACL chiama la funzione [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per convertire le stringhe SDDL in un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly). Il descrittore di sicurezza a cui fa riferimento il membro **lpSecurityDescriptor** della struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . CreateMyDACL invia il valore restituito da **ConvertStringSecurityDescriptorToSecurityDescriptor ha** alla funzione Main.
4.  La funzione Main usa la struttura aggiornata degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) per specificare l'elenco DACL per una nuova cartella creata dalla funzione [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .
5.  Quando la funzione Main viene terminata usando la struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , la funzione Main libera la memoria allocata per il membro **LpSecurityDescriptor** chiamando la funzione [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

> [!Note]  
> Per compilare correttamente le funzioni SDDL, ad esempio [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), è necessario definire la \_ \_ costante WinNT Win32 come 0x0500 o versione successiva.

 


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



 

 
