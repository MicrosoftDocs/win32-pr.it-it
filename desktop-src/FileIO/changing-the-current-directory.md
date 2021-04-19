---
description: Un'applicazione può modificare la directory corrente chiamando la funzione SetCurrentDirectory.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Modifica della directory corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e507d206bcd988a7c00f557bde2b8a0ad39c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319530"
---
# <a name="changing-the-current-directory"></a><span data-ttu-id="89427-103">Modifica della directory corrente</span><span class="sxs-lookup"><span data-stu-id="89427-103">Changing the Current Directory</span></span>

<span data-ttu-id="89427-104">La directory alla fine del percorso attivo viene chiamata directory corrente. si tratta della directory in cui è stata avviata l'applicazione attiva, a meno che non sia stata modificata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="89427-104">The directory at the end of the active path is called the current directory; it is the directory in which the active application started, unless it has been explicitly changed.</span></span> <span data-ttu-id="89427-105">Un'applicazione è in grado di determinare la directory corrente chiamando la funzione [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="89427-105">An application can determine which directory is current by calling the [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) function.</span></span> <span data-ttu-id="89427-106">A volte è necessario usare la funzione [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) per assicurarsi che la lettera di unità venga inclusa se richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="89427-106">It is sometimes necessary to use the [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) function to ensure the drive letter is included if the application requires it.</span></span>

> [!Note]  
> <span data-ttu-id="89427-107">Anche se ogni processo può avere una sola directory corrente, se l'applicazione passa i volumi tramite la funzione [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) , il sistema memorizza l'ultimo percorso corrente per ogni volume (lettera di unità).</span><span class="sxs-lookup"><span data-stu-id="89427-107">Although each process can have only one current directory, if the application switches volumes by using the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function, the system remembers the last current path for each volume (drive letter).</span></span> <span data-ttu-id="89427-108">Questo comportamento si manifesterà solo quando si specifica una lettera di unità senza un percorso completo quando si modifica il punto di directory corrente di riferimento su un volume diverso.</span><span class="sxs-lookup"><span data-stu-id="89427-108">This behavior will manifest itself only when specifying a drive letter without a fully qualified path when changing the current directory point of reference to a different volume.</span></span> <span data-ttu-id="89427-109">Questo vale per le operazioni get o set.</span><span class="sxs-lookup"><span data-stu-id="89427-109">This applies to either Get or Set operations.</span></span>

 

<span data-ttu-id="89427-110">Un'applicazione può modificare la directory corrente chiamando la funzione [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="89427-110">An application can change the current directory by calling the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function.</span></span>

<span data-ttu-id="89427-111">Nell'esempio seguente viene illustrato l'utilizzo di [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) e [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span><span class="sxs-lookup"><span data-stu-id="89427-111">The following example demonstrates the use of [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) and [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH
 
void _tmain(int argc, TCHAR **argv) 
{ 
   TCHAR Buffer[BUFSIZE];
   DWORD dwRet;

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }

   dwRet = GetCurrentDirectory(BUFSIZE, Buffer);

   if( dwRet == 0 )
   {
      printf("GetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   if(dwRet > BUFSIZE)
   {
      printf("Buffer too small; need %d characters\n", dwRet);
      return;
   }

   if( !SetCurrentDirectory(argv[1]))
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Set current directory to %s\n"), argv[1]);

   if( !SetCurrentDirectory(Buffer) )
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Restored previous directory (%s)\n"), Buffer);
}
```



 

 



