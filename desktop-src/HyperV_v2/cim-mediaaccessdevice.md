---
description: Rappresenta un dispositivo che può usare supporti per archiviare e recuperare dati.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: CIM_MediaAccessDevice classe (gestione Hyper-V)
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
ms.openlocfilehash: bb97ded03cfc853fc0dde6ede26083be01cf218f210c31f947f315634599e179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900261"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a>CIM_MediaAccessDevice classe (gestione Hyper-V)

Rappresenta un dispositivo che può usare supporti per archiviare e recuperare dati.

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

La **classe CIM \_ MediaAccessDevice** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe CIM \_ MediaAccessDevice** dispone di questi metodi.



| Metodo                                               | Descrizione                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**LockMedia**](cim-mediaaccessdevice-lockmedia.md) | Blocca e sblocca supporti rimovibili in un dispositivo di accesso ai supporti.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe CIM \_ MediaAccessDevice** ha queste proprietà.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Archiviazione dispositivi \| 001.9", "MIF. DMTF \| Archiviazione dispositivi \| 001.11", "MIF. DMTF \| Archiviazione dispositivi \| 001.12", "MIF. DMTF \| Disks \| 003.7", "MIF. DMTF \| Host Disk \| 001.2", "MIF. DMTF \| Host Disk \| 001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")
</dt> </dl>

Matrice che contiene le funzionalità del dispositivo di accesso ai supporti.

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

**Supporta supporti rimovibili** (7)


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**Pulizia manuale** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**Pulizia automatica** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**Notifica SMART** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**Supporta supporti a doppio lato** (11)


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**Predismount Eject Not Required** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Funzionalità**")
</dt> </dl>

Matrice di descrizioni delle funzionalità per gli elementi nella matrice **Capabilities.**

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'algoritmo o dello strumento usato dal dispositivo per supportare la compressione.

Se non viene specificato un tipo di compressione, è possibile usare uno dei valori seguenti:

-   Il supporto della compressione "Sconosciuto" è sconosciuto o non è specificato.
-   La compressione "Compressa" è supportata, ma il tipo è sconosciuto o non specificato.
-   "Non compresso" il dispositivo non supporta le funzionalità di compressione.

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Byte"), **PUnit** ("byte")
</dt> </dl>

Dimensioni del blocco predefinite, in byte, per il dispositivo.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di rilevamento e correzione degli errori supportati dal dispositivo.

</dd> <dt>

**LastCleaned**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultima pulizia del dispositivo.

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")
</dt> </dl>

Tempo necessario, in millisecondi, per la lettura o la scrittura di un supporto dopo l'avvio del caricamento del dispositivo. Ad esempio, per le unità disco, questo è l'intervallo tra un disco che non ruota sul disco segnalando che è pronto per le operazioni di lettura/scrittura. Per le unità nastro, viene avviato quando il supporto viene inserito e termina quando l'unità segnala che è pronto per un'applicazione. In genere si trova nell'area di inizio del nastro (BOT).

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")
</dt> </dl>

Tempo massimo di accesso del supporto, espresso in millisecondi. Per un'unità disco, rappresenta la ricerca completa e il ritardo di rotazione completo. Per le unità nastro, rappresenta una ricerca dall'inizio del nastro al punto più distante fisicamente.

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Byte"), **PUnit** ("byte")
</dt> </dl>

Dimensioni massime in byte del blocco per i supporti a cui accede il dispositivo.

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Sequential Access Devices \| 001.2", "MIF. DMTF \| Host Disk \| 001.5")
</dt> </dl>

Dimensioni massime, in kilobyte, dei supporti supportati da questo dispositivo.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")
</dt> </dl>

Numero massimo di unità che è possibile usare prima della pulizia del dispositivo. **UnitsDescription** definisce il tipo di unità.

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se il supporto è bloccato nel dispositivo e non può essere espulso; in caso contrario, **false**. Per i dispositivi non rimovibili, questo valore deve essere **true.**

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Byte"), **PUnit** ("byte")
</dt> </dl>

Dimensioni minime del blocco, in byte, per i supporti a cui accede il dispositivo.

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Contatore**
</dt> </dl>

Numero di volte in cui il supporto è stato montato per il trasferimento dei dati o per pulire il dispositivo. Se il dispositivo non supporta supporti rimovibili, questa proprietà deve essere impostata su zero.

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se il dispositivo richiede la pulizia; in caso contrario, **false**.

> [!Note]  
> La **proprietà Capabilities** indica se è possibile eseguire la pulizia manuale o automatica.

 

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se il dispositivo supporta più supporti singoli, questa proprietà definisce il numero massimo che può essere supportato o inserito.

</dd> <dt>

**Sicurezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Disks \| 003.22")
</dt> </dl>

Sicurezza operativa per il dispositivo.

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

**Bypass di** avvio (6)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**Bypass di avvio e sola lettura** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora più recenti in cui è stato montato il supporto nel dispositivo. Questa proprietà viene usata solo dai dispositivi che supportano supporti rimovibili.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in secondi, in cui il supporto è stato montato per il trasferimento dei dati o per pulire il dispositivo. Se il dispositivo non supporta supporti rimovibili, questa proprietà deve essere impostata su zero.

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloByte al secondo"), **PUnit** ("byte/secondo \* 10^3")
</dt> </dl>

Velocità di trasferimento dei dati sostenuta in kilobyte con cui il dispositivo può leggere e scrivere in un supporto. Si tratta di una frequenza di dati non elaborati sostenuta. Le tariffe massime con compressione non devono essere segnalate in questa proprietà.

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM \_ MediaAccessDevice**.**UnitsUsed**")
</dt> </dl>

Descrive il tipo di unità delle **proprietà MaxUnitsBeforeCleaning** **e UnitsUsed.**

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**", "**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**")
</dt> </dl>

Numero di unità usate dal dispositivo. Questa proprietà viene usata per determinare quando pulire il dispositivo. **UnitsDescription** definisce il tipo di unità.

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")
</dt> </dl>

Tempo necessario, in millisecondi, per il dispositivo per la transizione dalla lettura o dalla scrittura di supporti a quello di scaricamento. Ad esempio, per le unità disco, questo è l'intervallo tra un disco che ruota a velocità nominale e un disco che non ruota. Per le unità nastro, questo è il momento in cui un supporto passa dal bot all'espulso completamente e accessibile a un elemento di selezione o a un operatore umano.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

