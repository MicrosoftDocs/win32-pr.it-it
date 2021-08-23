---
description: Strutture NTFS transazionali (TxF).
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: Strutture TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6acdbaac0798ef2dac3b3fefad9a1f5de505eb9781316fca82d45cfad26af0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765841"
---
# <a name="txf-structures"></a>Strutture TxF

Ntfs transazionale (TxF) fornisce le strutture seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Struttura                                                                                                    | Descrizione                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ CREATE \_ MINIVERSION \_ INFO**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Contiene le informazioni sulla versione della miniversione creata da [**FSCTL \_ TXFS \_ CREATE \_ MINIVERSION.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion)<br/>                                            |
| [**TXFS \_ GET \_ METADATA \_ INFO \_ OUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Contiene le informazioni sulla versione della miniversione creata.<br/>                                                                                                                 |
| [**TXF \_ ID**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Rappresenta un identificatore univoco all'interno del contesto del Resource Manager.<br/>                                                                                                              |
| [**TXFS \_ GET \_ TRANSACTED \_ VERSION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Contiene le informazioni sulle versioni di base e più recenti del file specificato.<br/>                                                                                                      |
| [**ELENCARE I \_ FILE \_ BLOCCATI DELLE \_ TRANSAZIONI \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Contiene un elenco di file bloccati da un writer transazione.<br/>                                                                                                                                 |
| [**VOCE ELENCA \_ FILE BLOCCATI \_ \_ \_ TRANSAZIONE \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Contiene informazioni su una transazione bloccata.<br/>                                                                                                                                        |
| [**ELENCO TRANSAZIONI TXFS \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Contiene un elenco di transazioni.<br/>                                                                                                                                                        |
| [**VOCE LIST \_ \_ TRANSACTIONS DI \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Contiene informazioni su una transazione.<br/>                                                                                                                                               |
| [**FILE INTERESSATO \_ DEL RECORD DEL \_ LOG \_ \_ TXF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Contiene informazioni per un file interessato da una transazione.<br/>                                                                                                                     |
| [**TXF \_ LOG \_ RECORD \_ BASE**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Contiene le informazioni di base sui record.<br/>                                                                                                                                                  |
| [**TRONCAMENTO \_ \_ DEL RECORD DI LOG TXF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Contiene il record per un'operazione di troncamento.<br/>                                                                                                                                           |
| [**TXF \_ LOG \_ RECORD \_ WRITE**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Contiene il record per un'operazione di scrittura.<br/>                                                                                                                                              |
| [**TXFS \_ MODIFY \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Contiene le informazioni necessarie quando si modificano i parametri di log e la modalità di registrazione per un gestore di risorse secondario.<br/>                                                                      |
| [**INFORMAZIONI \_ SULL'RM DI QUERY \_ TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Contiene informazioni su Resource Manager (RM).<br/>                                                                                                                                   |
| [**TXFS \_ READ \_ BACKUP \_ INFORMATION \_ OUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Contiene una struttura specifica di NTFS transazionale (TxF). Queste informazioni devono essere usate solo quando si chiama [**TXFS \_ WRITE \_ BACKUP \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information).<br/>    |
| [**TXFS \_ SAVEPOINT \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | La [**struttura FSCTL \_ TXFS \_ SAVEPOINT \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) specifica l'azione da eseguire e la transazione.<br/>                                      |
| [**TXFS \_ TRANSACTION \_ ACTIVE \_ INFO**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Contiene il flag che indica se le transazioni erano attive o meno quando è stato creato uno snapshot.<br/>                                                                                     |
| [**INFORMAZIONI DI BACKUP \_ DI SCRITTURA TXFS \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Contiene una struttura specifica di NTFS transazionale (TxF). Queste informazioni devono essere usate solo quando si chiama [**TXFS \_ WRITE \_ BACKUP \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out).<br/> |



 

 

