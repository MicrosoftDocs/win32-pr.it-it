---
description: Nell'esempio seguente viene utilizzata la funzione GetSystemInfo per ottenere informazioni sull'hardware, ad esempio l'identificatore OEM, il tipo di processore, le dimensioni della pagina e così via. Nell'esempio vengono visualizzate le informazioni nella console di.
ms.assetid: 9f943926-9ca7-4d4c-ad1e-b68c248e0e01
title: Recupero delle informazioni sull'hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89ab5083e9d88e60d962ebcdd7b701a90e279cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319892"
---
# <a name="getting-hardware-information"></a><span data-ttu-id="b4c88-104">Recupero delle informazioni sull'hardware</span><span class="sxs-lookup"><span data-stu-id="b4c88-104">Getting Hardware Information</span></span>

<span data-ttu-id="b4c88-105">Nell'esempio seguente viene utilizzata la funzione [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) per ottenere informazioni sull'hardware, ad esempio l'identificatore OEM, il tipo di processore, le dimensioni della pagina e così via.</span><span class="sxs-lookup"><span data-stu-id="b4c88-105">The following example uses the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function to obtain hardware information such as the OEM identifier, processor type, page size, and so on.</span></span> <span data-ttu-id="b4c88-106">Nell'esempio vengono visualizzate le informazioni nella console di.</span><span class="sxs-lookup"><span data-stu-id="b4c88-106">The example displays the information in the console.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "user32.lib")

void main()
{
   SYSTEM_INFO siSysInfo;
 
   // Copy the hardware information to the SYSTEM_INFO structure. 
 
   GetSystemInfo(&siSysInfo); 
 
   // Display the contents of the SYSTEM_INFO structure. 

   printf("Hardware information: \n");  
   printf("  OEM ID: %u\n", siSysInfo.dwOemId);
   printf("  Number of processors: %u\n", 
      siSysInfo.dwNumberOfProcessors); 
   printf("  Page size: %u\n", siSysInfo.dwPageSize); 
   printf("  Processor type: %u\n", siSysInfo.dwProcessorType); 
   printf("  Minimum application address: %lx\n", 
      siSysInfo.lpMinimumApplicationAddress); 
   printf("  Maximum application address: %lx\n", 
      siSysInfo.lpMaximumApplicationAddress); 
   printf("  Active processor mask: %u\n", 
      siSysInfo.dwActiveProcessorMask); 
}
```



 

 
