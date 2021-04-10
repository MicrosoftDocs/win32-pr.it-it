---
description: Il \_ Codecfile Win32&\# 32; Classe WMI che rappresenta il codec audio o video installato nel computer.
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Classe Win32_CodecFile
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
ms.openlocfilehash: fc7a6073ab2841fde4492cd59ae1696aeca9f6a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127350"
---
# <a name="win32_codecfile-class"></a>\_Classe codecfile Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ codecfile Win32** rappresenta il codec audio o video installato nel computer. I codec convertono un tipo di formato multimediale in un altro, in genere un formato compresso in un formato non compresso. Il nome "codec" deriva da una combinazione di comprimere e decomprimere. Un codec, ad esempio, può convertire un formato compresso, ad esempio MS-ADPCM, in un formato non compresso, ad esempio PCM, che può essere riprodotto direttamente dalla maggior parte dell'hardware audio.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

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

La classe **Win32 \_ codecfile** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ codecfile** presenta questi metodi.



| Metodo                                                                                             | Descrizione                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-codecfile.md)     | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                         |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                         |
| [**Comprimere**](compress-method-in-class-win32-codecfile.md)                                       | Comprime il file o la directory logica specificata nel percorso dell'oggetto.<br/>                                                                                                                                    |
| [**CompressEx**](compressex-method-in-class-win32-codecfile.md)                                   | Comprime il file o la directory logica specificata nel percorso dell'oggetto.<br/>                                                                                                                                    |
| [**Copia**](copy-method-in-class-win32-codecfile.md)                                               | Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.<br/>                                                                                         |
| [**CopyEx**](copyex-method-in-class-win32-codecfile.md)                                           | Metodo della classe che copia il file o la directory logica specificata nel percorso dell'oggetto nella posizione specificata dal parametro FileName.<br/>                                                                    |
| [**Delete**](delete-method-in-class-win32-codecfile.md)                                           | Elimina il file o la directory logica specificata nel percorso dell'oggetto.<br/>                                                                                                                                       |
| [**DeleteEx**](deleteex-method-in-class-win32-codecfile.md)                                       | Elimina il file o la directory logica specificata nel percorso dell'oggetto.<br/>                                                                                                                                       |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-codecfile.md)           | Determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di **autorizzazione** non solo per l'oggetto file, ma sulla condivisione in cui risiede il file o la directory (se si trova in una condivisione).<br/> |
| [**Rinominare**](rename-method-in-class-win32-codecfile.md)                                           | Metodo della classe che rinomina il file logico o la directory specificata nel percorso dell'oggetto.<br/>                                                                                                                     |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-codecfile.md)                             | Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                                         |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-codecfile.md)                         | Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.<br/>                                                                                                                       |
| [**Decomprimere**](uncompress-method-in-class-win32-codecfile.md)                                   | Decomprime il file o la directory logica specificata nel percorso dell'oggetto.<br/>                                                                                                                                  |
| [**UncompressEx**](uncompressex-method-in-class-win32-codecfile.md)                               | Decomprime il file o la directory logica specificata nel percorso dell'oggetto.<br/>                                                                                                                                  |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ codecfile** dispone di queste proprietà.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("diritti di accesso")
</dt> </dl>

Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file di codec. Per i valori di bit, vedere [**costanti di diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> Nei volumi FAT viene invece restituito il valore di **\_ accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.

 

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**File \_ Leggi \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**File \_ Scrivi \_ EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**File \_ Elimina \_ elemento figlio (directory)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**File \_ Leggi \_ attributi** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**File \_ Scrivi \_ attributi** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**Elimina** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**Leggi \_ CONTROLLO** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**Scrivi \_ Applicazione livello dati** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**Scrivi \_ PROPRIETARIO** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**Sincronizza** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Archiviazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve essere archiviato")
</dt> </dl>

Se **true**, il file deve essere archiviato.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compresso")
</dt> </dl>

Se **true**, il file è compresso.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di compressione")
</dt> </dl>

Algoritmo o strumento utilizzato per comprimere il file logico. Se non è possibile (o non si desidera) descrivere lo schema di compressione (probabilmente perché non è noto), utilizzare le parole seguenti: "Unknown" per indicare che non è noto se il file logico è compresso o meno. "Compresso" per indicare che il file è compresso, ma lo schema di compressione non è noto o non è stato divulgato; e "non compressi" per indicare che il file logico non è compresso.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza. Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data creazione")
</dt> </dl>

Data di creazione del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema computer ")
</dt> </dl>

Classe del sistema del computer.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema computer ")
</dt> </dl>

Stringa che rappresenta il nome del sistema del computer.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (descrizione), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ MediaResources \\ \\ ICM \| Description")
</dt> </dl>

Nome completo del driver del codec. Questa stringa deve essere visualizzata in spazi di grandi dimensioni (descrittivi).

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Esempio: "convertitore Microsoft PCM"

</dd> <dt>

**Unità**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("unità")
</dt> </dl>

Lettera di unità (inclusi i due punti) del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Esempio: "c:"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("otto punto tre nome file")
</dt> </dl>

Nome file compatibile con DOS per questo file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Esempio: "c: \\ PROGRA ~ 1"

</dd> <dt>

**Crittografata**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")
</dt> </dl>

Se **true**, il file è crittografato.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di crittografia")
</dt> </dl>

Algoritmo o strumento utilizzato per crittografare il file logico. Se non è possibile (o non si desidera) descrivere lo schema di crittografia (ad esempio per motivi di sicurezza), utilizzare le parole seguenti: "Unknown" per indicare che non è noto se il file logico è crittografato o meno. "Encrypted" per indicare che il file è crittografato, ma lo schema di crittografia non è noto o non è stato divulgato; e "non crittografato" per indicare che il file logico non è crittografato.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Estensione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estensione di file")
</dt> </dl>

Estensione del nome file (senza il punto).

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Esempi: "txt", "MOF", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")
</dt> </dl>

Nome (senza estensione) del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Esempio: "Autoexec"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Dimensioni del file (in byte).

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di file")
</dt> </dl>

Tipo di file (indicato dalla proprietà **Extension** ).

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe file System ")
</dt> </dl>

Classe del file system.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome file System ")
</dt> </dl>

Nome del file system.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Gruppo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ drivers. desc")
</dt> </dl>

Codec rappresentato da questa classe.

I valori possibili sono:

<dl> <dd>Audio</dd> <dd>Video</dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

**Audio** ("audio")


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Video** ("video")


</dt> <dd></dd> </dl>

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("hidden")
</dt> </dl>

Se **true**, il file è nascosto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")
</dt> </dl>

L'oggetto è stato installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggio aperto file corrente")
</dt> </dl>

Numero di "file aperti" attualmente attivi sul file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ultimo accesso")
</dt> </dl>

Ultimo accesso al file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultima modifica")
</dt> </dl>

Data dell'Ultima modifica del file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("produttore")
</dt> </dl>

Stringa del produttore dalla risorsa di versione, se presente.

Questa proprietà viene ereditata da file di [**\_ DataFile CIM**](cim-datafile.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome ereditato che funge da chiave di un'istanza di file logica all'interno di una file system. È necessario specificare i nomi dei percorsi completi.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Esempio: "C: \\ Windows \\ System \\win.ini"

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Percorso del file. Sono incluse le barre rovesciate iniziali e finali.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Esempio: " \\ \\ sistema Windows \\ "

</dd> <dt>

**Leggibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("leggibile")
</dt> </dl>

Il file può essere letto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

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

**Sistema**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file di sistema")
</dt> </dl>

Se **true**, il file è un file di sistema.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")
</dt> </dl>

Stringa di versione dalla risorsa di versione, se presente.

Questa proprietà viene ereditata da file di [**\_ DataFile CIM**](cim-datafile.md).

</dd> <dt>

**Scrivibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("scrivibile")
</dt> </dl>

Se **true**, il file può essere scritto.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ codecfile** è derivata da file di [**\_ DataFile CIM**](cim-datafile.md).

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

[**File di \_ DataFile CIM**](cim-datafile.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

