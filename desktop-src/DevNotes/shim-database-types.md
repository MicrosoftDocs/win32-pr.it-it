---
description: Rappresentano i tipi per i database di shim principale e personalizzati.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Tipi di database shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747674"
---
# <a name="shim-database-types"></a>Tipi di database shim

Rappresentano i tipi per i database di shim principale e personalizzati.



| Costante/valore                                                                                                                                                                                                                                                | Descrizione                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**Sdb \_ 0x80000000 \_ principale database**</dt> <dt></dt> </dl>                    | Database principale. Se questo flag non è presente, il database è un database personalizzato.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**Sdb \_ 0x00010000 \_ shim database**</dt> <dt></dt> </dl>                    | Il database contiene le voci dell'applicazione da sottoposto a shim.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**Sdb \_ 0x00020000 \_ MSI del database**</dt> <dt></dt> </dl>                       | Il database contiene voci MSI.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**Sdb \_ \_Driver di database**</dt> <dt>0x00040000</dt> </dl>           | Il database contiene voci di blocco del driver.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**Sdb \_ \_Dettagli database**</dt> <dt>0x00080000</dt> </dl>           | Il database contiene i dettagli apphelp.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**Sdb \_ \_ \_ Dettagli SP database**</dt> <dt>0x00100000</dt> </dl> | Il database contiene i dettagli di SP apphelp.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**Sdb \_ 0x00200000 \_ risorsa database**</dt> <dt></dt> </dl>        | La DLL della risorsa contiene i dettagli apphelp.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**Sdb \_ \_ \_ Maschera del tipo di database**</dt> <dt>0xF02F0000</dt> </dl>    | Maschera utilizzata per estrarre le informazioni sul database principale.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**\_ \_ shim principale del database sdb \_**</dt> </dl>                                                                    | Metodo SDB database shim SDB database MSI SDB database \_ \_ \| \_ \_ \| \_ \_ principale<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**\_ \_ MSI principale del database sdb \_**</dt> </dl>                                                                       | database \_ sdb \_ MSI \| sdb \_ database \_ Main<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**\_ \_ driver principali del database sdb \_**</dt> </dl>                                                           | \_driver di database sdb \_ \| sdb \_ database \_ Main<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**\_ \_ Dettagli principale del database sdb \_**</dt> </dl>                                                           | informazioni di base sul \_ database sdb \_ \| sdb \_ database \_ Main<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**\_ \_ \_ Dettagli SP principale del database sdb \_**</dt> </dl>                                                 | \_database sdb \_ Dettagli SP database \_ \| sdb \_ \_ principale<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**\_ \_ risorsa principale del database sdb \_**</dt> </dl>                                                        | risorsa del database sdb \_ \_ \| sdb \_ database \_ Main<br/>                                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




