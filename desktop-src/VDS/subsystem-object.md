---
description: Oggetto sottosistema
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Oggetto sottosistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104550183"
---
# <a name="subsystem-object"></a><span data-ttu-id="2b3ab-103">Oggetto sottosistema</span><span class="sxs-lookup"><span data-stu-id="2b3ab-103">Subsystem Object</span></span>

<span data-ttu-id="2b3ab-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2b3ab-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="2b3ab-105">Un oggetto del sottosistema modella un sottosistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-105">A subsystem object models a storage subsystem.</span></span> <span data-ttu-id="2b3ab-106">Un sottosistema è un'enclosure RAID o una scheda RAID PCI.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-106">A subsystem is either a RAID enclosure or a PCI RAID card.</span></span> <span data-ttu-id="2b3ab-107">Un singolo computer host può essere connesso a un numero qualsiasi di sottosistemi.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-107">A single host computer can be connected to any number of subsystems.</span></span> <span data-ttu-id="2b3ab-108">Ogni sottosistema è gestito da un solo provider hardware.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-108">Each subsystem is managed by exactly one hardware provider.</span></span> <span data-ttu-id="2b3ab-109">In una configurazione SAN la classe del sottosistema rappresenta un'enclosure di archiviazione SAN.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-109">In a SAN configuration, the subsystem class represents a SAN storage enclosure.</span></span>

<span data-ttu-id="2b3ab-110">Un sottosistema può contenere un numero qualsiasi di controller e unità e può rendere visibile (annullare il mascheramento) un numero qualsiasi di lun nel computer in cui è in esecuzione il provider hardware.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-110">A subsystem can contain any number of controllers and drives, and can surface (unmask) any number of LUNs to the computer on which the hardware provider is running.</span></span> <span data-ttu-id="2b3ab-111">I sottosistemi di fascia superiore possono annullare il mascheramento dei LUN in altri computer della rete.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-111">Higher-end subsystems can unmask LUNs to other computers on the network.</span></span> <span data-ttu-id="2b3ab-112">Ogni unità disco all'interno di un sottosistema è connessa a un bus e occupa uno slot del bus.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-112">Each disk drive within a subsystem is connected to a bus and occupies a slot in the bus.</span></span> <span data-ttu-id="2b3ab-113">Ogni controller all'interno di un sottosistema dispone di una o più porte del controller.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-113">Each controller within a subsystem has one or more controller ports.</span></span>

<span data-ttu-id="2b3ab-114">L'illustrazione seguente mostra i dispositivi fisici contenuti in un sottosistema (i LUN non vengono visualizzati) e le relazioni tra di essi.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-114">The illustration that follows shows the physical devices contained in a subsystem (LUNs are not shown) and the relationships among them.</span></span>

![Diagramma che mostra un sottosistema che inizia con "Ports" a sinistra, che passa a "Controllers" e quindi a "bus" con "slot" che portano a singole "unità".](images/vdssubsystem.png)

<span data-ttu-id="2b3ab-116">Le applicazioni VDS usano il metodo [**IVdsHwProvider:: QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) per eseguire query sui sottosistemi che appartengono a un provider hardware specifico.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-116">VDS applications use the [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) method to query the subsystems that belong to a specific hardware provider.</span></span> <span data-ttu-id="2b3ab-117">I chiamanti possono ottenere un puntatore a un sottosistema specifico selezionando l'oggetto del sottosistema desiderato dall'enumerazione restituita dal metodo **QuerySubSystems** .</span><span class="sxs-lookup"><span data-stu-id="2b3ab-117">Callers can get a pointer to a specific subsystem by selecting the desired subsystem object from the enumeration that is returned by the **QuerySubSystems** method.</span></span> <span data-ttu-id="2b3ab-118">Con un oggetto sottosistema è possibile impostare lo stato del sottosistema, creare lun, sostituire unità ed eseguire query per controller, unità e lun.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-118">With a subsystem object, you can set the subsystem status, create LUNs, replace drives, and query for controllers, drives, and LUNs.</span></span>

<span data-ttu-id="2b3ab-119">Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto sottosistema includono lo stato, l'integrità e i flag del sottosistema. numero di controller, slot e bus; e un'impostazione della priorità di ricompilazione.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-119">In addition to an object identifier, a name, and a serial number, subsystem object properties include the subsystem status, health, and flags; a count of the controllers, slots, and buses; and a rebuild priority setting.</span></span>

<span data-ttu-id="2b3ab-120">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-120">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="2b3ab-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b3ab-121">Type</span></span>                                                                                      | <span data-ttu-id="2b3ab-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="2b3ab-122">Element</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3ab-123">Interfacce sempre esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="2b3ab-123">Interfaces that are always exposed by this object</span></span>                                         | <span data-ttu-id="2b3ab-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span><span class="sxs-lookup"><span data-stu-id="2b3ab-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span></span>                                                                                          |
| <span data-ttu-id="2b3ab-125">Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0</span><span class="sxs-lookup"><span data-stu-id="2b3ab-125">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="2b3ab-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) e [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span><span class="sxs-lookup"><span data-stu-id="2b3ab-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) and [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span></span>             |
| <span data-ttu-id="2b3ab-127">Interfacce che possono essere esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="2b3ab-127">Interfaces that may be exposed by this object</span></span>                                             | <span data-ttu-id="2b3ab-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) e [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span><span class="sxs-lookup"><span data-stu-id="2b3ab-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) and [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span></span>                               |
| <span data-ttu-id="2b3ab-129">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="2b3ab-129">Associated enumerations</span></span>                                                                   | <span data-ttu-id="2b3ab-130">[**VDS \_ \_ \_ Flag del sottosistema**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) e [**\_ \_ \_ stato del sottosistema VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span><span class="sxs-lookup"><span data-stu-id="2b3ab-130">[**VDS\_SUB\_SYSTEM\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) and [**VDS\_SUB\_SYSTEM\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span></span>             |
| <span data-ttu-id="2b3ab-131">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="2b3ab-131">Associated structures</span></span>                                                                     | <span data-ttu-id="2b3ab-132">[**VDS \_ Sottosistema \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) e [**\_ \_ \_ notifica del sottosistema VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span><span class="sxs-lookup"><span data-stu-id="2b3ab-132">[**VDS\_SUB\_SYSTEM\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) and [**VDS\_SUB\_SYSTEM\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2b3ab-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b3ab-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b3ab-134">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="2b3ab-134">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="2b3ab-135">**IVdsHwProvider::QuerySubSystems**</span><span class="sxs-lookup"><span data-stu-id="2b3ab-135">**IVdsHwProvider::QuerySubSystems**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
