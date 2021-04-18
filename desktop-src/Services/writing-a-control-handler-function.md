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
# <a name="writing-a-control-handler-function"></a><span data-ttu-id="f0fcf-103">Scrittura di una funzione del gestore di controllo</span><span class="sxs-lookup"><span data-stu-id="f0fcf-103">Writing a Control Handler Function</span></span>

<span data-ttu-id="f0fcf-104">Quando una funzione del [**gestore**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) viene chiamata dal thread del dispatcher, gestisce il codice di controllo passato nel parametro *OpCode* , quindi chiama la funzione ReportSvcStatus per aggiornare lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="f0fcf-104">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function is called by the dispatcher thread, it handles the control code passed in the *Opcode* parameter and then calls the ReportSvcStatus function to update the service status.</span></span> <span data-ttu-id="f0fcf-105">Quando una [**funzione di gestione riceve**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) un codice di controllo, deve segnalare lo stato del servizio solo se la gestione del codice di controllo causa la modifica dello stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="f0fcf-105">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function receives a control code, it should report the service status only if handling the control code causes the service status to change.</span></span> <span data-ttu-id="f0fcf-106">Se il servizio non agisce sul controllo, non dovrebbe segnalare lo stato a gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="f0fcf-106">If the service does not act on the control, it should not report status to the service control manager.</span></span> <span data-ttu-id="f0fcf-107">Per il codice sorgente per ReportSvcStatus, vedere [scrittura di una funzione ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="f0fcf-107">For the source code for ReportSvcStatus, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span>

<span data-ttu-id="f0fcf-108">Nell'esempio seguente, la funzione SvcCtrlHandler è un esempio di una funzione del [**gestore**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) .</span><span class="sxs-lookup"><span data-stu-id="f0fcf-108">In the following example, the SvcCtrlHandler function is an example of a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function.</span></span> <span data-ttu-id="f0fcf-109">Si noti che la variabile ghSvcStopEvent è una variabile globale che deve essere inizializzata e usata come illustrato in [scrittura di una funzione ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="f0fcf-109">Note that the ghSvcStopEvent variable is a global variable that should be initialized and used as demonstrated in [Writing a ServiceMain function](writing-a-servicemain-function.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f0fcf-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0fcf-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0fcf-111">Funzione Handler di controllo dei servizi</span><span class="sxs-lookup"><span data-stu-id="f0fcf-111">Service Control Handler Function</span></span>](service-control-handler-function.md)
</dt> <dt>

[<span data-ttu-id="f0fcf-112">Esempio di servizio completo</span><span class="sxs-lookup"><span data-stu-id="f0fcf-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



