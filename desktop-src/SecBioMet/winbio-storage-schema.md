---
title: WINBIO_STORAGE_SCHEMA struttura (Winbio \_ types.h)
description: Descrive le funzionalità di una scheda di archiviazione biometrica.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- WINBIO_STORAGE_SCHEMA struttura Windows'API Biometric Framework
- PWINBIO_STORAGE_SCHEMA puntatore alla struttura Windows'API Biometric Framework
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
ms.openlocfilehash: 2bc0bd0d61814b4133c3789b0c8119edcaf79945452cc26aa313504c055ac2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909258"
---
# <a name="winbio_storage_schema-structure"></a>Struttura DELLO SCHEMA DI ARCHIVIAZIONE WINBIO \_ \_

La **struttura WINBIO \_ STORAGE \_ SCHEMA** descrive le funzionalità di una scheda di archiviazione biometrica. Questa struttura viene usata dalla [**funzione WinBioEnumDatabases.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)

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

Tipo di misura biometrica salvata nel database.

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

Informazioni sulle caratteristiche del database. Può trattarsi di **un'operazione OR** bit per bit delle costanti seguenti.



| Valore                                                                                                                                                                                                                                                                              | Significato                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ MASCHERA \_ FLAG \_ DATABASE**</dt> <dt>0xFFFF0000</dt> </dl>                | Rappresenta una maschera per i bit del flag.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ FLAG \_ DATABASE \_ REMOTE**</dt> <dt>0x00020000</dt> </dl>          | Il database si trova in un computer remoto.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ FLAG \_ DATABASE \_ REMOVABLE**</dt> <dt>0x00010000</dt> </dl> | Il database si trova in un'unità rimovibile.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | Il database è gestito da un sistema di gestione di database.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ FILE**</dt> <dt>0x00000001</dt> </dl>                | Il database è contenuto in un file.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ MASCHERA \_ DEL \_ TIPO DI**</dt> DATABASE <dt>0x0000FFFF</dt> </dl>                | Rappresenta una maschera per i bit di tipo.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ TIPO \_ DI \_ DATABASE ONCHIP**</dt> <dt>0x00000003</dt> </dl>          | Il database risiede nel sensore biometrico.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ SMARTCARD \_ \_ DI TIPO**</dt> DATABASE <dt>0x00000004</dt> </dl> | Il database si trova in un smart card.<br/>                    |



 

</dd> <dt>

**Filepath**
</dt> <dd>

Percorso e nome file del database, se si trova sul disco del computer.

</dd> <dt>

**Connectionstring**
</dt> <dd>

Valore stringa che può essere inviato a un server di database per identificare il database.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





