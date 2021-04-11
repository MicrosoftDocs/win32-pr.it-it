---
description: Nell'esempio seguente vengono usate le funzioni helper dell'API Version per determinare la versione del sistema operativo corrente, se si tratta di una versione server o client, quindi le informazioni vengono visualizzate nella console.
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: Recupero della versione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fa259378b81f9255846694927ee2b68e6f38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885833"
---
# <a name="getting-the-system-version"></a>Recupero della versione del sistema

Nell'esempio seguente vengono usate le [funzioni helper dell'API Version](version-helper-apis.md) per determinare la versione del sistema operativo corrente, se si tratta di una versione server o client, quindi le informazioni vengono visualizzate nella console. Se è attiva la modalità di compatibilità, nell'esempio viene visualizzato il sistema operativo selezionato per la [compatibilità delle applicazioni](/previous-versions/bb757005(v=msdn.10)).

Basarsi sulle informazioni sulla versione non è il modo migliore per verificare la presenza di una funzionalità. In alternativa, fare riferimento alla documentazione per la funzionalità di interesse. Per ulteriori informazioni sulle tecniche comuni per il rilevamento delle funzionalità, vedere [versione del sistema operativo](operating-system-version.md).


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



 

 
