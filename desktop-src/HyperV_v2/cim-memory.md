---
description: Rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: Classe CIM_Memory (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529503"
---
# <a name="cim_memory-class-hyper-v-management"></a>Classe CIM_Memory (gestione Hyper-V)

Rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a>Members

La classe **CIM \_ Memory** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ memoria CIM** dispone di queste proprietà.

<dl> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,18 "," MIF. DMTF \| matrice di memoria fisica \| 001,13 ")
</dt> </dl>

Matrice di ottetti che contiene informazioni aggiuntive sull'errore. Un esempio è la sindrome ECC o il ritorno dei bit di controllo se viene usata una metodologia di errore basata su CRC. Nel secondo caso, se viene riconosciuto un errore di bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.

Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,8 ")
</dt> </dl>

**true** se l'errore più recente è correggibile. in caso contrario, **false**. Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,4 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,5 "), **punito** (" byte \* 10 ^ 3 ")
</dt> </dl>

Indirizzo finale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per l'oggetto memoria. L'indirizzo finale è specificato in kilobyte.

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,10 ")
</dt> </dl>

Operazione di accesso alla memoria che ha causato l'ultimo errore. Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Lettura** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Scrittura** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Scrittura parziale** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. IndirizzoIniziale"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,19 "," MIF. DMTF \| matrice di memoria fisica \| 001,14 ")
</dt> </dl>

Indirizzo dell'ultimo errore di memoria. Il tipo di errore è descritto dalla proprietà **errorInfo** . Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorData"), **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,12 ")
</dt> </dl>

Matrice che contiene i dati acquisiti durante l'ultimo accesso errato alla memoria. I dati occupano i primi n ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .

Se la proprietà **ErrorTransferSize** contiene "0" (OK), questa proprietà non viene utilizzata.

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")
</dt> </dl>

Ordinamento dei dati archiviati nella proprietà **ErrorData** . È possibile specificare "byte meno significativo per primo" (valore = 1) o "primo byte significativo" (2). Se la proprietà **ErrorTransferSize** contiene "0" (OK), questa proprietà non viene utilizzata.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**Byte meno significativi prima** (1)


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**Primo byte significativo** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,12 "," MIF. \|Matrice di memoria fisica DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**OtherErrorDescription**")
</dt> </dl>

Tipo dell'ultimo errore che si verifica.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (3)


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

**Lettura non valida** (4)


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

**Errore di parità** (5)


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

**Errore a bit singolo** (6)


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

**Errore a doppio bit** (7)


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

**Errore a più bit** (8)


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

**Errore di roditura** (9)


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

**Errore di checksum** (10)


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

**Errore CRC** (11)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Non **definito** (12)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Non **definito** (13)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Non **definito** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,7 ")
</dt> </dl>

Indica se gli algoritmi di parità, gli algoritmi CRC, ECC o altri meccanismi vengono utilizzati dall'oggetto memoria. È anche possibile specificare i dettagli sull'algoritmo.

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,21 "," MIF. DMTF \| matrice di memoria fisica \| 001,15 "), **punito** (" byte ")
</dt> </dl>

Intervallo, in byte, in cui è possibile risolvere l'ultimo errore. Ad esempio, se gli indirizzi di errore vengono risolti in bit 11, ad esempio in base a una pagina tipica; gli errori possono quindi essere risolti in limiti di 4K e questa proprietà è impostata su "4000". Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTime")
</dt> </dl>

Ora in cui si è verificato l'ultimo errore di memoria. Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| array di memoria fisica \| 001,11 "), **punito** (" bit ")
</dt> </dl>

Dimensioni del trasferimento dati, in bit, che hanno causato l'ultimo errore. "0" indica che non è presente alcun errore. Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**ErrorInfo**")
</dt> </dl>

Descrizione del tipo di errore, quando la proprietà **ErrorType** è impostata su "1" (other).

</dd> <dt>

**IndirizzoIniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,3 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,4 "), **punito** (" byte \* 10 ^ 3 ")
</dt> </dl>

Indirizzo iniziale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per l'oggetto memoria. L'indirizzo iniziale è specificato in kilobyte.

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.SystemLevelAddress")
</dt> </dl>

**true** se le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema, **false** se è un indirizzo fisico.

</dd> <dt>

**Volatile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se la memoria è volatile; in caso contrario, **false**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> </dl>

 

