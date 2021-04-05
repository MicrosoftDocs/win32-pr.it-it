---
title: Rilevamento dello stato di installazione
description: Rilevamento dello stato di installazione
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Media Format SDK, ridistribuzione software
- ASF (Advanced Systems Format), ridistribuzione del software
- ASF (formato avanzato dei sistemi), ridistribuzione del software
- Windows Media Format SDK, ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ASF (formato avanzato dei sistemi), ridistribuzione
- ridistribuzione del software, rilevamento dello stato di installazione
- ridistribuzione, rilevamento dello stato di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714218"
---
# <a name="detecting-setup-status"></a>Rilevamento dello stato di installazione

Quando il file eseguibile di ridistribuzione viene eseguito in un computer, registra lo stato di installazione nel registro di sistema come valore **HRESULT** . Lo stato dell'installazione viene archiviato nella voce del registro di sistema **InstallResult** nella sottochiave seguente:

**Programma \_ di \_ \\ installazione di \\ Microsoft \\ MediaPlayer \\ per HKEY software utente corrente**

La voce del registro di sistema **InstallResult** ha il formato seguente.



| Nome              | Type           | valore                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | **HRESULT** che indica se l'installazione di Windows Media Player è stata completata e se è necessario un riavvio. |



 

Il codice seguente imposta le variabili *fSucess* e *fRebootNeeded* su **true** o **false**, a seconda dei casi, in base al valore **HRESULT** scritto dal programma di installazione di Windows Media nel pacchetto di ridistribuzione dei componenti.


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

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione del software**](software-redistribution.md)
</dt> </dl>

 

 




