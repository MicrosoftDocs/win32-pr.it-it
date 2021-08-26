---
description: CodecFile Win32 \_&\# 32; La classe WMI rappresenta il codec audio o video installato nel sistema del computer.
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Win32_CodecFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d9f41178c69f40513b26de5221af6eb7b5e425acf5c4893f2de87fb18211291
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079911"
---
# <a name="win32_codecfile-class"></a>Classe CodecFile Win32 \_

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ Win32 CodecFile** rappresenta il codec audio o video installato nel sistema. I codec convertono un tipo di formato multimediale in un altro, in genere un formato compresso in un formato non compresso. Il nome "codec" deriva da una combinazione di compressione e decompressione. Ad esempio, un codec può convertire un formato compresso, ad esempio MS-ADPCM, in un formato non compresso, ad esempio PCM, che la maggior parte dell'hardware audio può riprodurre direttamente.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a>Members

La **classe \_ CodecFile Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ CodecFile Win32** include questi metodi.



| Metodo                                                                                             | Descrizione                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-codecfile.md)     | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                         |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                         |
| [**Comprimere**](compress-method-in-class-win32-codecfile.md)                                       | Comprime il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                    |
| [**CompressEx**](compressex-method-in-class-win32-codecfile.md)                                   | Comprime il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                    |
| [**Copia**](copy-method-in-class-win32-codecfile.md)                                               | Copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.<br/>                                                                                         |
| [**CopyEx**](copyex-method-in-class-win32-codecfile.md)                                           | Metodo della classe che copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro FileName.<br/>                                                                    |
| [**Elimina**](delete-method-in-class-win32-codecfile.md)                                           | Elimina il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                       |
| [**DeleteEx**](deleteex-method-in-class-win32-codecfile.md)                                       | Elimina il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                       |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-codecfile.md)           | Determina se il chiamante dispone delle  autorizzazioni aggregate specificate dall'argomento di autorizzazione non solo sull'oggetto file, ma sulla condivisione in cui risiede il file o la directory (se si trova in una condivisione).<br/> |
| [**Rinominare**](rename-method-in-class-win32-codecfile.md)                                           | Metodo della classe che rinomina il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                     |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-codecfile.md)                             | Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                                         |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-codecfile.md)                         | Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                       |
| [**Decomprimere**](uncompress-method-in-class-win32-codecfile.md)                                   | Decomprime il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                  |
| [**UncompressEx**](uncompressex-method-in-class-win32-codecfile.md)                               | Decomprime il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                  |



 

### <a name="properties"></a>Proprietà

La **classe \_ CodecFile Win32** ha queste proprietà.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Diritti di accesso")
</dt> </dl>

Maschera di bit che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file codec. Per i valori di bit, vedere [**Costanti dei diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> Nei volumi FAT viene invece restituito il valore **FULL \_ ACCESS,** che indica che non è stata impostata alcuna sicurezza per l'oggetto.

 

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

**FILE \_ LETTURA \_ ATTRIBUTI** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**FILE \_ ATTRIBUTI \_ WRITE** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**DELETE** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**LETTURA \_ CONTROL** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**WRITE \_ Applicazione livello dati** (262144)


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

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")
</dt> </dl>

Se **True,** il file deve essere archiviato.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto.

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

Se **True**, il file viene compresso.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Metodo di compressione")
</dt> </dl>

Algoritmo o strumento usato per comprimere il file logico. Se non è possibile (o non desiderato) descrivere lo schema di compressione ,ad esempio perché non è noto, usare le parole seguenti: "Sconosciuto" per indicare che non è noto se il file logico è compresso o meno. "Compressed" per indicare che il file è compresso, ma il relativo schema di compressione non è noto o non viene divulgato; e "Not Compressed" per rappresentare che il file logico non è compresso.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata nella creazione di un'istanza. Se usata con le altre proprietà chiave della classe , la proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

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

Data di creazione del file.

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

Stringa che rappresenta il nome del computer.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Descrizione), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet control \\ \\ \\ \\ MediaResources \\ \\ icm \| Description")
</dt> </dl>

Nome completo del driver codec. Questa stringa deve essere visualizzata in spazi di grandi dimensioni (descrittivi).

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Esempio: "Microsoft PCM Converter"

</dd> <dt>

**Unità**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**corretto**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Unità")
</dt> </dl>

Lettera di unità (inclusi i due punti) del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Esempio: "c:"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("eight dot three file name")
</dt> </dl>

Nome file compatibile con DOS per questo file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Esempio: "c: \\ progra~1"

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

Algoritmo o strumento utilizzato per crittografare il file logico. Se non è possibile (o non si desidera) descrivere lo schema di crittografia (forse per motivi di sicurezza), usare le parole seguenti: "Sconosciuto" per indicare che non è noto se il file logico è crittografato o meno. "Encrypted" per indicare che il file è crittografato, ma il relativo schema di crittografia non è noto o non è divulgato; e "Not Encrypted" per rappresentare che il file logico non è crittografato.

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

Estensione del nome file (senza il punto).

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Esempi: "txt", "mof", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**corretto**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")
</dt> </dl>

Nome (senza l'estensione) del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Esempio: "autoexec"

</dd> <dt>

**Dimensione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Dimensioni del file (in byte).

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Filetype**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tipo di file")
</dt> </dl>

Tipo di file (indicato dalla **proprietà Extension).**

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

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ FileSystem CIM**](cim-filesystem.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")
</dt> </dl>

Nome del file system.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Gruppo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ drivers.desc")
</dt> </dl>

Codec rappresentato da questa classe.

I valori possibili sono:

<dl> <dd>"Audio"</dd> <dd>"Video"</dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

**Audio** ("Audio")


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Video** ("Video")


</dt> <dd></dd> </dl>

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

L'oggetto è stato installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

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

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultimo accesso")
</dt> </dl>

Ultimo accesso al file.

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

Il file è stato modificato per l'ultima volta.

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

Stringa del produttore dalla risorsa di versione, se presente.

Questa proprietà viene ereditata da [**CIM \_ DataFile.**](cim-datafile.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome ereditato che funge da chiave di un'istanza di file logico all'interno di un file system. È necessario che siano specificati nomi di percorso completi.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Esempio: "C: \\ Windows \\ sistema \\win.ini"

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Percorso del file. Sono incluse le barre rovesciate iniziali e finali.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Esempio: " \\ windows \\ system \\ "

</dd> <dt>

**Leggibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Leggibile")
</dt> </dl>

È possibile leggere il file.

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

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un disco rigido abilitato per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati non di operazione includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

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

Stringa di versione dalla risorsa di versione, se presente.

Questa proprietà viene ereditata da [**CIM \_ DataFile.**](cim-datafile.md)

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

La **classe \_ CodecFile Win32** è derivata da [**CIM \_ DataFile**](cim-datafile.md).

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

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

