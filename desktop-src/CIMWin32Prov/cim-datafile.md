---
description: La \_ classe CIM DataFile rappresenta una raccolta denominata di dati o codice eseguibile. Verranno restituite solo le istanze di file nei dischi fissi locali.
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: Classe CIM_DataFile
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
ms.openlocfilehash: 0badba05eafa5cba06e48b8494ca893936af360e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877917"
---
# <a name="cim_datafile-class"></a><span data-ttu-id="06110-104">\_Classe di DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="06110-104">CIM\_DataFile class</span></span>

<span data-ttu-id="06110-105">La classe **CIM \_ DataFile** rappresenta una raccolta denominata di dati o codice eseguibile.</span><span class="sxs-lookup"><span data-stu-id="06110-105">The **CIM\_DataFile** class represents a named collection of data or executable code.</span></span> <span data-ttu-id="06110-106">Verranno restituite solo le istanze di file nei dischi fissi locali.</span><span class="sxs-lookup"><span data-stu-id="06110-106">Only instances of files on local fixed disks will be returned.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06110-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06110-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="06110-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06110-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="06110-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="06110-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="06110-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06110-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06110-111">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="06110-112">Members</span><span class="sxs-lookup"><span data-stu-id="06110-112">Members</span></span>

<span data-ttu-id="06110-113">La classe **CIM \_ DataFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06110-113">The **CIM\_DataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="06110-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="06110-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="06110-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06110-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06110-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="06110-116">Methods</span></span>

<span data-ttu-id="06110-117">La classe **CIM \_ DataFile** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="06110-117">The **CIM\_DataFile** class has these methods.</span></span>



| <span data-ttu-id="06110-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="06110-118">Method</span></span>                                                                                          | <span data-ttu-id="06110-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06110-119">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06110-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="06110-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)     | <span data-ttu-id="06110-121">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="06110-122">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-122">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="06110-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="06110-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md) | <span data-ttu-id="06110-124">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="06110-125">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-125">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="06110-126">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="06110-126">**Compress**</span></span>](compress-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="06110-127">Usa la compressione NTFS per comprimere il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-127">Uses NTFS compression to compress the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="06110-128">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-128">Implemented by WMI.</span></span><br/>                       |
| [<span data-ttu-id="06110-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="06110-129">**CompressEx**</span></span>](compressex-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="06110-130">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="06110-131">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-131">Implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="06110-132">**Copia**</span><span class="sxs-lookup"><span data-stu-id="06110-132">**Copy**</span></span>](copy-method-in-class-cim-datafile.md)                                               | <span data-ttu-id="06110-133">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="06110-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="06110-134">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-134">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="06110-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="06110-135">**CopyEx**</span></span>](copyex-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="06110-136">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="06110-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="06110-137">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-137">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="06110-138">**Delete**</span><span class="sxs-lookup"><span data-stu-id="06110-138">**Delete**</span></span>](delete-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="06110-139">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="06110-140">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-140">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="06110-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="06110-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="06110-142">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="06110-143">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-143">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="06110-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="06110-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-datafile.md)           | <span data-ttu-id="06110-145">Determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di **autorizzazione** .</span><span class="sxs-lookup"><span data-stu-id="06110-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="06110-146">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-146">Implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="06110-147">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="06110-147">**Rename**</span></span>](rename-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="06110-148">Rinomina il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="06110-149">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-149">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="06110-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="06110-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-datafile.md)                             | <span data-ttu-id="06110-151">Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="06110-152">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-152">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="06110-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="06110-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-datafile.md)                         | <span data-ttu-id="06110-154">Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="06110-155">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-155">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="06110-156">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="06110-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="06110-157">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="06110-158">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-158">Implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="06110-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="06110-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-datafile.md)                               | <span data-ttu-id="06110-160">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="06110-161">Implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="06110-161">Implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="06110-162">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06110-162">Properties</span></span>

<span data-ttu-id="06110-163">La classe **CIM \_ DataFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06110-163">The **CIM\_DataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06110-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="06110-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06110-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06110-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-167">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("diritti di accesso")</span><span class="sxs-lookup"><span data-stu-id="06110-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="06110-168">Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file.</span><span class="sxs-lookup"><span data-stu-id="06110-168">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="06110-169">Per i valori di bit, vedere [**costanti di diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="06110-169">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="06110-170">Nei volumi FAT viene invece restituito il valore di **\_ accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-170">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="06110-171">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-171">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="06110-172">**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="06110-172">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="06110-173">**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="06110-173">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="06110-174">**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)</span><span class="sxs-lookup"><span data-stu-id="06110-174">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="06110-175">**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="06110-175">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="06110-176">**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="06110-176">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="06110-177">**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="06110-177">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="06110-178">**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="06110-178">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="06110-179">**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="06110-179">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="06110-180">**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="06110-180">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="06110-181">**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="06110-181">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="06110-182">**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="06110-182">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="06110-183">**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="06110-183">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="06110-184">**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="06110-184">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="06110-185">**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="06110-185">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06110-186">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="06110-186">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-187">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="06110-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06110-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-189">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve essere archiviato")</span><span class="sxs-lookup"><span data-stu-id="06110-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="06110-190">Se **true**, il file deve essere archiviato.</span><span class="sxs-lookup"><span data-stu-id="06110-190">If **True**, the file should be archived.</span></span>

<span data-ttu-id="06110-191">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-191">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-192">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="06110-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-195">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="06110-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="06110-196">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-196">A short textual description of the object.</span></span>

<span data-ttu-id="06110-197">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06110-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-198">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="06110-198">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-199">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="06110-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06110-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-201">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compresso")</span><span class="sxs-lookup"><span data-stu-id="06110-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="06110-202">Se **true**, il file è compresso.</span><span class="sxs-lookup"><span data-stu-id="06110-202">If **True**, the file is compressed.</span></span>

<span data-ttu-id="06110-203">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-203">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-204">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="06110-204">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-207">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di compressione")</span><span class="sxs-lookup"><span data-stu-id="06110-207">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="06110-208">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="06110-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="06110-209">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="06110-209">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="06110-210">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="06110-210">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="06110-211">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="06110-211">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="06110-212">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-213">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06110-213">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-216">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="06110-216">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="06110-217">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="06110-217">Name of the class.</span></span>

<span data-ttu-id="06110-218">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-219">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="06110-219">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-220">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="06110-220">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06110-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-222">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data creazione")</span><span class="sxs-lookup"><span data-stu-id="06110-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="06110-223">Data e ora di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="06110-223">Date and time of the file's creation.</span></span>

<span data-ttu-id="06110-224">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-224">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-225">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06110-225">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-226">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-228">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="06110-228">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="06110-229">Classe del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="06110-229">Class of the computer system.</span></span>

<span data-ttu-id="06110-230">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-230">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-231">**CSName**</span><span class="sxs-lookup"><span data-stu-id="06110-231">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-234">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="06110-234">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="06110-235">Nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="06110-235">Name of the computer system.</span></span>

<span data-ttu-id="06110-236">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-236">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-237">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="06110-237">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-238">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-240">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="06110-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="06110-241">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-241">A textual description of the object.</span></span>

<span data-ttu-id="06110-242">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06110-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-243">**Unità**</span><span class="sxs-lookup"><span data-stu-id="06110-243">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-246">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("unità")</span><span class="sxs-lookup"><span data-stu-id="06110-246">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="06110-247">Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file.</span><span class="sxs-lookup"><span data-stu-id="06110-247">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="06110-248">Esempio: "c:"</span><span class="sxs-lookup"><span data-stu-id="06110-248">Example: "c:"</span></span>

<span data-ttu-id="06110-249">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-249">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-250">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="06110-250">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-253">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("otto punto tre nome file")</span><span class="sxs-lookup"><span data-stu-id="06110-253">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="06110-254">Nome file compatibile con DOS.</span><span class="sxs-lookup"><span data-stu-id="06110-254">DOS-compatible file name.</span></span>

<span data-ttu-id="06110-255">Esempio: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="06110-255">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="06110-256">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-256">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-257">**Crittografata**</span><span class="sxs-lookup"><span data-stu-id="06110-257">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-258">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="06110-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06110-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-260">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="06110-260">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="06110-261">Se **true**, il file è crittografato.</span><span class="sxs-lookup"><span data-stu-id="06110-261">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="06110-262">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-263">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="06110-263">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-266">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di crittografia")</span><span class="sxs-lookup"><span data-stu-id="06110-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="06110-267">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="06110-267">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="06110-268">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="06110-268">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="06110-269">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="06110-269">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="06110-270">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="06110-270">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="06110-271">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-271">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-272">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="06110-272">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-275">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estensione di file")</span><span class="sxs-lookup"><span data-stu-id="06110-275">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="06110-276">Estensione del nome file senza il periodo precedente (punto).</span><span class="sxs-lookup"><span data-stu-id="06110-276">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="06110-277">Esempio: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="06110-277">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="06110-278">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-278">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-279">**FileName**</span><span class="sxs-lookup"><span data-stu-id="06110-279">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-282">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")</span><span class="sxs-lookup"><span data-stu-id="06110-282">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="06110-283">Nome file senza l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="06110-283">File name without the file name extension.</span></span> <span data-ttu-id="06110-284">Esempio: "DataFile"</span><span class="sxs-lookup"><span data-stu-id="06110-284">Example: "MyDataFile"</span></span>

<span data-ttu-id="06110-285">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-285">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-286">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="06110-286">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-287">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06110-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06110-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-289">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="06110-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="06110-290">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="06110-290">Size of the file, in bytes.</span></span>

<span data-ttu-id="06110-291">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="06110-291">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="06110-292">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-293">**FileType**</span><span class="sxs-lookup"><span data-stu-id="06110-293">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-296">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di file")</span><span class="sxs-lookup"><span data-stu-id="06110-296">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="06110-297">Descrittore che rappresenta il tipo di file indicato dalla proprietà di **estensione** .</span><span class="sxs-lookup"><span data-stu-id="06110-297">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="06110-298">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-299">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06110-299">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-302">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe file System ")</span><span class="sxs-lookup"><span data-stu-id="06110-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="06110-303">Classe del file system.</span><span class="sxs-lookup"><span data-stu-id="06110-303">Class of the file system.</span></span>

<span data-ttu-id="06110-304">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-304">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-305">**FSName**</span><span class="sxs-lookup"><span data-stu-id="06110-305">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-308">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome file System ")</span><span class="sxs-lookup"><span data-stu-id="06110-308">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="06110-309">Nome del file system.</span><span class="sxs-lookup"><span data-stu-id="06110-309">Name of the file system.</span></span>

<span data-ttu-id="06110-310">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-311">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="06110-311">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-312">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="06110-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06110-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-314">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("hidden")</span><span class="sxs-lookup"><span data-stu-id="06110-314">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="06110-315">Se **true**, il file è nascosto.</span><span class="sxs-lookup"><span data-stu-id="06110-315">If **True**, the file is hidden.</span></span>

<span data-ttu-id="06110-316">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-316">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06110-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-318">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="06110-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06110-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-320">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="06110-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="06110-321">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="06110-321">Indicates when the object was installed.</span></span> <span data-ttu-id="06110-322">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="06110-322">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="06110-323">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06110-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-324">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="06110-324">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-325">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06110-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06110-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-327">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggio aperto file corrente")</span><span class="sxs-lookup"><span data-stu-id="06110-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="06110-328">Numero di "file aperti" attualmente attivi sul file.</span><span class="sxs-lookup"><span data-stu-id="06110-328">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="06110-329">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="06110-329">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="06110-330">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-331">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="06110-331">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-332">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="06110-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06110-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-334">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ultimo accesso")</span><span class="sxs-lookup"><span data-stu-id="06110-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="06110-335">Data e ora dell'ultimo accesso al file.</span><span class="sxs-lookup"><span data-stu-id="06110-335">Date and time the file was last accessed.</span></span>

<span data-ttu-id="06110-336">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-337">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="06110-337">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-338">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="06110-338">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06110-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-340">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultima modifica")</span><span class="sxs-lookup"><span data-stu-id="06110-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="06110-341">Data e ora dell'Ultima modifica apportata al file.</span><span class="sxs-lookup"><span data-stu-id="06110-341">Date and time the file was last modified.</span></span>

<span data-ttu-id="06110-342">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-342">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-343">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="06110-343">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-344">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-346">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("produttore")</span><span class="sxs-lookup"><span data-stu-id="06110-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="06110-347">Stringa del produttore dalla risorsa della versione (se presente).</span><span class="sxs-lookup"><span data-stu-id="06110-347">Manufacturer string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="06110-348">**Nome**</span><span class="sxs-lookup"><span data-stu-id="06110-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-351">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="06110-351">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="06110-352">La proprietà Name è una stringa che rappresenta il nome ereditato che funge da chiave di un'istanza di file logico all'interno di una file system.</span><span class="sxs-lookup"><span data-stu-id="06110-352">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="06110-353">È necessario specificare i nomi dei percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="06110-353">Full path names should be provided.</span></span>

<span data-ttu-id="06110-354">Esempio: C: \\ \\ sistema Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="06110-354">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="06110-355">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-355">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-356">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="06110-356">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-357">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-359">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="06110-359">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="06110-360">Percorso del file, incluse le barre rovesciate iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="06110-360">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="06110-361">Esempio: " \\ \\ sistema Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="06110-361">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="06110-362">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-362">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-363">**Leggibile**</span><span class="sxs-lookup"><span data-stu-id="06110-363">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-364">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="06110-364">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06110-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-366">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("leggibile")</span><span class="sxs-lookup"><span data-stu-id="06110-366">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="06110-367">Se **true**, il file può essere letto.</span><span class="sxs-lookup"><span data-stu-id="06110-367">If **True**, the file can be read.</span></span>

<span data-ttu-id="06110-368">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-368">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-369">**Status**</span><span class="sxs-lookup"><span data-stu-id="06110-369">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-370">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-372">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="06110-372">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="06110-373">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06110-373">String that indicates the current status of the object.</span></span> <span data-ttu-id="06110-374">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="06110-374">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="06110-375">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="06110-375">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="06110-376">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="06110-376">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="06110-377">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="06110-377">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="06110-378">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="06110-378">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="06110-379">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="06110-379">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="06110-380">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06110-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="06110-381">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="06110-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="06110-382">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="06110-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="06110-383">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="06110-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="06110-384">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="06110-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06110-385">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="06110-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="06110-386">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="06110-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="06110-387">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="06110-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="06110-388">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="06110-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="06110-389">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="06110-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="06110-390">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="06110-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="06110-391">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="06110-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="06110-392">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="06110-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="06110-393">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="06110-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06110-394">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="06110-394">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-395">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="06110-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06110-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-397">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file di sistema")</span><span class="sxs-lookup"><span data-stu-id="06110-397">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="06110-398">Se **true**, il file è un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="06110-398">If **True**, the file is a system file.</span></span>

<span data-ttu-id="06110-399">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="06110-400">**Versione**</span><span class="sxs-lookup"><span data-stu-id="06110-400">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-401">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06110-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06110-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-403">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span><span class="sxs-lookup"><span data-stu-id="06110-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="06110-404">Stringa di versione dalla risorsa della versione (se presente).</span><span class="sxs-lookup"><span data-stu-id="06110-404">Version string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="06110-405">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="06110-405">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06110-406">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="06110-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06110-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06110-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06110-408">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("scrivibile")</span><span class="sxs-lookup"><span data-stu-id="06110-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="06110-409">Se **true**, il file può essere scritto.</span><span class="sxs-lookup"><span data-stu-id="06110-409">If **True**, the file can be written.</span></span>

<span data-ttu-id="06110-410">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06110-411">Commenti</span><span class="sxs-lookup"><span data-stu-id="06110-411">Remarks</span></span>

<span data-ttu-id="06110-412">La classe **CIM \_ DataFile** è derivata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="06110-412">The **CIM\_DataFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="06110-413">WMI implementa la classe di **\_ DataFile CIM** e tutti i relativi metodi.</span><span class="sxs-lookup"><span data-stu-id="06110-413">WMI implements the **CIM\_DataFile** class and all of its methods.</span></span> <span data-ttu-id="06110-414">La classe **CIM \_ DataFile** è una classe dinamica.</span><span class="sxs-lookup"><span data-stu-id="06110-414">The **CIM\_DataFile** class is a dynamic class.</span></span>

<span data-ttu-id="06110-415">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="06110-415">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06110-416">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="06110-416">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="06110-417">Per motivi di sicurezza, WMI non supporta direttamente la chiamata a un computer remoto e indica a tale computer di copiare i file in se stesso.</span><span class="sxs-lookup"><span data-stu-id="06110-417">Due to security purposes, WMI does not directly support calling a remote computer and instructing it to copy files to itself.</span></span> <span data-ttu-id="06110-418">Tuttavia, è possibile utilizzare il linguaggio di programmazione pertinente per chiamare FTP o RoboCopy, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="06110-418">However, you can use the relevant programming language to call FTP or RoboCopy, for example.</span></span>

## <a name="examples"></a><span data-ttu-id="06110-419">Esempio</span><span class="sxs-lookup"><span data-stu-id="06110-419">Examples</span></span>

<span data-ttu-id="06110-420">Il seguente [esempio di codice](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) di Scripting Center USA una classe di file di dati **CIM \_** come parte di un'applicazione più grande per generare report dell'ambiente Exchange usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06110-420">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) uses a **CIM\_DataFile** class as part of a larger application to Generate exchange environment reports using Powershell.</span></span>

<span data-ttu-id="06110-421">L'esempio di codice per [trovare i file con WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) nella raccolta TechNet usa un file di dati **CIM \_** per cercare uno o più file in più computer.</span><span class="sxs-lookup"><span data-stu-id="06110-421">The [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) code sample in TechNet Gallery uses a **CIM\_DataFile** to search for one or more files across multiple computers.</span></span>

<span data-ttu-id="06110-422">Nell'esempio di codice VBS seguente viene descritto come eseguire una ricerca con caratteri jolly standard in un file di file.</span><span class="sxs-lookup"><span data-stu-id="06110-422">The following VBS code sample describes how to perform a standard wildcard search on a datafile.</span></span> <span data-ttu-id="06110-423">Si noti che i delimitatori della barra rovesciata devono essere preceduti da un'altra barra rovesciata ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="06110-423">Note that the backslash delimiters must be escaped with another backslash (\\\\).</span></span> <span data-ttu-id="06110-424">Inoltre, quando si usa "**CIM \_ DataFile**.**FileName**"nella clausola WHERE il processo Wmiprvse analizzerà tutte le directory in qualsiasi dispositivo di archiviazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="06110-424">Also, when using "**CIM\_DataFile**.**FileName**" in the WHERE clause, the WMIPRVSE process will scan all directories on any available storage device.</span></span> <span data-ttu-id="06110-425">Questa operazione può richiedere del tempo, soprattutto se è stato eseguito il mapping delle condivisioni remote e possono essere generati avvisi antivirus.</span><span class="sxs-lookup"><span data-stu-id="06110-425">This may take some time, especially if you have mapped remote shares, and can trigger antivirus warnings.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



<span data-ttu-id="06110-426">Il frammento di codice seguente limita l'intervallo di ricerca a un'unità, un percorso e un'estensione di file specifici.</span><span class="sxs-lookup"><span data-stu-id="06110-426">The following snippet limits the search range to a specific drive, path, and file extension.</span></span>


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



<span data-ttu-id="06110-427">Nell'esempio di codice PowerShell seguente viene recuperato un valore di attributo singolo.</span><span class="sxs-lookup"><span data-stu-id="06110-427">The following PowerShell code sample retrieves a single attribute value.</span></span>


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## <a name="requirements"></a><span data-ttu-id="06110-428">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06110-428">Requirements</span></span>



| <span data-ttu-id="06110-429">Requisito</span><span class="sxs-lookup"><span data-stu-id="06110-429">Requirement</span></span> | <span data-ttu-id="06110-430">Valore</span><span class="sxs-lookup"><span data-stu-id="06110-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06110-431">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06110-431">Minimum supported client</span></span><br/> | <span data-ttu-id="06110-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06110-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06110-433">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06110-433">Minimum supported server</span></span><br/> | <span data-ttu-id="06110-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06110-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06110-435">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06110-435">Namespace</span></span><br/>                | <span data-ttu-id="06110-436">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="06110-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06110-437">MOF</span><span class="sxs-lookup"><span data-stu-id="06110-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06110-438"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06110-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06110-439">DLL</span><span class="sxs-lookup"><span data-stu-id="06110-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06110-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06110-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06110-441">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06110-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06110-442">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="06110-442">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="06110-443">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="06110-443">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="06110-444">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="06110-444">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

