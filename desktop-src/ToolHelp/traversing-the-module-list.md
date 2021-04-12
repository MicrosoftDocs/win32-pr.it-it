---
title: Attraversamento dell'elenco dei moduli
description: Nell'esempio seguente viene ottenuto un elenco di moduli per il processo specificato.
ms.assetid: 8efe1e13-6222-496a-bff3-90f53b03c750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be7df4d992b8958a09ec92f722cd7bb9c151f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396451"
---
# <a name="traversing-the-module-list"></a><span data-ttu-id="aaebf-103">Attraversamento dell'elenco dei moduli</span><span class="sxs-lookup"><span data-stu-id="aaebf-103">Traversing the Module List</span></span>

<span data-ttu-id="aaebf-104">Nell'esempio seguente viene ottenuto un elenco di moduli per il processo specificato.</span><span class="sxs-lookup"><span data-stu-id="aaebf-104">The following example obtains a list of modules for the specified process.</span></span> <span data-ttu-id="aaebf-105">La `ListProcessModules` funzione acquisisce uno snapshot dei moduli associati a un determinato processo usando la funzione [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) e quindi esamina l'elenco usando le funzioni [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) e [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) .</span><span class="sxs-lookup"><span data-stu-id="aaebf-105">The `ListProcessModules` function takes a snapshot of the modules associated with a given process using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) and [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) functions.</span></span> <span data-ttu-id="aaebf-106">Il `dwPID` parametro di `ListProcessModules` identifica il processo per il quale devono essere enumerati i moduli e viene in genere ottenuto chiamando **CreateToolhelp32Snapshot** per enumerare i processi in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="aaebf-106">The `dwPID` parameter of `ListProcessModules` identifies the process for which modules are to be enumerated, and is usually obtained by calling **CreateToolhelp32Snapshot** to enumerate the processes running on the system.</span></span> <span data-ttu-id="aaebf-107">Vedere [acquisizione di uno snapshot e visualizzazione dei processi](taking-a-snapshot-and-viewing-processes.md) per una semplice applicazione console che usa questa funzione.</span><span class="sxs-lookup"><span data-stu-id="aaebf-107">See [Taking a Snapshot and Viewing Processes](taking-a-snapshot-and-viewing-processes.md) for a simple console application that uses this function.</span></span>

<span data-ttu-id="aaebf-108">Una semplice funzione di segnalazione degli errori, `printError` , Visualizza la causa di eventuali errori, che in genere risultano da restrizioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="aaebf-108">A simple error-reporting function, `printError`, displays the reason for any failures, which usually result from security restrictions.</span></span>


```C++
#include <windows.h> 
#include <tlhelp32.h> 
#include <tchar.h> 
 
//  Forward declarations: 
BOOL ListProcessModules( DWORD dwPID ); 
void printError( TCHAR* msg ); 
 
int main( void )
{
  ListProcessModules(GetCurrentProcessId() );
  return 0;
}

BOOL ListProcessModules( DWORD dwPID ) 
{ 
  HANDLE hModuleSnap = INVALID_HANDLE_VALUE; 
  MODULEENTRY32 me32; 
 
//  Take a snapshot of all modules in the specified process. 
  hModuleSnap = CreateToolhelp32Snapshot( TH32CS_SNAPMODULE, dwPID ); 
  if( hModuleSnap == INVALID_HANDLE_VALUE ) 
  { 
    printError( TEXT("CreateToolhelp32Snapshot (of modules)") ); 
    return( FALSE ); 
  } 
 
//  Set the size of the structure before using it. 
  me32.dwSize = sizeof( MODULEENTRY32 ); 
 
//  Retrieve information about the first module, 
//  and exit if unsuccessful 
  if( !Module32First( hModuleSnap, &me32 ) ) 
  { 
    printError( TEXT("Module32First") );  // Show cause of failure 
    CloseHandle( hModuleSnap );     // Must clean up the snapshot object! 
    return( FALSE ); 
  } 
 
//  Now walk the module list of the process, 
//  and display information about each module 
  do 
  { 
    _tprintf( TEXT("\n\n     MODULE NAME:     %s"),             me32.szModule ); 
    _tprintf( TEXT("\n     executable     = %s"),             me32.szExePath ); 
    _tprintf( TEXT("\n     process ID     = 0x%08X"),         me32.th32ProcessID ); 
    _tprintf( TEXT("\n     ref count (g)  =     0x%04X"),     me32.GlblcntUsage ); 
    _tprintf( TEXT("\n     ref count (p)  =     0x%04X"),     me32.ProccntUsage ); 
    _tprintf( TEXT("\n     base address   = 0x%08X"), (DWORD) me32.modBaseAddr ); 
    _tprintf( TEXT("\n     base size      = %d"),             me32.modBaseSize ); 
 
  } while( Module32Next( hModuleSnap, &me32 ) ); 

    _tprintf( TEXT("\n"));
 
//  Do not forget to clean up the snapshot object. 
  CloseHandle( hModuleSnap ); 
  return( TRUE ); 
} 
 
 
void printError( TCHAR* msg )
{
  DWORD eNum;
  TCHAR sysMsg[256];
  TCHAR* p;

  eNum = GetLastError( );
  FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS,
         NULL, eNum,
         MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // Default language
         sysMsg, 256, NULL );

  // Trim the end of the line and terminate it with a null
  p = sysMsg;
  while( ( *p > 31 ) || ( *p == 9 ) )
    ++p;
  do { *p-- = 0; } while( ( p >= sysMsg ) &&
                          ( ( *p == '.' ) || ( *p < 33 ) ) );

  // Display the message
  _tprintf( TEXT("\n  WARNING: %s failed with error %d (%s)"), msg, eNum, sysMsg );
}
```



## <a name="related-topics"></a><span data-ttu-id="aaebf-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aaebf-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaebf-110">Esplorazione del modulo</span><span class="sxs-lookup"><span data-stu-id="aaebf-110">Module Walking</span></span>](module-walking.md)
</dt> </dl>

 

 




