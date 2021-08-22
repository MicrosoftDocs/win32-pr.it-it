---
description: Come creare una cartella montata.
ms.assetid: c97bfd10-66ff-41e1-ba3b-f98a019948d5
title: Creazione di una cartella montata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ee89e029a0ce546687341f3da929a22219dff2b128d793d9f7f5130774f834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068671"
---
# <a name="creating-a-mounted-folder"></a>Creazione di una cartella montata

L'esempio seguente illustra come creare una cartella montata. Per altre informazioni, vedere [Creazione di cartelle montate.](mounting-and-dismounting-a-volume.md)

Questo esempio usa le funzioni seguenti: [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) e [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa).


```C++
#define _WIN32_WINNT 0x0501

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE MAX_PATH 

int _tmain( int argc, TCHAR *argv[] )
{
   BOOL bFlag;
   TCHAR Buf[BUFSIZE];     // temporary buffer for volume name

   if( argc != 3 ) 
   {
      _tprintf( TEXT("Usage: %s <mount_point> <volume>\n"), argv[0] );
      _tprintf( TEXT("For example, \"%s c:\\mnt\\fdrive\\ f:\\\"\n"), argv[0]);
      return( -1 );
   }

  // We should do some error checking on the inputs. Make sure there 
  // are colons and backslashes in the right places, and so on 

   bFlag = GetVolumeNameForVolumeMountPoint(
              argv[2], // input volume mount point or directory
                  Buf, // output volume name buffer
              BUFSIZE  // size of volume name buffer
           );

   if (bFlag != TRUE) 
   {
      _tprintf( TEXT("Retrieving volume name for %s failed.\n"), argv[2] );
      return (-2);
   }

   _tprintf( TEXT("Volume name of %s is %s\n"), argv[2], Buf );
   bFlag = SetVolumeMountPoint(
              argv[1], // mount point
                  Buf  // volume to be mounted
           );

   if (!bFlag)
     _tprintf (TEXT("Attempt to mount %s at %s failed.\n"), argv[2], argv[1]);

   return (bFlag);
}
```



 

 



