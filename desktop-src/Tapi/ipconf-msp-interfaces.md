---
description: Il provider di servizi di audioconferenza IP implementa diverse interfacce specifiche del provider per il controllo partecipante. Queste interfacce sono esposte nell'oggetto chiamata, se questo MSP è associato alla chiamata.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Interfacce MSP IPConf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131043"
---
# <a name="ipconf-msp-interfaces"></a><span data-ttu-id="20e19-104">Interfacce MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="20e19-104">IPConf MSP Interfaces</span></span>

<span data-ttu-id="20e19-105">\[ Le interfacce MSP IPConf non sono disponibili per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="20e19-105">\[ The IPConf MSP Interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="20e19-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="20e19-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="20e19-107">Il provider di servizi di audioconferenza IP implementa diverse interfacce specifiche del provider per il controllo partecipante.</span><span class="sxs-lookup"><span data-stu-id="20e19-107">The IP conferencing MSP implements several provider-specific interfaces for participant control.</span></span> <span data-ttu-id="20e19-108">Queste interfacce sono esposte nell'oggetto chiamata, se questo MSP è associato alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="20e19-108">These interfaces are exposed on the call object, if this MSP is associated with the call.</span></span>

<span data-ttu-id="20e19-109">Le interfacce [**ITParticipantEvent**](itparticipantevent.md) e [**IEnumParticipant**](ienumparticipant.md) sono oggetti autonomi e sono elencate di seguito per praticità di riferimento.</span><span class="sxs-lookup"><span data-stu-id="20e19-109">The [**ITParticipantEvent**](itparticipantevent.md) and [**IEnumParticipant**](ienumparticipant.md) interfaces are stand-alone objects, and are listed here for reference convenience.</span></span>



| <span data-ttu-id="20e19-110">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="20e19-110">Interface</span></span>                                            | <span data-ttu-id="20e19-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20e19-111">Description</span></span>                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20e19-112">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="20e19-112">**IMulticastControl**</span></span>](imulticastcontrol.md)       | <span data-ttu-id="20e19-113">Consente a un'applicazione di impostare e ottenere la modalità loopback [**( \_ \_ modalità loopback multicast**](multicast-loopback-mode.md)) per un oggetto conferenza multicast.</span><span class="sxs-lookup"><span data-stu-id="20e19-113">Allows an application to set and get the loopback mode ( [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md)) for a multicast conference object.</span></span> |
| [<span data-ttu-id="20e19-114">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="20e19-114">**ITParticipant**</span></span>](itparticipant.md)               | <span data-ttu-id="20e19-115">Consente a un'applicazione di recuperare informazioni sui partecipanti alla conferenza e ottenere i puntatori ai flussi associati a tali partecipanti.</span><span class="sxs-lookup"><span data-stu-id="20e19-115">Allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>             |
| [<span data-ttu-id="20e19-116">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="20e19-116">**ITParticipantControl**</span></span>](itparticipantcontrol.md) | <span data-ttu-id="20e19-117">Consente a un'applicazione di recuperare i puntatori ai partecipanti a una conferenza.</span><span class="sxs-lookup"><span data-stu-id="20e19-117">Allows an application to retrieve pointers to the participants in a conference.</span></span>                                                                           |
| [<span data-ttu-id="20e19-118">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="20e19-118">**ITParticipantEvent**</span></span>](itparticipantevent.md)     | <span data-ttu-id="20e19-119">Consente a un'applicazione di recuperare informazioni sugli eventi relativi a un partecipante alla conferenza.</span><span class="sxs-lookup"><span data-stu-id="20e19-119">Allows an application to retrieve event information concerning a conference participant.</span></span>                                                                  |
| [<span data-ttu-id="20e19-120">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="20e19-120">**IEnumParticipant**</span></span>](ienumparticipant.md)         | <span data-ttu-id="20e19-121">Enumera [**ITParticipant**](itparticipant.md).</span><span class="sxs-lookup"><span data-stu-id="20e19-121">Enumerates [**ITParticipant**](itparticipant.md).</span></span>                                                                                                        |



 

 

 



