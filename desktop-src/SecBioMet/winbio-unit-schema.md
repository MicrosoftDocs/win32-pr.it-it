---
title: Struttura WINBIO_UNIT_SCHEMA ( \_ tipi WINBIO. h)
description: Descrive le funzionalità di un'unità biometrica.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- Struttura di WINBIO_UNIT_SCHEMA Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_UNIT_SCHEMA
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
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964907"
---
# <a name="winbio_unit_schema-structure"></a>\_ \_ Struttura dello schema dell'unità WINBIO

La **struttura \_ \_ dello schema dell'unità WINBIO** descrive le funzionalità di un'unità biometrica. Viene usato dalla funzione [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .

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
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_pool WINBIO \_ sconosciuto**</dt> </dl> | Tipo sconosciuto.<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_sistema pool \_ WINBIO**</dt> </dl>    | La sessione si connette a una raccolta condivisa di unità biometriche gestite dal provider di servizi.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**\_pool WINBIO \_ privato**</dt> </dl> | La sessione si connette a una raccolta di unità biometriche gestite dal chiamante.<br/>         |



 

</dd> <dt>

**BiometricFactor**
</dt> <dd>

Valore che specifica il tipo di unità biometrica. Attualmente è supportata solo l' **\_ \_ impronta digitale di tipo WINBIO** .

</dd> <dt>

**SensorSubType**
</dt> <dd>

Sottotipo di sensore definito per il tipo di biometria specificato dal membro **BiometricFactor** . Attualmente sono supportati solo i tipi di impronta digitale (**WINBIO \_ tipo \_ impronta digitale**). Per le impronte digitali sono attualmente definiti i sottotipi seguenti:

-   sottotipo del \_ sensore WINBIO \_ \_ sconosciuto
-   \_scorrimento del \_ sottotipo di sensore FP \_ \_ WINBIO
-   \_tocco del \_ sottotipo del sensore FP \_ \_ WINBIO

</dd> <dt>

**Capabilities**
</dt> <dd>

Maschera di maschera delle funzionalità del sensore biometrico. Può trattarsi di un **or** bit per bit dei valori seguenti:

-   \_sensore funzionalità \_ WINBIO
-   \_corrispondenza funzionalità \_ WINBIO
-   \_database funzionalità \_ WINBIO
-   \_elaborazione della funzionalità WINBIO \_
-   \_crittografia funzionalità \_ WINBIO
-   \_navigazione della funzionalità WINBIO \_
-   \_indicatore funzionalità \_ WINBIO
-   \_ \_ sensore virtuale funzionalità \_ WINBIO
    > [!Note]  
    > La costante del **\_ \_ \_ sensore virtuale della funzionalità WINBIO** si applica solo a Windows 10 e versioni successive.

     

</dd> <dt>

**DeviceInstanceId**
</dt> <dd>

Valore stringa che contiene l'ID del dispositivo. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .

</dd> <dt>

**Descrizione**
</dt> <dd>

Valore stringa che contiene una descrizione dell'unità biometrica. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .

</dd> <dt>

**Produttore**
</dt> <dd>

Valore stringa che contiene il nome del produttore. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .

</dd> <dt>

**Modello**
</dt> <dd>

Valore stringa che contiene il numero di modello dell'unità biometrica. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .

</dd> <dt>

**SerialNumber**
</dt> <dd>

Stringa Unicode con terminazione **null** che contiene il numero di serie dell'unità biometrica. La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .

</dd> <dt>

**FirmwareVersion**
</dt> <dd>

Struttura [**di \_ versione di WINBIO**](winbio-version.md) che contiene i numeri di versione principale e secondaria per l'unità biometrica.

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

[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





