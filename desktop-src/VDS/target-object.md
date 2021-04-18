---
description: Oggetto di destinazione
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Oggetto di destinazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318209"
---
# <a name="target-object"></a><span data-ttu-id="88190-103">Oggetto di destinazione</span><span class="sxs-lookup"><span data-stu-id="88190-103">Target Object</span></span>

<span data-ttu-id="88190-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="88190-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="88190-105">Un oggetto di destinazione modella una destinazione iSCSI contenuta all'interno di un sottosistema iSCSI.</span><span class="sxs-lookup"><span data-stu-id="88190-105">A target object models an iSCSI target that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="88190-106">Usare il metodo [**IVdsSubSystemIscsi:: QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) per determinare le destinazioni iSCSI del sottosistema.</span><span class="sxs-lookup"><span data-stu-id="88190-106">Use the [**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) method to determine the iSCSI targets of the subsystem.</span></span> <span data-ttu-id="88190-107">I chiamanti possono ottenere un puntatore a una destinazione specifica selezionando l'oggetto di destinazione desiderato dall'enumerazione restituita dal metodo **QueryTargets** .</span><span class="sxs-lookup"><span data-stu-id="88190-107">Callers can get a pointer to a specific target by selecting the desired target object from the enumeration that is returned by the **QueryTargets** method.</span></span> <span data-ttu-id="88190-108">Con un oggetto di destinazione è possibile impostare il nome descrittivo e la query della destinazione per le proprietà di destinazione, i LUN associati e il sottosistema che contiene la destinazione.</span><span class="sxs-lookup"><span data-stu-id="88190-108">With a target object, you can set the target's friendly name and query for target properties, associated LUNs, and the subsystem that contains the target.</span></span>

<span data-ttu-id="88190-109">I computer host devono accedere alle destinazioni per accedere ai Lun associati.</span><span class="sxs-lookup"><span data-stu-id="88190-109">Host computers must log on to targets to access their associated LUNs.</span></span> <span data-ttu-id="88190-110">Per eseguire un accesso a una destinazione, è necessario che la destinazione disponga di almeno un portale associato in uno dei relativi gruppi di portale.</span><span class="sxs-lookup"><span data-stu-id="88190-110">To perform a logon to a target, the target must have at least one associated portal in one of its portal groups.</span></span> <span data-ttu-id="88190-111">L'input e l'output dei lun associati vengono gestiti tramite questa sessione di accesso.</span><span class="sxs-lookup"><span data-stu-id="88190-111">Input to and output from associated LUNs is handled through this logon session.</span></span>

<span data-ttu-id="88190-112">Le proprietà dell'oggetto di destinazione includono un identificatore di oggetto, un nome iSCSI, un nome descrittivo e un flag abilitato per CHAP.</span><span class="sxs-lookup"><span data-stu-id="88190-112">Target object properties include an object identifier, an iSCSI name, a friendly name, and a CHAP-enabled flag.</span></span>

<span data-ttu-id="88190-113">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="88190-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="88190-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="88190-114">Type</span></span>                                                                                      | <span data-ttu-id="88190-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="88190-115">Element</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88190-116">Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0</span><span class="sxs-lookup"><span data-stu-id="88190-116">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="88190-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span><span class="sxs-lookup"><span data-stu-id="88190-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span></span>                                                                                 |
| <span data-ttu-id="88190-118">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="88190-118">Associated enumerations</span></span>                                                                   | <span data-ttu-id="88190-119">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="88190-119">None.</span></span>                                                                                                                       |
| <span data-ttu-id="88190-120">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="88190-120">Associated structures</span></span>                                                                     | <span data-ttu-id="88190-121">[**VDS \_ Notifica \_ di \_ destinazione iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) e [**\_ destinazione \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span><span class="sxs-lookup"><span data-stu-id="88190-121">[**VDS\_ISCSI\_TARGET\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) and [**VDS\_TARGET\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="88190-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88190-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88190-123">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="88190-123">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="88190-124">**IVdsSubSystemIscsi::QueryTargets**</span><span class="sxs-lookup"><span data-stu-id="88190-124">**IVdsSubSystemIscsi::QueryTargets**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
