---
description: Nell'esempio seguente viene associata una funzione APC (Asynchronous Procedure Call), nota anche come routine di completamento, a un timer waitable quando viene impostato il timer.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Uso di timer waitable con una chiamata di procedura asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62436011a3da0ac17525a0ce977e7bcd25382c5c267b62b9c972381e0f28562d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661151"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Uso di timer waitable con una chiamata di procedura asincrona

Nell'esempio seguente viene associata una funzione APC [(Asynchronous Procedure Call),](asynchronous-procedure-calls.md) nota anche come routine di completamento, a un [timer waitable](waitable-timer-objects.md) quando viene impostato il timer. L'indirizzo della routine di completamento è il quarto parametro della [**funzione SetWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) Il quinto parametro è un puntatore void che è possibile usare per passare argomenti alla routine di completamento.

La routine di completamento verrà eseguita dallo stesso thread che ha chiamato [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Questo thread deve essere in uno stato di avviso per eseguire la routine di completamento. A tale scopo, chiamare la [**funzione SleepEx,**](/windows/win32/api/synchapi/nf-synchapi-sleepex) che è una funzione di avviso.

Ogni thread ha una coda APC. Se è presente una voce nella coda APC del thread al momento della chiamata a una delle funzioni di avviso, il thread non viene messo in sospensione. Al contrario, la voce viene rimossa dalla coda APC e viene chiamata la routine di completamento.

Se non esiste alcuna voce nella coda APC, il thread viene sospeso fino a quando non viene soddisfatta l'attesa. L'attesa può essere soddisfatta aggiungendo una voce alla coda APC, da un timeout o da un handle che diventa segnalato. Se l'attesa viene soddisfatta da una voce nella coda APC, il thread viene svegliato e viene chiamata la routine di completamento. In questo caso, il valore restituito della funzione è **WAIT \_ IO \_ COMPLETION.**

Dopo l'esecuzione della routine di completamento, il sistema verifica la presenza di un'altra voce nella coda APC da elaborare. Una funzione di avviso restituirà solo dopo l'elaborazione di tutte le voci APC. Pertanto, se le voci vengono aggiunte alla coda APC più velocemente di quanto possano essere elaborate, è possibile che una chiamata a una funzione che invia avvisi non restituirà mai . Ciò è particolarmente possibile con i timer waitable, se il periodo è più breve del tempo necessario per eseguire la routine di completamento.

Quando si usa un timer waitable con un APC, il thread che imposta il timer non deve attendere l'handle del timer. In questo modo, il thread viene riattivato in seguito alla segnalazione del timer anziché come risultato dell'aggiunta di una voce alla coda APC. Di conseguenza, il thread non è più in uno stato di avviso e la routine di completamento non viene chiamata. Nel codice seguente, la chiamata a [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) risveglierà il thread quando viene aggiunta una voce alla coda APC del thread dopo che il timer è stato impostato sullo stato segnalato.


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

 

 
