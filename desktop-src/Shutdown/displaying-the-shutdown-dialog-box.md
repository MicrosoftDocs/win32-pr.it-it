---
description: Nell'esempio seguente viene riavviato il sistema locale utilizzando la funzione InitiateSystemShutdown.
ms.assetid: 928c2d48-daa5-4c27-816b-766adedba7eb
title: Visualizzazione della finestra di dialogo Shutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedfee9e96fa1e6183cbe1d9322a603b65ae4b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311918"
---
# <a name="displaying-the-shutdown-dialog-box"></a><span data-ttu-id="fb039-103">Visualizzazione della finestra di dialogo Shutdown</span><span class="sxs-lookup"><span data-stu-id="fb039-103">Displaying the Shutdown Dialog Box</span></span>

<span data-ttu-id="fb039-104">Nell'esempio seguente viene riavviato il sistema locale utilizzando la funzione [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) .</span><span class="sxs-lookup"><span data-stu-id="fb039-104">The following example reboots the local system using the [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) function.</span></span> <span data-ttu-id="fb039-105">Il sistema Visualizza una finestra di dialogo con un messaggio personalizzato e un messaggio all'utente per chiudere le applicazioni entro l'intervallo di timeout specificato (30 secondi).</span><span class="sxs-lookup"><span data-stu-id="fb039-105">The system displays a dialog box with a custom message and a message to the user to close applications within the specified time-out interval (30 seconds).</span></span> <span data-ttu-id="fb039-106">Una volta trascorso l'intervallo di timeout, il sistema viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="fb039-106">After the time-out interval elapses, the system is restarted.</span></span>

<span data-ttu-id="fb039-107">\_ \_ Prima di chiamare [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), l'applicazione deve abilitare il privilegio di arresto del nome se.</span><span class="sxs-lookup"><span data-stu-id="fb039-107">The application must enable the SE\_SHUTDOWN\_NAME privilege before calling [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna).</span></span> <span data-ttu-id="fb039-108">Per ulteriori informazioni, vedere [privilegi](../secauthz/privileges.md).</span><span class="sxs-lookup"><span data-stu-id="fb039-108">For more information, see [Privileges](../secauthz/privileges.md).</span></span>


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL MySystemShutdown( LPTSTR lpMsg )
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   BOOL fResult;               // system shutdown flag 
 
   // Get the current process token handle so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
      (PTOKEN_PRIVILEGES) NULL, 0); 
 
   // Cannot test the return value of AdjustTokenPrivileges. 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Display the shutdown dialog box and start the countdown. 
 
   fResult = InitiateSystemShutdown( 
      NULL,    // shut down local computer 
      lpMsg,   // message for user
      30,      // time-out period, in seconds 
      FALSE,   // ask user to close apps 
      TRUE);   // reboot after shutdown 
 
   if (!fResult) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE; 
}
```



<span data-ttu-id="fb039-109">Se la funzione [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) viene eseguita nel periodo di timeout specificato da [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), il sistema non viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="fb039-109">If the [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) function is executed in the time-out period specified by [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), the system does not shut down.</span></span> <span data-ttu-id="fb039-110">Se, ad esempio, PreventSystemShutdown viene chiamato dopo MySystemShutdown, il sistema chiude la finestra di dialogo e non riavvia il sistema.</span><span class="sxs-lookup"><span data-stu-id="fb039-110">For example, if PreventSystemShutdown is called after MySystemShutdown, the system closes the dialog box and does not restart the system.</span></span>


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL PreventSystemShutdown()
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   // Get the current process token handle  so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
         TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
         &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Prevent the system from shutting down. 
 
   if ( !AbortSystemShutdown(NULL) ) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
       (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE;
}
```



 

 
