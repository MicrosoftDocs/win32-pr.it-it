---
description: Un'applicazione può modificare la directory corrente chiamando la funzione SetCurrentDirectory.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Modifica della directory corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf742c872bab7d37e115afa815fff961d2f975bfbd3db75ff61a5e992d64a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632111"
---
# <a name="changing-the-current-directory"></a>Modifica della directory corrente

La directory alla fine del percorso attivo è denominata directory corrente. è la directory in cui è stata avviata l'applicazione attiva, a meno che non sia stata modificata in modo esplicito. Un'applicazione può determinare quale directory è corrente chiamando la [**funzione GetCurrentDirectory.**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) A volte è necessario usare la [**funzione GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) per assicurarsi che la lettera di unità sia inclusa se l'applicazione la richiede.

> [!Note]  
> Anche se ogni processo può avere una sola directory corrente, se l'applicazione cambia volume usando la [**funzione SetCurrentDirectory,**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) il sistema memorizza l'ultimo percorso corrente per ogni volume (lettera di unità). Questo comportamento si manifesterà solo quando si specifica una lettera di unità senza un percorso completo quando si modifica il punto di riferimento della directory corrente in un volume diverso. Questo vale per le operazioni Get o Set.

 

Un'applicazione può modificare la directory corrente chiamando la [**funzione SetCurrentDirectory.**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)

Nell'esempio seguente viene illustrato l'uso [**di GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) e [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).


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



 

 



