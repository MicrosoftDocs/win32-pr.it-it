---
description: Come ottenere un percorso GUID del volume per ogni volume locale associato a una lettera di unità attualmente in uso nel computer.
ms.assetid: f6590a46-2e09-472c-8231-bb24c9b0b5f6
title: Enumerazione dei percorsi GUID del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e363369d3ea26abb054c8b9321c0147ace7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313882"
---
# <a name="enumerating-volume-guid-paths"></a>Enumerazione dei percorsi GUID del volume

Nell'esempio di codice in questo argomento viene illustrato come ottenere un percorso **GUID** del volume per ogni volume locale associato a una lettera di unità attualmente in uso nel computer.

Nell'esempio di codice viene utilizzata la funzione [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH 

void main(void)
 {
  BOOL bFlag;
  TCHAR Buf[BUFSIZE];           // temporary buffer for volume name
  TCHAR Drive[] = TEXT("c:\\"); // template drive specifier
  TCHAR I;                      // generic loop counter

  // Walk through legal drive letters, skipping floppies.
  for (I = TEXT('c'); I < TEXT('z');  I++ ) 
   {
    // Stamp the drive for the appropriate letter.
    Drive[0] = I;

    bFlag = GetVolumeNameForVolumeMountPoint(
                Drive,     // input volume mount point or directory
                Buf,       // output volume name buffer
                BUFSIZE ); // size of volume name buffer

    if (bFlag) 
     {
      _tprintf (TEXT("The ID of drive \"%s\" is \"%s\"\n"), Drive, Buf);
     }
   }
 }
```



Per un esempio che enumera tutti i volumi collegati localmente e visualizza il percorso del dispositivo, il percorso del **GUID** del volume e i percorsi montati (incluse le lettere di unità), vedere [visualizzazione dei percorsi dei volumi](displaying-volume-paths.md).

 

 



