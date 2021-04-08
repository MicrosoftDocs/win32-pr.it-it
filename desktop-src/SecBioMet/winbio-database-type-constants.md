---
title: Costanti WINBIO_DATABASE_TYPE (tipi WinBio \_ . h)
description: Flag che possono essere utilizzati per il membro Attributes della \_ \_ struttura dello schema di archiviazione WINBIO.
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
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741527"
---
# <a name="winbio_database_type-constants"></a>Costanti del tipo di \_ database WINBIO \_

I flag seguenti possono essere usati per il membro **Attributes** della [**struttura \_ \_ dello schema di archiviazione WINBIO**](winbio-storage-schema.md) .



| Costante/valore                                                                                                                                                                                                                                                                     | Descrizione                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Maschera del tipo di database**</dt> <dt>0x0000FFFF</dt> </dl>                | Rappresenta una maschera per tutti i \_ bit di tipo \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ \_ \_ File di tipo database**</dt> <dt>0x00000001</dt> </dl>                | Il database è contenuto in un file.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ Tipo di DATABASE \_ \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | Il database è gestito da un componente del sistema di gestione di database (DBMS) esterno, ad esempio Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ Tipo di DATABASE \_ \_ OnChip**</dt> <dt>0x00000003</dt> </dl>          | Il database risiede nel sensore biometrico.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ Tipo di DATABASE \_ \_ smartcard**</dt> <dt>0x00000004</dt> </dl> | Il database risiede in una smart card.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Maschera di flag del database**</dt> <dt>0xFFFF0000</dt> </dl>                | Rappresenta una maschera per tutti i \_ bit del flag \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ FLAG di DATABASE 0x00010000 \_ \_ rimovibile**</dt> <dt></dt> </dl> | Il supporto di archiviazione che contiene il database può essere rimosso fisicamente dal computer.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ FLAG di DATABASE 0x00020000 \_ \_ remoto**</dt> <dt></dt> </dl>          | Il database si trova in un computer remoto.<br/>                                                                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





