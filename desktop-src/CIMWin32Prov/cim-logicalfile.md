---
description: La classe CiM LogicalFile rappresenta una raccolta denominata di dati, che può essere codice eseguibile, che si trova in un file system \_ in un extent di archiviazione.
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: CIM_LogicalFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile
- CIM_LogicalFile.Caption
- CIM_LogicalFile.Description
- CIM_LogicalFile.InstallDate
- CIM_LogicalFile.Status
- CIM_LogicalFile.AccessMask
- CIM_LogicalFile.Archive
- CIM_LogicalFile.Compressed
- CIM_LogicalFile.CompressionMethod
- CIM_LogicalFile.CreationClassName
- CIM_LogicalFile.CreationDate
- CIM_LogicalFile.CSCreationClassName
- CIM_LogicalFile.CSName
- CIM_LogicalFile.Drive
- CIM_LogicalFile.EightDotThreeFileName
- CIM_LogicalFile.Encrypted
- CIM_LogicalFile.EncryptionMethod
- CIM_LogicalFile.Name
- CIM_LogicalFile.Extension
- CIM_LogicalFile.FileName
- CIM_LogicalFile.FileSize
- CIM_LogicalFile.FileType
- CIM_LogicalFile.FSCreationClassName
- CIM_LogicalFile.FSName
- CIM_LogicalFile.Hidden
- CIM_LogicalFile.InUseCount
- CIM_LogicalFile.LastAccessed
- CIM_LogicalFile.LastModified
- CIM_LogicalFile.Path
- CIM_LogicalFile.Readable
- CIM_LogicalFile.System
- CIM_LogicalFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 457bf0e094e4196c2ff60b05581daf5dc6a51349530d3563119962e01c94c40d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548271"
---
# <a name="cim_logicalfile-class"></a>Classe \_ CiM LogicalFile

La **classe \_ CiM LogicalFile** rappresenta una raccolta denominata di dati, che può essere codice eseguibile, che si trova in un file system in un extent di archiviazione.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C559-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Files (CIM)"), AMENDMENT]
class CIM_LogicalFile : CIM_LogicalElement
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
};
```

## <a name="members"></a>Members

La **classe \_ CiM LogicalFile** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ CiM LogicalFile** include questi metodi.



| Metodo                                                                                             | Descrizione                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autorizzazioni changeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                   |
| [**Comprimere**](compress-method-in-class-cim-logicalfile.md)                                       | Comprime il file logico (o la directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                              |
| [**CompressEx**](compressex-method-in-class-cim-logicalfile.md)                                   | Comprime il file logico (o la directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                              |
| [**Copia**](copy-method-in-class-cim-logicalfile.md)                                               | Copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input. Non implementato da WMI.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-logicalfile.md)                                           | Copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input. Non implementato da WMI.<br/> |
| [**Elimina**](delete-method-in-class-cim-logicalfile.md)                                           | Elimina il file logico (o la directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-logicalfile.md)                                       | Elimina il file logico (o la directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-logicalfile.md)           | Determina se il chiamante dispone delle autorizzazioni aggregate specificate **dall'argomento Permission.** Non implementato da WMI.<br/>                |
| [**Rinominare**](rename-method-in-class-cim-logicalfile.md)                                           | Rinomina il file logico (o la directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md)                             | Ottiene la proprietà del file logico (o directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                    |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-logicalfile.md)                         | Ottiene la proprietà del file logico (o directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                    |
| [**Decomprimere**](uncompress-method-in-class-cim-logicalfile.md)                                   | Decomprime il file logico (o la directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-logicalfile.md)                               | Decomprime il file logico (o la directory) specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                            |



 

### <a name="properties"></a>Proprietà

La **classe \_ CiM LogicalFile** ha queste proprietà.

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

Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file. Questa proprietà viene ereditata da **CIM \_ LogicalFile.** Esempio: "c:"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("eight dot three file name")
</dt> </dl>

Nome file compatibile con DOS. Esempio: "c: \\ progra~1"

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

</dd> <dt>

**Estensione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**corretto**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estensione file")
</dt> </dl>

Estensione del nome file senza il punto precedente (punto). Esempio: "txt", "mof", "mdb"

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

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

Se **True**, il file è nascosto.

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

Numero di "file di apertura" attualmente attivi per il file.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")
</dt> </dl>

Data e ora dell'ultimo accesso al file.

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

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

La proprietà Name è una stringa che rappresenta il nome ereditato che funge da chiave di un'istanza di file logico all'interno di un file system. È necessario che siano specificati nomi di percorso completi. Esempio: C: Windows \\ \\ sistema \\win.ini

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**corretto**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Percorso del file, incluse le barre rovesciate iniziali e finali. Esempio: " \\ windows \\ system \\ "

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

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
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

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File di sistema")
</dt> </dl>

Se **True**, il file è un file di sistema.

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

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ CiM LogicalFile** è derivata da [**CIM \_ LogicalElement.**](cim-logicalelement.md)

WMI non implementa questa classe. Per le classi derivate **da \_ CIM LogicalFile,** vedere [Classi Win32.](win32-provider.md)

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

