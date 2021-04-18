---
description: Una pagina Guard fornisce un allarme monouso per l'accesso alle pagine di memoria.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Creazione di pagine Guard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10768da75090a28ffecd5302d88dbc142ae9c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307265"
---
# <a name="creating-guard-pages"></a>Creazione di pagine Guard

Una pagina Guard fornisce un allarme monouso per l'accesso alle pagine di memoria. Questa operazione può essere utile per un'applicazione che deve monitorare la crescita di strutture di dati dinamiche di grandi dimensioni. Esistono, ad esempio, sistemi operativi che usano le pagine di Guard per implementare il controllo dello stack automatico.

Per creare una pagina di protezione, impostare il modificatore di protezione della pagina **Page \_ Guard** per la pagina. Questo valore può essere specificato, insieme ad altri modificatori di protezione della pagina, nelle funzioni [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)e [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) . Il modificatore di pagina può essere utilizzato con qualsiasi altro modificatore di protezione della pagina, ad eccezione della **pagina \_ NoAccess**. **\_**

Se un programma tenta di accedere a un indirizzo all'interno di una pagina di protezione, il sistema genera un'eccezione 0x80000001 ( **status \_ Guard \_ Page \_ violazioni** ). Il sistema cancella inoltre il modificatore di **Page \_ Guard** , rimuovendo lo stato della pagina di protezione della pagina di memoria. Il sistema non arresterà il tentativo successivo di accedere alla pagina di memoria con un'eccezione di violazione della pagina relativa alla **protezione dello stato \_ \_ \_** .

Se si verifica un'eccezione della pagina Guard durante un servizio di sistema, il servizio ha esito negativo e in genere restituisce un indicatore di stato di errore. Poiché il sistema rimuove anche lo stato della pagina di protezione della pagina di memoria pertinente, la chiamata successiva dello stesso servizio di sistema non riuscirà a causa di un'eccezione di **\_ violazione della \_ pagina \_ di protezione dello stato** (a meno che qualcuno ristabilisca la pagina di protezione).

Il breve programma seguente illustra il comportamento della protezione della pagina Guard.


```C++
/* A program to demonstrate the use of guard pages of memory. Allocate
   a page of memory as a guard page, then try to access the page. That
   will fail, but doing so releases the lock on the guard page, so the
   next access works correctly.

   The output will look like this. The actual address may vary.

   This computer has a page size of 4096.
   Committed 4096 bytes at address 0x00520000
   Cannot lock at 00520000, error = 0x80000001
   2nd Lock Achieved at 00520000

   This sample does not show how to use the guard page fault to
   "grow" a dynamic array, such as a stack. */

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <tchar.h>

int main()
{
  LPVOID lpvAddr;               // address of the test memory
  DWORD dwPageSize;             // amount of memory to allocate.
  BOOL bLocked;                 // address of the guarded memory
  SYSTEM_INFO sSysInfo;         // useful information about the system

  GetSystemInfo(&sSysInfo);     // initialize the structure

  _tprintf(TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

  dwPageSize = sSysInfo.dwPageSize;

  // Try to allocate the memory.

  lpvAddr = VirtualAlloc(NULL, dwPageSize,
                         MEM_RESERVE | MEM_COMMIT,
                         PAGE_READONLY | PAGE_GUARD);

  if(lpvAddr == NULL) {
    _tprintf(TEXT("VirtualAlloc failed. Error: %ld\n"),
             GetLastError());
    return 1;

  } else {
    _ftprintf(stderr, TEXT("Committed %lu bytes at address 0x%lp\n"),
              dwPageSize, lpvAddr);
  }

  // Try to lock the committed memory. This fails the first time 
  // because of the guard page.

  bLocked = VirtualLock(lpvAddr, dwPageSize);
  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot lock at %lp, error = 0x%lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("Lock Achieved at %lp\n"), lpvAddr);
  }

  // Try to lock the committed memory again. This succeeds the second
  // time because the guard page status was removed by the first 
  // access attempt.

  bLocked = VirtualLock(lpvAddr, dwPageSize);

  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot get 2nd lock at %lp, error = %lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("2nd Lock Achieved at %lp\n"), lpvAddr);
  }

  return 0;
}
```



Il primo tentativo di blocco del blocco di memoria ha esito negativo, generando un'eccezione di **\_ violazione della \_ pagina \_ status Guard** . Il secondo tentativo ha esito positivo, perché la protezione della pagina Guard del blocco di memoria è stata disattivata dal primo tentativo.

 

 
