---
description: Nell'esempio seguente viene utilizzata la funzione VerifyVersionInfo per determinare se le suite di prodotti specificate sono installate nel computer locale.
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: Rilevamento di una suite di prodotti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319900"
---
# <a name="detecting-a-product-suite"></a>Rilevamento di una suite di prodotti

Nell'esempio seguente viene utilizzata la funzione [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) per determinare se le suite di prodotti specificate sono installate nel computer locale.

Questo esempio usa la versione VER \_ e il flag. Se vengono specificati due flag nella maschera del gruppo, la funzione restituisce **true** solo se sono presenti entrambi i gruppi di prodotti. Se l'esempio è stato modificato per l'utilizzo del \_ flag ver o, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) restituisce **true** se è presente una serie di prodotti.


```C++
#include <windows.h>
#include <stdio.h>

BOOL CheckProductSuite ( WORD wSuite ) 
{
  OSVERSIONINFOEX osvi;
  DWORDLONG dwlConditionMask = 0;

  // Initialize the OSVERSIONINFOEX structure.

  ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
  osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
  osvi.wSuiteMask = wSuite;

  // Set up the condition mask.

  VER_SET_CONDITION( dwlConditionMask, 
          VER_SUITENAME, VER_AND );

  // Perform the test.

  return VerifyVersionInfo(
          &osvi, 
          VER_SUITENAME,
          dwlConditionMask);
}

void main()
{
    if( CheckProductSuite(VER_SUITE_ENTERPRISE) )
        printf( "The system meets the requirements.\n" );
    else printf( "The system does not meet the requirements.\n");
}
```



 

 



