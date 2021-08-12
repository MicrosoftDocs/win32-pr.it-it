---
description: Notifiche VDS
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: Notifiche VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931731cc9c2b4aa73f7599c1fcbfad2f885bc74978ab15ba4e1efbf9d2a7522c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603114"
---
# <a name="vds-notifications"></a>Notifiche VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un provider può inviare una notifica degli eventi a VDS e VDS può a sua volta inoltrare la notifica alle applicazioni. Il modello di notifica usato da VDS è simile al modello del punto di connessione usato dagli oggetti COM.

VDS genera notifiche del servizio per eventi come l'assegnazione di una lettera di unità o l'arrivo di un disco non allocato. Dopo che VDS ha allocato un disco a un provider, il provider è responsabile della generazione delle notifiche associate. L'illustrazione seguente mostra le interfacce e i metodi usati nel modello di notifica VDS.

![Diagramma che illustra l'interfaccia e i metodi (Advise, OnLoad e OnNotify) tra applicazioni, servizio dischi virtuali e provider V D S.](images/vdsnotification.png)

Per ricevere notifiche, VDS registra [**l'interfaccia IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) con l'oggetto provider chiamando il metodo [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) e passando un puntatore all'interfaccia. Quando si verifica un evento di notifica, ad esempio l'arrivo di un nuovo volume o unità, il provider passa la struttura di notifica appropriata a VDS come parametro del metodo [**IVdsAdviseSink::OnNotify.**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)

Il processo è simile tra un'applicazione e VDS. In particolare, per ricevere notifiche, un'applicazione registra l'interfaccia [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) con VDS chiamando il metodo [**IVdsService::Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) e passando un puntatore all'interfaccia. Quando VDS riceve una notifica da un provider, passa la struttura di notifica appropriata alle applicazioni registrate come parametro del metodo [**IVdsAdviseSink::OnNotify.**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)

> [!Note]  
> Un'applicazione che chiama [**Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) deve chiamare infine il [**metodo IVdsService::Unadvise.**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) Idealmente, dovrebbe chiamare **Unadvise** non appena non deve più ricevere notifiche.

 

La tabella seguente elenca le notifiche generate dal provider in base al tipo di oggetto.



| Oggetto     | Notifica                              | Valore | Collegamento alla descrizione dell'evento                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **VDS \_ NF \_ PACK \_ ARRIVE**                 | 1     | [**NOTIFICA DEL PACCHETTO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ PACK \_ DEPART**                 | 2     | [**NOTIFICA DEL PACCHETTO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ PACK \_ MODIFY**                 | 3     | [**NOTIFICA DEL PACCHETTO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Volume     | **ARRIVO DEL \_ VOLUME VDS NF \_ \_**               | 4     | [**NOTIFICA DEL VOLUME VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **PARTENZA VOLUME \_ VDS NF \_ \_**               | 5     | [**NOTIFICA DEL VOLUME VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **VDS \_ NF \_ VOLUME \_ MODIFY**               | 6     | [**NOTIFICA DEL VOLUME VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **STATO DI \_ RICOMPILAZIONE DEL VOLUME VDS NF \_ \_ \_** | 7     | [**NOTIFICA DEL VOLUME VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Disco       | **VDS \_ NF \_ DISK \_ ARRIVE**                 | 8     | [**NOTIFICA DEL DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **DISCO VDS \_ NF \_ IN \_ PARTENZA**                 | 9     | [**NOTIFICA DEL DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **VDS \_ NF \_ DISK \_ MODIFY**                 | 10    | [**NOTIFICA DEL DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partition  | **ARRIVO DELLA PARTIZIONE \_ VDS NF \_ \_**            | 11    | [**NOTIFICA DELLA PARTIZIONE \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **RIPARTIZIONE \_ PARTIZIONE VDS NF \_ \_**            | 12    | [**NOTIFICA DELLA PARTIZIONE \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **VDS \_ NF \_ PARTITION \_ MODIFY**            | 13    | [**NOTIFICA DELLA PARTIZIONE \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **VDS \_ NF \_ SUB \_ SYSTEM \_ ARRIVE**          | 101   | [**NOTIFICA DEL \_ SISTEMA \_ SECONDARIO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF \_ SUB \_ SYSTEM \_ DEPART**          | 102   | [**NOTIFICA DEL \_ SISTEMA \_ SECONDARIO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF \_ SUB \_ SYSTEM \_ MODIFY**          | 151   | [**NOTIFICA DEL \_ SISTEMA \_ SECONDARIO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Controller | **ARRIVO DEL \_ CONTROLLER VDS NF \_ \_**           | 103   | [**NOTIFICA DEL CONTROLLER VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **VDS \_ NF \_ CONTROLLER \_ DEPART**           | 104   | [**NOTIFICA DEL CONTROLLER VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **VDS \_ NF \_ CONTROLLER \_ MODIFY**           | 350   | [**NOTIFICA DEL CONTROLLER VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **CONTROLLER VDS \_ NF \_ \_ RIMOSSO**          | 351   | [**NOTIFICA DEL CONTROLLER VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Porta       | **MODIFICA \_ PORTA VDS NF \_ \_**                 | 352   | [**NOTIFICA DELLE PORTE VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Porta       | **PORTA \_ VDS NF \_ \_ RIMOSSA**                | 353   | [**NOTIFICA DELLE PORTE VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Unità      | **VDS \_ NF \_ DRIVE \_ ARRIVE**                | 105   | [**NOTIFICA DELL'UNITÀ VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unità      | **VDS \_ NF \_ DRIVE \_ DEPART**                | 106   | [**NOTIFICA DELL'UNITÀ VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unità      | **VDS \_ NF \_ DRIVE \_ MODIFY**                | 107   | [**NOTIFICA DELL'UNITÀ VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unità      | **UNITÀ VDS \_ NF \_ \_ RIMOSSA**               | 354   | [**NOTIFICA DELL'UNITÀ VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **ARRIVO LUN \_ VDS NF \_ \_**                  | 108   | [**NOTIFICA LUN VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **PARTENZA LUN \_ VDS NF \_ \_**                  | 109   | [**NOTIFICA LUN VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **VDS \_ NF \_ LUN \_ MODIFY**                  | 110   | [**NOTIFICA LUN VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

VDS genera le notifiche rimanenti. Nella tabella seguente sono elencate le costanti di notifica basate sul servizio per categoria.



| Category     | Notifica                                | Valore | Collegamento alla descrizione dell'evento                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Disco         | **VDS \_ NF \_ DISK \_ ARRIVE**                   | 8     | [**NOTIFICA DEL DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **DISCO VDS \_ NF \_ IN \_ PARTENZA**                   | 9     | [**NOTIFICA DEL DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **VDS \_ NF \_ DISK \_ MODIFY**                   | 10    | [**NOTIFICA DEL DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Lettera unità | **VDS \_ NF \_ DRIVE \_ LETTER \_ FREE**            | 201   | [**NOTIFICA DELLA \_ LETTERA DI \_ UNITÀ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Lettera unità | **ASSEGNAZIONE LETTERA \_ DI UNITÀ VDS NF \_ \_ \_**          | 202   | [**NOTIFICA DELLA \_ LETTERA DI \_ UNITÀ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| File system  | **VDS \_ NF \_ FILE \_ SYSTEM \_ MODIFY**           | 203   | [**NOTIFICA DEL \_ FILE \_ SYSTEM VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| File system  | **STATO DEL \_ \_ FORMATO DEL FILE \_ SYSTEM \_ VDS NF \_** | 204   | [**NOTIFICA DEL \_ FILE \_ SYSTEM VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Volume       | **MODIFICA DEI \_ PUNTI DI \_ MONTAGGIO VDS NF \_ \_**          | 205   | [**NOTIFICA DEL PUNTO \_ DI \_ MONTAGGIO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**IVdsAdviseSink::OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**IVdsService::Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
