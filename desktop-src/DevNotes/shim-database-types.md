---
description: Rappresentano i tipi per i database shim principali e personalizzati.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Tipi di database shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cc36cbb198570618fbd1a6524e4e7c6dc6812fb01bd74fe04cf1bd91b31f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075925"
---
# <a name="shim-database-types"></a>Tipi di database shim

Rappresentano i tipi per i database shim principali e personalizzati.



| Costante/valore                                                                                                                                                                                                                                                | Descrizione                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN**</dt> <dt>0x80000000</dt> </dl>                    | Database principale. Se questo flag non è presente, il database è un database personalizzato.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**SDB \_ Database \_ SHIM**</dt> <dt>0x00010000</dt> </dl>                    | Il database contiene le voci dell'applicazione di cui eseguire lo s shimmed.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**SDB \_ Database \_ MSI**</dt> <dt>0x00020000</dt> </dl>                       | Il database contiene voci MSI.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**SDB \_ DRIVER \_ DI**</dt> <dt>DATABASE 0x00040000</dt> </dl>           | Il database contiene voci del blocco di driver.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**SDB \_ DETTAGLI \_ DATABASE**</dt> <dt>0x00080000</dt> </dl>           | Il database contiene i dettagli di Apphelp.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**SDB \_ DATABASE \_ SP \_ DETAILS**</dt> <dt>0x00100000</dt> </dl> | Il database contiene i dettagli di SP Apphelp.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**SDB \_ DATABASE \_ RESOURCE**</dt> <dt>0x00200000</dt> </dl>        | La DLL della risorsa contiene i dettagli di Apphelp.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**SDB \_ MASCHERA \_ DEL \_ TIPO DI**</dt> DATABASE <dt>0xF02F0000</dt> </dl>    | Maschera utilizzata per estrarre le informazioni principali del database.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SHIM \_ PRINCIPALE DEL DATABASE \_ \_ SDB**</dt> </dl>                                                                    | SDB \_ DATABASE \_ SHIM \| SDB \_ DATABASE \_ MSI \| SDB \_ DATABASE \_ MAIN<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**FILE MSI \_ PRINCIPALE DEL DATABASE \_ \_ SDB**</dt> </dl>                                                                       | SDB \_ DATABASE \_ MSI \| SDB \_ DATABASE \_ MAIN<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**DRIVER PRINCIPALI \_ DEL DATABASE \_ \_ SDB**</dt> </dl>                                                           | SDB \_ DATABASE \_ DRIVERS \| SDB \_ DATABASE \_ MAIN<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**DETTAGLI PRINCIPALI \_ DEL DATABASE \_ \_ SDB**</dt> </dl>                                                           | SDB \_ DATABASE \_ DETAILS \| SDB \_ DATABASE \_ MAIN<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**SDB \_ DATABASE MAIN SP DETAILS (DETTAGLI SP PRINCIPALI DEL DATABASE \_ \_ \_ SDB)**</dt> </dl>                                                 | SDB \_ DATABASE \_ SP \_ DETAILS \| SDB \_ DATABASE \_ MAIN<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**RISORSA PRINCIPALE \_ DEL DATABASE \_ \_ SDB**</dt> </dl>                                                        | SDB \_ DATABASE \_ RESOURCE \| SDB \_ DATABASE \_ MAIN<br/>                                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




