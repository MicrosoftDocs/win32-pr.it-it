---
description: Lo stato di alimentazione del sistema indica se l'origine di alimentazione per un computer è una batteria di sistema o un alimentatore AC. Per i computer che utilizzano batterie, lo stato di alimentazione del sistema indica anche la quantità di durata della batteria e l'eventuale ricarica della batteria.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: Stato di alimentazione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312013"
---
# <a name="system-power-status"></a><span data-ttu-id="a17d4-104">Stato di alimentazione del sistema</span><span class="sxs-lookup"><span data-stu-id="a17d4-104">System Power Status</span></span>

<span data-ttu-id="a17d4-105">Lo stato di alimentazione del sistema indica se l'origine di alimentazione per un computer è una batteria di sistema o un alimentatore AC.</span><span class="sxs-lookup"><span data-stu-id="a17d4-105">The system power status indicates whether the source of power for a computer is a system battery or AC power.</span></span> <span data-ttu-id="a17d4-106">Per i computer che utilizzano batterie, lo stato di alimentazione del sistema indica anche la quantità di durata della batteria e l'eventuale ricarica della batteria.</span><span class="sxs-lookup"><span data-stu-id="a17d4-106">For computers that use batteries, the system power status also indicates how much battery life remains and whether the battery is charging.</span></span>

<span data-ttu-id="a17d4-107">Le informazioni di risparmio energia vengono recuperate eseguendo la registrazione per le notifiche di impostazioni di risparmio energia tramite la funzione [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) .</span><span class="sxs-lookup"><span data-stu-id="a17d4-107">Power information is retrieved by registering for power setting notifications through the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function.</span></span> <span data-ttu-id="a17d4-108">Questa funzione consente alle applicazioni di eseguire la registrazione per impostazioni di risparmio energia specifiche e ricevere notifiche quando cambiano.</span><span class="sxs-lookup"><span data-stu-id="a17d4-108">This function allows applications to register for specific power settings and be notified when they change.</span></span>

> [!Note]  
> <span data-ttu-id="a17d4-109">Per eseguire una query per ottenere informazioni sullo stato dell'alimentazione senza notifiche, usare [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span><span class="sxs-lookup"><span data-stu-id="a17d4-109">To query for power status information without notifications, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span></span>

 

<span data-ttu-id="a17d4-110">Le applicazioni e i driver installabili usano in genere lo stato di alimentazione del sistema per determinare se è possibile eseguire l'operazione continua.</span><span class="sxs-lookup"><span data-stu-id="a17d4-110">Applications and installable drivers typically use the system power status to determine whether continued operation is feasible.</span></span> <span data-ttu-id="a17d4-111">Ad esempio, prima che un'applicazione esegua operazioni in background, ad esempio la compressione o la paginazione di un file, deve controllare se il sistema è su batterie.</span><span class="sxs-lookup"><span data-stu-id="a17d4-111">For example, before an application performs background operations such as compressing or paginating a file, it should check whether the system is on batteries.</span></span> <span data-ttu-id="a17d4-112">Come altro esempio, un'applicazione che sta iniziando un'operazione di lunga durata deve controllare lo stato per determinare se è disponibile una quantità sufficiente di energia elettrica per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a17d4-112">As another example, an application that is beginning a lengthy operation should check the status to determine whether enough battery power exists to complete the operation.</span></span>

<span data-ttu-id="a17d4-113">Per impostazione predefinita, il sistema non esegue query su applicazioni o driver durante le transizioni di sospensione.</span><span class="sxs-lookup"><span data-stu-id="a17d4-113">By default, the system does not query applications or drivers during sleep transitions.</span></span>

> [!Note]  
> <span data-ttu-id="a17d4-114">Se il risparmio di energia è basso, un'applicazione può richiedere l'intervento dell'utente o richiedere che il sistema si sospenda automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a17d4-114">If power is low, an application can request user intervention or request that the system suspend itself.</span></span> <span data-ttu-id="a17d4-115">È possibile sospendere l'operazione di sistema utilizzando la funzione [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="a17d4-115">You can suspend system operation by using the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a17d4-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a17d4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a17d4-117">Informazioni sul risparmio energia</span><span class="sxs-lookup"><span data-stu-id="a17d4-117">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



