---
description: Notifiche VDS
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: Notifiche VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa99751912f110a77b061d50134135413baf2894
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104561449"
---
# <a name="vds-notifications"></a>Notifiche VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un provider può inviare una notifica degli eventi a VDS e VDS può a sua volta inoltrare la notifica alle applicazioni. Il modello di notifica utilizzato da VDS è simile al modello del punto di connessione utilizzato dagli oggetti COM.

VDS genera notifiche di servizio per eventi quali l'assegnazione di una lettera di unità o l'arrivo di un disco non allocato. Quando VDS alloca un disco a un provider, il provider è responsabile della generazione delle notifiche associate. La figura seguente illustra le interfacce e i metodi usati nel modello di notifica VDS.

![Diagramma che mostra l'interfaccia e i metodi (Advise, OnLoad e OnNotify) tra le applicazioni, il servizio dischi virtuali e i provider V D.](images/vdsnotification.png)

Per ricevere le notifiche, VDS registra l'interfaccia [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) con l'oggetto provider chiamando il metodo [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) e passando un puntatore all'interfaccia. Quando si verifica un evento di notifica, ad esempio l'arrivo di un nuovo volume o unità, il provider passa la struttura di notifica appropriata a VDS come parametro del metodo [**IVdsAdviseSink:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

Il processo è simile tra un'applicazione e VDS. In particolare, per ricevere le notifiche, un'applicazione registra l'interfaccia [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) con VDS chiamando il metodo [**IVdsService:: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) e passando un puntatore all'interfaccia. Quando VDS riceve una notifica da un provider, passa la struttura di notifica appropriata alle applicazioni registrate come parametro del metodo [**IVdsAdviseSink:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

> [!Note]  
> Un'applicazione che chiama [**Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) deve infine chiamare il metodo [**IVdsService:: Unadvise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) . Idealmente, deve chiamare **Unadvise** non appena non è più necessario ricevere le notifiche.

 

Nella tabella seguente sono elencate le notifiche generate dal provider per tipo di oggetto.



| Oggetto     | Notifica                              | Valore | Collegamento alla descrizione dell'evento                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **arrivo a VDS \_ NF \_ pack \_**                 | 1     | [**\_notifica del pacchetto VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **\_componente VDS NF \_ pack \_**                 | 2     | [**\_notifica del pacchetto VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **\_modifica del \_ pacchetto VDS VDS \_**                 | 3     | [**\_notifica del pacchetto VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Volume     | **arrivo del volume VDS- \_ NF \_ \_**               | 4     | [**\_notifica volume \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **VOLUME di VDS \_ NF \_ \_**               | 5     | [**\_notifica volume \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **\_ \_ Modifica volume di VDS NF \_**               | 6     | [**\_notifica volume \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **\_ \_ \_ stato ricompilazione volume VDS \_ NF** | 7     | [**\_notifica volume \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Disco       | **\_ \_ arrivo disco VDS \_ NF**                 | 8     | [**\_notifica del disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **\_ \_ ripartire dischi VDS NF \_**                 | 9     | [**\_notifica del disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **\_ \_ modifica dischi VDS \_ NF**                 | 10    | [**\_notifica del disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partition  | **\_ \_ arrivo partizione VDS-NF \_**            | 11    | [**\_notifica della partizione VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **\_ \_ suddivisione partizione VDS \_ NF**            | 12    | [**\_notifica della partizione VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **modifica della partizione di VDS \_ NF \_ \_**            | 13    | [**\_notifica della partizione VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **\_arrivo del \_ \_ sottosistema VDS. \_**          | 101   | [**\_notifica del \_ SOTTOsistema VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **\_ \_ \_ ripartire il sottosistema VDS NF \_**          | 102   | [**\_notifica del \_ SOTTOsistema VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **\_modifica del \_ \_ sottosistema VDS VDS \_**          | 151   | [**\_notifica del \_ SOTTOsistema VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Controller | **\_arrivo del \_ controller VDS VDS \_**           | 103   | [**\_notifica del controller VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **PARTE del controller di VDS \_ NF \_ \_**           | 104   | [**\_notifica del controller VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **modificare il controller di VDS \_ NF \_ \_**           | 350   | [**\_notifica del controller VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **il \_ controller VDS NF è stato \_ \_ rimosso**          | 351   | [**\_notifica del controller VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Porta       | **\_ \_ modifica porta VDS \_ NF**                 | 352   | [**\_notifica porta \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Porta       | **\_porta VDS \_ NF \_ rimossa**                | 353   | [**\_notifica porta \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Unità      | **\_ \_ arrivo unità VDS-NF \_**                | 105   | [**\_notifica unità \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unità      | **\_ \_ parte unità di VDS NF \_**                | 106   | [**\_notifica unità \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unità      | **\_ \_ modifica unità VDS-NF \_**                | 107   | [**\_notifica unità \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unità      | **\_unità VDS \_ NF \_ rimossa**               | 354   | [**\_notifica unità \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **\_ \_ arrivo lun da VDS NF \_**                  | 108   | [**\_notifica lun \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **\_ \_ parte lun NF \_ VDS**                  | 109   | [**\_notifica lun \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **\_ \_ modifica lun NF \_ VDS**                  | 110   | [**\_notifica lun \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

VDS genera le notifiche rimanenti. Nella tabella seguente sono elencate le costanti di notifica basate sul servizio per categoria.



| Category     | Notifica                                | Valore | Collegamento alla descrizione dell'evento                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Disco         | **\_ \_ arrivo disco VDS \_ NF**                   | 8     | [**\_notifica del disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **\_ \_ ripartire dischi VDS NF \_**                   | 9     | [**\_notifica del disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **\_ \_ modifica dischi VDS \_ NF**                   | 10    | [**\_notifica del disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Lettera unità | **\_lettera unità di VDS NF \_ \_ \_ gratuita**            | 201   | [**\_ \_ notifica lettera unità \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Lettera unità | **\_ \_ \_ assegnazione lettera unità VDS \_ NF**          | 202   | [**\_ \_ notifica lettera unità \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| File system  | **\_modifica del \_ file \_ System VDS NF \_**           | 203   | [**\_notifica del file \_ System \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| File system  | **\_stato del \_ formato del file \_ System VDS \_ NF \_** | 204   | [**\_notifica del file \_ System \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Volume       | **\_ \_ Modifica punti di montaggio VDS NF \_ \_**          | 205   | [**\_ \_ notifica punto di montaggio VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**IVdsAdviseSink:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**IVdsService:: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
