---
description: Le enumerazioni seguenti sono definite nell'API copia shadow del volume.
ms.assetid: f2f09791-b17e-4f54-9d29-83a4189bffc1
title: Enumerazioni API copia shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ade0af4637e9c057c9743dfaf0778e86b3d81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307178"
---
# <a name="volume-shadow-copy-api-enumerations"></a>Enumerazioni API copia shadow del volume

Le enumerazioni seguenti sono definite nell'API copia shadow del volume.



| Nome                                                                           | Descrizione                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_stato del \_ writer \_ alternativo VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_alternate_writer_state)            | Definisce il set di stati validi utilizzato per indicare se a un writer è associato un writer alternativo.                                                              |
| [**\_livello applicazione \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_application_level)                       | Definisce il set di livelli di applicazione validi.                                                                                                                       |
| [**\_schema di backup VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)                               | Definisce il set di schemi di backup, ovvero le operazioni a cui un writer può partecipare.                                                                                          |
| [**\_tipo di backup VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)                                   | Definisce il set di tipi di backup.                                                                                                                                   |
| [**\_flag componente \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)                           | Indica il supporto per il ripristino automatico.                                                                                                                               |
| [**\_tipo di componente VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)                             | Definisce il set di tipi di componenti.                                                                                                                                |
| [**\_ \_ Stato ripristino file \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_file_restore_status)                  | Definisce il set di Stati di un'operazione di ripristino di file.                                                                                                           |
| [**\_tipo di \_ backup delle specifiche del file VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)             | Definisce il set di operazioni di backup supportate dai writer.                                                                                                         |
| [**\_\_Opzioni hardware \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)                      | Definisce i flag LUN della copia shadow.                                                                                                                                     |
| [**\_tipo di \_ oggetto \_ Mgmt di VSS**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_mgmt_object_type)                        | Discriminante per l'Unione dell'Unione di [**\_ \_ oggetti \_ VSS Mgmt**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001) all'interno della struttura di [**\_ \_ \_ prop oggetto**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) di gestione VSS. |
| [**\_tipo di oggetto VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_object_type)                                   | Utilizzato per identificare un oggetto come set di copie shadow, copia shadow o provider.                                                                                         |
| [**\_errore di protezione VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)                         | Definisce il set di errori di protezione della copia shadow.                                                                                                                  |
| [**\_livello di protezione VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)                         | Definisce il set di livelli di protezione della copia shadow del volume.                                                                                                           |
| [**\_funzionalità del provider VSS \_**](/windows/desktop/api/vss/ne-vss-vss_provider_capabilities)              | Riservato per utilizzi futuri.                                                                                                                                           |
| [**\_tipo di provider VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_provider_type)                               | Definisce il set di tipi di provider.                                                                                                                                 |
| [**\_Opzioni di ripristino VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)                         | Utilizzato da un richiedente per specificare la modalità di esecuzione di un'operazione di risincronizzazione.                                                                               |
| [**\_destinazione ripristino \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)                             | Definisce il set di destinazioni di ripristino.                                                                                                                                |
| [**\_tipo di ripristino VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)                                 | Definisce il set di operazioni di ripristino da eseguire.                                                                                                              |
| [**\_enumerazione RESTOREMETHOD \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)                     | Definisce il set di metodi predefiniti per il ripristino dei file per un writer.                                                                                                      |
| [**\_tipo di rollforward VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)                         | Utilizzato da un richiedente per indicare il tipo di operazione di rollforward che sta per essere eseguita.                                                                         |
| [**\_compatibilità snapshot \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_compatibility)             | Definisce il set di operazioni di I/O dei file o del controllo del volume che è possibile disabilitare per un volume di cui è stata eseguita la copia shadow.                                            |
| [**\_\_contesto snapshot \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)                      | Specifica il modo in cui deve essere creata, sottoposta a query o eliminata una copia shadow e il livello di coinvolgimento del writer.                                                            |
| [**\_stato snapshot \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)                             | Definisce il set di Stati di un'operazione di copia shadow.                                                                                                              |
| [**\_tipo di origine VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)                                   | Definisce il set di tipi di dati che un writer può gestire.                                                                                                         |
| [**\_maschera di sottoscrizione VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_subscribe_mask)                             | Definisce il set di eventi che un writer può ricevere.                                                                                                               |
| [**\_tipo di utilizzo VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)                                     | Specifica la modalità di utilizzo dei dati gestiti da un writer da parte del sistema host.                                                                                                   |
| [**\_\_ \_ attributi snapshot del volume VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) | Definisce il set di attributi di una copia shadow.                                                                                                                    |
| [**\_stato VSS writer \_**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)                                 | Definisce il set di Stati del writer.                                                                                                                           |
| [**\_enumerazione WRITERRESTORE \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)                     | Definisce il set di condizioni in base alle quali un writer gestirà gli eventi generati durante un'operazione di ripristino.                                                        |



 

 

 



