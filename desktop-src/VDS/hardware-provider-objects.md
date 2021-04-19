---
description: Oggetti provider hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Oggetti provider hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320217"
---
# <a name="hardware-provider-objects"></a><span data-ttu-id="da270-103">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="da270-103">Hardware Provider Objects</span></span>

<span data-ttu-id="da270-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="da270-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="da270-105">Il modello a oggetti VDS include un set di oggetti per eseguire query e configurare le entità del provider hardware.</span><span class="sxs-lookup"><span data-stu-id="da270-105">The VDS object model includes a set of objects to query and configure hardware provider entities.</span></span> <span data-ttu-id="da270-106">Si noti che mentre VDS include un provider di software, è necessario acquistare un provider hardware e l'hardware associato separatamente per sfruttare i vantaggi degli oggetti provider hardware. Questi oggetti provider hardware rappresentano i dispositivi fisici (ad esempio, sottosistemi, unità e controller) e i dispositivi virtuali, ad esempio lun e i PLEX LUN.</span><span class="sxs-lookup"><span data-stu-id="da270-106">(Note that while VDS includes a software provider, you must purchase a hardware provider and the associated hardware separately to take advantage of the hardware provider objects.) These hardware provider objects represent physical devices (such as subsystems, drives, and controllers) and virtual devices (such as LUNs and LUN plexes).</span></span>

<span data-ttu-id="da270-107">Un provider hardware deve creare un oggetto COM per ogni dispositivo fisico o virtuale.</span><span class="sxs-lookup"><span data-stu-id="da270-107">A hardware provider should create one COM object for each physical or virtual device.</span></span>

<span data-ttu-id="da270-108">Nell'illustrazione seguente viene illustrata la relazione tra l'oggetto provider e il set di oggetti provider hardware, nonché la relazione tra i vari oggetti provider hardware.</span><span class="sxs-lookup"><span data-stu-id="da270-108">The illustration that follows shows the relationship between the provider object and the set of hardware provider objects, as well as the relationship between the various hardware provider objects themselves.</span></span>

![<span data-ttu-id="da270-109">Diagramma che mostra la relazione tra' provider ' è Subsystem ',' controller ',' LUN ',' LUN Plex ',' drive ' è mandrino '.</span><span class="sxs-lookup"><span data-stu-id="da270-109">Diagram that shows the relationship between the 'Provider' and 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive', and 'Spindle'.</span></span> ](images/vdshwobjects.png)

<span data-ttu-id="da270-110">Un oggetto provider può contenere un numero qualsiasi di sottosistemi.</span><span class="sxs-lookup"><span data-stu-id="da270-110">A provider object can contain any number of subsystems.</span></span> <span data-ttu-id="da270-111">Tutti i provider hardware sono in grado di gestire più istanze dello stesso modello di sottosistema.</span><span class="sxs-lookup"><span data-stu-id="da270-111">All hardware providers are capable of managing multiple instances of the same subsystem model.</span></span> <span data-ttu-id="da270-112">Molti provider di hardware sono inoltre in grado di gestire più istanze di modelli di sottosistema diversi.</span><span class="sxs-lookup"><span data-stu-id="da270-112">Many hardware providers are also capable of managing multiple instances of different subsystem models.</span></span> <span data-ttu-id="da270-113">Un singolo computer può ospitare un numero qualsiasi di provider hardware.</span><span class="sxs-lookup"><span data-stu-id="da270-113">A single computer can host any number of hardware providers.</span></span>

<span data-ttu-id="da270-114">Un oggetto sottosistema può contenere un numero qualsiasi di controller e unità e può presentare un numero qualsiasi di lun.</span><span class="sxs-lookup"><span data-stu-id="da270-114">A subsystem object can contain any number of controllers and drives, and can surface any number of LUNs.</span></span> <span data-ttu-id="da270-115">Un oggetto LUN è costituito da almeno un PLEX LUN e ogni PLEX LUN esegue il mapping a una o più unità, a seconda del tipo di Plex.</span><span class="sxs-lookup"><span data-stu-id="da270-115">A LUN object comprises of at least one LUN plex, and each LUN plex maps to one or more drives, depending on the plex type.</span></span> <span data-ttu-id="da270-116">Gli oggetti controller possono gestire l'input/output dei dati per qualsiasi numero di oggetti LUN.</span><span class="sxs-lookup"><span data-stu-id="da270-116">Controller objects can manage data input/output for any number of LUN objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da270-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da270-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da270-118">Modello a oggetti VDS</span><span class="sxs-lookup"><span data-stu-id="da270-118">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
