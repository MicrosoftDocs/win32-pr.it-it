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
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Uso di timer waitable con una chiamata di procedura asincrona

Nell'esempio seguente viene associata una funzione di [chiamata di procedura asincrona](asynchronous-procedure-calls.md) (APC), nota anche come routine di completamento, con un [timer waitable](waitable-timer-objects.md) quando il timer è impostato. L'indirizzo della routine di completamento è il quarto parametro della funzione [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) . Il quinto parametro è un puntatore void che è possibile usare per passare argomenti alla routine di completamento.

La routine di completamento verrà eseguita dallo stesso thread che ha chiamato [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Questo thread deve essere in uno stato di avviso per eseguire la routine di completamento. Questa operazione viene eseguita chiamando la funzione [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , che è una funzione inviabile come avviso.

Ogni thread ha una coda APC. Se è presente una voce nella coda APC del thread nel momento in cui viene chiamata una delle funzioni alertable, il thread non viene messo in sospensione. Al contrario, la voce viene rimossa dalla coda APC e viene chiamata la routine di completamento.

Se nella coda APC non è presente alcuna voce, il thread viene sospeso fino a quando l'attesa non viene soddisfatta. L'attesa può essere soddisfatta aggiungendo una voce alla coda APC, da un timeout o da un handle che diventa segnalato. Se l'attesa viene soddisfatta da una voce nella coda APC, il thread viene riattivato e viene chiamata la routine di completamento. In questo caso, il valore restituito della funzione è il **\_ \_ completamento** i/o di attesa.

Dopo l'esecuzione della routine di completamento, il sistema controlla la presenza di un'altra voce nella coda APC da elaborare. Una funzione alertable restituirà solo dopo l'elaborazione di tutte le voci APC. Se pertanto le voci vengono aggiunte alla coda APC più velocemente di quanto possano essere elaborate, è possibile che una chiamata a una funzione segnalabile non venga mai restituita. Questa operazione è particolarmente utile con i timer in attesa, se il periodo è più breve della quantità di tempo necessaria per eseguire la routine di completamento.

Quando si usa un timer waitable con un APC, il thread che imposta il timer non deve attendere l'handle del timer. In questo modo, il thread verrà riattivato come risultato del timer che diventa segnalato anziché come il risultato di una voce aggiunta alla coda APC. Di conseguenza, il thread non è più in uno stato di avviso e la routine di completamento non viene chiamata. Nel codice seguente, la chiamata a [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) risveglia il thread quando una voce viene aggiunta alla coda APC del thread dopo che il timer è impostato sullo stato segnalato.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di oggetti timer waitable](using-waitable-timer-objects.md)
</dt> </dl>

 

 
