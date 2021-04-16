---
description: Controller (oggetto)
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Controller (oggetto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104558103"
---
# <a name="controller-object"></a><span data-ttu-id="ad6e2-103">Controller (oggetto)</span><span class="sxs-lookup"><span data-stu-id="ad6e2-103">Controller Object</span></span>

<span data-ttu-id="ad6e2-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ad6e2-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="ad6e2-105">Un oggetto controller modella un controller in un sottosistema.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-105">A controller object models a controller in a subsystem.</span></span> <span data-ttu-id="ad6e2-106">I controller sono contenuti in sottosistemi e ogni controller dispone di una o più porte del controller attraverso le quali il computer host può scrivere e leggere da lun.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-106">Controllers are contained by subsystems, and each controller has one or more controller ports through which the host computer can write to and read from LUNs.</span></span> <span data-ttu-id="ad6e2-107">Un singolo controller può essere impostato contemporaneamente su attivo per un LUN e inattivo per altri.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-107">A single controller can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="ad6e2-108">Un controller attivo per un LUN specificato ha la responsabilità di gestire l'input e l'output del LUN.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-108">A controller that is active for a specified LUN carries the responsibility for handling input to and output from the LUN.</span></span> <span data-ttu-id="ad6e2-109">Questa idea è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-109">The following figure illustrates this idea.</span></span>

![Diagramma che mostra un "controller" con un LUN attivo a sinistra e due LUN attivi a destra.](images/vdscontroller.png)

<span data-ttu-id="ad6e2-111">**VDS 1,0:** Ognuno dei controller di un sottosistema è impostato su attivo o inattivo in relazione a ogni LUN del sottosistema.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-111">**VDS 1.0:** Each of a subsystem's controllers is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span>

<span data-ttu-id="ad6e2-112">Le applicazioni VDS usano il metodo [**IVdsSubSystem:: QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) per determinare i controller contenuti in un sottosistema specifico.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-112">VDS applications use the [**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) method to determine the controllers that are contained by a specific subsystem.</span></span> <span data-ttu-id="ad6e2-113">I chiamanti possono ottenere un puntatore a un controller specifico selezionando l'oggetto controller desiderato dall'enumerazione restituita dal metodo **QueryControllers** .</span><span class="sxs-lookup"><span data-stu-id="ad6e2-113">Callers can get a pointer to a specific controller by selecting the desired controller object from the enumeration that is returned by the **QueryControllers** method.</span></span> <span data-ttu-id="ad6e2-114">Con un oggetto controller, un chiamante può impostare lo stato del controller, eseguire una query per i LUN associati, eseguire una query per le porte del controller e scaricare e invalidare la cache.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-114">With a controller object, a caller can set the controller status, query for its associated LUNs, query for its controller ports, and flush and invalidate the cache.</span></span>

<span data-ttu-id="ad6e2-115">Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto controller includono lo stato e l'integrità del controller e un conteggio delle porte.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-115">In addition to an object identifier, a name, and a serial number, controller object properties include the controller status and health, and a count of the ports.</span></span>

<span data-ttu-id="ad6e2-116">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="ad6e2-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="ad6e2-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad6e2-117">Type</span></span>                                                                                              | <span data-ttu-id="ad6e2-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="ad6e2-118">Element</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6e2-119">Interfacce sempre esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="ad6e2-119">Interfaces that are always exposed by this object</span></span>                                                 | [<span data-ttu-id="ad6e2-120">**IVdsController**</span><span class="sxs-lookup"><span data-stu-id="ad6e2-120">**IVdsController**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| <span data-ttu-id="ad6e2-121">Interfacce sempre esposte da questo oggetto in VDS 1,1 e 2,0 Fibre Channel solo provider</span><span class="sxs-lookup"><span data-stu-id="ad6e2-121">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="ad6e2-122">**IVdsControllerControllerPort**</span><span class="sxs-lookup"><span data-stu-id="ad6e2-122">**IVdsControllerControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| <span data-ttu-id="ad6e2-123">Interfacce che possono essere esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="ad6e2-123">Interfaces that may be exposed by this object</span></span>                                                     | [<span data-ttu-id="ad6e2-124">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="ad6e2-124">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| <span data-ttu-id="ad6e2-125">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="ad6e2-125">Associated enumerations</span></span>                                                                           | <span data-ttu-id="ad6e2-126">[**VDS \_ \_stato del controller**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span><span class="sxs-lookup"><span data-stu-id="ad6e2-126">[**VDS\_CONTROLLER\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span></span>                                                                      |
| <span data-ttu-id="ad6e2-127">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="ad6e2-127">Associated structures</span></span>                                                                             | <span data-ttu-id="ad6e2-128">[**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) Notifiche del controller prop e del [**\_ controller \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span><span class="sxs-lookup"><span data-stu-id="ad6e2-128">[**VDS\_CONTROLLER\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) and [**VDS\_CONTROLLER\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ad6e2-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad6e2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad6e2-130">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="ad6e2-130">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="ad6e2-131">**IVdsSubSystem::QueryControllers**</span><span class="sxs-lookup"><span data-stu-id="ad6e2-131">**IVdsSubSystem::QueryControllers**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
