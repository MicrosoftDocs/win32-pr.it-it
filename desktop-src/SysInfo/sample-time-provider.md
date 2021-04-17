---
description: Nell'esempio seguente viene illustrato come strutturare un provider di tempo. In questo esempio, la DLL supporta due provider di tempo hardware.
ms.assetid: 6be08c49-be68-4b75-b740-fc1d5a2ff592
title: Provider ora di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a5f04f7515d73f8851b764ad5758c47848b07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529634"
---
# <a name="sample-time-provider"></a><span data-ttu-id="f2017-104">Provider ora di esempio</span><span class="sxs-lookup"><span data-stu-id="f2017-104">Sample Time Provider</span></span>

<span data-ttu-id="f2017-105">Nell'esempio seguente viene illustrato come strutturare un provider di tempo.</span><span class="sxs-lookup"><span data-stu-id="f2017-105">The following example demonstrates how to structure a time provider.</span></span> <span data-ttu-id="f2017-106">In questo esempio, la DLL supporta due provider di tempo hardware.</span><span class="sxs-lookup"><span data-stu-id="f2017-106">In this example, the DLL supports two hardware time providers.</span></span>

``` syntax
#include <windows.h>
#include "timeprov.h"

// Global variables.
TimeProvSysCallbacks sc;
WCHAR ProviderName1[] = L"MyCompanyMyAppProvider1";
WCHAR ProviderName2[] = L"MyCompanyMyAppProvider2";
const TimeProvHandle htp1 = (TimeProvHandle)1;
const TimeProvHandle htp2 = (TimeProvHandle)2;

// Stores the current set of best samples.
TpcGetSamplesArgs Samples;

// Stores the polling interval the system requires to maintain clock
// stability. The provider need not poll more often.
DWORD dwPollInterval;

HRESULT CALLBACK TimeProvOpen(
   WCHAR *wszName,
   TimeProvSysCallbacks *pSysCallback,
   TimeProvHandle *phTimeProv)
{
   // Spawn a thread to read configuration information from the 
   // registry.
   ;

   // Copy the system callback pointers to a buffer.
   CopyMemory(&sc, (PVOID)pSysCallback, sizeof(TimeProvSysCallbacks));

   // Return the handle to the appropriate time provider.
   if ( lstrcmp(wszName, ProviderName1) == 0 )
      *phTimeProv = htp1;
   else *phTimeProv = htp2;

   return S_OK;
}

HRESULT CALLBACK TimeProvCommand(
   TimeProvHandle hTimeProv,
   TimeProvCmd eCmd,
   PVOID pvArgs)
{
   switch( eCmd )
   {
      case TPC_GetSamples:
      // Return the Samples structure in pvArgs.
         CopyMemory(pvArgs, &Samples, sizeof(TpcGetSamplesArgs));
         break;
      case TPC_PollIntervalChanged:
      // Retrieve the new value.
         sc.pfnGetTimeSysInfo( TSI_PollInterval, &dwPollInterval );
         break;
      case TPC_TimeJumped:
      // Discard samples saved in the Samples structure.
         ZeroMemory(&Samples, sizeof(TpcGetSamplesArgs));
         break;
      case TPC_UpdateConfig:
      // Read the configuration information from the registry.
         break;
   }
   return S_OK;
}

HRESULT CALLBACK TimeProvClose(
   TimeProvHandle hTimeProv)
{
   if( hTimeProv == htp1 )
   {
   // Terminate MyCompanyMyAppProvider1, performing any cleanup.
   ;
   }
   else
   {
   // Terminate MyCompanyMyAppProvider2, performing any cleanup.
   ;
   }

   return S_OK;
}
```

 

 



