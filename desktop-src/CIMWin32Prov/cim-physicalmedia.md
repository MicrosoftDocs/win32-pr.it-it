---
description: La \_ classe CIM PhysicalMedia rappresenta i tipi di documentazione e supporti di archiviazione, ad esempio nastri, CD ROM e così via.
ms.assetid: ba258e53-4a82-4b30-aadd-54448841cd06
ms.tgt_platform: multiple
title: Classe CIM_PhysicalMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMedia
- CIM_PhysicalMedia.Capacity
- CIM_PhysicalMedia.Caption
- CIM_PhysicalMedia.CleanerMedia
- CIM_PhysicalMedia.CreationClassName
- CIM_PhysicalMedia.Description
- CIM_PhysicalMedia.HotSwappable
- CIM_PhysicalMedia.InstallDate
- CIM_PhysicalMedia.Manufacturer
- CIM_PhysicalMedia.MediaDescription
- CIM_PhysicalMedia.MediaType
- CIM_PhysicalMedia.Model
- CIM_PhysicalMedia.Name
- CIM_PhysicalMedia.OtherIdentifyingInfo
- CIM_PhysicalMedia.PartNumber
- CIM_PhysicalMedia.PoweredOn
- CIM_PhysicalMedia.Removable
- CIM_PhysicalMedia.Replaceable
- CIM_PhysicalMedia.SerialNumber
- CIM_PhysicalMedia.SKU
- CIM_PhysicalMedia.Status
- CIM_PhysicalMedia.Tag
- CIM_PhysicalMedia.Version
- CIM_PhysicalMedia.WriteProtectOn
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8709128c189956bba4bc371e0f5bfb30d67b49f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234524"
---
# <a name="cim_physicalmedia-class"></a>CIM \_ PhysicalMedia (classe)

La classe **CIM \_ PhysicalMedia** rappresenta i tipi di documentazione e supporti di archiviazione, ad esempio nastri, CD ROM e così via. Questa classe viene in genere usata per individuare e gestire supporti rimovibili (rispetto ai supporti bloccati con il dispositivo di accesso multimediale come singolo pacchetto, ad esempio dischi rigidi). I supporti sealed, tuttavia, possono essere modellati anche usando questa classe quando il supporto è associato al pacchetto fisico usando la relazione [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) .

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B7D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMedia : CIM_PhysicalComponent
{
  uint64   Capacity;
  string   Caption;
  boolean  CleanerMedia;
  string   CreationClassName;
  string   Description;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   MediaDescription;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  WriteProtectOn;
};
```

## <a name="members"></a>Members

La classe **CIM \_ PhysicalMedia** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ PhysicalMedia** dispone di queste proprietà.

<dl> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")
</dt> </dl>

Numero di byte che possono essere letti o scritti in un supporto. Questa proprietà non è applicabile a una copia (documentazione) o a un supporto più pulito. La compressione dei dati non deve essere presupposta, in quanto aumenterebbe il valore in questa proprietà. Per i nastri, è preferibile che non vengano registrate tracce di file o spazi vuoti sul supporto.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CleanerMedia**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il supporto fisico viene usato per scopi di pulizia e non per l'archiviazione di dati.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il pacchetto può essere scambiato a caldo. Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato. Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo. Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome dell'organizzazione responsabile della creazione dell'elemento fisico. Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**MediaDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaType**")
</dt> </dl>

Dettagli aggiuntivi relativi all'enumerazione **mediaType** . Se, ad esempio, viene specificato il valore 3 ("QIC cartuccia"), questa proprietà indicherà se il nastro è in larghezza o 1/4 pollice, preformattato, compatibile con Travan e così via.

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaDescription**")
</dt> </dl>

Tipo di supporti fisici. La proprietà **MEDIADESCRIPTION** fornisce una definizione più esplicita del tipo di supporto.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Cartuccia nastro** (2)


</dt> <dd></dd> <dt>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**Cartuccia QIC** (3)


</dt> <dd></dd> <dt>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**Cartuccia AIT** (4)


</dt> <dd></dd> <dt>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**Cartuccia DTF** (5)


</dt> <dd></dd> <dt>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**Cartuccia dat** (6)


</dt> <dd></dd> <dt>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**cartuccia nastro 8mm** (7)


</dt> <dd></dd> <dt>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19 mm cartuccia nastro** (8)


</dt> <dd></dd> <dt>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**Cartuccia DLT** (9)


</dt> <dd></dd> <dt>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Cartuccia nastro magnetico da metà pollice** (10)


</dt> <dd></dd> <dt>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Disco cartuccia** (11)


</dt> <dd></dd> <dt>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**Disco Jaz** (12)


</dt> <dd></dd> <dt>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**Disco zip** (13)


</dt> <dd></dd> <dt>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**Disco SyQuest** (14)


</dt> <dd></dd> <dt>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Disco rimovibile Winchester** (15)


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD registrabile** (19)


</dt> <dd></dd> <dt>

<span id="WORM"></span><span id="worm"></span>

<span id="WORM"></span><span id="worm"></span>**Worm** (20)


</dt> <dd></dd> <dt>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-ottico** (21)


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span id="DVD"></span><span id="dvd"></span>**DVD** (22)


</dt> <dd></dd> <dt>

<span id="DVD_RW"></span><span id="dvd_rw"></span>

<span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD + RW** (23)


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-video** (26)


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)


</dt> <dd></dd> <dt>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/dischetto** (28)


</dt> <dd>

Disco floppy

</dd> <dt>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Disco rigido** (29)


</dt> <dd></dd> <dt>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Scheda memoria** (30)


</dt> <dd></dd> <dt>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Copia disco rigido** (31)


</dt> <dd></dd> <dt>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Disco clik** (32)


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span id="CD_"></span><span id="cd_"></span>**CD +** (35)


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD registrabile** (36)


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-ottico riscrivibile** (43)


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Scrittura magneto-ottico una volta** (44)


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical riscrivibile (LIMDOW)** (45)


</dt> <dd></dd> <dt>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Modifica della fase scrittura una volta** (46)


</dt> <dd></dd> <dt>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Modifica della fase riscrivibile** (47)


</dt> <dd></dd> <dt>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Modifica della fase doppio riscrivibile** (48)


</dt> <dd></dd> <dt>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Scrittura ablativo** (49)


</dt> <dd></dd> <dt>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Registrazione Near Field** (50)


</dt> <dd></dd> <dt>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQIC** (51)


</dt> <dd></dd> <dt>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)


</dt> <dd></dd> <dt>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**particella 8mm Metal** (53)


</dt> <dd></dd> <dt>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**evaporazione metallo avanzata 8mm** (54)


</dt> <dd></dd> <dt>

<span id="NCTP"></span><span id="nctp"></span>

<span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)


</dt> <dd></dd> <dt>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)


</dt> <dd></dd> <dt>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**Accelis LTO** (57)


</dt> <dd></dd> <dt>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 track tape** (58)


</dt> <dd>

9-tenere traccia del nastro

</dd> <dt>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 track tape** (59)


</dt> <dd>

18-track tape

</dd> <dt>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 track tape** (60)


</dt> <dd>

36-track tape

</dd> <dt>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)


</dt> <dd></dd> <dt>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**MP Magstar** (62)


</dt> <dd></dd> <dt>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**Nastro D2** (63)


</dt> <dd></dd> <dt>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape-DST Small** (64)


</dt> <dd>

Tape DST Small

</dd> <dt>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Nastro-DST medio** (65)


</dt> <dd>

Media DST nastro

</dd> <dt>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape-DST grande** (66)


</dt> <dd>

DST nastro grande

</dd> </dl>

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome in base al quale l'elemento fisico è generalmente noto.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico. Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset. Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** . Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**NumeroArticolo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'elemento fisico è acceso.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Rimovibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, questo elemento è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti. Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione. Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo. Ad esempio, un chip del processore non aggiornabile è rimovibile.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

</dd> <dt>

**Sostituibili**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso. Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate. In questo caso, il processore viene definito sostituibile. Tutti i componenti rimovibili sono intrinsecamente sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Numero allocato dal produttore utilizzato per identificare l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Numero di unità per l'elemento fisico che mantiene le scorte.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Stato corrente dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Ridotto **("danneggiato"** )


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Errore di predazione** ("Predator fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** di ("avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** in corso ("arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sottolineato** (sottolineato)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Noncover** ("noncover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicazione persa** ("comunicazione persa")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento. Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie. La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via. Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato. L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito. La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Versione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**WriteProtectOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il supporto è attualmente protetto da scrittura da un meccanismo fisico, ad esempio una scheda Proteggi su un disco floppy.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ PhysicalMedia** è derivata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_PHYSICALCOMPONENT CIM**](cim-physicalcomponent.md)
</dt> </dl>

 

