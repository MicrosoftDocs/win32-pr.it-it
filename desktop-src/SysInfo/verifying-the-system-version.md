---
description: Sono inclusi esempi che usano la funzione VerifyVersionInfo per determinare se l'applicazione è in esecuzione in un sistema operativo specifico.
ms.assetid: f39c35ae-9be5-4a03-9079-6fcc63387f6b
title: Verifica della versione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ddb3562230d0708ddc55d0f8214286ea6c3008
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227044"
---
# <a name="verifying-the-system-version"></a>Verifica della versione del sistema

\[ L'uso della funzione [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) per verificare che il sistema operativo attualmente in esecuzione non è consigliato. Usare invece le [ **API della versione Helper**](version-helper-apis.md)\]

Sono inclusi esempi che usano la funzione [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) per determinare se l'applicazione è in esecuzione in un sistema operativo specifico.

Di seguito sono riportati i passaggi principali di ogni esempio:

1.  Impostare i valori appropriati nella struttura [**OSVERSIONINFOEX**](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa) .
2.  Impostare la maschera di condizione appropriata utilizzando la macro della [**\_ \_ condizione set ver**](/windows/desktop/api/Winnt/nf-winnt-ver_set_condition) .
3.  Chiamare [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) per eseguire il test.

## <a name="example-1"></a>Esempio 1

Nell'esempio seguente viene determinato se l'applicazione è in esecuzione in Windows XP con Service Pack 2 (SP2) o in una versione successiva di Windows, ad esempio Windows Server 2003 o Windows Vista.


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_WinXP_SP2_or_Later () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 1;
   osvi.wServicePackMajor = 2;
   osvi.wServicePackMinor = 0;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR,
      dwlConditionMask);
}

void main()
{
    if(Is_WinXP_SP2_or_Later())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



## <a name="example-2"></a>Esempio 2

Il codice seguente verifica che l'applicazione sia in esecuzione in un server Windows 2000 o versione successiva, ad esempio Windows Server 2003 o Windows Server 2008.


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_Win_Server() 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 0;
   osvi.wServicePackMajor = 0;
   osvi.wServicePackMinor = 0;
   osvi.wProductType = VER_NT_SERVER;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, VER_EQUAL );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR |
      VER_PRODUCT_TYPE,
      dwlConditionMask);
}

void main()
{
    if(Is_Win_Server())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



 

 



