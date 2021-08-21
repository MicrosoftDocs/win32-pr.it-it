---
title: Rilevamento dello stato di installazione per l Windows dei supporti
description: Rilevamento dello stato di installazione per l Windows dei supporti
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player,rilevamento dello stato dell'installazione
- Windows Media Player,stato dell'installazione
- Windows Media Player,ridistribuzione del software
- Windows Media Player, ridistribuzione software
- rilevamento dello stato di installazione
- stato di installazione
- ridistribuzione di software
- ridistribuzione del software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797c7cb5fe4d34895109777c4da7e15489a0d32acd9cf42660b3346521f6f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340900"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>Rilevamento dello stato di installazione per l Windows dei supporti

Il codice seguente può essere usato con i pacchetti Windows Media Player ridistribuzione. Lo stato dell'installazione viene archiviato nella **voce del Registro di sistema InstallResult** nella sottochiave seguente:

**HKEY \_ CURRENT USER Software Installazione di Microsoft \_ \\ \\ \\ MediaPlayer \\**

La voce del Registro di sistema **InstallResult** ha il formato seguente.



| Nome              | Type           | valore                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | Valore **HRESULT che** indica se l Windows Media Player installazione è riuscita e se è necessario un riavvio. |



 

Di seguito è riportato un esempio di codice C++ che può essere incorporato in un'applicazione di configurazione chiamante. Questo codice imposta le variabili e su true o false, in base al valore HRESULT scritto dal programma di installazione di Windows Media Player nel pacchetto `fSuccess` `fRebootNeeded` di ridistribuzione dei componenti.   


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

[**Ridistribuzione Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




