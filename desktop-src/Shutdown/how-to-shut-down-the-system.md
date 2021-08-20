---
description: Nell'esempio seguente viene utilizzata la funzione ExitWindowsEx per arrestare il sistema.
ms.assetid: bf8723aa-1c7f-4761-9034-d5a9447a4bc4
title: Come arrestare il sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb366a3a6159cd43cf1f88f050d01ea75d365035c2f55598f69e91e89fc81de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963622"
---
# <a name="how-to-shut-down-the-system"></a>Come arrestare il sistema

Nell'esempio seguente viene [**utilizzata la funzione ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) per arrestare il sistema. L'arresto scarica i buffer di file su disco e porta il sistema a una condizione in cui è sicuro spegnere il computer. L'applicazione deve prima abilitare il privilegio \_ EDIZIONE STANDARD SHUTDOWN \_ NAME. Per altre informazioni, vedere [Privilegi](../secauthz/privileges.md).


```C++
#include <windows.h>

#pragma comment(lib, "user32.lib")
#pragma comment(lib, "advapi32.lib")

BOOL MySystemShutdown()
{
   HANDLE hToken; 
   TOKEN_PRIVILEGES tkp; 
 
   // Get a token for this process. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return( FALSE ); 
 
   // Get the LUID for the shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get the shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Shut down the system and force all applications to close. 
 
   if (!ExitWindowsEx(EWX_SHUTDOWN | EWX_FORCE, 
               SHTDN_REASON_MAJOR_OPERATINGSYSTEM |
               SHTDN_REASON_MINOR_UPGRADE |
               SHTDN_REASON_FLAG_PLANNED)) 
      return FALSE; 

   //shutdown was successful
   return TRUE;
}
```



Il parametro finale nella chiamata [**a ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) indica che il sistema è stato arrestato per un aggiornamento di pianificazione del sistema operativo. Per altre informazioni, vedere [Codici motivo arresto sistema](system-shutdown-reason-codes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Arresto](shutting-down.md)
</dt> </dl>

 

 
