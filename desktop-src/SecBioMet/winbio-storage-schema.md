---
title: Struttura WINBIO_STORAGE_SCHEMA ( \_ tipi WINBIO. h)
description: Descrive le funzionalità di un adattatore di archiviazione biometrico.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- Struttura di WINBIO_STORAGE_SCHEMA Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_STORAGE_SCHEMA
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302620"
---
# <a name="winbio_storage_schema-structure"></a>\_ \_ Struttura dello schema di archiviazione WINBIO

La **struttura \_ \_ dello schema di archiviazione WINBIO** descrive le funzionalità di un adattatore di archiviazione biometrico. Questa struttura viene utilizzata dalla funzione [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a>Members

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Tipo di misurazione biometrica salvata nel database.

</dd> <dt>

**DatabaseId**
</dt> <dd>

GUID che identifica il database.

</dd> <dt>

**DataFormat**
</dt> <dd>

GUID che identifica il formato dei modelli nel database.

</dd> <dt>

**Attributes (Attributi)**
</dt> <dd>

Informazioni sulle caratteristiche del database. Può trattarsi di un **or** bit per bit delle costanti seguenti.



| Valore                                                                                                                                                                                                                                                                              | Significato                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Maschera di flag del database**</dt> <dt>0xFFFF0000</dt> </dl>                | Rappresenta una maschera per i bit del flag.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ FLAG di DATABASE 0x00020000 \_ \_ remoto**</dt> <dt></dt> </dl>          | Il database si trova in un computer remoto.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ FLAG di DATABASE 0x00010000 \_ \_ rimovibile**</dt> <dt></dt> </dl> | Il database risiede in un'unità rimovibile.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ Tipo di DATABASE \_ \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | Il database è gestito da un sistema di gestione di database.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ \_ \_ File di tipo database**</dt> <dt>0x00000001</dt> </dl>                | Il database è contenuto in un file.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Maschera del tipo di database**</dt> <dt>0x0000FFFF</dt> </dl>                | Rappresenta una maschera per i bit del tipo.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ Tipo di DATABASE \_ \_ OnChip**</dt> <dt>0x00000003</dt> </dl>          | Il database risiede nel sensore biometrico.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ Tipo di DATABASE \_ \_ smartcard**</dt> <dt>0x00000004</dt> </dl> | Il database risiede in una smart card.<br/>                    |



 

</dd> <dt>

**FilePath**
</dt> <dd>

Il percorso e il nome file del database se si trova sul disco del computer.

</dd> <dt>

**ConnectionString**
</dt> <dd>

Valore stringa che può essere inviato a un server di database per identificare il database.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





