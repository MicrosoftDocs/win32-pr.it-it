---
description: L'esempio seguente usa le funzioni dell'helper API Versione per determinare la versione del sistema operativo corrente, se si tratta di una versione server o client, e quindi visualizza queste informazioni nella console.
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: Recupero della versione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb9cfd0c1a4cfe1ee0789cb609bf22319bdd019bf3310bf439dabf907bfd138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958526"
---
# <a name="getting-the-system-version"></a>Recupero della versione del sistema

L'esempio seguente usa le funzioni [dell'helper API](version-helper-apis.md) Versione per determinare la versione del sistema operativo corrente, se si tratta di una versione server o client, e quindi visualizza queste informazioni nella console. Se è attiva la modalità di compatibilità, nell'esempio viene visualizzato il sistema operativo selezionato per la [compatibilità delle applicazioni.](/previous-versions/bb757005(v=msdn.10))

Basarsi sulle informazioni sulla versione non è il modo migliore per testare una funzionalità. Fare invece riferimento alla documentazione relativa alla funzionalità di interesse. Per altre informazioni sulle tecniche comuni per il rilevamento delle funzionalità, vedere [Versione del sistema operativo](operating-system-version.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <VersionHelpers.h>

int 
__cdecl
wmain(
    __in int argc, 
    __in_ecount(argc) PCWSTR argv[]
    )
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

    if (IsWindowsXPOrGreater())
    {
        printf("XPOrGreater\n");
    }

    if (IsWindowsXPSP1OrGreater())
    {
        printf("XPSP1OrGreater\n");
    }

    if (IsWindowsXPSP2OrGreater())
    {
        printf("XPSP2OrGreater\n");
    }

    if (IsWindowsXPSP3OrGreater())
    {
        printf("XPSP3OrGreater\n");
    }

    if (IsWindowsVistaOrGreater())
    {
        printf("VistaOrGreater\n");
    }

    if (IsWindowsVistaSP1OrGreater())
    {
        printf("VistaSP1OrGreater\n");
    }

    if (IsWindowsVistaSP2OrGreater())
    {
        printf("VistaSP2OrGreater\n");
    }

    if (IsWindows7OrGreater())
    {
        printf("Windows7OrGreater\n");
    }

    if (IsWindows7SP1OrGreater())
    {
        printf("Windows7SP1OrGreater\n");
    }

    if (IsWindows8OrGreater())
    {
        printf("Windows8OrGreater\n");
    }

    if (IsWindows8Point1OrGreater())
    {
        printf("Windows8Point1OrGreater\n");
    }

    if (IsWindows10OrGreater())
    {
        printf("Windows10OrGreater\n");
    }

    if (IsWindowsServer())
    {
        printf("Server\n");
    }
    else
    {
        printf("Client\n");
    }
}
```



 

 
