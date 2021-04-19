---
description: Nell'esempio seguente viene usata la funzione ExitWindowsEx per arrestare il sistema.
ms.assetid: bf8723aa-1c7f-4761-9034-d5a9447a4bc4
title: Come arrestare il sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3880319e0ada6c82c6c6c12a7f3b5faf00415a93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311917"
---
# <a name="how-to-shut-down-the-system"></a><span data-ttu-id="1da68-103">Come arrestare il sistema</span><span class="sxs-lookup"><span data-stu-id="1da68-103">How to Shut Down the System</span></span>

<span data-ttu-id="1da68-104">Nell'esempio seguente viene usata la funzione [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) per arrestare il sistema.</span><span class="sxs-lookup"><span data-stu-id="1da68-104">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to shut down the system.</span></span> <span data-ttu-id="1da68-105">Quando si arresta lo svuotamento dei buffer di file su disco e il sistema viene portato a una condizione in cui è sicuro spegnere il computer.</span><span class="sxs-lookup"><span data-stu-id="1da68-105">Shutting down flushes file buffers to disk and brings the system to a condition in which it is safe to turn off the computer.</span></span> <span data-ttu-id="1da68-106">L'applicazione deve prima abilitare il privilegio di arresto del nome di SE \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1da68-106">The application must first enable the SE\_SHUTDOWN\_NAME privilege.</span></span> <span data-ttu-id="1da68-107">Per ulteriori informazioni, vedere [privilegi](../secauthz/privileges.md).</span><span class="sxs-lookup"><span data-stu-id="1da68-107">For more information, see [Privileges](../secauthz/privileges.md).</span></span>


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



<span data-ttu-id="1da68-108">Il parametro finale nella chiamata a [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) indica che il sistema è stato arrestato per un aggiornamento della pianificazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1da68-108">The final parameter in the call to [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) indicates that the system was shut down for a planning update of the operating system.</span></span> <span data-ttu-id="1da68-109">Per ulteriori informazioni, vedere [codici motivo dell'arresto del sistema](system-shutdown-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1da68-109">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1da68-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1da68-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1da68-111">Chiusura in corso</span><span class="sxs-lookup"><span data-stu-id="1da68-111">Shutting Down</span></span>](shutting-down.md)
</dt> </dl>

 

 
