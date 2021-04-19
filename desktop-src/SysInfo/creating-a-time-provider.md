---
description: Un provider di ora viene implementato come una DLL. Ogni DLL può supportare più provider di tempo. Ogni provider è responsabile della propria configurazione e della propria sincronizzazione.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Creazione di un provider Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319899"
---
# <a name="creating-a-time-provider"></a><span data-ttu-id="e781d-105">Creazione di un provider Time</span><span class="sxs-lookup"><span data-stu-id="e781d-105">Creating a Time Provider</span></span>

<span data-ttu-id="e781d-106">Un provider di ora viene implementato come una DLL.</span><span class="sxs-lookup"><span data-stu-id="e781d-106">A time provider is implemented as a DLL.</span></span> <span data-ttu-id="e781d-107">Ogni DLL può supportare più provider di tempo.</span><span class="sxs-lookup"><span data-stu-id="e781d-107">Each DLL can support multiple time providers.</span></span> <span data-ttu-id="e781d-108">Ogni provider è responsabile della propria configurazione e della propria sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e781d-108">Each provider is responsible for its own configuration and synchronization.</span></span>

<span data-ttu-id="e781d-109">I provider di servizi temporali devono implementare le funzioni di callback seguenti:</span><span class="sxs-lookup"><span data-stu-id="e781d-109">Time providers must implement the following callback functions:</span></span>

-   [<span data-ttu-id="e781d-110">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="e781d-110">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [<span data-ttu-id="e781d-111">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="e781d-111">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [<span data-ttu-id="e781d-112">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="e781d-112">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

<span data-ttu-id="e781d-113">Dopo aver caricato la DLL del provider, il gestore del provider di servizi temporali chiama [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passando il nome del provider e i puntatori alle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e781d-113">After it has loaded the provider DLL, the time provider manager calls [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passing the name of the provider and pointers to the following functions:</span></span>

-   [<span data-ttu-id="e781d-114">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="e781d-114">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [<span data-ttu-id="e781d-115">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="e781d-115">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [<span data-ttu-id="e781d-116">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="e781d-116">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

<span data-ttu-id="e781d-117">Queste funzioni sono destinate all'uso da parte del provider di servizi temporali.</span><span class="sxs-lookup"><span data-stu-id="e781d-117">These functions are for use by the time provider.</span></span> <span data-ttu-id="e781d-118">Il provider Time USA [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) per restituire un handle del provider usato da gestione provider di servizi temporali per l'invio di comandi al provider di servizi temporali.</span><span class="sxs-lookup"><span data-stu-id="e781d-118">The time provider uses [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) to return a provider handle that the time provider manager uses when sending commands to the time provider.</span></span> <span data-ttu-id="e781d-119">Il valore dell'handle viene definito dal provider di tempo e viene utilizzato principalmente per distinguere tra provider diversi implementati nella stessa DLL.</span><span class="sxs-lookup"><span data-stu-id="e781d-119">The handle value is defined by the time provider and is used primarily to distinguish between different providers implemented in the same DLL.</span></span> <span data-ttu-id="e781d-120">Il provider di servizi temporali può registrare eventi significativi usando [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span><span class="sxs-lookup"><span data-stu-id="e781d-120">The time provider can log significant events using [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span></span>

<span data-ttu-id="e781d-121">Gestione provider di servizi temporali USA [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) per inviare comandi al provider di servizi temporali.</span><span class="sxs-lookup"><span data-stu-id="e781d-121">The time provider manager uses [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) to send commands to the time provider.</span></span> <span data-ttu-id="e781d-122">Quando il provider del tempo deve notificare al gestore del provider di servizi temporali la disponibilità di esempi temporali, viene chiamato [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span><span class="sxs-lookup"><span data-stu-id="e781d-122">When the time provider needs to notify the time provider manager that it has time samples available, it calls [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span></span> <span data-ttu-id="e781d-123">Il gestore del provider di servizi ora chiama **TimeProvCommand** con il \_ comando TPC getSamples per recuperare gli esempi temporali.</span><span class="sxs-lookup"><span data-stu-id="e781d-123">The time provider manager then calls **TimeProvCommand** with the TPC\_GetSamples command to retrieve the time samples.</span></span> <span data-ttu-id="e781d-124">Potrebbero essere richiesti fino a 16 secondi affinché il gestore del provider di servizi temporali richieda l'esempio.</span><span class="sxs-lookup"><span data-stu-id="e781d-124">It can take up to 16 seconds for the time provider manager to request the sample.</span></span> <span data-ttu-id="e781d-125">Pertanto, l'applicazione non deve attendere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e781d-125">Therefore, the application should not wait for the request.</span></span>

<span data-ttu-id="e781d-126">Per garantire l'accuratezza, il provider di tempo deve recuperare tutte le informazioni relative al tempo usando [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span><span class="sxs-lookup"><span data-stu-id="e781d-126">To ensure accuracy, the time provider should retrieve all time-related information using [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span></span>

<span data-ttu-id="e781d-127">Quando è il momento di arrestare il provider di tempo, il gestore del provider di servizi ora chiama [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span><span class="sxs-lookup"><span data-stu-id="e781d-127">When it is time to shut down the time provider, the time provider manager calls [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span></span>

 

 



