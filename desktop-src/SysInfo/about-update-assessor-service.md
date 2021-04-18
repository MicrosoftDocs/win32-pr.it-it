---
description: Nell'argomento seguente viene descritto il funzionamento dell'API della piattaforma di valutazione di Windows As a Service (WaaS).
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Informazioni sulla piattaforma di valutazione WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313270"
---
# <a name="about-the-waas-assessment-platform"></a><span data-ttu-id="54032-103">Informazioni sulla piattaforma di valutazione WaaS</span><span class="sxs-lookup"><span data-stu-id="54032-103">About the WaaS Assessment Platform</span></span>

<span data-ttu-id="54032-104">Nell'argomento seguente viene descritto il funzionamento dell'API della piattaforma di valutazione di Windows As a Service (WaaS).</span><span class="sxs-lookup"><span data-stu-id="54032-104">The following topic describes how the Windows as a Service (WaaS) Assessment Platform API works.</span></span>

<span data-ttu-id="54032-105">L'API WaaS Assessment offre al chiamante le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="54032-105">The WaaS Assessment API offers the caller the following information:</span></span>

-   <span data-ttu-id="54032-106">Se un dispositivo si trova negli aggiornamenti Microsoft più recenti.</span><span class="sxs-lookup"><span data-stu-id="54032-106">If a device is on the latest Microsoft updates.</span></span>
-   <span data-ttu-id="54032-107">Indica se il dispositivo ha raggiunto la fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="54032-107">Whether the device has reached end of support.</span></span>
-   <span data-ttu-id="54032-108">Ora di rilascio per gli aggiornamenti applicabili più recenti per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54032-108">The release times for the latest applicable updates for the device.</span></span>
-   <span data-ttu-id="54032-109">Una valutazione del motivo per cui un dispositivo non è aggiornato e il potenziale impatto sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54032-109">An assessment of why a device is not up-to-date and the potential impact it may have on the device.</span></span>

<span data-ttu-id="54032-110">La piattaforma di valutazione WaaS usa il modello API COM e viene eseguita automaticamente almeno una volta al giorno.</span><span class="sxs-lookup"><span data-stu-id="54032-110">The WaaS Assessment Platform uses the COM API model and runs automatically at least once a day.</span></span> <span data-ttu-id="54032-111">Questo ciclo rileva le informazioni sulla versione applicabili.</span><span class="sxs-lookup"><span data-stu-id="54032-111">This cycle catches applicable release information.</span></span> <span data-ttu-id="54032-112">Durante il periodo di memorizzazione nella cache, le valutazioni vengono effettuate rispetto alle informazioni sulla versione memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="54032-112">During the cached period, assessments are made against the cached release information.</span></span> <span data-ttu-id="54032-113">Se viene eseguita una chiamata al di fuori della finestra di scadenza della cache, viene effettuata una chiamata e una valutazione aggiornate, memorizzate nella cache e restituite.</span><span class="sxs-lookup"><span data-stu-id="54032-113">If a call is made outside of the cache expiration window, a fresh call and assessment is made, cached, and returned.</span></span> <span data-ttu-id="54032-114">Quando viene effettuata una chiamata, il client di valutazione WaaS Contatta il servizio di valutazione WaaS con gli attributi del dispositivo e riceve un dossier di informazioni applicabili al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54032-114">When a call is made, the WaaS Assessment Client contacts the WaaS Assessment Service with the device's attributes, and receives back a dossier of information applicable to the device.</span></span> <span data-ttu-id="54032-115">Il client usa quindi queste informazioni a fronte delle informazioni raccolte sul dispositivo per eseguire la valutazione.</span><span class="sxs-lookup"><span data-stu-id="54032-115">The client then uses this information against the information it gathers about the device to perform the assessment.</span></span>

> [!NOTE]
> <span data-ttu-id="54032-116">Il codice deve disporre dei privilegi di amministratore per chiamare l'API WAAS assessment.</span><span class="sxs-lookup"><span data-stu-id="54032-116">Your code must have administrator privileges to call the Waas Assessment API.</span></span> <span data-ttu-id="54032-117">Per ulteriori informazioni sullo sviluppo di applicazioni che richiedono privilegi di amministratore, vedere [questo articolo](../secauthz/developing-applications-that-require-administrator-privilege.md).</span><span class="sxs-lookup"><span data-stu-id="54032-117">For more details about developing applications that require administrator privileges, see [this article](../secauthz/developing-applications-that-require-administrator-privilege.md).</span></span>

 
