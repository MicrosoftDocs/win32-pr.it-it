---
description: Come creare una cartella montata.
ms.assetid: c97bfd10-66ff-41e1-ba3b-f98a019948d5
title: Creazione di una cartella montata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad8a16c4a8c06ae22fa7faf2c2b0a2e8cdfc38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319068"
---
# <a name="creating-a-mounted-folder"></a><span data-ttu-id="eddfe-103">Creazione di una cartella montata</span><span class="sxs-lookup"><span data-stu-id="eddfe-103">Creating a Mounted Folder</span></span>

<span data-ttu-id="eddfe-104">Nell'esempio seguente viene illustrato come creare una cartella montata.</span><span class="sxs-lookup"><span data-stu-id="eddfe-104">The following sample demonstrates how to create a mounted folder.</span></span> <span data-ttu-id="eddfe-105">Per ulteriori informazioni, vedere [creazione di cartelle montate](mounting-and-dismounting-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="eddfe-105">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>

<span data-ttu-id="eddfe-106">In questo esempio vengono utilizzate le funzioni seguenti: [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) e [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa).</span><span class="sxs-lookup"><span data-stu-id="eddfe-106">This sample uses the following functions: [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) and [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa).</span></span>


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



 

 



