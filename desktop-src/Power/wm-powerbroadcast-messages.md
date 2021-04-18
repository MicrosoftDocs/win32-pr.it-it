---
description: Il sistema trasmette un messaggio a tutte le applicazioni e i driver installabili ogni volta che si verifica un evento di risparmio energia.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: Messaggi di WM_POWERBROADCAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312004"
---
# <a name="wm_powerbroadcast-messages"></a><span data-ttu-id="b5a87-103">\_Messaggi WM POWERBROADCAST</span><span class="sxs-lookup"><span data-stu-id="b5a87-103">WM\_POWERBROADCAST Messages</span></span>

<span data-ttu-id="b5a87-104">Il sistema trasmette un messaggio a tutte le applicazioni e i driver installabili ogni volta che si verifica un evento di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b5a87-104">The system broadcasts a message to all applications and installable drivers whenever a power management event occurs.</span></span> <span data-ttu-id="b5a87-105">Il sistema trasmette questi eventi tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , impostando il parametro *wParam* sull'evento di risparmio energia appropriato.</span><span class="sxs-lookup"><span data-stu-id="b5a87-105">The system broadcasts these events through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message, setting the *wParam* parameter to the appropriate power management event.</span></span> <span data-ttu-id="b5a87-106">Ad esempio, l'evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indica una modifica dello stato di alimentazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5a87-106">For example, the [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) event indicates a system power status change.</span></span> <span data-ttu-id="b5a87-107">È necessario assicurarsi che l'applicazione risponda correttamente al messaggio **WM \_ POWERBROADCAST** .</span><span class="sxs-lookup"><span data-stu-id="b5a87-107">You must ensure that your application responds properly to the **WM\_POWERBROADCAST** message.</span></span>

<span data-ttu-id="b5a87-108">Il sistema trasmette un evento [ \_ APMSUSPEND PBT](pbt-apmsuspend.md) immediatamente prima di sospendere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b5a87-108">The system broadcasts a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event immediately before suspending operation.</span></span> <span data-ttu-id="b5a87-109">In questo modo, le applicazioni e i driver potranno prepararsi per l'evento.</span><span class="sxs-lookup"><span data-stu-id="b5a87-109">This gives applications and drivers one last chance to prepare for the event.</span></span> <span data-ttu-id="b5a87-110">In molti casi, il sistema trasmette questi messaggi senza richiedere l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="b5a87-110">In many cases, the system broadcasts these messages without requesting permission to do so.</span></span> <span data-ttu-id="b5a87-111">Ciò si verifica, ad esempio, se un'applicazione forza la sospensione con la funzione [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="b5a87-111">This happens, for example, if an application forces suspension with the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

<span data-ttu-id="b5a87-112">Il sistema trasmette l'evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) o [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) quando l'operazione di sistema è stata ripristinata.</span><span class="sxs-lookup"><span data-stu-id="b5a87-112">The system broadcasts the [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) or [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event when system operation has been restored.</span></span> <span data-ttu-id="b5a87-113">Se un'applicazione ha ricevuto un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) prima della sospensione del computer, riceverà l' \_ evento PBT APMRESUMESUSPEND.</span><span class="sxs-lookup"><span data-stu-id="b5a87-113">If an application received a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended, it will receive the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="b5a87-114">In caso contrario, riceverà l' \_ evento PBT APMRESUMECRITICAL.</span><span class="sxs-lookup"><span data-stu-id="b5a87-114">Otherwise, it will receive the PBT\_APMRESUMECRITICAL event.</span></span>

<span data-ttu-id="b5a87-115">Il sistema invia un evento [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) alle applicazioni registrate per l'evento specifico usando [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span><span class="sxs-lookup"><span data-stu-id="b5a87-115">The system sends a [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) event to applications that have registered for the specific event using [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span></span> <span data-ttu-id="b5a87-116">Per ulteriori informazioni, vedere [la pagina relativa alla registrazione per gli eventi di alimentazione](registering-for-power-events.md).</span><span class="sxs-lookup"><span data-stu-id="b5a87-116">For more information, see [Registering for Power Events](registering-for-power-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5a87-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5a87-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5a87-118">Informazioni sul risparmio energia</span><span class="sxs-lookup"><span data-stu-id="b5a87-118">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



