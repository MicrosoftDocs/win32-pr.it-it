---
description: Un evento temporizzato o ripetuto è un evento che si verifica in un'ora e una data specifiche o ripetutamente a intervalli regolari. Ad esempio, un evento può verificarsi a mezzanotte solo il 2 dicembre 2015 o una volta ogni settimana il martedì alle 2:31 PM.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Ricezione di un evento temporizzato o ripetuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226837"
---
# <a name="receiving-a-timed-or-repeating-event"></a><span data-ttu-id="31f92-104">Ricezione di un evento temporizzato o ripetuto</span><span class="sxs-lookup"><span data-stu-id="31f92-104">Receiving a Timed or Repeating Event</span></span>

<span data-ttu-id="31f92-105">Un evento temporizzato o ripetuto è un evento che si verifica in un'ora e una data specifiche o ripetutamente a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="31f92-105">A timed or repeating event is an event that occurs at one specific time and date, or repeatedly at regular intervals.</span></span> <span data-ttu-id="31f92-106">Ad esempio, un evento può verificarsi a mezzanotte solo il 2 dicembre 2015 o una volta ogni settimana il martedì alle 2:31 PM.</span><span class="sxs-lookup"><span data-stu-id="31f92-106">For example, an event can occur at midnight on only December 2, 2015, or one time each week on Tuesdays at 2:31 PM.</span></span>

<span data-ttu-id="31f92-107">La tabella seguente elenca le diverse classi usate per creare un evento temporizzato o ripetuto.</span><span class="sxs-lookup"><span data-stu-id="31f92-107">The following table lists the different classes that are used to create a timed or repeating event.</span></span>



| <span data-ttu-id="31f92-108">Classe</span><span class="sxs-lookup"><span data-stu-id="31f92-108">Class</span></span>                                                                                            | <span data-ttu-id="31f92-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31f92-109">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f92-110">[**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [ **\_ UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span><span class="sxs-lookup"><span data-stu-id="31f92-110">[**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span></span> | <span data-ttu-id="31f92-111">Modello di eventi Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="31f92-111">Standard Microsoft event model.</span></span><br/> <span data-ttu-id="31f92-112">Per ulteriori informazioni, vedere [creazione di un evento timer con Win32 \_ LocalTime o Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span><span class="sxs-lookup"><span data-stu-id="31f92-112">For more information, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span><br/> |
| [<span data-ttu-id="31f92-113">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="31f92-113">**\_\_TimerInstruction**</span></span>](--timerinstruction.md)                                               | <span data-ttu-id="31f92-114">Tecnica legacy.</span><span class="sxs-lookup"><span data-stu-id="31f92-114">Legacy technique.</span></span><br/> <span data-ttu-id="31f92-115">Per ulteriori informazioni, vedere [creazione di un evento timer con \_ TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="31f92-115">For more information, see [Creating a Timer Event with \_TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span></span><br/>                                             |



 

<span data-ttu-id="31f92-116">Se si desidera pianificare l'esecuzione di un'attività o di un processo in un momento specifico o ripetutamente, utilizzare la classe [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) e i relativi metodi.</span><span class="sxs-lookup"><span data-stu-id="31f92-116">If you want to schedule a task or job to occur at a specific time or repeatedly, use the [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) class and its methods.</span></span> <span data-ttu-id="31f92-117">Questa classe rappresenta un processo creato con il comando AT in una finestra di comando da **Start** , quindi da **eseguire** o dalle **attività pianificate** nel **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="31f92-117">This class represents a job created with the AT command in a command window from **Start** and then **Run**, or from the **Scheduled Tasks** in **Control Panel**.</span></span>

 

