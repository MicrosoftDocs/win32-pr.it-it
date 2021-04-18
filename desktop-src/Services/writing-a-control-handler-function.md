---
description: Quando una funzione del gestore viene chiamata dal thread del dispatcher, gestisce il codice di controllo passato nel parametro opcode, quindi chiama la funzione ReportSvcStatus per aggiornare lo stato del servizio.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Scrittura di una funzione del gestore di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724a04aa20143d2c4a506da7ac17119388a8c82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306526"
---
# <a name="writing-a-control-handler-function"></a>Scrittura di una funzione del gestore di controllo

Quando una funzione del [**gestore**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) viene chiamata dal thread del dispatcher, gestisce il codice di controllo passato nel parametro *OpCode* , quindi chiama la funzione ReportSvcStatus per aggiornare lo stato del servizio. Quando una [**funzione di gestione riceve**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) un codice di controllo, deve segnalare lo stato del servizio solo se la gestione del codice di controllo causa la modifica dello stato del servizio. Se il servizio non agisce sul controllo, non dovrebbe segnalare lo stato a gestione controllo servizi. Per il codice sorgente per ReportSvcStatus, vedere [scrittura di una funzione ServiceMain](writing-a-servicemain-function.md).

Nell'esempio seguente, la funzione SvcCtrlHandler è un esempio di una funzione del [**gestore**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) . Si noti che la variabile ghSvcStopEvent è una variabile globale che deve essere inizializzata e usata come illustrato in [scrittura di una funzione ServiceMain](writing-a-servicemain-function.md).


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

 

 



