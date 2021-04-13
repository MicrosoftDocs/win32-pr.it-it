---
title: Assegnazione di un'unità a una condivisione
description: Nell'esempio seguente viene illustrato come connettere una lettera di unità a una condivisione server remota con una chiamata alla funzione WNetAddConnection2. Nell'esempio viene segnalata all'utente se la chiamata ha avuto esito positivo o negativo.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cb4c930250f74cc549d9b5a31f121b92abad0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399368"
---
# <a name="assigning-a-drive-to-a-share"></a><span data-ttu-id="9fb9a-104">Assegnazione di un'unità a una condivisione</span><span class="sxs-lookup"><span data-stu-id="9fb9a-104">Assigning a Drive to a Share</span></span>

<span data-ttu-id="9fb9a-105">Nell'esempio seguente viene illustrato come connettere una lettera di unità a una condivisione server remota con una chiamata alla funzione [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) .</span><span class="sxs-lookup"><span data-stu-id="9fb9a-105">The following example demonstrates how to connect a drive letter to a remote server share with a call to the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function.</span></span> <span data-ttu-id="9fb9a-106">Nell'esempio viene segnalata all'utente se la chiamata ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="9fb9a-106">The sample informs the user whether or not the call was successful.</span></span>

<span data-ttu-id="9fb9a-107">Per testare l'esempio di codice seguente, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="9fb9a-107">To test the following code sample, perform the following steps:</span></span>

1.  <span data-ttu-id="9fb9a-108">Modificare le righe seguenti in stringhe valide:</span><span class="sxs-lookup"><span data-stu-id="9fb9a-108">Change the following lines to valid strings:</span></span>

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  <span data-ttu-id="9fb9a-109">Aggiungere il file a un'applicazione console denominata AddConn2.</span><span class="sxs-lookup"><span data-stu-id="9fb9a-109">Add the file to a console application called AddConn2.</span></span>
3.  <span data-ttu-id="9fb9a-110">Collegare la libreria MPR. LIB all'elenco di librerie del compilatore.</span><span class="sxs-lookup"><span data-stu-id="9fb9a-110">Link the library MPR.LIB to the compiler list of libraries.</span></span>
4.  <span data-ttu-id="9fb9a-111">Compilare ed eseguire il programma AddConn2.EXE.</span><span class="sxs-lookup"><span data-stu-id="9fb9a-111">Compile and run the program AddConn2.EXE.</span></span>


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



 

 