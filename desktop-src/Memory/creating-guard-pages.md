---
description: Una pagina di protezione fornisce un allarme con un solo colpo per l'accesso alla pagina di memoria.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Creazione di pagine di protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee4d4a44a6e64d6af81e4b847347f357c3590edbd7e6b806e8f32653e1f869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963291"
---
# <a name="creating-guard-pages"></a>Creazione di pagine di protezione

Una pagina di protezione fornisce un allarme con un solo colpo per l'accesso alla pagina di memoria. Ciò può essere utile per un'applicazione che deve monitorare l'aumento delle strutture di dati dinamici di grandi dimensioni. Ad esempio, esistono sistemi operativi che usano pagine di protezione per implementare il controllo automatico dello stack.

Per creare una pagina di protezione, impostare il modificatore di protezione della pagina **PAGE \_ GUARD** per la pagina. Questo valore può essere specificato, insieme ad altri modificatori di protezione della pagina, nelle funzioni [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)e [**VirtualProtectEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) Il **\_ modificatore PAGE GUARD può** essere usato con qualsiasi altro modificatore di protezione della pagina, ad eccezione **di PAGE \_ NOACCESS**.

Se un programma tenta di accedere a un indirizzo all'interno di una pagina di protezione, il sistema genera un'eccezione **STATUS \_ GUARD PAGE \_ \_ VIOLATION** (0x80000001). Il sistema cancella anche il modificatore **PAGE \_ GUARD,** rimuovendo lo stato della pagina di protezione della pagina di memoria. Il sistema non arresterà il tentativo successivo di accedere alla pagina di memoria con **un'eccezione DI \_ \_ VIOLAZIONE DI PAGINA DI \_ STATUS GUARD.**

Se si verifica un'eccezione di guard page durante un servizio di sistema, il servizio ha esito negativo e in genere restituisce un indicatore di stato dell'errore. Poiché il sistema rimuove anche lo stato della pagina di protezione della pagina di memoria pertinente, la chiamata successiva dello stesso servizio di sistema non avrà esito negativo a causa di un'eccezione DI VIOLAZIONE DI PAGINA DI **STATUS \_ GUARD \_ \_** (a meno che, naturalmente, qualcuno non ristabilisca la pagina di protezione).

Il programma breve seguente illustra il comportamento della protezione delle pagine di protezione.


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



Il primo tentativo di bloccare il blocco di memoria ha esito negativo, generando **un'eccezione STATUS GUARD PAGE \_ \_ \_ VIOLATION.** Il secondo tentativo ha esito positivo, perché la protezione della pagina di protezione del blocco di memoria è stata disattivata dal primo tentativo.

 

 
