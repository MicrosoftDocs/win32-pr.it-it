---
description: La classe CiM \_ DataFile rappresenta una raccolta denominata di dati o codice eseguibile. Verranno restituite solo le istanze dei file nei dischi fissi locali.
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: CIM_DataFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile
- CIM_DataFile.Caption
- CIM_DataFile.Description
- CIM_DataFile.InstallDate
- CIM_DataFile.Status
- CIM_DataFile.AccessMask
- CIM_DataFile.Archive
- CIM_DataFile.Compressed
- CIM_DataFile.CompressionMethod
- CIM_DataFile.CreationClassName
- CIM_DataFile.CreationDate
- CIM_DataFile.CSCreationClassName
- CIM_DataFile.CSName
- CIM_DataFile.Drive
- CIM_DataFile.EightDotThreeFileName
- CIM_DataFile.Encrypted
- CIM_DataFile.EncryptionMethod
- CIM_DataFile.Name
- CIM_DataFile.Extension
- CIM_DataFile.FileName
- CIM_DataFile.FileSize
- CIM_DataFile.FileType
- CIM_DataFile.FSCreationClassName
- CIM_DataFile.FSName
- CIM_DataFile.Hidden
- CIM_DataFile.InUseCount
- CIM_DataFile.LastAccessed
- CIM_DataFile.LastModified
- CIM_DataFile.Path
- CIM_DataFile.Readable
- CIM_DataFile.System
- CIM_DataFile.Writeable
- CIM_DataFile.Manufacturer
- CIM_DataFile.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6bbc73534914f1b6dc1bfd9f620a436bbcea2056a70cb50757afccf60beea04c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924651"
---
# <a name="cim_datafile-class"></a>Classe \_ CiM DataFile

La **classe CiM \_ DataFile** rappresenta una raccolta denominata di dati o codice eseguibile. Verranno restituite solo le istanze dei file nei dischi fissi locali.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Name;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
  string   Manufacturer;
  string   Version;
};
```

## <a name="members"></a>Members

La **classe \_ CiM DataFile** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ CiM DataFile** include questi metodi.



| Metodo                                                                                          | Descrizione                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autorizzazioni changeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md)     | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-datafile.md) | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                   |
| [**Comprimere**](compress-method-in-class-cim-datafile.md)                                       | Utilizza la compressione NTFS per comprimere il file logico (o la directory) specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                       |
| [**CompressEx**](compressex-method-in-class-cim-datafile.md)                                   | Comprime il file logico (o la directory) specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                              |
| [**Copia**](copy-method-in-class-cim-datafile.md)                                               | Copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input. Implementato da WMI.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-datafile.md)                                           | Copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input. Implementato da WMI.<br/> |
| [**Elimina**](delete-method-in-class-cim-datafile.md)                                           | Elimina il file logico (o la directory) specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-datafile.md)                                       | Elimina il file logico (o la directory) specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-datafile.md)           | Determina se il chiamante dispone delle autorizzazioni aggregate specificate **dall'argomento Permission.** Implementato da WMI.<br/>                |
| [**Rinominare**](rename-method-in-class-cim-datafile.md)                                           | Rinomina il file logico (o la directory) specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md)                             | Ottiene la proprietà del file logico specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-datafile.md)                         | Ottiene la proprietà del file logico specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                                   |
| [**Decomprimere**](uncompress-method-in-class-cim-datafile.md)                                   | Decomprime il file logico (o la directory) specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-datafile.md)                               | Decomprime il file logico (o la directory) specificato nel percorso dell'oggetto. Implementato da WMI.<br/>                                            |



 

### <a name="properties"></a>Proprietà

La **classe \_ CiM DataFile** ha queste proprietà.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Diritti di accesso")
</dt> </dl>

Maschera di bit che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file. Per i valori di bit, vedere [**Costanti dei diritti di accesso a file e directory.**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)

> [!Note]  
> Nei volumi FAT viene invece restituito il valore **FULL \_ ACCESS,** che indica che per l'oggetto non è stata impostata alcuna sicurezza.

 

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**FILE \_ READ \_ DATA (file) o FILE \_ LIST DIRECTORY \_ (directory)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**FILE \_ WRITE \_ DATA (file) o FILE \_ ADD FILE \_ (directory)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**FILE \_ APPEND \_ DATA (file) o FILE \_ ADD \_ SUBDIRECTORY (directory)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**FILE \_ READ \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**FILE \_ WRITE \_ EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**FILE \_ EXECUTE (file) o FILE \_ TRAVERSE (directory)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**FILE \_ DELETE \_ CHILD (directory)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**FILE \_ ATTRIBUTI \_ DI** LETTURA (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**FILE \_ ATTRIBUTI \_ DI** SCRITTURA (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**DELETE** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**READ \_ CONTROL** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**WRITE \_ Applicazione livello** dati (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**WRITE \_ OWNER** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**SYNCHRONIZE** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Archiviazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve essere archiviato")
</dt> </dl>

Se **True,** il file deve essere archiviato.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")
</dt> </dl>

Se **True**, il file è compresso.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Metodo di compressione")
</dt> </dl>

Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico. Se lo schema di compressione è sconosciuto o non è descritto, usare "Sconosciuto". Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, usare "Compressed". Se il file logico non è compresso, usare "Non compresso".

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")
</dt> </dl>

Nome della classe.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data di creazione")
</dt> </dl>

Data e ora di creazione del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ FileSystem CIM**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")
</dt> </dl>

Classe del computer.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ FileSystem CIM**](cim-filesystem.md).**CSName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")
</dt> </dl>

Nome del computer.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Unità**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**corretto**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Unità")
</dt> </dl>

Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file.

Esempio: "c:"

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("eight dot three file name")
</dt> </dl>

Nome file compatibile con DOS.

Esempio: "c: \\ progra~1"

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Crittografata**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")
</dt> </dl>

Se **True,** il file è crittografato.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Encryptionmethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Metodo di crittografia")
</dt> </dl>

Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico. Se lo schema di crittografia non è in uso,ad esempio per motivi di sicurezza, usare "Sconosciuto". Se il file è crittografato, ma il relativo schema di crittografia è sconosciuto o non viene divulgato, usare "Encrypted". Se il file logico non è crittografato, usare "Non crittografato".

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Estensione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**corretto**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estensione file")
</dt> </dl>

Estensione del nome file senza il punto precedente (punto).

Esempio: "txt", "mof", "mdb"

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**corretto**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")
</dt> </dl>

Nome file senza l'estensione del nome file. Esempio: "MyDataFile"

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Dimensione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Dimensioni del file, in byte.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Filetype**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tipo di file")
</dt> </dl>

Descrittore che rappresenta il tipo di file indicato dalla **proprietà Extension.**

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ FileSystem CIM**](cim-filesystem.md).**CreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")
</dt> </dl>

Classe dell'file system.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ FileSystem CIM**](cim-filesystem.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")
</dt> </dl>

Nome del file system.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

Se **True,** il file è nascosto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")
</dt> </dl>

Numero di "file aperto" attualmente attivi sul file.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultimo accesso")
</dt> </dl>

Data e ora dell'ultimo accesso al file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultima modifica")
</dt> </dl>

Data e ora dell'ultima modifica del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")
</dt> </dl>

Stringa del produttore dalla risorsa della versione (se presente).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

La proprietà Name è una stringa che rappresenta il nome ereditato che funge da chiave di un'istanza di file logico all'interno di un file system. È necessario che siano specificati nomi di percorso completi.

Esempio: C: \\ Windows \\ sistema \\win.ini

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Percorso del file, incluse le barre rovesciate iniziali e finali. Esempio: " \\ windows \\ system \\ "

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Leggibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Leggibile")
</dt> </dl>

Se **True,** il file può essere letto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto . È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "Degraded" e "Pred Fail". "Pred Fail" indica che un elemento funziona correttamente, ma sta stimando un errore (ad esempio, un disco rigido abilitato per SMART).

Lo stato non operativo può includere "Error", "Starting", "Stopping" e "Service". "Servizio" può essere applicato durante il ridimensionamento del mirror del disco, il ricaricamento di un elenco di autorizzazioni utente o altre operazioni amministrative. Non tutte queste operazioni sono online, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradato** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** ("Avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** ("Arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("Servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("Nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**Sistema**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File di sistema")
</dt> </dl>

Se **True**, il file è un file di sistema.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")
</dt> </dl>

Stringa di versione dalla risorsa di versione (se presente).

</dd> <dt>

**Scrivibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Scrivibile")
</dt> </dl>

Se **True,** il file può essere scritto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ DataFile** è derivata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

WMI implementa la **classe CIM \_ DataFile** e tutti i relativi metodi. La **classe CIM \_ DataFile** è una classe dinamica.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

Per motivi di sicurezza, WMI non supporta direttamente la chiamata a un computer remoto e indica di copiare i file in se stesso. È tuttavia possibile usare il linguaggio di programmazione pertinente per chiamare FTP o RoboCopy, ad esempio.

## <a name="examples"></a>Esempio

Nell'esempio di [codice](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) di Scripting Center seguente viene utilizzata una classe **CIM \_ DataFile** come parte di un'applicazione più grande per generare report dell'ambiente di scambio tramite PowerShell.

L'esempio di codice Find [files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) in TechNet Gallery usa **un CIM \_ DataFile** per cercare uno o più file in più computer.

L'esempio di codice VBS seguente descrive come eseguire una ricerca con caratteri jolly standard in un file di dati. Si noti che i delimitatori della barra rovesciata devono essere preceduti da un'altra barra rovesciata ( \\ \\ ). Inoltre, quando si usa "**CIM \_ DataFile**.**FileName**" nella clausola WHERE, il processo WMIPRVSE eseguirà l'analisi di tutte le directory in qualsiasi dispositivo di archiviazione disponibile. Questa operazione può richiedere tempo, soprattutto se sono state mappate condivisioni remote, e può attivare avvisi antivirus.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



Il frammento di codice seguente limita l'intervallo di ricerca a un'unità, un percorso ed un'estensione di file specifici.


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



L'esempio di codice di PowerShell seguente recupera un singolo valore di attributo.


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dt>

[Attività WMI: File e cartelle](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Costanti dei diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

