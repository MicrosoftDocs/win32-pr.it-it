---
title: Configurazione dei timeout specifici dell'applicazione
description: Configurazione dei timeout specifici dell'applicazione
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configurazione dei timeout specifici dell'applicazione HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1cbcdb0b0796820282673c41507f6bfcc0ebd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109739"
---
# <a name="configuring-the-application-specific-timeouts"></a><span data-ttu-id="08dac-104">Configurazione dei timeout specifici dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="08dac-104">Configuring the Application Specific Timeouts</span></span>

<span data-ttu-id="08dac-105">Le impostazioni a livello di API del server HTTP si applicano a tutte le sessioni del server e a tutti i gruppi di URL nel computer.</span><span class="sxs-lookup"><span data-stu-id="08dac-105">The HTTP Server API-wide settings apply to all the server sessions and URL groups on the computer.</span></span> <span data-ttu-id="08dac-106">Queste configurazioni possono essere sostituite dall'applicazione impostando i valori di timeout specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08dac-106">These configurations can be overridden by the application by setting the application-specific timeout values.</span></span> <span data-ttu-id="08dac-107">I timeout di sessione del server eseguono l'override dei timeout a livello di API del server HTTP e si applicano a tutti i gruppi di URL creati al loro interno.</span><span class="sxs-lookup"><span data-stu-id="08dac-107">The server session timeouts override the HTTP Server API-wide timeouts and apply to all the URL groups created under them.</span></span> <span data-ttu-id="08dac-108">La configurazione della proprietà timeouts in un gruppo di URL sostituisce i timeout di sessione del server per tutti gli URL nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="08dac-108">Configuring the timeouts property on a URL group overrides the server session timeouts for all the URLs in the group.</span></span>

<span data-ttu-id="08dac-109">Se si specifica zero per uno dei timer nella struttura [**HTTP \_ TIMEOUT LIMIT \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) per un gruppo di URL, l'API server HTTP ripristina i timeout di sessione del server, se presenti, o le impostazioni predefinite dell'API del server HTTP se i timeout della sessione del server non esistono.</span><span class="sxs-lookup"><span data-stu-id="08dac-109">Specifying zero for any of the timers in the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure for a URL group causes the HTTP Server API to revert to the server session timeouts, if they exist, or the HTTP Server API default settings if the server session timeouts do not exist.</span></span> <span data-ttu-id="08dac-110">Ad esempio, quando la proprietà timeout del server è presente in un gruppo di URL e il timer **EntityBody** è zero, viene usato il timeout della sessione del server.</span><span class="sxs-lookup"><span data-stu-id="08dac-110">For example, when the server timeout property is present on a URL group and the **EntityBody** timer is zero, the server session timeout is used.</span></span> <span data-ttu-id="08dac-111">Se la proprietà timeouts non è impostata in una sessione del server, viene usata la configurazione predefinita dell'API server HTTP.</span><span class="sxs-lookup"><span data-stu-id="08dac-111">If the timeouts property is not set on a server session, the HTTP Server API default configuration is used.</span></span> <span data-ttu-id="08dac-112">Per disabilitare un timer, impostare il valore su **MAXUSHORT**, ad eccezione del timer **MinSendRate** impostato su **MAXULONG**.</span><span class="sxs-lookup"><span data-stu-id="08dac-112">To disable a timer, set the value to **MAXUSHORT**, except for the **MinSendRate** timer which is set to **MAXULONG**.</span></span>

<span data-ttu-id="08dac-113">L'API server HTTP può configurare solo i timer **HeaderWait** specifici dell'applicazione e **IdleConnection** sono effettivi solo dopo la ricezione della prima richiesta.</span><span class="sxs-lookup"><span data-stu-id="08dac-113">The HTTP Server API can only configure the application-specific **HeaderWait** and the **IdleConnection** timers are only effective after the first request has been received.</span></span> <span data-ttu-id="08dac-114">Prima della ricezione della prima richiesta, vengono applicati i valori di timeout a livello di API del server HTTP.</span><span class="sxs-lookup"><span data-stu-id="08dac-114">Before the first request is received, the HTTP Server API-wide timeout values are enforced.</span></span> <span data-ttu-id="08dac-115">Quando la prima richiesta arriva e viene associata a una coda di richieste, è possibile applicare i timer **HeaderWait** e **IdleConnection** specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08dac-115">After the first request arrives and is associated with a request queue, the application-specific **HeaderWait** and **IdleConnection** timers can be applied.</span></span> <span data-ttu-id="08dac-116">I timer specifici dell'applicazione vengono applicati a tutte le richieste successive che arrivano nella coda delle richieste per una connessione keep-alive.</span><span class="sxs-lookup"><span data-stu-id="08dac-116">The application-specific timers are applied to all subsequent requests that arrive on the request queue for a keep-alive connection.</span></span>

<span data-ttu-id="08dac-117">Per altre informazioni sulla configurazione dei timer, vedere gli argomenti [Configuring the URL Group](configuring-the-url-group.md) (Configurazione del gruppo di URL) e [Configuring the Server Session (Configurazione della sessione server).](configuring-the-server-session.md)</span><span class="sxs-lookup"><span data-stu-id="08dac-117">For more information about configuring timers, see the [Configuring the URL Group](configuring-the-url-group.md) and [Configuring the Server Session](configuring-the-server-session.md) topics.</span></span>

 

 




