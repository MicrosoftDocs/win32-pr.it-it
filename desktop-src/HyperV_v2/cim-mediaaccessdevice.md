---
description: Rappresenta un dispositivo che può utilizzare supporti per archiviare e recuperare i dati.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: Classe CIM_MediaAccessDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320468"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a>Classe CIM_MediaAccessDevice (gestione Hyper-V)

Rappresenta un dispositivo che può utilizzare supporti per archiviare e recuperare i dati.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a>Members

La classe **CIM \_ MediaAccessDevice** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ MediaAccessDevice** presenta questi metodi.



| Metodo                                               | Descrizione                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**LockMedia**](cim-mediaaccessdevice-lockmedia.md) | Blocca e sblocca i supporti rimovibili in un dispositivo di accesso multimediale.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **CIM \_ MediaAccessDevice** dispone di queste proprietà.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "," MIF. \|Disco host DMTF \| 001,2 "," MIF. \|Disco host DMTF \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")
</dt> </dl>

Matrice che contiene le funzionalità del dispositivo di accesso multimediale.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

**Accesso sequenziale** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**Accesso casuale** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**Supporta la scrittura** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

**Crittografia** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

**Compressione** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

**Supporta supporti rimuovibili** (7)


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**Pulizia manuale** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**Pulizia automatica** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**Notifica intelligente** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**Supporta supporti a doppio lato** (11)


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**Espulsione Predismount non obbligatoria** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Funzionalità**")
</dt> </dl>

Matrice di descrizioni delle funzionalità per gli elementi nella matrice di **funzionalità** .

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'algoritmo o dello strumento utilizzato dal dispositivo per supportare la compressione.

Se non si specifica un tipo di compressione, è possibile usare uno dei valori seguenti:

-   Il supporto per la compressione "Unknown" è sconosciuto o non è specificato.
-   La compressione "compresso" è supportata, ma il tipo è sconosciuto o non è specificato.
-   "Non compresso" il dispositivo non supporta le funzionalità di compressione.

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")
</dt> </dl>

Dimensioni del blocco predefinite, in byte, per il dispositivo.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di rilevamento e correzione degli errori supportato dal dispositivo.

</dd> <dt>

**LastCleaned**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultima pulizia del dispositivo.

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi"), **punito** ("secondo \* 10 ^-3")
</dt> </dl>

Tempo necessario, in millisecondi, per consentire al dispositivo di leggere o scrivere un supporto dopo l'avvio del caricamento del dispositivo. Ad esempio, per le unità disco, questo è l'intervallo tra un disco che non viene ruotato sul disco che è pronto per le operazioni di lettura/scrittura. Per le unità nastro, questa operazione viene avviata quando si inserisce un supporto e termina quando l'unità segnala che è pronta per un'applicazione. Si tratta in genere dell'area di BOT (inizio del nastro) del nastro.

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi"), **punito** ("secondo \* 10 ^-3")
</dt> </dl>

Tempo di accesso massimo del supporto, in millisecondi. Per un'unità disco, rappresenta la ricerca completa e il ritardo rotazionale completo. Per le unità nastro, rappresenta una ricerca dall'inizio del nastro al punto più distante fisicamente.

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")
</dt> </dl>

Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF i \| dispositivi di accesso sequenziale \| 001,2 "," MIF. \|Disco host DMTF \| 001,5 ")
</dt> </dl>

Dimensione massima, in kilobyte, del supporto supportato da questo dispositivo.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")
</dt> </dl>

Numero massimo di unità che è possibile utilizzare prima di pulire il dispositivo. **UnitsDescription** definisce il tipo di unità.

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se il supporto è bloccato nel dispositivo e non può essere espulso; in caso contrario, **false**. Per i dispositivi non rimovibili, questo valore deve essere **true**.

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")
</dt> </dl>

Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **contatore**
</dt> </dl>

Il numero di volte in cui il supporto è stato montato per il trasferimento dei dati o per la pulizia del dispositivo. Se il dispositivo non supporta supporti rimovibili, questa proprietà deve essere impostata su zero.

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se il dispositivo deve essere pulito. in caso contrario, **false**.

> [!Note]  
> La proprietà **capabilities** indica se è possibile la pulizia manuale o automatica.

 

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se il dispositivo supporta più supporti singoli, questa proprietà definisce il numero massimo che può essere supportato o inserito.

</dd> <dt>

**Sicurezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dischi DMTF \| 003,22 ")
</dt> </dl>

Sicurezza operativa del dispositivo.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (3)


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

**Sola lettura** (4)


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

**Bloccato** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Bypass di avvio** (6)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**Bypass di avvio e di sola lettura** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora più recenti in cui il supporto è stato montato sul dispositivo. Questa proprietà viene usata solo dai dispositivi che supportano supporti rimovibili.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in secondi, per cui il supporto è stato montato per il trasferimento dei dati o per la pulizia del dispositivo. Se il dispositivo non supporta supporti rimovibili, questa proprietà deve essere impostata su zero.

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte al secondo"), **punito** ("byte/secondo \* 10 ^ 3")
</dt> </dl>

Velocità di trasferimento dati prolungata, espressa in kilobyte, in cui il dispositivo può leggere e scrivere su un supporto. Si tratta di una velocità dati continua e non elaborata. In questa proprietà non devono essere segnalate le tariffe o le tariffe massime con compressione.

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**","**CIM \_ MediaAccessDevice**.**UnitsUsed**")
</dt> </dl>

Descrive il tipo di unità delle proprietà **MaxUnitsBeforeCleaning** e **UnitsUsed** .

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**misuratore**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MediaAccessDevice**.**UnitsDescription**","**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**")
</dt> </dl>

Il numero di unità usate dal dispositivo. Questa proprietà viene usata per determinare quando il dispositivo deve essere pulito. **UnitsDescription** definisce il tipo di unità.

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi"), **punito** ("secondo \* 10 ^-3")
</dt> </dl>

Tempo necessario, in millisecondi, per la transizione del dispositivo alla lettura o alla scrittura di contenuti multimediali da scaricare. Ad esempio, per le unità disco, questo è l'intervallo tra un disco con velocità nominale e un disco non in rotazione. Per le unità nastro, questo è il momento in cui un supporto passa dal BOT a essere completamente espulso e accessibile a un elemento di selezione o a un operatore umano.

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

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

