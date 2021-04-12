---
title: Rilevamento dello stato di installazione per l'installazione di Windows Media
description: Rilevamento dello stato di installazione per l'installazione di Windows Media
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player, rilevamento dello stato di installazione
- Windows Media Player, stato del programma di installazione
- Windows Media Player, ridistribuzione del software
- Media Player di Windows, ridistribuzione del software
- rilevamento dello stato di installazione
- stato dell'installazione
- ridistribuzione del software
- ridistribuzione del software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28a4df9b842a1b6491a0ec98ca0a3182630c389
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396719"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>Rilevamento dello stato di installazione per l'installazione di Windows Media

Il codice seguente può essere utilizzato con i pacchetti di ridistribuzione di Windows Media Player. Lo stato dell'installazione viene archiviato nella voce del registro di sistema **InstallResult** nella sottochiave seguente:

**Programma \_ di \_ \\ installazione di \\ Microsoft \\ MediaPlayer \\ per HKEY software utente corrente**

La voce del registro di sistema **InstallResult** ha il formato seguente.



| Nome              | Type           | valore                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | **HRESULT** che indica se l'installazione di Windows Media Player è stata completata e se è necessario un riavvio. |



 

Di seguito è riportato un esempio di codice C++ che può essere incorporato in un'applicazione di configurazione chiamante. Questo codice imposterà `fSuccess` le `fRebootNeeded` variabili e su **true** o **false**, a seconda dei casi, in base al valore **HRESULT** scritto dal programma di installazione di Windows Media Player nel pacchetto di ridistribuzione dei componenti.


```C++
#include <windows.h>
#include <stdio.h>
 
// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
 
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;
 
if( ERROR_SUCCESS == RegOpenKeyExA( 
                         HKEY_CURRENT_USER, 
                         "Software\\Microsoft\\MediaPlayer\\Setup", 
                         0, KEY_QUERY_VALUE, &hKey ))
    {
        char szResult[64];
        DWORD dwResult = sizeof( szResult );
 
if( ERROR_SUCCESS == RegQueryValueExA( 
                         hKey, "InstallResult", NULL, NULL, 
                         (LPBYTE)szResult, &dwResult ) )
        {
            sscanf_s( szResult, "%x", &dwResult );
            fSuccess = SUCCEEDED( dwResult );
            fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwResult );
        }
 
        RegCloseKey( hKey );
    }
 
    if( fSuccess )
    {
        printf( "Setup Succeeded..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
    else
    {
        printf( "Setup Failed..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione del software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




