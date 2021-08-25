---
description: Controllare i diritti di accesso che un descrittore di sicurezza consente per un client.
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: Verifica dell'accesso client con gli ACL in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2160b48a3b88a617eaaea1e8fae63168db5a85e82cad62be5aef248ff51581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906691"
---
# <a name="verifying-client-access-with-acls-in-c"></a>Verifica dell'accesso client con gli ACL in C++

L'esempio seguente illustra come un server può controllare i diritti di accesso che un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) consente per un client. Nell'esempio viene utilizzata [**la funzione ImpersonateNamedPipeClient.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) tuttavia, funziona allo stesso modo usando una qualsiasi delle altre funzioni di rappresentazione. Dopo la rappresentazione del client, nell'esempio viene chiamata [**la funzione OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) per ottenere il [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly). Chiama quindi la funzione [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) per convertire tutti i diritti di accesso generici nei diritti di accesso specifici e standard corrispondenti in base al mapping specificato nella struttura [**GENERIC \_ MAPPING.**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)

La [**funzione AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) controlla i diritti di accesso richiesti rispetto ai diritti consentiti per il client nell'elenco DACL del descrittore di sicurezza. Per controllare l'accesso e generare una voce nel registro eventi di sicurezza, usare la [**funzione AccessCheckAndAuditAlarm.**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)


```C++
#include <windows.h>
#pragma comment(lib, "advapi32.lib")

BOOL ImpersonateAndCheckAccess(
  HANDLE hNamedPipe,               // handle of pipe to impersonate
  PSECURITY_DESCRIPTOR pSD,        // security descriptor to check
  DWORD dwAccessDesired,           // access rights to check
  PGENERIC_MAPPING pGeneric,       // generic mapping for object
  PDWORD pdwAccessAllowed          // returns allowed access rights
) 
{
   HANDLE hToken;
   PRIVILEGE_SET PrivilegeSet;
   DWORD dwPrivSetSize = sizeof( PRIVILEGE_SET );
   BOOL fAccessGranted=FALSE;

// Impersonate the client.

   if (! ImpersonateNamedPipeClient(hNamedPipe) ) 
      return FALSE;

// Get an impersonation token with the client's security context.

   if (! OpenThreadToken( GetCurrentThread(), TOKEN_ALL_ACCESS,
         TRUE, &hToken ))
   {
      goto Cleanup;
   }

// Use the GENERIC_MAPPING structure to convert any 
// generic access rights to object-specific access rights.

   MapGenericMask( &dwAccessDesired, pGeneric );

// Check the client's access rights.

   if( !AccessCheck( 
      pSD,                 // security descriptor to check
      hToken,              // impersonation token
      dwAccessDesired,     // requested access rights
      pGeneric,            // pointer to GENERIC_MAPPING
      &PrivilegeSet,       // receives privileges used in check
      &dwPrivSetSize,      // size of PrivilegeSet buffer
      pdwAccessAllowed,    // receives mask of allowed access rights
      &fAccessGranted ))   // receives results of access check
   {
      goto Cleanup;
   }

Cleanup:

   RevertToSelf();

   if (hToken != INVALID_HANDLE_VALUE)
      CloseHandle(hToken);  

   return fAccessGranted;
}
```



 

 
