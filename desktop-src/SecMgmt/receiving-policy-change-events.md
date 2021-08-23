---
description: L'LSA fornisce funzioni che è possibile usare per ricevere notifiche in caso di modifica dei criteri nel sistema locale.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Ricezione di eventi di modifica dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1fc2328d0467dcfe5b6f85b9b8384cf4c8271d35fcda106a61ae5bb068f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005049"
---
# <a name="receiving-policy-change-events"></a>Ricezione di eventi di modifica dei criteri

L'LSA fornisce funzioni che è possibile usare per ricevere notifiche in caso di modifica dei criteri nel sistema locale.

Per ricevere la notifica, creare un nuovo oggetto evento chiamando la [**funzione CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) e quindi chiamare la [**funzione LsaRegisterPolicyChangeNotification.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) L'applicazione può quindi chiamare una funzione di attesa, ad esempio [**WaitForSingleObject,**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)o [**RegisterWaitForSingleObject,**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) per attendere che si verifichi l'evento. La funzione wait restituisce quando si verifica l'evento o quando scade il periodo di timeout. In genere, gli eventi di notifica vengono usati nelle applicazioni multithreading, in cui un thread attende un evento, mentre altri thread continuano l'elaborazione.

Quando l'applicazione non deve più ricevere notifiche, deve chiamare [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) e quindi [**chiamare CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per liberare l'handle dell'oggetto evento.

L'esempio seguente illustra come un'applicazione a thread singolo può ricevere eventi di notifica quando i criteri di controllo del sistema cambiano.


```C++
#include <windows.h>
#include <stdio.h>

void WaitForPolicyChanges()
{
  HANDLE hEvent;
  NTSTATUS ntsResult;
  DWORD dwResult;

  // Create an event object.
  hEvent = CreateEvent( 
    NULL,  // child processes cannot inherit 
    FALSE, // automatically reset event
    FALSE, // start as a nonsignaled event
    NULL   // do not need a name
  );

  // Check that the event was created.
  if (hEvent == NULL) 
  {
    wprintf(L"Event object creation failed: %d\n",GetLastError());
    return;
  }
  // Register to receive auditing policy change notifications.
  ntsResult = LsaRegisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );
  if (STATUS_SUCCESS != ntsResult)
  {
    wprintf(L"LsaRegisterPolicyChangeNotification failed.\n");
    CloseHandle(hEvent);
    return;
  }

  // Wait for the event to be triggered.
  dwResult = WaitForSingleObject( 
    hEvent, // handle to the event object
    300000  // time-out interval, in milliseconds
  );

  // The wait function returned.
  if (dwResult == WAIT_OBJECT_0)
  {  // received the notification signal
    wprintf(L"Notification received.\n");
  } 
  else 
  {  // received a time-out or error
    wprintf(L"Notification was not received.\n");
  }
  // Unregister for notification.
  LsaUnregisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );

  // Free the event handle.
  CloseHandle(hEvent);
}
```



Per altre informazioni su oggetti evento, funzioni di attesa e sincronizzazione, vedere [Uso di oggetti evento](/windows/desktop/Sync/using-event-objects).

 

 
