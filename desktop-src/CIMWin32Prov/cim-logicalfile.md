---
description: La \_ classe CIM LogicalFile rappresenta una raccolta denominata di dati, che può essere un codice eseguibile, che si trova in un file System in un extent di archiviazione.
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: Classe CIM_LogicalFile
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
ms.openlocfilehash: a06d2abd1c4ad92d751afa6c8aa47c0cfaa8b1f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304545"
---
# <a name="cim_logicalfile-class"></a><span data-ttu-id="55d88-103">CIM \_ LogicalFile (classe)</span><span class="sxs-lookup"><span data-stu-id="55d88-103">CIM\_LogicalFile class</span></span>

<span data-ttu-id="55d88-104">La classe **CIM \_ LogicalFile** rappresenta una raccolta denominata di dati, che può essere un codice eseguibile, che si trova in un file System in un extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="55d88-104">The **CIM\_LogicalFile** class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55d88-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55d88-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="55d88-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55d88-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="55d88-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="55d88-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="55d88-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d88-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55d88-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="55d88-110">Members</span><span class="sxs-lookup"><span data-stu-id="55d88-110">Members</span></span>

<span data-ttu-id="55d88-111">La classe **CIM \_ LogicalFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="55d88-111">The **CIM\_LogicalFile** class has these types of members:</span></span>

-   [<span data-ttu-id="55d88-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="55d88-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="55d88-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55d88-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55d88-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="55d88-114">Methods</span></span>

<span data-ttu-id="55d88-115">La classe **CIM \_ LogicalFile** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="55d88-115">The **CIM\_LogicalFile** class has these methods.</span></span>



| <span data-ttu-id="55d88-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="55d88-116">Method</span></span>                                                                                             | <span data-ttu-id="55d88-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55d88-117">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55d88-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="55d88-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | <span data-ttu-id="55d88-119">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="55d88-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="55d88-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="55d88-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | <span data-ttu-id="55d88-122">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="55d88-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="55d88-124">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="55d88-124">**Compress**</span></span>](compress-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="55d88-125">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="55d88-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="55d88-127">**CompressEx**</span></span>](compressex-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="55d88-128">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-129">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="55d88-130">**Copia**</span><span class="sxs-lookup"><span data-stu-id="55d88-130">**Copy**</span></span>](copy-method-in-class-cim-logicalfile.md)                                               | <span data-ttu-id="55d88-131">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="55d88-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="55d88-132">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="55d88-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="55d88-133">**CopyEx**</span></span>](copyex-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="55d88-134">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="55d88-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="55d88-135">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="55d88-136">**Delete**</span><span class="sxs-lookup"><span data-stu-id="55d88-136">**Delete**</span></span>](delete-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="55d88-137">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-138">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="55d88-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="55d88-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="55d88-140">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-141">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="55d88-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="55d88-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)           | <span data-ttu-id="55d88-143">Determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di **autorizzazione** .</span><span class="sxs-lookup"><span data-stu-id="55d88-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="55d88-144">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="55d88-145">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="55d88-145">**Rename**</span></span>](rename-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="55d88-146">Rinomina il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-147">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="55d88-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="55d88-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-logicalfile.md)                             | <span data-ttu-id="55d88-149">Ottiene la proprietà del file o della directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-149">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-150">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-150">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="55d88-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="55d88-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)                         | <span data-ttu-id="55d88-152">Ottiene la proprietà del file o della directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-152">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-153">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-153">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="55d88-154">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="55d88-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="55d88-155">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-156">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="55d88-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="55d88-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-logicalfile.md)                               | <span data-ttu-id="55d88-158">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55d88-159">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="55d88-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="55d88-160">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55d88-160">Properties</span></span>

<span data-ttu-id="55d88-161">La classe **CIM \_ LogicalFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="55d88-161">The **CIM\_LogicalFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55d88-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="55d88-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55d88-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-165">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("diritti di accesso")</span><span class="sxs-lookup"><span data-stu-id="55d88-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-166">Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file.</span><span class="sxs-lookup"><span data-stu-id="55d88-166">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="55d88-167">Per i valori di bit, vedere [**costanti di diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="55d88-167">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="55d88-168">Nei volumi FAT viene invece restituito il valore di **\_ accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="55d88-169">**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="55d88-169">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="55d88-170">**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="55d88-170">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="55d88-171">**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)</span><span class="sxs-lookup"><span data-stu-id="55d88-171">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="55d88-172">**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="55d88-172">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="55d88-173">**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="55d88-173">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="55d88-174">**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="55d88-174">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="55d88-175">**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="55d88-175">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="55d88-176">**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="55d88-176">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="55d88-177">**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="55d88-177">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="55d88-178">**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="55d88-178">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="55d88-179">**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="55d88-179">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="55d88-180">**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="55d88-180">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="55d88-181">**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="55d88-181">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="55d88-182">**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="55d88-182">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55d88-183">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="55d88-183">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d88-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-186">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve essere archiviato")</span><span class="sxs-lookup"><span data-stu-id="55d88-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-187">Se **true**, il file deve essere archiviato.</span><span class="sxs-lookup"><span data-stu-id="55d88-187">If **True**, the file should be archived.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-188">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="55d88-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-191">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="55d88-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-192">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-192">A short textual description of the object.</span></span>

<span data-ttu-id="55d88-193">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55d88-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55d88-194">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="55d88-194">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-195">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d88-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-197">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compresso")</span><span class="sxs-lookup"><span data-stu-id="55d88-197">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-198">Se **true**, il file è compresso.</span><span class="sxs-lookup"><span data-stu-id="55d88-198">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="55d88-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-202">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di compressione")</span><span class="sxs-lookup"><span data-stu-id="55d88-202">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-203">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="55d88-203">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="55d88-204">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="55d88-204">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="55d88-205">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="55d88-205">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="55d88-206">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="55d88-206">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="55d88-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="55d88-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-210">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="55d88-210">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-211">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="55d88-211">Name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-212">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="55d88-212">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-213">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55d88-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-215">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data creazione")</span><span class="sxs-lookup"><span data-stu-id="55d88-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-216">Data e ora di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="55d88-216">Date and time of the file's creation.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-217">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="55d88-217">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-220">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="55d88-220">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-221">Classe del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="55d88-221">Class of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-222">**CSName**</span><span class="sxs-lookup"><span data-stu-id="55d88-222">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-225">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="55d88-225">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-226">Nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="55d88-226">Name of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-227">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="55d88-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-230">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="55d88-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-231">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-231">A textual description of the object.</span></span>

<span data-ttu-id="55d88-232">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55d88-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55d88-233">**Unità**</span><span class="sxs-lookup"><span data-stu-id="55d88-233">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-236">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("unità")</span><span class="sxs-lookup"><span data-stu-id="55d88-236">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-237">Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file.</span><span class="sxs-lookup"><span data-stu-id="55d88-237">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="55d88-238">Questa proprietà viene ereditata da **CIM \_ LogicalFile**. Esempio: "c:"</span><span class="sxs-lookup"><span data-stu-id="55d88-238">This property is inherited from **CIM\_LogicalFile**.Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="55d88-239">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="55d88-239">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-242">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("otto punto tre nome file")</span><span class="sxs-lookup"><span data-stu-id="55d88-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-243">Nome file compatibile con DOS.</span><span class="sxs-lookup"><span data-stu-id="55d88-243">DOS-compatible file name.</span></span> <span data-ttu-id="55d88-244">Esempio: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="55d88-244">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="55d88-245">**Crittografata**</span><span class="sxs-lookup"><span data-stu-id="55d88-245">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-246">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d88-246">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-248">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="55d88-248">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-249">Se **true**, il file è crittografato.</span><span class="sxs-lookup"><span data-stu-id="55d88-249">If **True**, the file is encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-250">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="55d88-250">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-253">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di crittografia")</span><span class="sxs-lookup"><span data-stu-id="55d88-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-254">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="55d88-254">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="55d88-255">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="55d88-255">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="55d88-256">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="55d88-256">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="55d88-257">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="55d88-257">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="55d88-258">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="55d88-258">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-259">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-261">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estensione di file")</span><span class="sxs-lookup"><span data-stu-id="55d88-261">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-262">Estensione del nome file senza il periodo precedente (punto).</span><span class="sxs-lookup"><span data-stu-id="55d88-262">File name extension without the preceding period (dot).</span></span> <span data-ttu-id="55d88-263">Esempio: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="55d88-263">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="55d88-264">**FileName**</span><span class="sxs-lookup"><span data-stu-id="55d88-264">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-265">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-267">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")</span><span class="sxs-lookup"><span data-stu-id="55d88-267">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-268">Nome file senza l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="55d88-268">File name without the file name extension.</span></span> <span data-ttu-id="55d88-269">Esempio: "DataFile"</span><span class="sxs-lookup"><span data-stu-id="55d88-269">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="55d88-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="55d88-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-271">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55d88-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-273">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="55d88-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-274">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="55d88-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="55d88-275">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55d88-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="55d88-276">**FileType**</span><span class="sxs-lookup"><span data-stu-id="55d88-276">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-277">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-279">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di file")</span><span class="sxs-lookup"><span data-stu-id="55d88-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-280">Descrittore che rappresenta il tipo di file indicato dalla proprietà di **estensione** .</span><span class="sxs-lookup"><span data-stu-id="55d88-280">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="55d88-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-284">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe file System ")</span><span class="sxs-lookup"><span data-stu-id="55d88-284">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-285">Classe del file system.</span><span class="sxs-lookup"><span data-stu-id="55d88-285">Class of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-286">**FSName**</span><span class="sxs-lookup"><span data-stu-id="55d88-286">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-287">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-289">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome file System ")</span><span class="sxs-lookup"><span data-stu-id="55d88-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-290">Nome del file system.</span><span class="sxs-lookup"><span data-stu-id="55d88-290">Name of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-291">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="55d88-291">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-292">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d88-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-294">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("hidden")</span><span class="sxs-lookup"><span data-stu-id="55d88-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-295">Se **true**, il file è nascosto.</span><span class="sxs-lookup"><span data-stu-id="55d88-295">If **True**, the file is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-296">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="55d88-296">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-297">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55d88-297">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-299">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="55d88-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-300">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="55d88-300">Indicates when the object was installed.</span></span> <span data-ttu-id="55d88-301">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="55d88-301">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="55d88-302">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55d88-302">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55d88-303">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="55d88-303">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-304">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55d88-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-306">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggio aperto file corrente")</span><span class="sxs-lookup"><span data-stu-id="55d88-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-307">Numero di "file aperti" attualmente attivi sul file.</span><span class="sxs-lookup"><span data-stu-id="55d88-307">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="55d88-308">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55d88-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="55d88-309">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="55d88-309">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-310">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55d88-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-312">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ultimo accesso")</span><span class="sxs-lookup"><span data-stu-id="55d88-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-313">Data e ora dell'ultimo accesso al file.</span><span class="sxs-lookup"><span data-stu-id="55d88-313">Date and time the file was last accessed.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-314">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="55d88-314">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-315">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55d88-315">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-317">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultima modifica")</span><span class="sxs-lookup"><span data-stu-id="55d88-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-318">Data e ora dell'Ultima modifica apportata al file.</span><span class="sxs-lookup"><span data-stu-id="55d88-318">Date and time the file was last modified.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-319">**Nome**</span><span class="sxs-lookup"><span data-stu-id="55d88-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-322">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55d88-322">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="55d88-323">La proprietà Name è una stringa che rappresenta il nome ereditato che funge da chiave di un'istanza di file logico all'interno di una file system.</span><span class="sxs-lookup"><span data-stu-id="55d88-323">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="55d88-324">È necessario specificare i nomi dei percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="55d88-324">Full path names should be provided.</span></span> <span data-ttu-id="55d88-325">Esempio: C: \\ \\ sistema Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="55d88-325">Example: C:\\Windows\\system\\win.ini</span></span>

</dd> <dt>

<span data-ttu-id="55d88-326">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="55d88-326">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-327">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-329">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="55d88-329">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-330">Percorso del file, incluse le barre rovesciate iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="55d88-330">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="55d88-331">Esempio: " \\ \\ sistema Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="55d88-331">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="55d88-332">**Leggibile**</span><span class="sxs-lookup"><span data-stu-id="55d88-332">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-333">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d88-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-335">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("leggibile")</span><span class="sxs-lookup"><span data-stu-id="55d88-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-336">Se **true**, il file può essere letto.</span><span class="sxs-lookup"><span data-stu-id="55d88-336">If **True**, the file can be read.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-337">**Status**</span><span class="sxs-lookup"><span data-stu-id="55d88-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-338">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55d88-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-340">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="55d88-340">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-341">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55d88-341">String that indicates the current status of the object.</span></span> <span data-ttu-id="55d88-342">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="55d88-342">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="55d88-343">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="55d88-343">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="55d88-344">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="55d88-344">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="55d88-345">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="55d88-345">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="55d88-346">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="55d88-346">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="55d88-347">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="55d88-347">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="55d88-348">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55d88-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="55d88-349">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="55d88-349">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="55d88-350">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="55d88-350">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="55d88-351">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="55d88-351">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="55d88-352">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="55d88-352">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55d88-353">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="55d88-353">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="55d88-354">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="55d88-354">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="55d88-355">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="55d88-355">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="55d88-356">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="55d88-356">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="55d88-357">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="55d88-357">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="55d88-358">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="55d88-358">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="55d88-359">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="55d88-359">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="55d88-360">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="55d88-360">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="55d88-361">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="55d88-361">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55d88-362">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="55d88-362">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-363">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d88-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-365">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file di sistema")</span><span class="sxs-lookup"><span data-stu-id="55d88-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-366">Se **true**, il file è un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="55d88-366">If **True**, the file is a system file.</span></span>

</dd> <dt>

<span data-ttu-id="55d88-367">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="55d88-367">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55d88-368">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d88-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55d88-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d88-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55d88-370">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("scrivibile")</span><span class="sxs-lookup"><span data-stu-id="55d88-370">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="55d88-371">Se **true**, il file può essere scritto.</span><span class="sxs-lookup"><span data-stu-id="55d88-371">If **True**, the file can be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55d88-372">Commenti</span><span class="sxs-lookup"><span data-stu-id="55d88-372">Remarks</span></span>

<span data-ttu-id="55d88-373">La classe **CIM \_ LogicalFile** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="55d88-373">The **CIM\_LogicalFile** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="55d88-374">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="55d88-374">WMI does not implement this class.</span></span> <span data-ttu-id="55d88-375">Per le classi derivate da **CIM \_ LogicalFile**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="55d88-375">For classes derived from **CIM\_LogicalFile**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="55d88-376">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="55d88-376">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55d88-377">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="55d88-377">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55d88-378">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55d88-378">Requirements</span></span>



| <span data-ttu-id="55d88-379">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d88-379">Requirement</span></span> | <span data-ttu-id="55d88-380">Valore</span><span class="sxs-lookup"><span data-stu-id="55d88-380">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55d88-381">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d88-381">Minimum supported client</span></span><br/> | <span data-ttu-id="55d88-382">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55d88-382">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55d88-383">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d88-383">Minimum supported server</span></span><br/> | <span data-ttu-id="55d88-384">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55d88-384">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55d88-385">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="55d88-385">Namespace</span></span><br/>                | <span data-ttu-id="55d88-386">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="55d88-386">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55d88-387">MOF</span><span class="sxs-lookup"><span data-stu-id="55d88-387">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55d88-388"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55d88-388"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55d88-389">DLL</span><span class="sxs-lookup"><span data-stu-id="55d88-389">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55d88-390"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55d88-390"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55d88-391">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55d88-391">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d88-392">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="55d88-392">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

