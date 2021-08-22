---
description: Illustra come creare correttamente un elenco DACL.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Creazione di un elenco DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af1c7c43c24c07d3d301642b93db41496f2ff70742ce8e2e95fd3f7364ad765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516051"
---
# <a name="creating-a-dacl"></a>Creazione di un elenco DACL

La creazione di [*un elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) appropriato è una parte necessaria e importante dello sviluppo di applicazioni. Poiché un **DACL NULL** consente tutti i tipi di accesso a tutti gli utenti, non utilizzare **DACL NULL.**

Nell'esempio seguente viene illustrato come creare correttamente un elenco DACL. L'esempio contiene una funzione, CreateMyDACL, che usa il linguaggio SDDL [(Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) per definire il controllo di accesso concesso e negato in un elenco DACL. Per fornire un accesso diverso per gli oggetti dell'applicazione, modificare la funzione CreateMyDACL in base alle esigenze.

Nell'esempio:

1.  La funzione main passa un indirizzo di [**una struttura SECURITY \_ ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) alla funzione CreateMyDACL.
2.  La funzione CreateMyDACL usa stringhe SDDL per:
    -   Negare l'accesso agli utenti con accesso guest e anonimo.
    -   Consentire l'accesso in lettura, scrittura ed esecuzione agli utenti autenticati.
    -   Consentire il controllo completo agli amministratori.

    Per altre informazioni sui formati di stringa SDDL, vedere [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  La funzione CreateMyDACL chiama la [**funzione ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per convertire le stringhe SDDL in un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly). Il descrittore di sicurezza fa riferimento al membro **lpSecurityDescriptor** della [**struttura SECURITY \_ ATTRIBUTES.**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) CreateMyDACL invia il valore restituito da **ConvertStringSecurityDescriptorToSecurityDescriptor** alla funzione main.
4.  La funzione main usa la struttura [**DEGLI \_ ATTRIBUTI DI**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) SICUREZZA aggiornata per specificare l'elenco DACL per una nuova cartella creata dalla funzione [**CreateDirectory.**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya)
5.  Quando la funzione main termina di usare la struttura [**SECURITY \_ ATTRIBUTES,**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) la funzione main libera la memoria allocata per il membro **lpSecurityDescriptor** chiamando la [**funzione LocalFree.**](/windows/desktop/api/winbase/nf-winbase-localfree)

> [!Note]  
> Per compilare correttamente funzioni SDDL come [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), è necessario definire la costante \_ WIN32 WINNT come 0x0500 \_ o superiore.

 


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



 

 
