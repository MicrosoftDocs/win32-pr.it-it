---
description: Interazioni e comportamenti del provider hardware
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interazioni e comportamenti del provider hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227041"
---
# <a name="hardware-provider-interactions-and-behaviors"></a><span data-ttu-id="bd513-103">Interazioni e comportamenti del provider hardware</span><span class="sxs-lookup"><span data-stu-id="bd513-103">Hardware Provider Interactions and Behaviors</span></span>

<span data-ttu-id="bd513-104">I provider hardware possono supportare le copie shadow del mirroring copy-on-Write e/o di copia completa (differenziale e/o Plex).</span><span class="sxs-lookup"><span data-stu-id="bd513-104">Hardware providers may support copy-on-write and/or full copy mirror (differential and/or plex) shadow copies.</span></span> <span data-ttu-id="bd513-105">L'allocazione delle risorse per le copie shadow deve seguire il contesto specificato dal richiedente in [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerato dal [**\_ \_ \_ contesto dello snapshot VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), per il set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="bd513-105">Resource allocation for shadow copies should follow the context specified by the requester in [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerated by [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), for the shadow copy set.</span></span>

-   <span data-ttu-id="bd513-106">Se il richiedente specifica un contesto di copia shadow supportato dal provider, il provider deve creare una copia shadow usando tale metodo.</span><span class="sxs-lookup"><span data-stu-id="bd513-106">If the requester specifies a shadow copy context that is supported by the provider, the provider should create a shadow copy using that method.</span></span>
-   <span data-ttu-id="bd513-107">Se il richiedente specifica un contesto di copia shadow non supportato dal provider, il provider non deve tentare di creare la copia shadow e restituire **false** tramite il parametro *pbIsSupported* in [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span><span class="sxs-lookup"><span data-stu-id="bd513-107">If the requester specifies a shadow copy context that is not supported by the provider, then the provider should not attempt to create the shadow copy and return **FALSE** through the *pbIsSupported* parameter in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span></span>
-   <span data-ttu-id="bd513-108">Se il richiedente non specifica in modo esplicito un contesto di copia shadow, il provider deve usare un comportamento predefinito ragionevole per la creazione di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="bd513-108">If the requester does not explicitly specify a shadow copy context, then the provider should use reasonable default behavior for shadow copy creation.</span></span>

<span data-ttu-id="bd513-109">I provider di hardware associati ai sottosistemi RAID SAN devono supportare copie shadow trasportabili per consentire lo spostamento tra gli host in una rete SAN.</span><span class="sxs-lookup"><span data-stu-id="bd513-109">Hardware providers associated with SAN RAID subsystems should support transportable shadow copies to allow movement between hosts on a SAN.</span></span>

<span data-ttu-id="bd513-110">I provider hardware in esecuzione su più computer in una rete SAN che gestiscono lo stesso sottosistema RAID non devono coordinarsi tra i provider di una rete SAN.</span><span class="sxs-lookup"><span data-stu-id="bd513-110">Hardware providers running on multiple machines on a SAN yet managing the same RAID subsystem do not need to coordinate between providers on a SAN.</span></span> <span data-ttu-id="bd513-111">Il coordinatore mantiene lo stato necessario.</span><span class="sxs-lookup"><span data-stu-id="bd513-111">The coordinator maintains any necessary state.</span></span> <span data-ttu-id="bd513-112">Sono stati riconosciuti due tipi di stato:</span><span class="sxs-lookup"><span data-stu-id="bd513-112">Two kinds of state are recognized:</span></span>

-   <span data-ttu-id="bd513-113">Stato necessario per supportare l'accesso ai dati nei volumi contenuti in una copia shadow dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="bd513-113">State necessary to support data access to the volumes contained on a hardware shadow copy.</span></span> <span data-ttu-id="bd513-114">Sono inclusi i tag di un volume come di sola lettura o nascosti.</span><span class="sxs-lookup"><span data-stu-id="bd513-114">This includes any tagging of a volume as read-only or hidden.</span></span> <span data-ttu-id="bd513-115">Questo stato deve essere sul LUN hardware e viaggiare con il LUN.</span><span class="sxs-lookup"><span data-stu-id="bd513-115">This state must be on the hardware LUN and travel with the LUN.</span></span> <span data-ttu-id="bd513-116">Questo stato viene mantenuto tra le Epoch di avvio e/o l'individuazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd513-116">This state is preserved across boot epochs and/or device discovery.</span></span> <span data-ttu-id="bd513-117">VSS gestisce questo stato per la durata della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="bd513-117">VSS manages this state for the lifetime of the shadow copy.</span></span>
-   <span data-ttu-id="bd513-118">Stato necessario per riconoscere un volume specifico come parte di un set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="bd513-118">State necessary to recognize a specific volume as part of a shadow copy set.</span></span> <span data-ttu-id="bd513-119">Questo stato viene reso permanente da VSS insieme al richiedente che ha creato originariamente il set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="bd513-119">This state is persisted by VSS in conjunction with the requester that originally created the shadow copy set.</span></span>

<span data-ttu-id="bd513-120">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="bd513-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="bd513-121">Processo di creazione della copia shadow</span><span class="sxs-lookup"><span data-stu-id="bd513-121">The Shadow Copy Creation Process</span></span>](the-shadow-copy-creation-process.md)
-   [<span data-ttu-id="bd513-122">Comportamenti necessari per i provider di copie shadow</span><span class="sxs-lookup"><span data-stu-id="bd513-122">Required Behaviors for Shadow Copy Providers</span></span>](required-behaviors-for-shadow-copy-providers.md)
-   [<span data-ttu-id="bd513-123">Transizioni di stato nei provider di copie shadow</span><span class="sxs-lookup"><span data-stu-id="bd513-123">State Transitions in shadow copy providers</span></span>](state-transitions-in-shadow-copy-providers.md)
-   [<span data-ttu-id="bd513-124">Gestione degli errori nei provider di copie shadow</span><span class="sxs-lookup"><span data-stu-id="bd513-124">Error Handling in shadow copy providers</span></span>](error-handling-in-shadow-copy-providers.md)

 

 



