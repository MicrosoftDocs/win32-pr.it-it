---
description: Strutture transazionali NTFS (TxF).
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: Strutture TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d490f608ef9ebfa6906d1acffa374a0c9327489b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308371"
---
# <a name="txf-structures"></a>Strutture TxF

Transactional NTFS (TxF) fornisce le seguenti strutture.

## <a name="in-this-section"></a>Contenuto della sezione



| Struttura                                                                                                    | Descrizione                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ Crea \_ \_ informazioni miniversione**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Contiene le informazioni sulla versione di miniversione create da [**FSCTL \_ TXFS \_ Create \_ miniversione**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion).<br/>                                            |
| [**TXFS \_ ottenere \_ informazioni sui metadati \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Contiene le informazioni sulla versione relative al miniversione creato.<br/>                                                                                                                 |
| [**\_ID TXF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Rappresenta un identificatore univoco all'interno del contesto del Gestione risorse.<br/>                                                                                                              |
| [**TXFS \_ ottenere la \_ versione transazionale \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Contiene le informazioni relative alla base e alle versioni più recenti del file specificato.<br/>                                                                                                      |
| [**TXFS \_ Elenca \_ \_ i file bloccati della transazione \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Contiene un elenco di file bloccati da un writer transazionale.<br/>                                                                                                                                 |
| [**TXFS \_ elenco \_ di \_ file bloccati della transazione \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Contiene informazioni su una transazione bloccata.<br/>                                                                                                                                        |
| [**TXFS \_ elenco \_ transazioni**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Contiene un elenco di transazioni.<br/>                                                                                                                                                        |
| [**\_voce TXFS List \_ Transactions \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Contiene informazioni su una transazione.<br/>                                                                                                                                               |
| [**\_file TXF \_ record di log \_ interessato \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Contiene informazioni per un file interessato da una transazione.<br/>                                                                                                                     |
| [**\_ \_ base record di log TXF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Contiene le informazioni di base sul record.<br/>                                                                                                                                                  |
| [**\_ \_ troncamento record di log TXF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Contiene il record per un'operazione di troncamento.<br/>                                                                                                                                           |
| [**\_ \_ scrittura record log \_ TXF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Contiene il record per un'operazione di scrittura.<br/>                                                                                                                                              |
| [**TXFS \_ modificare \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Contiene le informazioni necessarie per la modifica dei parametri del log e della modalità di registrazione per un gestore di risorse secondario.<br/>                                                                      |
| [**\_ \_ informazioni RM query \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Contiene informazioni su Resource Manager (RM).<br/>                                                                                                                                   |
| [**TXFS \_ leggere \_ \_ le informazioni di backup \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Contiene una struttura specifica di Transactional NTFS (TxF). Queste informazioni devono essere usate solo quando si [**chiamano \_ \_ \_ le informazioni di backup di TXFS Write**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information).<br/>    |
| [**\_informazioni TXFS salvataggio \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | La struttura di [**\_ \_ \_ informazioni salvataggio FSCTL TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) specifica l'azione da eseguire e la transazione.<br/>                                      |
| [**\_ \_ informazioni attive transazione \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Contiene il flag che indica se le transazioni sono attive o meno quando è stato utilizzato uno snapshot.<br/>                                                                                     |
| [**TXFS \_ scrivere \_ \_ le informazioni di backup**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Contiene una struttura specifica di Transactional NTFS (TxF). Queste informazioni devono essere usate solo quando si [**chiamano \_ \_ \_ le informazioni di backup di TXFS Write**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out).<br/> |



 

 

