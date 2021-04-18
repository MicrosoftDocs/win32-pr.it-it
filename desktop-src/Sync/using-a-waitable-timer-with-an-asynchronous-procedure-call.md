---
description: Nell'esempio seguente viene associata una funzione di chiamata di procedura asincrona (APC), nota anche come routine di completamento, con un timer waitable quando il timer è impostato.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Uso di timer waitable con una chiamata di procedura asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628288b1c5e1ce7c83e104cf6daa9e6fdcc3eb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312744"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a><span data-ttu-id="2bd19-103">Uso di timer waitable con una chiamata di procedura asincrona</span><span class="sxs-lookup"><span data-stu-id="2bd19-103">Using Waitable Timers with an Asynchronous Procedure Call</span></span>

<span data-ttu-id="2bd19-104">Nell'esempio seguente viene associata una funzione di [chiamata di procedura asincrona](asynchronous-procedure-calls.md) (APC), nota anche come routine di completamento, con un [timer waitable](waitable-timer-objects.md) quando il timer è impostato.</span><span class="sxs-lookup"><span data-stu-id="2bd19-104">The following example associates an [asynchronous procedure call](asynchronous-procedure-calls.md) (APC) function, also known as a completion routine, with a [waitable timer](waitable-timer-objects.md) when the timer is set.</span></span> <span data-ttu-id="2bd19-105">L'indirizzo della routine di completamento è il quarto parametro della funzione [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) .</span><span class="sxs-lookup"><span data-stu-id="2bd19-105">The address of the completion routine is the fourth parameter to the [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) function.</span></span> <span data-ttu-id="2bd19-106">Il quinto parametro è un puntatore void che è possibile usare per passare argomenti alla routine di completamento.</span><span class="sxs-lookup"><span data-stu-id="2bd19-106">The fifth parameter is a void pointer that you can use to pass arguments to the completion routine.</span></span>

<span data-ttu-id="2bd19-107">La routine di completamento verrà eseguita dallo stesso thread che ha chiamato [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span><span class="sxs-lookup"><span data-stu-id="2bd19-107">The completion routine will be executed by the same thread that called [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span></span> <span data-ttu-id="2bd19-108">Questo thread deve essere in uno stato di avviso per eseguire la routine di completamento.</span><span class="sxs-lookup"><span data-stu-id="2bd19-108">This thread must be in an alertable state to execute the completion routine.</span></span> <span data-ttu-id="2bd19-109">Questa operazione viene eseguita chiamando la funzione [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , che è una funzione inviabile come avviso.</span><span class="sxs-lookup"><span data-stu-id="2bd19-109">It accomplishes this by calling the [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) function, which is an alertable function.</span></span>

<span data-ttu-id="2bd19-110">Ogni thread ha una coda APC.</span><span class="sxs-lookup"><span data-stu-id="2bd19-110">Each thread has an APC queue.</span></span> <span data-ttu-id="2bd19-111">Se è presente una voce nella coda APC del thread nel momento in cui viene chiamata una delle funzioni alertable, il thread non viene messo in sospensione.</span><span class="sxs-lookup"><span data-stu-id="2bd19-111">If there is an entry in the thread's APC queue at the time that one of the alertable functions is called, the thread is not put to sleep.</span></span> <span data-ttu-id="2bd19-112">Al contrario, la voce viene rimossa dalla coda APC e viene chiamata la routine di completamento.</span><span class="sxs-lookup"><span data-stu-id="2bd19-112">Instead, the entry is removed from the APC queue and the completion routine is called.</span></span>

<span data-ttu-id="2bd19-113">Se nella coda APC non è presente alcuna voce, il thread viene sospeso fino a quando l'attesa non viene soddisfatta.</span><span class="sxs-lookup"><span data-stu-id="2bd19-113">If no entry exists in the APC queue, the thread is suspended until the wait is satisfied.</span></span> <span data-ttu-id="2bd19-114">L'attesa può essere soddisfatta aggiungendo una voce alla coda APC, da un timeout o da un handle che diventa segnalato.</span><span class="sxs-lookup"><span data-stu-id="2bd19-114">The wait can be satisfied by adding an entry to the APC queue, by a timeout, or by a handle becoming signaled.</span></span> <span data-ttu-id="2bd19-115">Se l'attesa viene soddisfatta da una voce nella coda APC, il thread viene riattivato e viene chiamata la routine di completamento.</span><span class="sxs-lookup"><span data-stu-id="2bd19-115">If the wait is satisfied by an entry in the APC queue, the thread is awakened and the completion routine is called.</span></span> <span data-ttu-id="2bd19-116">In questo caso, il valore restituito della funzione è il **\_ \_ completamento** i/o di attesa.</span><span class="sxs-lookup"><span data-stu-id="2bd19-116">In this case, the return value of the function is **WAIT\_IO\_COMPLETION**.</span></span>

<span data-ttu-id="2bd19-117">Dopo l'esecuzione della routine di completamento, il sistema controlla la presenza di un'altra voce nella coda APC da elaborare.</span><span class="sxs-lookup"><span data-stu-id="2bd19-117">After the completion routine is executed, the system checks for another entry in the APC queue to process.</span></span> <span data-ttu-id="2bd19-118">Una funzione alertable restituirà solo dopo l'elaborazione di tutte le voci APC.</span><span class="sxs-lookup"><span data-stu-id="2bd19-118">An alertable function will return only after all APC entries have been processed.</span></span> <span data-ttu-id="2bd19-119">Se pertanto le voci vengono aggiunte alla coda APC più velocemente di quanto possano essere elaborate, è possibile che una chiamata a una funzione segnalabile non venga mai restituita.</span><span class="sxs-lookup"><span data-stu-id="2bd19-119">Therefore, if entries are being added to the APC queue faster than they can be processed, it is possible that a call to an alertable function will never return.</span></span> <span data-ttu-id="2bd19-120">Questa operazione è particolarmente utile con i timer in attesa, se il periodo è più breve della quantità di tempo necessaria per eseguire la routine di completamento.</span><span class="sxs-lookup"><span data-stu-id="2bd19-120">This is especially possible with waitable timers, if the period is shorter than the amount of time required to execute the completion routine.</span></span>

<span data-ttu-id="2bd19-121">Quando si usa un timer waitable con un APC, il thread che imposta il timer non deve attendere l'handle del timer.</span><span class="sxs-lookup"><span data-stu-id="2bd19-121">When you are using a waitable timer with an APC, the thread that sets the timer should not wait on the handle of the timer.</span></span> <span data-ttu-id="2bd19-122">In questo modo, il thread verrà riattivato come risultato del timer che diventa segnalato anziché come il risultato di una voce aggiunta alla coda APC.</span><span class="sxs-lookup"><span data-stu-id="2bd19-122">By doing so, you would cause the thread to wake up as a result of the timer becoming signaled rather than as the result of an entry being added to the APC queue.</span></span> <span data-ttu-id="2bd19-123">Di conseguenza, il thread non è più in uno stato di avviso e la routine di completamento non viene chiamata.</span><span class="sxs-lookup"><span data-stu-id="2bd19-123">As a result, the thread is no longer in an alertable state and the completion routine is not called.</span></span> <span data-ttu-id="2bd19-124">Nel codice seguente, la chiamata a [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) risveglia il thread quando una voce viene aggiunta alla coda APC del thread dopo che il timer è impostato sullo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="2bd19-124">In the following code, the call to [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) awakens the thread when an entry is added to the thread's APC queue after the timer is set to the signaled state.</span></span>


```C++
#define UNICODE 1
#define _UNICODE 1

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define _SECOND 10000000

typedef struct _MYDATA {
   TCHAR *szText;
   DWORD dwValue;
} MYDATA;

VOID CALLBACK TimerAPCProc(
   LPVOID lpArg,               // Data value
   DWORD dwTimerLowValue,      // Timer low value
   DWORD dwTimerHighValue )    // Timer high value

{
   // Formal parameters not used in this example.
   UNREFERENCED_PARAMETER(dwTimerLowValue);
   UNREFERENCED_PARAMETER(dwTimerHighValue);

   MYDATA *pMyData = (MYDATA *)lpArg;

   _tprintf( TEXT("Message: %s\nValue: %d\n\n"), pMyData->szText,
          pMyData->dwValue );
   MessageBeep(0);

}

int main( void ) 
{
   HANDLE          hTimer;
   BOOL            bSuccess;
   __int64         qwDueTime;
   LARGE_INTEGER   liDueTime;
   MYDATA          MyData;

   MyData.szText = TEXT("This is my data");
   MyData.dwValue = 100;

   hTimer = CreateWaitableTimer(
           NULL,                   // Default security attributes
           FALSE,                  // Create auto-reset timer
           TEXT("MyTimer"));       // Name of waitable timer
   if (hTimer != NULL)
   {
      __try 
      {
         // Create an integer that will be used to signal the timer 
         // 5 seconds from now.
         qwDueTime = -5 * _SECOND;

         // Copy the relative time into a LARGE_INTEGER.
         liDueTime.LowPart  = (DWORD) ( qwDueTime & 0xFFFFFFFF );
         liDueTime.HighPart = (LONG)  ( qwDueTime >> 32 );

         bSuccess = SetWaitableTimer(
            hTimer,           // Handle to the timer object
            &liDueTime,       // When timer will become signaled
            2000,             // Periodic timer interval of 2 seconds
            TimerAPCProc,     // Completion routine
            &MyData,          // Argument to the completion routine
            FALSE );          // Do not restore a suspended system

         if ( bSuccess ) 
         {
            for ( ; MyData.dwValue < 1000; MyData.dwValue += 100 ) 
            {
               SleepEx(
                  INFINITE,     // Wait forever
                  TRUE );       // Put thread in an alertable state
            }

         } 
         else 
         {
            printf("SetWaitableTimer failed with error %d\n", GetLastError());
         }

      } 
      __finally 
      {
         CloseHandle( hTimer );
      }
   } 
   else 
   {
      printf("CreateWaitableTimer failed with error %d\n", GetLastError());
   }

   return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="2bd19-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bd19-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd19-126">Uso di oggetti timer waitable</span><span class="sxs-lookup"><span data-stu-id="2bd19-126">Using Waitable Timer Objects</span></span>](using-waitable-timer-objects.md)
</dt> </dl>

 

 
