---
title: Determinazione del percorso di una condivisione
description: Nell'esempio seguente viene illustrato come chiamare la funzione WNetGetUniversalName per determinare il percorso di una condivisione in un'unità reindirizzata.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963289"
---
# <a name="determining-the-location-of-a-share"></a>Determinazione del percorso di una condivisione

Nell'esempio seguente viene illustrato come chiamare la funzione [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) per determinare il percorso di una condivisione in un'unità reindirizzata.

Innanzitutto, nell'esempio di codice viene chiamata la funzione **WNetGetUniversalName** , specificando il livello di informazioni del [**nome universale per recuperare un puntatore a una stringa \_ \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) del nome Universal Naming Convention (UNC) per la risorsa. L'esempio chiama quindi **WNetGetUniversalName** una seconda volta, specificando il livello informazioni sul [**\_ nome remoto \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) per recuperare due stringhe di informazioni di connessione di rete aggiuntive. Se le chiamate hanno esito positivo, l'esempio stampa il percorso della condivisione.

Per testare l'esempio di codice seguente, seguire questa procedura:

1.  Denominare l'esempio di codice GetUni. cpp.
2.  Aggiungere l'esempio a un'applicazione console denominata GetUni.
3.  Collegare le librerie shell32. lib, MPR. lib e NetApi32. lib all'elenco di librerie del compilatore.
4.  Al prompt dei comandi passare alla directory GetUni
5.  Compilare GetUni. cpp.
6.  Eseguire il file GetUni.exe seguito da una lettera di unità e due punti, come indicato di seguito:

    **GetUni H:\\**


```C++
#define  STRICT
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")

#define BUFFSIZE = 1000

void main( int argc, char *argv[] )
{
  DWORD cbBuff = 1000;    // Size of Buffer
  TCHAR szBuff[1000];    // Buffer to receive information
  REMOTE_NAME_INFO  * prni = (REMOTE_NAME_INFO *)   &szBuff;
  UNIVERSAL_NAME_INFO * puni = (UNIVERSAL_NAME_INFO *) &szBuff;
  DWORD res;

  if((argc < 2) | (lstrcmp(argv[1], "/?") == 0))
  {
    printf("Syntax:  GetUni DrivePathAndFilename\n"
         "Example: GetUni U:\\WINNT\\SYSTEM32\\WSOCK32.DLL\n");
    return;
  }
  
  // Call WNetGetUniversalName with the UNIVERSAL_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using UNIVERSAL_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1],
         UNIVERSAL_NAME_INFO_LEVEL, // The structure is written to this block of memory. 
         (LPVOID) &szBuff, 
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print the location of the share, 
    //  using the pointer to UNIVERSAL_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n\n", res); 
   
  else
    _tprintf(TEXT("Universal Name: \t%s\n\n"), puni->lpUniversalName); 
    
  //
  // Call WNetGetUniversalName with the REMOTE_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using REMOTE_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1], 
         REMOTE_NAME_INFO_LEVEL, 
         (LPVOID) &szBuff,    //Structure is written to this block of memory
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print
    //  the location of the share, using 
    //  the pointer to REMOTE_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n", res); 
  else
    _tprintf(TEXT("Universal Name: \t%s\nConnection Name:\t%s\nRemaining Path: \t%s\n"),
          prni->lpUniversalName, 
          prni->lpConnectionName, 
          prni->lpRemainingPath);
  return;
}
```



 

 