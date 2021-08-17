---
description: L'abilitazione di un privilegio in un token di accesso consente al processo di eseguire azioni a livello di sistema che non potevano essere eseguite in precedenza.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Abilitazione e disabilitazione dei privilegi in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc36e3db162b1a7a7f12f1849ab7708bda19d90991e58a65135d0eb4c0abd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781727"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Abilitazione e disabilitazione dei privilegi in C++

L'abilitazione di un privilegio in un token di accesso consente al processo di eseguire azioni a livello di sistema che non potevano essere eseguite in precedenza. L'applicazione deve verificare accuratamente che il privilegio sia appropriato per il tipo di account, in particolare per i privilegi potenti seguenti.



| Costante dei privilegi           | Valore stringa                  | Nome visualizzato                        |
|------------------------------|-------------------------------|-------------------------------------|
| \_edizione Standard NOME ASSIGNPRIMARYTOKEN \_ | SeAssignPrimaryTokenPrivilege | Sostituzione di token a livello di processo       |
| \_edizione Standard NOME \_ BACKUP             | SeBackupPrivilege             | Ripristino di file e directory       |
| \_edizione Standard NOME \_ DEBUG              | SeDebugPrivilege              | Debug di programmi                      |
| \_edizione Standard AUMENTARE \_ IL NOME DELLA \_ QUOTA    | SeIncreaseQuotaPrivilege      | Regolazione limite risorse memoria per un processo  |
| \_edizione Standard NOME \_ TCB                | SeTcbPrivilege                | Agisci come parte del sistema operativo |



 

Prima di abilitare uno di questi privilegi potenzialmente pericolosi, determinare che le funzioni o le operazioni nel codice richiedano effettivamente tali privilegi. Ad esempio, pochissime funzioni nel sistema operativo richiedono effettivamente **SeTcbPrivilege**. Per un elenco di tutti i privilegi disponibili, vedere [Costanti dei privilegi](authorization-constants.md).

Nell'esempio seguente viene illustrato come abilitare o disabilitare un privilegio in un [*token di accesso*](/windows/desktop/SecGloss/a-gly). Nell'esempio viene chiamata la [**funzione LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) per ottenere l'identificatore univoco locale (LUID) utilizzato dal sistema locale per identificare il privilegio. [](/windows/desktop/SecGloss/l-gly) L'esempio chiama quindi la [**funzione AdjustTokenPrivileges,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) che abilita o disabilita il privilegio che dipende dal valore del *parametro bEnablePrivilege.*


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



 

