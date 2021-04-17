---
description: Oggetto gruppo portale
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Oggetto gruppo portale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530151"
---
# <a name="portal-group-object"></a><span data-ttu-id="63386-103">Oggetto gruppo portale</span><span class="sxs-lookup"><span data-stu-id="63386-103">Portal Group Object</span></span>

<span data-ttu-id="63386-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63386-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="63386-105">Un oggetto gruppo di portali modella un gruppo di portale iSCSI contenuto all'interno di una destinazione iSCSI.</span><span class="sxs-lookup"><span data-stu-id="63386-105">A portal group object models an iSCSI portal group that is contained within an iSCSI target.</span></span>

<span data-ttu-id="63386-106">Usare il metodo [**IVdsIscsiTarget:: QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) per determinare i gruppi di portali contenuti in una destinazione specifica.</span><span class="sxs-lookup"><span data-stu-id="63386-106">Use the [**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) method to determine the portal groups that are contained by a specific target.</span></span> <span data-ttu-id="63386-107">Usare il metodo [**IVdsIscsiPortal:: QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) per determinare i gruppi di portale associati a un portale specificato.</span><span class="sxs-lookup"><span data-stu-id="63386-107">Use the [**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) method to determine the portal groups that are associated with a specified portal.</span></span> <span data-ttu-id="63386-108">I chiamanti possono ottenere un puntatore a un gruppo di portale specifico selezionando l'oggetto gruppo portale desiderato dall'enumerazione restituita dal metodo **QueryPortalGroups** o dal metodo **QueryAssociatedPortalGroups** .</span><span class="sxs-lookup"><span data-stu-id="63386-108">Callers can get a pointer to a specific portal group by selecting the desired portal group object from the enumeration that is returned by the **QueryPortalGroups** method or the **QueryAssociatedPortalGroups** method.</span></span> <span data-ttu-id="63386-109">Con un oggetto gruppo di portale è possibile aggiungere o rimuovere portali ed eseguire query per le proprietà dei gruppi di portali, i portali associati e la destinazione contenente il gruppo di portale.</span><span class="sxs-lookup"><span data-stu-id="63386-109">With a portal group object, you can add or remove portals and query for portal group properties, associated portals, and the target that contains the portal group.</span></span>

<span data-ttu-id="63386-110">Le proprietà dell'oggetto gruppo portale includono un [identificatore di oggetto](vds-data-types.md) e il tag di gruppo del portale.</span><span class="sxs-lookup"><span data-stu-id="63386-110">Portal group object properties include an [object identifier](vds-data-types.md) and the portal group tag.</span></span> <span data-ttu-id="63386-111">Per ulteriori informazioni sui tag dei gruppi di portale, vedere la specifica iSCSI all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=158752> .</span><span class="sxs-lookup"><span data-stu-id="63386-111">For more information about portal group tags, see the iSCSI specification at <https://go.microsoft.com/fwlink/p/?linkid=158752>.</span></span>

<span data-ttu-id="63386-112">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="63386-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="63386-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="63386-113">Type</span></span>                                                                                      | <span data-ttu-id="63386-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="63386-114">Element</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63386-115">Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0</span><span class="sxs-lookup"><span data-stu-id="63386-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="63386-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span><span class="sxs-lookup"><span data-stu-id="63386-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span></span>                                                                                              |
| <span data-ttu-id="63386-117">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="63386-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="63386-118">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="63386-118">None.</span></span>                                                                                                                                              |
| <span data-ttu-id="63386-119">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="63386-119">Associated structures</span></span>                                                                     | <span data-ttu-id="63386-120">[**VDS \_ Notifica del gruppo ISCSI \_ PORTALGROUP \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) e del [**\_ portale \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span><span class="sxs-lookup"><span data-stu-id="63386-120">[**VDS\_ISCSI\_PORTALGROUP\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) and [**VDS\_PORTAL\_GROUP\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="63386-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63386-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63386-122">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="63386-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="63386-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="63386-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[<span data-ttu-id="63386-124">**IVdsIscsiTarget::QueryPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="63386-124">**IVdsIscsiTarget::QueryPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
