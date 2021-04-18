---
description: Per inviare richieste di controllo a un servizio in esecuzione, un programma di controllo del servizio usa la funzione ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Richieste di controllo del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306533"
---
# <a name="service-control-requests"></a><span data-ttu-id="a7a3c-103">Richieste di controllo del servizio</span><span class="sxs-lookup"><span data-stu-id="a7a3c-103">Service Control Requests</span></span>

<span data-ttu-id="a7a3c-104">Per inviare richieste di controllo a un servizio in esecuzione, un programma di controllo del servizio usa la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="a7a3c-104">To send control requests to a running service, a service control program uses the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="a7a3c-105">Questa funzione specifica un valore di controllo che viene passato alla funzione [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) del servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="a7a3c-105">This function specifies a control value that is passed to the [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) function of the specified service.</span></span> <span data-ttu-id="a7a3c-106">Questo valore di controllo può essere un codice definito dall'utente o uno dei codici standard che consentono al programma chiamante di eseguire le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7a3c-106">This control value can be a user-defined code, or it can be one of the standard codes that enable the calling program to perform the following actions:</span></span>

-   <span data-ttu-id="a7a3c-107">Arrestare un servizio (arresto del controllo del servizio \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="a7a3c-107">Stop a service (SERVICE\_CONTROL\_STOP).</span></span>
-   <span data-ttu-id="a7a3c-108">Sospendere un servizio ( \_ sospensione del controllo del servizio \_ ).</span><span class="sxs-lookup"><span data-stu-id="a7a3c-108">Pause a service (SERVICE\_CONTROL\_PAUSE).</span></span>
-   <span data-ttu-id="a7a3c-109">Riprendere l'esecuzione di un servizio sospeso (il \_ controllo del servizio \_ continua).</span><span class="sxs-lookup"><span data-stu-id="a7a3c-109">Resume executing a paused service (SERVICE\_CONTROL\_CONTINUE).</span></span>
-   <span data-ttu-id="a7a3c-110">Recuperare le informazioni aggiornate sullo stato da un servizio ( \_ interrogazione del controllo del servizio \_ ).</span><span class="sxs-lookup"><span data-stu-id="a7a3c-110">Retrieve updated status information from a service (SERVICE\_CONTROL\_INTERROGATE).</span></span>

<span data-ttu-id="a7a3c-111">Ogni servizio specifica i valori di controllo che accetteranno ed elaborano.</span><span class="sxs-lookup"><span data-stu-id="a7a3c-111">Each service specifies the control values that it will accept and process.</span></span> <span data-ttu-id="a7a3c-112">Per determinare quali valori di controllo standard vengono accettati da un servizio, utilizzare la funzione [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) o specificare il valore del controllo interrogare il controllo del servizio \_ \_ in una chiamata alla funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="a7a3c-112">To determine which of the standard control values are accepted by a service, use the [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function or specify the SERVICE\_CONTROL\_INTERROGATE control value in a call to the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="a7a3c-113">Il membro **dwControlsAccepted** della struttura [**di \_ stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) restituito da queste funzioni indica se il servizio può essere arrestato, sospeso o ripreso.</span><span class="sxs-lookup"><span data-stu-id="a7a3c-113">The **dwControlsAccepted** member of the [**SERVICE\_STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) structure returned by these functions indicates whether the service can be stopped, paused, or resumed.</span></span> <span data-ttu-id="a7a3c-114">Tutti i servizi accettano il \_ \_ valore del controllo interrogare il controllo del servizio.</span><span class="sxs-lookup"><span data-stu-id="a7a3c-114">All services accept the SERVICE\_CONTROL\_INTERROGATE control value.</span></span>

<span data-ttu-id="a7a3c-115">La funzione [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) segnala lo stato più recente per un servizio specificato, ma non ottiene uno stato aggiornato dal servizio stesso.</span><span class="sxs-lookup"><span data-stu-id="a7a3c-115">The [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function reports the most recent status for a specified service, but does not get an updated status from the service itself.</span></span> <span data-ttu-id="a7a3c-116">L'utilizzo del \_ valore del controllo interrogare il controllo del servizio \_ in una chiamata a [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garantisce che le informazioni sullo stato restituite siano correnti.</span><span class="sxs-lookup"><span data-stu-id="a7a3c-116">Using the SERVICE\_CONTROL\_INTERROGATE control value in a call to [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) ensures that the status information returned is current.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7a3c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7a3c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7a3c-118">Controllo di un servizio con SC</span><span class="sxs-lookup"><span data-stu-id="a7a3c-118">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



