---
title: Assegnazione di un'unità a una condivisione
description: L'esempio seguente illustra come connettere una lettera di unità a una condivisione server remota con una chiamata alla funzione WNetAddConnection2. L'esempio informa l'utente se la chiamata ha avuto esito positivo.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37095f085b3124cfaa049de4bf61ae830c94191c94c5993f7532920b122b63d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053379"
---
# <a name="assigning-a-drive-to-a-share"></a>Assegnazione di un'unità a una condivisione

L'esempio seguente illustra come connettere una lettera di unità a una condivisione server remota con una chiamata alla [**funzione WNetAddConnection2.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) L'esempio informa l'utente se la chiamata ha avuto esito positivo.

Per testare l'esempio di codice seguente, seguire questa procedura:

1.  Modificare le righe seguenti in stringhe valide:

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  Aggiungere il file a un'applicazione console denominata AddConn2.
3.  Collegare la libreria MPR. LIB nell'elenco di librerie del compilatore.
4.  Compilare ed eseguire il programma AddConn2.EXE.


```C++
#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>
#pragma comment(lib, "mpr.lib")

void main()
{
NETRESOURCE nr;
DWORD res;
TCHAR szUserName[32] = "MyUserName",
    szPassword[32] = "MyPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
//
// Assign values to the NETRESOURCE structure.
//
nr.dwType = RESOURCETYPE_ANY;
nr.lpLocalName = szLocalName;
nr.lpRemoteName = szRemoteName;
nr.lpProvider = NULL;
//
// Call the WNetAddConnection2 function to assign
//   a drive letter to the share.
//
res = WNetAddConnection2(&nr, szPassword, szUserName, FALSE);
//
// If the call succeeds, inform the user; otherwise,
//  print the error.
//
if(res == NO_ERROR)
  printf("Connection added \n", szRemoteName);
else
  printf("Error: %ld\n", res);
  return;
}
```



 

 