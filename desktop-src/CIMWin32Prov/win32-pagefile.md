---
description: Il \_ paging Win32&\# 32; Classe WMI rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un sistema Win32. Questa classe è stata deprecata.
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb63c4242ae8fa3cca5133a25d2742d07210ca1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305156"
---
# <a name="win32_pagefile-class"></a><span data-ttu-id="70a3e-104">\_Classe pagefile Win32</span><span class="sxs-lookup"><span data-stu-id="70a3e-104">Win32\_PageFile class</span></span>

<span data-ttu-id="70a3e-105">La [classe WMI](../wmisdk/retrieving-a-class.md) del file di **\_ paging Win32** rappresenta il file utilizzato per gestire lo scambio di file di memoria virtuale in un sistema Win32.</span><span class="sxs-lookup"><span data-stu-id="70a3e-105">The **Win32\_PageFile** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="70a3e-106">Questa classe è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="70a3e-106">This class has been deprecated.</span></span>

<span data-ttu-id="70a3e-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="70a3e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="70a3e-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="70a3e-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a3e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70a3e-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
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
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="70a3e-110">Members</span><span class="sxs-lookup"><span data-stu-id="70a3e-110">Members</span></span>

<span data-ttu-id="70a3e-111">La classe del **\_ pagefile Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="70a3e-111">The **Win32\_PageFile** class has these types of members:</span></span>

-   [<span data-ttu-id="70a3e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="70a3e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="70a3e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="70a3e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70a3e-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="70a3e-114">Methods</span></span>

<span data-ttu-id="70a3e-115">La classe del **\_ pagefile Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="70a3e-115">The **Win32\_PageFile** class has these methods.</span></span>



| <span data-ttu-id="70a3e-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="70a3e-116">Method</span></span>                                                                                            | <span data-ttu-id="70a3e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70a3e-117">Description</span></span>                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70a3e-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="70a3e-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-pagefile.md)     | <span data-ttu-id="70a3e-119">Metodo della classe che modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="70a3e-120">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="70a3e-120">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | <span data-ttu-id="70a3e-121">Metodo della classe che modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-121">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="70a3e-122">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="70a3e-122">**Compress**</span></span>](compress-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="70a3e-123">Metodo della classe che comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="70a3e-124">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="70a3e-124">**CompressEx**</span></span>](compressex-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="70a3e-125">Metodo della classe che comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-125">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="70a3e-126">**Copia**</span><span class="sxs-lookup"><span data-stu-id="70a3e-126">**Copy**</span></span>](copy-method-in-class-win32-pagefile.md)                                               | <span data-ttu-id="70a3e-127">Metodo della classe che copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="70a3e-127">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                       |
| [<span data-ttu-id="70a3e-128">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="70a3e-128">**CopyEx**</span></span>](copyex-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="70a3e-129">Metodo della classe che copia il file o la directory logica specificata nel percorso dell'oggetto nella posizione specificata dal parametro FileName.</span><span class="sxs-lookup"><span data-stu-id="70a3e-129">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                                    |
| [<span data-ttu-id="70a3e-130">**Delete**</span><span class="sxs-lookup"><span data-stu-id="70a3e-130">**Delete**</span></span>](delete-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="70a3e-131">Metodo della classe che elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="70a3e-132">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="70a3e-132">**DeleteEx**</span></span>](deleteex-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="70a3e-133">Metodo della classe che elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-133">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="70a3e-134">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="70a3e-134">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-pagefile.md)           | <span data-ttu-id="70a3e-135">Metodo della classe che determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di *autorizzazione* non solo per l'oggetto file, ma sulla condivisione in cui risiede il file o la directory (se si trova in una condivisione).</span><span class="sxs-lookup"><span data-stu-id="70a3e-135">Class method that determines whether the caller has the aggregated permissions specified by the *Permission* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="70a3e-136">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="70a3e-136">**Rename**</span></span>](rename-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="70a3e-137">Metodo della classe che rinomina il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-137">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="70a3e-138">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="70a3e-138">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-pagefile.md)                             | <span data-ttu-id="70a3e-139">Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="70a3e-140">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="70a3e-140">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-pagefile.md)                         | <span data-ttu-id="70a3e-141">Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-141">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="70a3e-142">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="70a3e-142">**Uncompress**</span></span>](uncompress-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="70a3e-143">Metodo della classe che decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="70a3e-144">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="70a3e-144">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-pagefile.md)                               | <span data-ttu-id="70a3e-145">Metodo della classe che decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-145">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="70a3e-146">Proprietà</span><span class="sxs-lookup"><span data-stu-id="70a3e-146">Properties</span></span>

<span data-ttu-id="70a3e-147">La **classe \_ pagefile Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="70a3e-147">The **Win32\_PageFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70a3e-148">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="70a3e-148">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70a3e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-151">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("diritti di accesso")</span><span class="sxs-lookup"><span data-stu-id="70a3e-151">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-152">Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file.</span><span class="sxs-lookup"><span data-stu-id="70a3e-152">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="70a3e-153">Per i valori, vedere [**costanti di diritti di accesso a file e directory**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-153">For values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

<span data-ttu-id="70a3e-154">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-154">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="70a3e-155">**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="70a3e-155">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="70a3e-156">**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="70a3e-156">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="70a3e-157">**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)</span><span class="sxs-lookup"><span data-stu-id="70a3e-157">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="70a3e-158">**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="70a3e-158">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="70a3e-159">**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="70a3e-159">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="70a3e-160">**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="70a3e-160">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="70a3e-161">**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="70a3e-161">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="70a3e-162">**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="70a3e-162">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="70a3e-163">**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="70a3e-163">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="70a3e-164">**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="70a3e-164">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="70a3e-165">**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="70a3e-165">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="70a3e-166">**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="70a3e-166">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="70a3e-167">**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="70a3e-167">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="70a3e-168">**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="70a3e-168">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="70a3e-169">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="70a3e-169">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-170">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70a3e-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-172">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("deve essere archiviato")</span><span class="sxs-lookup"><span data-stu-id="70a3e-172">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-173">Se **true**, il file deve essere archiviato.</span><span class="sxs-lookup"><span data-stu-id="70a3e-173">If **True**, the file should be archived.</span></span>

<span data-ttu-id="70a3e-174">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-174">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-175">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="70a3e-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-178">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="70a3e-178">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-179">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-179">A short textual description of the object.</span></span>

<span data-ttu-id="70a3e-180">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-181">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="70a3e-181">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-182">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70a3e-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-184">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("compresso")</span><span class="sxs-lookup"><span data-stu-id="70a3e-184">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-185">Se **true**, il file è compresso.</span><span class="sxs-lookup"><span data-stu-id="70a3e-185">If **True**, the file is compressed.</span></span>

<span data-ttu-id="70a3e-186">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-186">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-187">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="70a3e-187">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-190">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("metodo di compressione")</span><span class="sxs-lookup"><span data-stu-id="70a3e-190">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-191">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="70a3e-191">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="70a3e-192">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="70a3e-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="70a3e-193">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="70a3e-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="70a3e-194">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="70a3e-194">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="70a3e-195">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70a3e-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-199">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="70a3e-199">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-200">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="70a3e-200">Name of the class.</span></span>

<span data-ttu-id="70a3e-201">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-202">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="70a3e-202">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-203">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70a3e-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-205">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Data creazione")</span><span class="sxs-lookup"><span data-stu-id="70a3e-205">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-206">Data e ora di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="70a3e-206">Date and time of the file's creation.</span></span>

<span data-ttu-id="70a3e-207">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-207">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-208">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70a3e-208">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-211">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="70a3e-211">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-212">Classe del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="70a3e-212">Class of the computer system.</span></span>

<span data-ttu-id="70a3e-213">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-213">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-214">**CSName**</span><span class="sxs-lookup"><span data-stu-id="70a3e-214">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-217">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="70a3e-217">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-218">Nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="70a3e-218">Name of the computer system.</span></span>

<span data-ttu-id="70a3e-219">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-220">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="70a3e-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-223">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="70a3e-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-224">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-224">A textual description of the object.</span></span>

<span data-ttu-id="70a3e-225">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-226">**Unità**</span><span class="sxs-lookup"><span data-stu-id="70a3e-226">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-229">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("unità")</span><span class="sxs-lookup"><span data-stu-id="70a3e-229">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-230">Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file.</span><span class="sxs-lookup"><span data-stu-id="70a3e-230">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="70a3e-231">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="70a3e-232">Esempio: "c:"</span><span class="sxs-lookup"><span data-stu-id="70a3e-232">Example: "c:"</span></span>

<span data-ttu-id="70a3e-233">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-234">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="70a3e-234">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-237">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("otto punto tre nome file")</span><span class="sxs-lookup"><span data-stu-id="70a3e-237">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-238">Nome file compatibile con DOS.</span><span class="sxs-lookup"><span data-stu-id="70a3e-238">DOS-compatible file name.</span></span>

<span data-ttu-id="70a3e-239">Esempio: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="70a3e-239">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="70a3e-240">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-240">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-241">**Crittografata**</span><span class="sxs-lookup"><span data-stu-id="70a3e-241">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-242">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70a3e-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-244">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="70a3e-244">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-245">Se **true**, il file è crittografato.</span><span class="sxs-lookup"><span data-stu-id="70a3e-245">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="70a3e-246">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-247">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="70a3e-247">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-250">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("metodo di crittografia")</span><span class="sxs-lookup"><span data-stu-id="70a3e-250">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-251">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="70a3e-251">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="70a3e-252">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="70a3e-252">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="70a3e-253">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="70a3e-253">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="70a3e-254">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="70a3e-254">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="70a3e-255">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-256">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="70a3e-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-259">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("estensione di file")</span><span class="sxs-lookup"><span data-stu-id="70a3e-259">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-260">Estensione del nome file senza il periodo precedente (punto).</span><span class="sxs-lookup"><span data-stu-id="70a3e-260">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="70a3e-261">Esempio: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="70a3e-261">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="70a3e-262">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="70a3e-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-266">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome file")</span><span class="sxs-lookup"><span data-stu-id="70a3e-266">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-267">Nome file senza l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="70a3e-267">File name without the file name extension.</span></span> <span data-ttu-id="70a3e-268">Esempio: "DataFile"</span><span class="sxs-lookup"><span data-stu-id="70a3e-268">Example: "MyDataFile"</span></span>

<span data-ttu-id="70a3e-269">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="70a3e-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-271">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70a3e-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-273">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("size"), [**unità**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="70a3e-273">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-274">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="70a3e-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="70a3e-275">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70a3e-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="70a3e-276">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-276">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="70a3e-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-280">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo di file")</span><span class="sxs-lookup"><span data-stu-id="70a3e-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-281">Descrittore che rappresenta il tipo di file indicato dalla proprietà di **estensione** .</span><span class="sxs-lookup"><span data-stu-id="70a3e-281">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="70a3e-282">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-283">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="70a3e-283">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-284">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70a3e-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-286">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="70a3e-286">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwAvailPageFile"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-287">Spazio disponibile nel file di paging.</span><span class="sxs-lookup"><span data-stu-id="70a3e-287">Space available in the paging file.</span></span> <span data-ttu-id="70a3e-288">Il sistema operativo può ingrandire il file di paging secondo necessità, fino al limite imposto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="70a3e-288">The operating system can enlarge the paging file as necessary, up to the limit imposed by the user.</span></span> <span data-ttu-id="70a3e-289">Questa proprietà Mostra la differenza tra le dimensioni della memoria vincolata corrente e le dimensioni correnti del file di paging; non Mostra le dimensioni massime possibili del file di paging.</span><span class="sxs-lookup"><span data-stu-id="70a3e-289">This property shows the difference between the size of current committed memory and the current size of the paging file; it does not show the largest possible size of the paging file.</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-290">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70a3e-290">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-291">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-293">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe file System ")</span><span class="sxs-lookup"><span data-stu-id="70a3e-293">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-294">Classe del file system.</span><span class="sxs-lookup"><span data-stu-id="70a3e-294">Class of the file system.</span></span>

<span data-ttu-id="70a3e-295">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-295">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-296">**FSName**</span><span class="sxs-lookup"><span data-stu-id="70a3e-296">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-299">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome file System ")</span><span class="sxs-lookup"><span data-stu-id="70a3e-299">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-300">Nome del file system.</span><span class="sxs-lookup"><span data-stu-id="70a3e-300">Name of the file system.</span></span>

<span data-ttu-id="70a3e-301">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-302">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="70a3e-302">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-303">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70a3e-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-305">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("hidden")</span><span class="sxs-lookup"><span data-stu-id="70a3e-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-306">Se **true**, il file è nascosto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-306">If **True**, the file is hidden.</span></span>

<span data-ttu-id="70a3e-307">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-307">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-308">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="70a3e-308">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-309">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70a3e-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-311">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="70a3e-311">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-312">Dimensioni iniziali del file di paging.</span><span class="sxs-lookup"><span data-stu-id="70a3e-312">Initial size of the page file.</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="70a3e-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-314">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70a3e-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-316">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="70a3e-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-317">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="70a3e-317">Indicates when the object was installed.</span></span> <span data-ttu-id="70a3e-318">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="70a3e-318">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="70a3e-319">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-320">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="70a3e-320">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-321">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70a3e-321">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-323">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("conteggio aperto file corrente")</span><span class="sxs-lookup"><span data-stu-id="70a3e-323">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-324">Numero di "file aperti" attualmente attivi sul file.</span><span class="sxs-lookup"><span data-stu-id="70a3e-324">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="70a3e-325">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70a3e-325">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="70a3e-326">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-326">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-327">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="70a3e-327">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-328">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70a3e-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-330">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ultimo accesso")</span><span class="sxs-lookup"><span data-stu-id="70a3e-330">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-331">Data e ora dell'ultimo accesso al file.</span><span class="sxs-lookup"><span data-stu-id="70a3e-331">Date and time the file was last accessed.</span></span>

<span data-ttu-id="70a3e-332">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-332">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-333">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="70a3e-333">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-334">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70a3e-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-336">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Ultima modifica")</span><span class="sxs-lookup"><span data-stu-id="70a3e-336">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-337">Data e ora dell'Ultima modifica apportata al file.</span><span class="sxs-lookup"><span data-stu-id="70a3e-337">Date and time the file was last modified.</span></span>

<span data-ttu-id="70a3e-338">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-339">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="70a3e-339">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-342">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("produttore")</span><span class="sxs-lookup"><span data-stu-id="70a3e-342">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-343">Stringa del produttore dalla risorsa della versione (se presente).</span><span class="sxs-lookup"><span data-stu-id="70a3e-343">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="70a3e-344">Questa proprietà viene ereditata da file di [**\_ DataFile CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-344">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-345">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="70a3e-345">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-346">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70a3e-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-348">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="70a3e-348">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-349">Dimensioni massime del file di paging impostate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="70a3e-349">Maximum size of the page file as set by the user.</span></span> <span data-ttu-id="70a3e-350">Il sistema operativo non consentirà al file di paging di superare questo limite.</span><span class="sxs-lookup"><span data-stu-id="70a3e-350">The operating system will not allow the page file to exceed this limit.</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-351">**Nome**</span><span class="sxs-lookup"><span data-stu-id="70a3e-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-354">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemPageFileInformation \| nomefilepagina")</span><span class="sxs-lookup"><span data-stu-id="70a3e-354">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemPageFileInformation\|PageFileName")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-355">Nome del file di paging.</span><span class="sxs-lookup"><span data-stu-id="70a3e-355">Name of the page file.</span></span>

<span data-ttu-id="70a3e-356">Esempio: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="70a3e-356">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-357">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="70a3e-357">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-358">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-360">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span><span class="sxs-lookup"><span data-stu-id="70a3e-360">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-361">Percorso del file, incluse le barre rovesciate iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="70a3e-361">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="70a3e-362">Esempio: " \\ \\ sistema Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="70a3e-362">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="70a3e-363">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-363">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-364">**Leggibile**</span><span class="sxs-lookup"><span data-stu-id="70a3e-364">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-365">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70a3e-365">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-367">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("leggibile")</span><span class="sxs-lookup"><span data-stu-id="70a3e-367">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-368">Se **true**, il file può essere letto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-368">If **True**, the file can be read.</span></span>

<span data-ttu-id="70a3e-369">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-369">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-370">**Status**</span><span class="sxs-lookup"><span data-stu-id="70a3e-370">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-371">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-373">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="70a3e-373">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-374">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-374">String that indicates the current status of the object.</span></span>

<span data-ttu-id="70a3e-375">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="70a3e-376">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="70a3e-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="70a3e-377">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="70a3e-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="70a3e-378">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="70a3e-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="70a3e-379">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="70a3e-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="70a3e-380">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="70a3e-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="70a3e-381">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="70a3e-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="70a3e-382">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="70a3e-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="70a3e-383">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="70a3e-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="70a3e-384">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="70a3e-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="70a3e-385">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="70a3e-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="70a3e-386">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="70a3e-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="70a3e-387">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="70a3e-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="70a3e-388">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="70a3e-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="70a3e-389">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="70a3e-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-390">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70a3e-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-392">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("file di sistema")</span><span class="sxs-lookup"><span data-stu-id="70a3e-392">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-393">Se **true**, il file è un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="70a3e-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="70a3e-394">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-395">**Versione**</span><span class="sxs-lookup"><span data-stu-id="70a3e-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-396">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70a3e-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-398">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span><span class="sxs-lookup"><span data-stu-id="70a3e-398">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-399">Stringa di versione dalla risorsa della versione (se presente).</span><span class="sxs-lookup"><span data-stu-id="70a3e-399">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="70a3e-400">Questa proprietà viene ereditata da file di [**\_ DataFile CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70a3e-401">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="70a3e-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a3e-402">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70a3e-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70a3e-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a3e-404">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("scrivibile")</span><span class="sxs-lookup"><span data-stu-id="70a3e-404">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="70a3e-405">Se **true**, il file può essere scritto.</span><span class="sxs-lookup"><span data-stu-id="70a3e-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="70a3e-406">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70a3e-407">Commenti</span><span class="sxs-lookup"><span data-stu-id="70a3e-407">Remarks</span></span>

<span data-ttu-id="70a3e-408">La classe del **\_ pagefile Win32** è derivata [**dalla \_ directory CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="70a3e-408">The **Win32\_PageFile** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="70a3e-409">Esempio</span><span class="sxs-lookup"><span data-stu-id="70a3e-409">Examples</span></span>

<span data-ttu-id="70a3e-410">Nell'esempio di codice VBScript seguente viene illustrato come recuperare le statistiche dei file di paging dalle istanze del file di **\_ paging Win32**.</span><span class="sxs-lookup"><span data-stu-id="70a3e-410">The following VBScript code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



<span data-ttu-id="70a3e-411">Nell'esempio di codice Perl seguente viene illustrato come recuperare le statistiche dei file di paging dalle istanze del file di **\_ paging Win32**.</span><span class="sxs-lookup"><span data-stu-id="70a3e-411">The following Perl code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="70a3e-412">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70a3e-412">Requirements</span></span>



| <span data-ttu-id="70a3e-413">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a3e-413">Requirement</span></span> | <span data-ttu-id="70a3e-414">Valore</span><span class="sxs-lookup"><span data-stu-id="70a3e-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70a3e-415">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70a3e-415">Minimum supported client</span></span><br/> | <span data-ttu-id="70a3e-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70a3e-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70a3e-417">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70a3e-417">Minimum supported server</span></span><br/> | <span data-ttu-id="70a3e-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70a3e-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70a3e-419">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70a3e-419">Namespace</span></span><br/>                | <span data-ttu-id="70a3e-420">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="70a3e-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="70a3e-421">MOF</span><span class="sxs-lookup"><span data-stu-id="70a3e-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70a3e-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70a3e-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="70a3e-423">DLL</span><span class="sxs-lookup"><span data-stu-id="70a3e-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a3e-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a3e-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a3e-425">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70a3e-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a3e-426">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="70a3e-426">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="70a3e-427">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="70a3e-427">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
