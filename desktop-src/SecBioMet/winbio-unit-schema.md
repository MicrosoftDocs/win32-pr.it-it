---
title: WINBIO_UNIT_SCHEMA struttura (Winbio \_ types.h)
description: Descrive le funzionalità di un'unità biometrica.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- WINBIO_UNIT_SCHEMA struttura Windows'API Biometric Framework
- PWINBIO_UNIT_SCHEMA puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae91ae5353aa0e9c02414e90a8364d86bdc56c0cdcc4f4586656f28f92f100ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909170"
---
# <a name="winbio_unit_schema-structure"></a>Struttura DELLO \_ SCHEMA UNITÀ WINBIO \_

La **struttura WINBIO \_ UNIT \_ SCHEMA** descrive le funzionalità di un'unità biometrica. Viene usato dalla [**funzione WinBioEnumBiometricUnits.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a>Members

<dl> <dt>

**UnitId**
</dt> <dd>

Valore che identifica l'unità biometrica.

</dd> <dt>

**PoolType**
</dt> <dd>

Valore **ULONG** che specifica il tipo di unità biometrica. I valori possibili sono i seguenti:



| Valore                                                                                                                                                                            | Significato                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**POOL WINBIO \_ \_ SCONOSCIUTO**</dt> </dl> | Tipo sconosciuto.<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**SISTEMA DI POOL WINBIO \_ \_**</dt> </dl>    | La sessione si connette a una raccolta condivisa di unità biometriche gestite dal provider di servizi.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**POOL WINBIO \_ \_ PRIVATO**</dt> </dl> | La sessione si connette a una raccolta di unità biometriche gestite dal chiamante.<br/>         |



 

</dd> <dt>

**BiometricFactor**
</dt> <dd>

Valore che specifica il tipo di unità biometrica. Attualmente è supportata solo l'impronta digitale DEL TIPO **WINBIO. \_ \_**

</dd> <dt>

**SensorSubType**
</dt> <dd>

Sottotipo di sensore definito per il tipo biometrico specificato dal membro **BiometricFactor.** Sono attualmente supportati solo i tipi di impronta digitale (**WINBIO \_ TYPE \_ FINGERPRINT).** Per le impronte digitali sono attualmente definiti i sottotipi seguenti:

-   SOTTOTIPO SENSORE WINBIO \_ \_ \_ SCONOSCIUTO
-   SCORRIMENTO DEL \_ \_ \_ SOTTOTIPO DEL SENSORE FP \_ WINBIO
-   TOCCO DEL SOTTOTIPO \_ DEL SENSORE FP WINBIO \_ \_ \_

</dd> <dt>

**Capabilities**
</dt> <dd>

Maschera di bit delle funzionalità del sensore biometrico. Può trattarsi di **un'operazione OR** bit per bit dei valori seguenti:

-   SENSORE DI FUNZIONALITÀ WINBIO \_ \_
-   CORRISPONDENZA DELLE FUNZIONALITÀ \_ WINBIO \_
-   DATABASE DELLE FUNZIONALITÀ \_ WINBIO \_
-   ELABORAZIONE DELLE FUNZIONALITÀ \_ WINBIO \_
-   CRITTOGRAFIA DELLE FUNZIONALITÀ \_ WINBIO \_
-   SPOSTAMENTO DELLE FUNZIONALITÀ \_ WINBIO \_
-   INDICATORE DI FUNZIONALITÀ WINBIO \_ \_
-   SENSORE VIRTUALE \_ DI FUNZIONALITÀ WINBIO \_ \_
    > [!Note]  
    > La **costante WINBIO \_ CAPABILITY VIRTUAL \_ \_ SENSOR** si applica solo Windows 10 e versioni successive.

     

</dd> <dt>

**DeviceInstanceId**
</dt> <dd>

Valore stringa che contiene l'ID dispositivo. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere **NULL di** terminazione.

</dd> <dt>

**Descrizione**
</dt> <dd>

Valore stringa contenente una descrizione dell'unità biometrica. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere **NULL di** terminazione.

</dd> <dt>

**Produttore**
</dt> <dd>

Valore stringa che contiene il nome del produttore. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere **NULL di** terminazione.

</dd> <dt>

**Modello**
</dt> <dd>

Valore stringa che contiene il numero di modello dell'unità biometrica. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere **NULL di** terminazione.

</dd> <dt>

**Serialnumber**
</dt> <dd>

Stringa **Unicode con** terminazione NULL che contiene il numero di serie dell'unità biometrica. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere **NULL di** terminazione.

</dd> <dt>

**FirmwareVersion**
</dt> <dd>

Struttura [**WINBIO \_ VERSION**](winbio-version.md) che contiene i numeri di versione principale e secondaria per l'unità biometrica.

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

[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





