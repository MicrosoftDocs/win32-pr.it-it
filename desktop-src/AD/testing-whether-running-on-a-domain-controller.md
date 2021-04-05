---
title: Verifica dell'esecuzione in un controller di dominio
description: Il codice seguente usa la funzione VerifyVersionInfo per determinare se il processo chiamante è in esecuzione in un controller di dominio di Windows 2000 Server.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8aeb73af18be9f0c787c2ee30b150689d760aec
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117522"
---
# <a name="testing-whether-running-on-a-domain-controller"></a><span data-ttu-id="904e3-103">Verifica dell'esecuzione in un controller di dominio</span><span class="sxs-lookup"><span data-stu-id="904e3-103">Testing Whether Running on a Domain Controller</span></span>

<span data-ttu-id="904e3-104">Il codice seguente usa la funzione [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) per determinare se il processo chiamante è in esecuzione in un controller di dominio di Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="904e3-104">The following code uses the [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) function to determine whether the calling process is running on a Windows 2000 Server domain controller.</span></span> <span data-ttu-id="904e3-105">Il programma di installazione del servizio può utilizzare questo test prima di installare un servizio con l'account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="904e3-105">Your service installation program could use this test before installing a service under the LocalSystem account.</span></span> <span data-ttu-id="904e3-106">Se il test indica che è in esecuzione in un controller di dominio, è necessario installare il servizio per l'esecuzione con un account utente oppure visualizzare una finestra di dialogo di avviso dei pericoli in esecuzione come LocalSystem in un controller di dominio (ovvero il servizio avrebbe accesso illimitato a Active Directory Domain Services, un contesto di sicurezza estremamente potente che può danneggiare l'intera rete).</span><span class="sxs-lookup"><span data-stu-id="904e3-106">If the test indicates that you are running on a domain controller, you either install the service to run under a user account, or display a dialog box warning of the dangers in running as LocalSystem on a domain controller (which are that the service would then have unrestricted access to Active Directory Domain Services, a supremely powerful security context that has the potential to damage the entire network).</span></span>


```C++
BOOL Is_Win2000_DomainController () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
 
   // Initialize the OSVERSIONINFOEX structure.
   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.wProductType = VER_NT_DOMAIN_CONTROLLER;
 
   // Initialize the condition mask.
   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, 
      VER_GREATER_EQUAL );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, 
      VER_EQUAL );
 
   // Perform the test.
   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_PRODUCT_TYPE,
      dwlConditionMask);
}
```



 

 