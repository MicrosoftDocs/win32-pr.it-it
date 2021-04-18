---
description: LSA fornisce funzioni che è possibile utilizzare per ricevere una notifica quando viene apportata una modifica ai criteri nel sistema locale.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Ricezione di eventi di modifica dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33145974ce712f21b338ba35f1571c8f3046c42c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306428"
---
# <a name="receiving-policy-change-events"></a>Ricezione di eventi di modifica dei criteri

LSA fornisce funzioni che è possibile utilizzare per ricevere una notifica quando viene apportata una modifica ai criteri nel sistema locale.

Per ricevere la notifica, creare un nuovo oggetto evento chiamando la funzione [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) e quindi chiamare la funzione [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) . L'applicazione può quindi chiamare una funzione Wait come [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)o [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) per attendere che si verifichi l'evento. La funzione wait restituisce quando si verifica l'evento o quando il periodo di timeout scade. Gli eventi di notifica vengono in genere utilizzati nelle applicazioni multithreading, in cui un thread è in attesa di un evento, mentre altri thread continuano l'elaborazione.

Quando l'applicazione non deve più ricevere notifiche, deve chiamare [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) e quindi chiamare [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per liberare l'handle dell'oggetto evento.

Nell'esempio seguente viene illustrato come un'applicazione a thread singolo può ricevere eventi di notifica quando vengono modificati i criteri di controllo del sistema.


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



Per ulteriori informazioni sugli oggetti evento, le funzioni di attesa e la sincronizzazione, vedere [utilizzo di oggetti evento](/windows/desktop/Sync/using-event-objects).

 

 
