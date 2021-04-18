---
description: Oggetto porta controller
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Oggetto porta controller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306510"
---
# <a name="controller-port-object"></a><span data-ttu-id="09b7a-103">Oggetto porta controller</span><span class="sxs-lookup"><span data-stu-id="09b7a-103">Controller Port Object</span></span>

<span data-ttu-id="09b7a-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="09b7a-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="09b7a-105">Un oggetto porta del controller modella una porta del controller in un sottosistema.</span><span class="sxs-lookup"><span data-stu-id="09b7a-105">A controller port object models a controller port in a subsystem.</span></span> <span data-ttu-id="09b7a-106">I computer host possono scrivere e leggere da lun attraverso le porte del controller.</span><span class="sxs-lookup"><span data-stu-id="09b7a-106">Host computers can write to and read from LUNs through controller ports.</span></span> <span data-ttu-id="09b7a-107">Le porte del controller sono contenute nei controller di un sottosistema.</span><span class="sxs-lookup"><span data-stu-id="09b7a-107">Controller ports are contained by controllers in a subsystem.</span></span> <span data-ttu-id="09b7a-108">In VDS 1,1 e VDS 2.0, ognuna delle porte del controller di un sottosistema è impostata su attivo o inattivo in relazione a ogni LUN del sottosistema.</span><span class="sxs-lookup"><span data-stu-id="09b7a-108">In VDS 1.1 and VDS2.0, each of a subsystem's controller ports is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span> <span data-ttu-id="09b7a-109">Una singola porta del controller, quindi, può essere impostata contemporaneamente su attivo per un LUN e inattivo per altri.</span><span class="sxs-lookup"><span data-stu-id="09b7a-109">A single controller port, then, can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="09b7a-110">Una porta del controller attiva per un determinato LUN ha la responsabilità di gestire l'input e l'output del LUN.</span><span class="sxs-lookup"><span data-stu-id="09b7a-110">A controller port that is active for a given LUN carries responsibility for handling input to and output from the LUN.</span></span>

<span data-ttu-id="09b7a-111">Le porte del controller attive vengono utilizzate come uno degli endpoint dei percorsi MPIO in Fibre Channel provider di hardware, su cui è possibile imporre i criteri di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="09b7a-111">Active controller ports serve as one of the endpoints of MPIO paths in Fibre Channel hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="09b7a-112">Usare il metodo [**IVdsControllerControllerPort:: QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) per determinare le porte del controller contenute in un controller specifico.</span><span class="sxs-lookup"><span data-stu-id="09b7a-112">Use the [**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) method to determine the controller ports that are contained by a specific controller.</span></span> <span data-ttu-id="09b7a-113">I chiamanti possono ottenere un puntatore a una porta del controller specifica selezionando l'oggetto porta del controller desiderato dall'enumerazione restituita dal metodo **QueryControllerPorts** .</span><span class="sxs-lookup"><span data-stu-id="09b7a-113">Callers can get a pointer to a specific controller port by selecting the desired controller port object from the enumeration that is returned by the **QueryControllerPorts** method.</span></span> <span data-ttu-id="09b7a-114">Con un oggetto controller, un chiamante può impostare lo stato della porta del controller e la query per i LUN associati.</span><span class="sxs-lookup"><span data-stu-id="09b7a-114">With a controller object, a caller can set the controller port status and query for its associated LUNs.</span></span>

<span data-ttu-id="09b7a-115">Le proprietà dell'oggetto controller includono un identificatore di oggetto, un nome, un numero di serie e lo stato della porta del controller.</span><span class="sxs-lookup"><span data-stu-id="09b7a-115">Controller object properties include an object identifier, a name, a serial number, and the controller port status.</span></span>

<span data-ttu-id="09b7a-116">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="09b7a-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="09b7a-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="09b7a-117">Type</span></span>                                                                                              | <span data-ttu-id="09b7a-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="09b7a-118">Element</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b7a-119">Interfacce sempre esposte da questo oggetto in VDS 1,1 e 2,0 Fibre Channel solo provider</span><span class="sxs-lookup"><span data-stu-id="09b7a-119">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="09b7a-120">**IVdsControllerPort**</span><span class="sxs-lookup"><span data-stu-id="09b7a-120">**IVdsControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| <span data-ttu-id="09b7a-121">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="09b7a-121">Associated enumerations</span></span>                                                                           | [<span data-ttu-id="09b7a-122">**\_stato porta \_ VDS**</span><span class="sxs-lookup"><span data-stu-id="09b7a-122">**VDS\_PORT\_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| <span data-ttu-id="09b7a-123">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="09b7a-123">Associated structures</span></span>                                                                             | <span data-ttu-id="09b7a-124">[**VDS \_ Notifica \_ della porta e della porta**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) [ **VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span><span class="sxs-lookup"><span data-stu-id="09b7a-124">[**VDS\_PORT\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="09b7a-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09b7a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09b7a-126">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="09b7a-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="09b7a-127">**IVdsControllerControllerPort::QueryControllerPorts**</span><span class="sxs-lookup"><span data-stu-id="09b7a-127">**IVdsControllerControllerPort::QueryControllerPorts**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
