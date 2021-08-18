---
description: Oggetto ShortcutFile Win32 \_&\# 32; La classe WMI rappresenta i file che sono collegamenti ad altri file, directory e comandi.
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Win32_ShortcutFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile
- Win32_ShortcutFile.Caption
- Win32_ShortcutFile.Description
- Win32_ShortcutFile.InstallDate
- Win32_ShortcutFile.Status
- Win32_ShortcutFile.AccessMask
- Win32_ShortcutFile.Archive
- Win32_ShortcutFile.Compressed
- Win32_ShortcutFile.CompressionMethod
- Win32_ShortcutFile.CreationClassName
- Win32_ShortcutFile.CreationDate
- Win32_ShortcutFile.CSCreationClassName
- Win32_ShortcutFile.CSName
- Win32_ShortcutFile.Drive
- Win32_ShortcutFile.EightDotThreeFileName
- Win32_ShortcutFile.Encrypted
- Win32_ShortcutFile.EncryptionMethod
- Win32_ShortcutFile.Name
- Win32_ShortcutFile.Extension
- Win32_ShortcutFile.FileName
- Win32_ShortcutFile.FileSize
- Win32_ShortcutFile.FileType
- Win32_ShortcutFile.FSCreationClassName
- Win32_ShortcutFile.FSName
- Win32_ShortcutFile.Hidden
- Win32_ShortcutFile.InUseCount
- Win32_ShortcutFile.LastAccessed
- Win32_ShortcutFile.LastModified
- Win32_ShortcutFile.Path
- Win32_ShortcutFile.Readable
- Win32_ShortcutFile.System
- Win32_ShortcutFile.Writeable
- Win32_ShortcutFile.Manufacturer
- Win32_ShortcutFile.Version
- Win32_ShortcutFile.Target
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f1951d4c52087330ac28e23e59e9403c67aff44bf7f9e94c63d3bfa7fc1bded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917501"
---
# <a name="win32_shortcutfile-class"></a>Classe ShortcutFile Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 ShortcutFile** rappresenta i file che sono collegamenti ad altri file, directory e comandi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE466-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_ShortcutFile : CIM_DataFile
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
  string   Target;
};
```

## <a name="members"></a>Members

La **classe \_ ShortcutFile Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ ShortcutFile Win32** include questi metodi.



| Metodo                                                                                                | Descrizione                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | Metodo della classe che modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                     |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | Metodo della classe che modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                     |
| [**Comprimere**](compress-method-in-class-win32-shortcutfile.md)                                       | Metodo della classe che comprime il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                |
| [**CompressEx**](compressex-method-in-class-win32-shortcutfile.md)                                   | Metodo della classe che comprime il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                |
| [**Copia**](copy-method-in-class-win32-shortcutfile.md)                                               | Metodo della classe che copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.<br/>                                                                                     |
| [**CopyEx**](copyex-method-in-class-win32-shortcutfile.md)                                           | Metodo della classe che copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal *parametro FileName.*<br/>                                                                                |
| [**Elimina**](delete-method-in-class-win32-shortcutfile.md)                                           | Metodo della classe che elimina il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                   |
| [**DeleteEx**](deleteex-method-in-class-win32-shortcutfile.md)                                       | Metodo della classe che elimina il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                   |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | Metodo della classe che determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento Permission non solo nell'oggetto file, ma nella condivisione in cui risiede il file o la directory (se si trova in una condivisione).<br/> |
| [**Rinominare**](rename-method-in-class-win32-shortcutfile.md)                                           | Metodo della classe che rinomina il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                                   |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-shortcutfile.md)                             | Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                                     |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-shortcutfile.md)                         | Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                                     |
| [**Decomprimere**](uncompress-method-in-class-win32-shortcutfile.md)                                   | Metodo della classe che decomprime il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                              |
| [**UncompressEx**](uncompressex-method-in-class-win32-shortcutfile.md)                               | Metodo della classe che decomprime il file logico (o la directory) specificato nel percorso dell'oggetto.<br/>                                                                                                                              |



 

### <a name="properties"></a>Proprietà

La **classe \_ ShortcutFile Win32** ha queste proprietà.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Diritti di accesso")
</dt> </dl>

Maschera di bit che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file. Per i valori di bit, vedere [**Costanti dei diritti di accesso a file e directory**](../wmisdk/file-and-directory-access-rights-constants.md).

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

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")
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

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")
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

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Metodo di compressione")
</dt> </dl>

Stringa in formato libero che indica l'algoritmo o lo strumento usato per comprimere il file logico. Se lo schema di compressione è sconosciuto o non è descritto, usare "Sconosciuto". Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non descritto, usare "Compressed". Se il file logico non è compresso, usare "Non compresso".

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")
</dt> </dl>

Nome della classe.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Data di creazione")
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

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**\_ FileSystem CIM**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")
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

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**\_ FileSystem CIM**](cim-filesystem.md).**CSName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")
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

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
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

Qualificatori: [**corretto**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Unità")
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

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("eight dot three file name")
</dt> </dl>

Nome file in formato 8.3.

Esempio: "c: \\ progra~1"

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Crittografata**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")
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

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Metodo di crittografia")
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

Qualificatori: [**corretto**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estensione file")
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

Qualificatori: [**corretto**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome file")
</dt> </dl>

Nome file senza l'estensione del nome file.

Esempio: "MyDataFile"

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Dimensione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Dimensioni del file, in byte.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](../wmisdk/creating-a-wmi-script.md)

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Filetype**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tipo di file")
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

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**\_ FileSystem CIM**](cim-filesystem.md).**CreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")
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

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**\_ FileSystem CIM**](cim-filesystem.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")
</dt> </dl>

Nome del file system.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")
</dt> </dl>

Se **True**, il file è nascosto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
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

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")
</dt> </dl>

Numero di "file di apertura" attualmente attivi per il file.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](../wmisdk/creating-a-wmi-script.md)

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")
</dt> </dl>

Data e ora dell'ultimo accesso al file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Ultima modifica")
</dt> </dl>

Data e ora dell'ultima modifica del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")
</dt> </dl>

Stringa del produttore dalla risorsa versione (se presente).

Questa proprietà viene ereditata da [**CIM \_ DataFile.**](cim-datafile.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Chiave**](../wmisdk/key-qualifier.md)
</dt> </dl>

La proprietà Name è una stringa che rappresenta il nome ereditato che funge da chiave di un'istanza di file logico all'interno di un file system. È necessario che siano specificati nomi di percorso completi.

Esempio: C: Windows \\ \\ sistema \\win.ini

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**corretto**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")
</dt> </dl>

Percorso del file, incluse le barre rovesciate iniziali e finali.

Esempio: " \\ windows \\ system \\ "

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Leggibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Leggibile")
</dt> </dl>

Se **True,** il file può essere letto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto . È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "Danneggiato" e "Pred Fail". "Pred Fail" indica che un elemento funziona correttamente, ma prevede un errore , ad esempio un'unità disco rigido abilitata per SMART.

Lo stato non operativo può includere "Error", "Starting", "Stopping" e "Service". Il "servizio" può essere applicato durante il ridimensionamento del mirror del disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degraded** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


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

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File di sistema")
</dt> </dl>

Se **True**, il file è un file di sistema.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| \_ beginthreadex")
</dt> </dl>

Nome dell'oggetto a cui questo è un collegamento.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")
</dt> </dl>

Stringa di versione dalla risorsa versione (se presente).

Questa proprietà viene ereditata da [**CIM \_ DataFile.**](cim-datafile.md)

</dd> <dt>

**Scrivibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Scrivibile")
</dt> </dl>

Se **True,** il file può essere scritto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ ShortcutFile Win32** deriva da [**CIM \_ DataFile**](cim-datafile.md).

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

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
