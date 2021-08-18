---
description: Quando una funzione Handler viene chiamata dal thread del dispatcher, gestisce il codice di controllo passato nel parametro Opcode e quindi chiama la funzione ReportSvcStatus per aggiornare lo stato del servizio.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Scrittura di una funzione del gestore di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bf8ab32edb73fdf11f3f0370a512b17b143b8af219a2bd539e59bdf062a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888062"
---
# <a name="writing-a-control-handler-function"></a>Scrittura di una funzione del gestore di controllo

Quando una [**funzione Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) viene chiamata dal thread del dispatcher, gestisce il codice di controllo passato nel parametro *Opcode* e quindi chiama la funzione ReportSvcStatus per aggiornare lo stato del servizio. Quando una [**funzione Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) riceve un codice di controllo, deve segnalare lo stato del servizio solo se la gestione del codice di controllo causa la modifica dello stato del servizio. Se il servizio non agisce sul controllo, non deve segnalare lo stato a Gestione controllo servizi. Per il codice sorgente per ReportSvcStatus, vedere [Scrittura di una funzione ServiceMain.](writing-a-servicemain-function.md)

Nell'esempio seguente la funzione SvcCtrlHandler è un esempio di funzione [**Handler.**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) Si noti che la variabile ghSvcStopEvent è una variabile globale che deve essere inizializzata e usata come illustrato in Scrittura di [una funzione ServiceMain](writing-a-servicemain-function.md).


```C++
//
// Purpose: 
//   Called by SCM whenever a control code is sent to the service
//   using the ControlService function.
//
// Parameters:
//   dwCtrl - control code
// 
// Return value:
//   None
//
VOID WINAPI SvcCtrlHandler( DWORD dwCtrl )
{
   // Handle the requested control code. 

   switch(dwCtrl) 
   {  
      case SERVICE_CONTROL_STOP: 
         ReportSvcStatus(SERVICE_STOP_PENDING, NO_ERROR, 0);

         // Signal the service to stop.

         SetEvent(ghSvcStopEvent);
         ReportSvcStatus(gSvcStatus.dwCurrentState, NO_ERROR, 0);
         
         return;
 
      case SERVICE_CONTROL_INTERROGATE: 
         break; 
 
      default: 
         break;
   } 
   
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzione Handler di controllo dei servizi](service-control-handler-function.md)
</dt> <dt>

[Esempio di servizio completo](the-complete-service-sample.md)
</dt> </dl>

 

 



