---
description: Rappresenta le informazioni mantenute in Gestione partizioni relative a un disco che fa parte di un cluster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: Struttura DISK_CLUSTER_INFO (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312357"
---
# <a name="disk_cluster_info-structure"></a><span data-ttu-id="b5608-103">\_Struttura informazioni cluster di dischi \_</span><span class="sxs-lookup"><span data-stu-id="b5608-103">DISK\_CLUSTER\_INFO structure</span></span>

<span data-ttu-id="b5608-104">Rappresenta le informazioni mantenute in Gestione partizioni relative a un disco che fa parte di un cluster.</span><span class="sxs-lookup"><span data-stu-id="b5608-104">Represents information maintained on the partition manager about a disk that is part of a cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5608-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5608-105">Syntax</span></span>


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a><span data-ttu-id="b5608-106">Members</span><span class="sxs-lookup"><span data-stu-id="b5608-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5608-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="b5608-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="b5608-108">Numero di versione.</span><span class="sxs-lookup"><span data-stu-id="b5608-108">The version number.</span></span> <span data-ttu-id="b5608-109">Questo valore deve essere impostato sulle dimensioni di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="b5608-109">This value must be set to the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5608-110">**Flag**</span><span class="sxs-lookup"><span data-stu-id="b5608-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b5608-111">Combinazione di flag correlati a dischi e cluster.</span><span class="sxs-lookup"><span data-stu-id="b5608-111">A combination of flags related to disks and clusters.</span></span>



| <span data-ttu-id="b5608-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b5608-112">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="b5608-113">Significato</span><span class="sxs-lookup"><span data-stu-id="b5608-113">Meaning</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <span data-ttu-id="b5608-114"><dt>**Disco \_ di \_Flag cluster \_ abilitato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b5608-114"><dt>**DISK\_CLUSTER\_FLAG\_ENABLED**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="b5608-115">Il disco viene utilizzato come parte del servizio cluster.</span><span class="sxs-lookup"><span data-stu-id="b5608-115">The disk is used as part of the cluster service.</span></span><br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <span data-ttu-id="b5608-116"><dt>**Disco \_ di \_Flag cluster \_ CSV**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b5608-116"><dt>**DISK\_CLUSTER\_FLAG\_CSV**</dt> <dt>2</dt></span></span> </dl>                                                      | <span data-ttu-id="b5608-117">I volumi sul disco vengono esposti da CSVFS in tutti i nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="b5608-117">Volumes on the disk are exposed by CSVFS on all nodes of the cluster.</span></span><br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <span data-ttu-id="b5608-118"><dt>**Disco \_ di \_Flag \_ del cluster nella \_ manutenzione**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b5608-118"><dt>**DISK\_CLUSTER\_FLAG\_IN\_MAINTENANCE**</dt> <dt>4</dt></span></span> </dl>                    | <span data-ttu-id="b5608-119">La risorsa cluster associata a questo disco si trova in modalità manutenzione.</span><span class="sxs-lookup"><span data-stu-id="b5608-119">The cluster resource associated with this disk is in maintenance mode.</span></span><br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <span data-ttu-id="b5608-120"><dt>**Disco \_ di \_Flag cluster \_ PNP \_ arrivo \_ completato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b5608-120"><dt>**DISK\_CLUSTER\_FLAG\_PNP\_ARRIVAL\_COMPLETE**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="b5608-121">Il driver del disco del cluster per la modalità kernel (Clusdisk) ha ricevuto una notifica PnP dell'arrivo del disco.</span><span class="sxs-lookup"><span data-stu-id="b5608-121">The cluster disk driver for kernel mode (clusdisk) has received PnP notification of the arrival of the disk.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b5608-122">**FlagsMask**</span><span class="sxs-lookup"><span data-stu-id="b5608-122">**FlagsMask**</span></span>
</dt> <dd>

<span data-ttu-id="b5608-123">Flag che vengono modificati nel membro dei **flag** .</span><span class="sxs-lookup"><span data-stu-id="b5608-123">The flags that are being modified in the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="b5608-124">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="b5608-124">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="b5608-125">**True** per inviare una notifica di modifica del layout. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b5608-125">**TRUE** to send a layout change notification; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5608-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5608-126">Requirements</span></span>



| <span data-ttu-id="b5608-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5608-127">Requirement</span></span> | <span data-ttu-id="b5608-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b5608-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5608-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5608-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b5608-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b5608-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="b5608-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5608-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b5608-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b5608-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5608-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5608-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5608-134"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5608-134"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5608-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5608-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5608-136">Strutture di gestione del disco</span><span class="sxs-lookup"><span data-stu-id="b5608-136">Disk Management Structures</span></span>](disk-management-structures.md)
</dt> <dt>

[<span data-ttu-id="b5608-137">**\_informazioni su disco IOCTL per \_ ottenere il \_ cluster \_**</span><span class="sxs-lookup"><span data-stu-id="b5608-137">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="b5608-138">**\_informazioni sul \_ cluster del set di dischi IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5608-138">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




