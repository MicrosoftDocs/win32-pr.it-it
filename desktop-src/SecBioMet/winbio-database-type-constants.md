---
title: WINBIO_DATABASE_TYPE costanti (Winbio \_ types.h)
description: Flag che possono essere utilizzati per il membro Attributes della struttura WINBIO \_ STORAGE \_ SCHEMA.
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba06dcd8809e53c5cfdf552a2c2c80b4d51faa5b80594b72ea1b50e2e7a2c0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910733"
---
# <a name="winbio_database_type-constants"></a>Costanti DI TIPO DATABASE WINBIO \_ \_

I flag seguenti possono essere usati per il **membro Attributes** della [**struttura WINBIO \_ STORAGE \_ SCHEMA.**](winbio-storage-schema.md)



| Costante/valore                                                                                                                                                                                                                                                                     | Descrizione                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ MASCHERA \_ DEL \_ TIPO**</dt> <dt>DI DATABASE 0x0000FFFF</dt> </dl>                | Rappresenta una maschera per tutti i \_ \_ bit TYPE.<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ FILE**</dt> <dt>0x00000001</dt> </dl>                | Il database è contenuto in un file.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | Il database è gestito da un componente DBMS (External Database Management System), ad esempio Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ TIPO \_ DI \_ DATABASE ONCHIP**</dt> <dt>0x00000003</dt> </dl>          | Il database risiede nel sensore biometrico.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ TIPO \_ DI \_ DATABASE SMARTCARD**</dt> <dt>0x00000004</dt> </dl> | Il database si trova in un smart card.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ MASCHERA \_ FLAG \_ DATABASE**</dt> <dt>0xFFFF0000</dt> </dl>                | Rappresenta una maschera per tutti i \_ \_ bit FLAG.<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ FLAG \_ DI DATABASE \_ RIMOVIBILI**</dt> <dt>0x00010000</dt> </dl> | Il supporto di archiviazione contenente il database può essere rimosso fisicamente dal computer.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ FLAG \_ DATABASE \_ REMOTE**</dt> <dt>0x00020000</dt> </dl>          | Il database si trova in un computer remoto.<br/>                                                                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





