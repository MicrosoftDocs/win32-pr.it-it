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
# <a name="determining-the-location-of-a-share"></a><span data-ttu-id="7a637-103">Determinazione del percorso di una condivisione</span><span class="sxs-lookup"><span data-stu-id="7a637-103">Determining the Location of a Share</span></span>

<span data-ttu-id="7a637-104">Nell'esempio seguente viene illustrato come chiamare la funzione [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) per determinare il percorso di una condivisione in un'unità reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="7a637-104">The following example demonstrates how to call the [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) function to determine the location of a share on a redirected drive.</span></span>

<span data-ttu-id="7a637-105">Innanzitutto, nell'esempio di codice viene chiamata la funzione **WNetGetUniversalName** , specificando il livello di informazioni del [**nome universale per recuperare un puntatore a una stringa \_ \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) del nome Universal Naming Convention (UNC) per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7a637-105">First the code sample calls the **WNetGetUniversalName** function, specifying the [**UNIVERSAL\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) information level to retrieve a pointer to a Universal Naming Convention (UNC) name string for the resource.</span></span> <span data-ttu-id="7a637-106">L'esempio chiama quindi **WNetGetUniversalName** una seconda volta, specificando il livello informazioni sul [**\_ nome remoto \_**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) per recuperare due stringhe di informazioni di connessione di rete aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="7a637-106">Then the sample calls **WNetGetUniversalName** a second time, specifying the [**REMOTE\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) information level to retrieve two additional network connection information strings.</span></span> <span data-ttu-id="7a637-107">Se le chiamate hanno esito positivo, l'esempio stampa il percorso della condivisione.</span><span class="sxs-lookup"><span data-stu-id="7a637-107">If the calls are successful, the sample prints the location of the share.</span></span>

<span data-ttu-id="7a637-108">Per testare l'esempio di codice seguente, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="7a637-108">To test the following code sample, perform the following steps:</span></span>

1.  <span data-ttu-id="7a637-109">Denominare l'esempio di codice GetUni. cpp.</span><span class="sxs-lookup"><span data-stu-id="7a637-109">Name the code sample GetUni.cpp.</span></span>
2.  <span data-ttu-id="7a637-110">Aggiungere l'esempio a un'applicazione console denominata GetUni.</span><span class="sxs-lookup"><span data-stu-id="7a637-110">Add the sample to a console application called GetUni.</span></span>
3.  <span data-ttu-id="7a637-111">Collegare le librerie shell32. lib, MPR. lib e NetApi32. lib all'elenco di librerie del compilatore.</span><span class="sxs-lookup"><span data-stu-id="7a637-111">Link the libraries Shell32.lib, Mpr.lib, and NetApi32.lib to the compiler list of libraries.</span></span>
4.  <span data-ttu-id="7a637-112">Al prompt dei comandi passare alla directory GetUni</span><span class="sxs-lookup"><span data-stu-id="7a637-112">From the command prompt, change to the GetUni directory.</span></span>
5.  <span data-ttu-id="7a637-113">Compilare GetUni. cpp.</span><span class="sxs-lookup"><span data-stu-id="7a637-113">Compile GetUni.cpp.</span></span>
6.  <span data-ttu-id="7a637-114">Eseguire il file GetUni.exe seguito da una lettera di unità e due punti, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="7a637-114">Run the file GetUni.exe followed by a drive letter and colon, like this:</span></span>

    <span data-ttu-id="7a637-115">**GetUni H:\\**</span><span class="sxs-lookup"><span data-stu-id="7a637-115">**GetUni H:\\**</span></span>


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



 

 