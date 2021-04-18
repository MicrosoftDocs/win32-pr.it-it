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
# <a name="disk_cluster_info-structure"></a>\_Struttura informazioni cluster di dischi \_

Rappresenta le informazioni mantenute in Gestione partizioni relative a un disco che fa parte di un cluster.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Versione**
</dt> <dd>

Numero di versione. Questo valore deve essere impostato sulle dimensioni di questa struttura.

</dd> <dt>

**Flag**
</dt> <dd>

Combinazione di flag correlati a dischi e cluster.



| Valore                                                                                                                                                                                                                                                                                               | Significato                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**Disco \_ di \_Flag cluster \_ abilitato**</dt> <dt>1</dt> </dl>                                          | Il disco viene utilizzato come parte del servizio cluster.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**Disco \_ di \_Flag cluster \_ CSV**</dt> <dt>2</dt> </dl>                                                      | I volumi sul disco vengono esposti da CSVFS in tutti i nodi del cluster.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**Disco \_ di \_Flag \_ del cluster nella \_ manutenzione**</dt> <dt>4</dt> </dl>                    | La risorsa cluster associata a questo disco si trova in modalità manutenzione.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**Disco \_ di \_Flag cluster \_ PNP \_ arrivo \_ completato**</dt> <dt>8</dt> </dl> | Il driver del disco del cluster per la modalità kernel (Clusdisk) ha ricevuto una notifica PnP dell'arrivo del disco.<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

Flag che vengono modificati nel membro dei **flag** .

</dd> <dt>

**Notificare**
</dt> <dd>

**True** per inviare una notifica di modifica del layout. in caso contrario, **false**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntdddisk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di gestione del disco](disk-management-structures.md)
</dt> <dt>

[**\_informazioni su disco IOCTL per \_ ottenere il \_ cluster \_**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**\_informazioni sul \_ cluster del set di dischi IOCTL \_ \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




