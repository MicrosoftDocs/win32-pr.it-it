---
description: In telefonia Microsoft i provider di servizi di telefonia vengono eseguiti in un processo separato dalle applicazioni di telefonia.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: Interfaccia DLL dell'interfaccia utente del provider di servizi di telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311853"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a><span data-ttu-id="49374-103">Interfaccia DLL dell'interfaccia utente del provider di servizi di telefonia</span><span class="sxs-lookup"><span data-stu-id="49374-103">The Telephony Service Provider UI DLL Interface</span></span>

<span data-ttu-id="49374-104">In telefonia Microsoft i provider di servizi di telefonia vengono eseguiti in un processo separato dalle applicazioni di telefonia.</span><span class="sxs-lookup"><span data-stu-id="49374-104">In Microsoft Telephony, telephony service providers execute in a separate process from telephony applications.</span></span> <span data-ttu-id="49374-105">I provider di servizi comunicano con TAPISRV tramite l'interfaccia TSPI (telefonia Service Provider Interface) ed eseguono nel processo. interfaccia delle applicazioni per TAPI, che vengono caricati nel contesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="49374-105">Service providers communicate with TAPISRV through the Telephony service provider interface (TSPI) and execute in its process; applications interface to TAPI, which are loaded in the application context.</span></span>

<span data-ttu-id="49374-106">I componenti di TAPI utilizzano vari meccanismi di comunicazione interprocesso per trasferire richieste di funzioni e messaggi tra le applicazioni e i provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="49374-106">The components of TAPI use various interprocess communications mechanisms to convey function requests and messages between applications and service providers.</span></span> <span data-ttu-id="49374-107">È possibile che le applicazioni e i provider di servizi siano in esecuzione non solo in processi distinti, ma in sistemi completamente distinti.</span><span class="sxs-lookup"><span data-stu-id="49374-107">The applications and the service providers may be executing not only in separate processes, but on completely separate systems.</span></span> <span data-ttu-id="49374-108">I provider di servizi non possono pertanto visualizzare le finestre di dialogo nel processo o anche nel computer in cui sono in esecuzione; L'interfaccia utente deve essere richiamata dall'interno del contesto dell'applicazione, nel computer in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="49374-108">Service providers therefore cannot display dialog boxes in the process or even on the computer on which they are executing; UI must be invoked from within the application context, on the computer on which the application is executing.</span></span>

<span data-ttu-id="49374-109">In questa sezione viene definito il meccanismo mediante il quale vengono caricate e richiamate le funzioni dell'interfaccia utente del provider di servizi nel contesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="49374-109">This section defines the mechanism by which service provider UI functions are loaded and invoked within the application context.</span></span> <span data-ttu-id="49374-110">Un meccanismo è definito anche da quali provider di servizi possono aprire spontaneamente le finestre di dialogo nel contesto dell'applicazione quando non sono altrimenti previste dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="49374-110">A mechanism is also defined by which service providers can spontaneously open dialog boxes in the application context when they would not otherwise be expected by the application.</span></span> <span data-ttu-id="49374-111">Un esempio di questo secondo caso è la finestra di dialogo **Talk/hangup** visualizzata da un provider di servizi del modem dati quando il modem viene usato come dialer per le chiamate vocali interattive e all'utente deve essere richiesto di prelevare il telefono e informare il provider di servizi quando inserire il modem OnHook.</span><span class="sxs-lookup"><span data-stu-id="49374-111">An example of this latter case would be the **Talk/Hangup** dialog box that is displayed by a data modem service provider when the modem is being used as a dialer for interactive voice calls, and the user must be told to pick up the phone and inform the service provider when to place the modem onhook.</span></span>

 

 



