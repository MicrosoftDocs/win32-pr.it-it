---
title: Test dell'esecuzione in un controller di dominio
description: Il codice seguente usa la funzione VerifyVersionInfo per determinare se il processo chiamante è in esecuzione in un controller di dominio Windows 2000 Server.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb49577994716598bb730fcc7e86a9cce76a2835e8cfa1558b7d608b9cbc5ea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024589"
---
# <a name="testing-whether-running-on-a-domain-controller"></a>Test dell'esecuzione in un controller di dominio

Nel codice seguente viene utilizzata la [**funzione VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) per determinare se il processo chiamante è in esecuzione in un controller di dominio Windows 2000 Server. Il programma di installazione del servizio potrebbe usare questo test prima di installare un servizio con l'account LocalSystem. Se il test indica che l'esecuzione è in esecuzione in un controller di dominio, installare il servizio per l'esecuzione con un account utente oppure visualizzare una finestra di dialogo che segnala i rischi dell'esecuzione come LocalSystem in un controller di dominio, ovvero che il servizio avrebbe accesso illimitato a Active Directory Domain Services, un contesto di sicurezza estremamente potente che potrebbe danneggiare l'intera rete.


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



 

 