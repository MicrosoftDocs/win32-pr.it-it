---
description: Per spostare una directory in un altro percorso, insieme ai file e alle sottodirectory in esso contenuti, chiamare la funzione MoveFileEx, MoveFileWithProgress o MoveFileTransacted.
ms.assetid: ca56c109-d6a3-456e-956c-126ce4aee8ba
title: Trasferimento di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56167f0831894350a044104bce1f41ef3c5770ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319065"
---
# <a name="moving-directories"></a>Trasferimento di directory

Per spostare una directory in un altro percorso, insieme ai file e alle sottodirectory in esso contenuti, chiamare la funzione [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)o [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) . La funzione [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa) ha la stessa funzionalità di [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), ad eccezione del fatto che **MoveFileWithProgress** consente di specificare una routine di callback che riceve le notifiche sullo stato di avanzamento dell'operazione. La funzione [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) consente di eseguire l'operazione come operazione transazionale.

Nell'esempio seguente viene illustrato l'utilizzo della funzione [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) con una directory.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    printf("\n");
    if( argc != 3 )
    {
        printf("ERROR:  Incorrect number of arguments\n\n");
        printf("Description:\n");
        printf("  Moves a directory and its contents\n\n");
        printf("Usage:\n");
        _tprintf(TEXT("  %s [source_dir] [target_dir]\n\n"), argv[0]);
        printf("  The target directory cannot exist already.\n\n");
        return;
    }

    // Move the source directory to the target directory location.
    // The target directory must be on the same drive as the source.
    // The target directory cannot already exist.

    if (!MoveFileEx(argv[1], argv[2], MOVEFILE_WRITE_THROUGH))
    { 
        printf ("MoveFileEx failed with error %d\n", GetLastError());
        return;
    }
    else _tprintf(TEXT("%s has been moved to %s\n"), argv[1], argv[2]);
}
```



 

 



