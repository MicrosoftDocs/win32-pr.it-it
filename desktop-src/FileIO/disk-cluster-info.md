---
description: Rappresenta le informazioni mantenute nella gestione partizioni su un disco che fa parte di un cluster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: DISK_CLUSTER_INFO (Ntdddisk.h)
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
ms.openlocfilehash: be4db89e888778c3d92090a32243f0203b527337b3734328a183b551a6181f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813793"
---
# <a name="disk_cluster_info-structure"></a>Struttura DISK \_ CLUSTER \_ INFO

Rappresenta le informazioni mantenute nella gestione partizioni su un disco che fa parte di un cluster.

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

**Version**
</dt> <dd>

Numero di versione. Questo valore deve essere impostato sulla dimensione di questa struttura .

</dd> <dt>

**Flag**
</dt> <dd>

Combinazione di flag correlati a dischi e cluster.



| Valore                                                                                                                                                                                                                                                                                               | Significato                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**DISK \_ FLAG \_ CLUSTER \_ ABILITATO**</dt> <dt>1</dt> </dl>                                          | Il disco viene usato come parte del servizio cluster.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**DISK \_ CLUSTER \_ FLAG \_ CSV**</dt> <dt>2</dt> </dl>                                                      | I volumi sul disco vengono esposti da CSVFS in tutti i nodi del cluster.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**DISK \_ FLAG \_ CLUSTER \_ NELLA \_ MANUTENZIONE**</dt> <dt>4</dt> </dl>                    | La risorsa cluster associata a questo disco è in modalità di manutenzione.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**DISK \_ CLUSTER \_ FLAG \_ PNP \_ ARRIVAL \_ COMPLETE**</dt> <dt>8</dt> </dl> | Il driver del disco del cluster per la modalità kernel (clusdisk) ha ricevuto la notifica PnP dell'arrivo del disco.<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

Flag modificati nel membro **Flags.**

</dd> <dt>

**Notificare**
</dt> <dd>

**TRUE per** inviare una notifica di modifica del layout. in caso contrario, **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntdddisk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di gestione del disco](disk-management-structures.md)
</dt> <dt>

[**INFORMAZIONI SUL \_ CLUSTER GET DEL \_ \_ DISCO \_ IOCTL**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**INFORMAZIONI SUL \_ \_ CLUSTER DEL SET DI \_ DISCHI \_ IOCTL**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




