---
title: Rilevamento dello stato dell'installazione
description: Rilevamento dello stato dell'installazione
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Media Format SDK, ridistribuzione software
- Advanced Systems Format (ASF), ridistribuzione software
- ASF (Advanced Systems Format),ridistribuzione software
- Windows Media Format SDK, ridistribuzione
- Advanced Systems Format (ASF), ridistribuzione
- ASF (Advanced Systems Format),ridistribuzione
- ridistribuzione del software, rilevamento dello stato dell'installazione
- ridistribuzione, rilevamento dello stato dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250ab87fd81592b868e1dbf13106577f83e680796310aff246f0c1483fa847cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931392"
---
# <a name="detecting-setup-status"></a>Rilevamento dello stato dell'installazione

Quando il file eseguibile di ridistribuzione viene eseguito in un computer, registra lo stato di installazione nel Registro di sistema come **valore HRESULT.** Lo stato dell'installazione viene archiviato nella **voce del Registro di sistema InstallResult** nella sottochiave seguente:

**HKEY \_ CURRENT USER Software Installazione di Microsoft \_ \\ \\ \\ MediaPlayer \\**

La voce del Registro di sistema **InstallResult** ha il formato seguente.



| Nome              | Type           | valore                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | Valore **HRESULT che** indica se l Windows Media Player installazione è riuscita e se è necessario un riavvio. |



 

Il codice seguente imposterà le variabili *fSucess* e *fRebootNeeded* su **True** o **False,** in base al valore **HRESULT** scritto dal programma di installazione di Windows Media nel pacchetto di ridistribuzione dei componenti.


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

 

 




