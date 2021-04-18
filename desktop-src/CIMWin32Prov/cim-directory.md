---
description: La \_ classe CIM directory rappresenta un tipo di file che raggruppa logicamente i file di dati che contiene e fornisce informazioni sul percorso per i file raggruppati.
ms.assetid: a9594f53-08f0-4a47-9edc-51686c80c5ea
ms.tgt_platform: multiple
title: Classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory
- CIM_Directory.AccessMask
- CIM_Directory.Archive
- CIM_Directory.Caption
- CIM_Directory.Compressed
- CIM_Directory.CompressionMethod
- CIM_Directory.CreationClassName
- CIM_Directory.CreationDate
- CIM_Directory.CSCreationClassName
- CIM_Directory.CSName
- CIM_Directory.Description
- CIM_Directory.Drive
- CIM_Directory.EightDotThreeFileName
- CIM_Directory.Encrypted
- CIM_Directory.EncryptionMethod
- CIM_Directory.Extension
- CIM_Directory.FileName
- CIM_Directory.FileSize
- CIM_Directory.FileType
- CIM_Directory.FSCreationClassName
- CIM_Directory.FSName
- CIM_Directory.Hidden
- CIM_Directory.InstallDate
- CIM_Directory.InUseCount
- CIM_Directory.LastAccessed
- CIM_Directory.LastModified
- CIM_Directory.Name
- CIM_Directory.Path
- CIM_Directory.Readable
- CIM_Directory.Status
- CIM_Directory.System
- CIM_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cebab65cc067018b3a57aa5f6890fffad1cb4c7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305036"
---
# <a name="cim_directory-class"></a>\_Classe Directory CIM

La classe **CIM \_ directory** rappresenta un tipo di file che raggruppa logicamente i file di dati che contiene e fornisce informazioni sul percorso per i file raggruppati.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C55F-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Directories (CIM)"), AMENDMENT]
class CIM_Directory : CIM_LogicalFile
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
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a>Members

La classe **CIM \_ directory** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ directory** presenta questi metodi.



| Metodo                                                                                           | Descrizione                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md)     | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-directory.md) | Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                   |
| [**Comprimere**](compress-method-in-class-cim-directory.md)                                       | Comprime il file o la directory logica specificata nel percorso dell'oggetto. Non implementato da WMI.<br/>                                              |
| [**CompressEx**](compressex-method-in-class-cim-directory.md)                                   | Comprime il file o la directory logica specificata nel percorso dell'oggetto. Non implementato da WMI.<br/>                                              |
| [**Copia**](copy-method-in-class-cim-directory.md)                                               | Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input. Non implementato da WMI.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-directory.md)                                           | Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input. Non implementato da WMI.<br/> |
| [**Delete**](delete-method-in-class-cim-directory.md)                                           | Elimina il file o la directory logica specificata nel percorso dell'oggetto. Non implementato da WMI.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-directory.md)                                       | Elimina il file o la directory logica specificata nel percorso dell'oggetto. Non implementato da WMI.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-directory.md)           | Determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di **autorizzazione** . Non implementato da WMI.<br/>                |
| [**Rinominare**](rename-method-in-class-cim-directory.md)                                           | Rinomina il file logico o la directory specificata nel percorso dell'oggetto. Non implementato da WMI.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md)                             | Ottiene la proprietà del file logico specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md)                         | Ottiene la proprietà del file logico specificato nel percorso dell'oggetto. Non implementato da WMI.<br/>                                                   |
| [**Decomprimere**](uncompress-method-in-class-cim-directory.md)                                   | Decomprime il file o la directory logica specificata nel percorso dell'oggetto. Non implementato da WMI.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-directory.md)                               | Decomprime il file o la directory logica specificata nel percorso dell'oggetto. Non implementato da WMI.<br/>                                            |



 

### <a name="properties"></a>Proprietà

La classe di **\_ directory CIM** dispone di queste proprietà.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("diritti di accesso")
</dt> </dl>

Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sulla directory. Per i valori, vedere [**costanti di diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

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

Breve descrizione testuale dell'oggetto.

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

Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico. Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown". Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso". Se il file logico non è compresso, utilizzare "non compresso".

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

Nome della classe.

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

Data e ora di creazione del file.

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

Nome del sistema del computer.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

**Unità**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("unità")
</dt> </dl>

Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file. Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Nome file compatibile con DOS. Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico. Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown". Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted". Se il file logico non è crittografato, utilizzare "non crittografato".

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

Estensione del nome file senza il periodo precedente (punto).

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Esempio: "txt", "MOF", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")
</dt> </dl>

Nome file senza l'estensione del nome file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

Esempio: "DataFile"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Dimensioni del file, in byte.

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

Descrittore che rappresenta il tipo di file (indicato dalla proprietà **Extension** ).

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

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

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

Data e ora dell'ultimo accesso al file.

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

Data e ora dell'Ultima modifica apportata al file.

Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome ereditato che funge da chiave di un'istanza di file logica all'interno di un file system (fornire nomi di percorso completi).

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

Percorso del file, incluse le barre rovesciate iniziali e finali. Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Se **true**, il file può essere letto.

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

Stringa che indica lo stato corrente dell'oggetto.

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

La classe **CIM \_ directory** è derivata da [**CIM \_ LogicalFile**](cim-logicalfile.md).

WMI non implementa questa classe. Per ulteriori informazioni sulle classi derivate dalla **\_ directory CIM**, vedere [classi Win32](win32-provider.md).

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

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

