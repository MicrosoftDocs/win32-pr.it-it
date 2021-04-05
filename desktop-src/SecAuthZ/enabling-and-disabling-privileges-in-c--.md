---
description: L'abilitazione di un privilegio in un token di accesso consente al processo di eseguire azioni a livello di sistema che non è stato possibile eseguire in precedenza.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Abilitazione e disabilitazione dei privilegi in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058031"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Abilitazione e disabilitazione dei privilegi in C++

L'abilitazione di un privilegio in un token di accesso consente al processo di eseguire azioni a livello di sistema che non è stato possibile eseguire in precedenza. L'applicazione deve verificare accuratamente che i privilegi siano appropriati per il tipo di account, specialmente per i seguenti privilegi avanzati.



| Costante Privilege           | Valore stringa                  | Nome visualizzato                        |
|------------------------------|-------------------------------|-------------------------------------|
| \_nome ASSIGNPRIMARYTOKEN \_ se | SeAssignPrimaryTokenPrivilege | Sostituzione di token a livello di processo       |
| \_nome backup \_ se             | SeBackupPrivilege             | Ripristino di file e directory       |
| \_nome debug \_ se              | SeDebugPrivilege              | Debug di programmi                      |
| SE \_ aumenta \_ il \_ nome della quota    | SeIncreaseQuotaPrivilege      | Regolazione limite risorse memoria per un processo  |
| \_nome TCB \_ se                | SeTcbPrivilege                | Agisci come parte del sistema operativo |



 

Prima di abilitare uno di questi privilegi potenzialmente pericolosi, determinare che le funzioni o le operazioni nel codice richiedono effettivamente i privilegi. Alcune funzioni del sistema operativo, ad esempio, richiedono effettivamente **SeTcbPrivilege**. Per un elenco di tutti i privilegi disponibili, vedere [costanti Privilege](authorization-constants.md).

Nell'esempio seguente viene illustrato come abilitare o disabilitare un privilegio in un [*token di accesso*](/windows/desktop/SecGloss/a-gly). Nell'esempio viene chiamata la funzione [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) per ottenere l' [*identificatore univoco locale*](/windows/desktop/SecGloss/l-gly) (LUID) utilizzato dal sistema locale per identificare il privilegio. Viene quindi chiamata la funzione [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , che Abilita o Disabilita il privilegio che dipende dal valore del parametro *bEnablePrivilege* .


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

