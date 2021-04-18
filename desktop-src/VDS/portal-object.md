---
description: Oggetto portale
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Oggetto portale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01328d8dccfe7a29c0686cde9b531df63d56e63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318594"
---
# <a name="portal-object"></a><span data-ttu-id="321b1-103">Oggetto portale</span><span class="sxs-lookup"><span data-stu-id="321b1-103">Portal Object</span></span>

<span data-ttu-id="321b1-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="321b1-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="321b1-105">Un oggetto portale modella un portale iSCSI contenuto all'interno di un sottosistema iSCSI.</span><span class="sxs-lookup"><span data-stu-id="321b1-105">A portal object models an iSCSI portal that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="321b1-106">Usare il metodo [**IVdsSubSystemIscsi:: QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) per determinare i portali iSCSI del sottosistema.</span><span class="sxs-lookup"><span data-stu-id="321b1-106">Use the [**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) method to determine the iSCSI portals of the subsystem.</span></span> <span data-ttu-id="321b1-107">I chiamanti possono ottenere un puntatore a un portale specifico selezionando l'oggetto portale desiderato dall'enumerazione restituita dal metodo **QueryPortals** .</span><span class="sxs-lookup"><span data-stu-id="321b1-107">Callers can get a pointer to a specific portal by selecting the desired portal object from the enumeration that is returned by the **QueryPortals** method.</span></span> <span data-ttu-id="321b1-108">Con un oggetto portale è possibile impostare lo stato del portale e la query per le proprietà del portale, i gruppi di portale associati e il sottosistema che contiene il portale.</span><span class="sxs-lookup"><span data-stu-id="321b1-108">With a portal object, you can set the portal status and query for portal properties, associated portal groups, and the subsystem that contains the portal.</span></span>

<span data-ttu-id="321b1-109">Un oggetto portale può essere associato al massimo un gruppo di portale di una destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="321b1-109">A portal object can only be associated with at most one portal group of a specified target.</span></span>

<span data-ttu-id="321b1-110">I portali servono come uno degli endpoint dei percorsi MPIO nei provider di hardware iSCSI, su cui è possibile imporre i criteri di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="321b1-110">Portals serve as one of the endpoints of MPIO paths in iSCSI hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="321b1-111">Le proprietà dell'oggetto portale includono un identificatore di oggetto, un indirizzo IP e una porta e lo stato del portale.</span><span class="sxs-lookup"><span data-stu-id="321b1-111">Portal object properties include an object identifier, an IP address and port, and the portal status.</span></span>

<span data-ttu-id="321b1-112">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="321b1-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="321b1-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="321b1-113">Type</span></span>                                                                                      | <span data-ttu-id="321b1-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="321b1-114">Element</span></span>                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321b1-115">Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0</span><span class="sxs-lookup"><span data-stu-id="321b1-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="321b1-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span><span class="sxs-lookup"><span data-stu-id="321b1-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span></span>                                                                             |
| <span data-ttu-id="321b1-117">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="321b1-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="321b1-118">[**VDS \_ \_ \_ stato del portale iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span><span class="sxs-lookup"><span data-stu-id="321b1-118">[**VDS\_ISCSI\_PORTAL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span></span>                                                          |
| <span data-ttu-id="321b1-119">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="321b1-119">Associated structures</span></span>                                                                     | <span data-ttu-id="321b1-120">[**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) [**Notifica delle \_ porte \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)del portale iSCSI e VDS.</span><span class="sxs-lookup"><span data-stu-id="321b1-120">[**VDS\_ISCSI\_PORTAL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="321b1-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="321b1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="321b1-122">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="321b1-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="321b1-123">**IVdsSubSystemIscsi::QueryPortals**</span><span class="sxs-lookup"><span data-stu-id="321b1-123">**IVdsSubSystemIscsi::QueryPortals**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
