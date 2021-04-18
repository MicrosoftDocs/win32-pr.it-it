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
# <a name="receiving-policy-change-events"></a><span data-ttu-id="67f76-103">Ricezione di eventi di modifica dei criteri</span><span class="sxs-lookup"><span data-stu-id="67f76-103">Receiving Policy Change Events</span></span>

<span data-ttu-id="67f76-104">LSA fornisce funzioni che è possibile utilizzare per ricevere una notifica quando viene apportata una modifica ai criteri nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="67f76-104">The LSA provides functions you can use to receive notification when there is a change in policy on the local system.</span></span>

<span data-ttu-id="67f76-105">Per ricevere la notifica, creare un nuovo oggetto evento chiamando la funzione [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) e quindi chiamare la funzione [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) .</span><span class="sxs-lookup"><span data-stu-id="67f76-105">To receive notification, create a new event object by calling the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function, and then call the [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) function.</span></span> <span data-ttu-id="67f76-106">L'applicazione può quindi chiamare una funzione Wait come [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)o [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) per attendere che si verifichi l'evento.</span><span class="sxs-lookup"><span data-stu-id="67f76-106">Your application can then call a wait function such as [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), or [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the event to occur.</span></span> <span data-ttu-id="67f76-107">La funzione wait restituisce quando si verifica l'evento o quando il periodo di timeout scade.</span><span class="sxs-lookup"><span data-stu-id="67f76-107">The wait function returns when the event occurs, or when the time-out period expires.</span></span> <span data-ttu-id="67f76-108">Gli eventi di notifica vengono in genere utilizzati nelle applicazioni multithreading, in cui un thread è in attesa di un evento, mentre altri thread continuano l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="67f76-108">Typically, notification events are used in multithreaded applications, in which one thread waits for an event, while other threads continue processing.</span></span>

<span data-ttu-id="67f76-109">Quando l'applicazione non deve più ricevere notifiche, deve chiamare [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) e quindi chiamare [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per liberare l'handle dell'oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="67f76-109">When your application no longer needs to receive notifications, it should call [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) and then call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to free the event object handle.</span></span>

<span data-ttu-id="67f76-110">Nell'esempio seguente viene illustrato come un'applicazione a thread singolo può ricevere eventi di notifica quando vengono modificati i criteri di controllo del sistema.</span><span class="sxs-lookup"><span data-stu-id="67f76-110">The following example shows how a single-threaded application can receive notification events when the system's auditing policy changes.</span></span>


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



<span data-ttu-id="67f76-111">Per ulteriori informazioni sugli oggetti evento, le funzioni di attesa e la sincronizzazione, vedere [utilizzo di oggetti evento](/windows/desktop/Sync/using-event-objects).</span><span class="sxs-lookup"><span data-stu-id="67f76-111">For more information about event objects, wait functions, and synchronization, see [Using Event Objects](/windows/desktop/Sync/using-event-objects).</span></span>

 

 
