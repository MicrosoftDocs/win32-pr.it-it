---
description: Win32 \_ ShortcutFile&\# 32; La classe WMI rappresenta i file che sono collegamenti ad altri file, directory e comandi.
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Classe Win32_ShortcutFile
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
ms.openlocfilehash: b714b4c8119f92931235734664726123744064d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305264"
---
# <a name="win32_shortcutfile-class"></a><span data-ttu-id="953e9-103">Win32 \_ ShortcutFile (classe)</span><span class="sxs-lookup"><span data-stu-id="953e9-103">Win32\_ShortcutFile class</span></span>

<span data-ttu-id="953e9-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ShortcutFile Win32** rappresenta i file che sono collegamenti ad altri file, directory e comandi.</span><span class="sxs-lookup"><span data-stu-id="953e9-104">The **Win32\_ShortcutFile** [WMI class](../wmisdk/retrieving-a-class.md) represents files that are shortcuts to other files, directories, and commands.</span></span>

<span data-ttu-id="953e9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="953e9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="953e9-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="953e9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="953e9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="953e9-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="953e9-108">Members</span><span class="sxs-lookup"><span data-stu-id="953e9-108">Members</span></span>

<span data-ttu-id="953e9-109">La classe **Win32 \_ ShortcutFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="953e9-109">The **Win32\_ShortcutFile** class has these types of members:</span></span>

-   [<span data-ttu-id="953e9-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="953e9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="953e9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="953e9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="953e9-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="953e9-112">Methods</span></span>

<span data-ttu-id="953e9-113">La classe **Win32 \_ ShortcutFile** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="953e9-113">The **Win32\_ShortcutFile** class has these methods.</span></span>



| <span data-ttu-id="953e9-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="953e9-114">Method</span></span>                                                                                                | <span data-ttu-id="953e9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="953e9-115">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="953e9-116">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="953e9-116">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | <span data-ttu-id="953e9-117">Metodo della classe che modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-117">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="953e9-118">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="953e9-118">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | <span data-ttu-id="953e9-119">Metodo della classe che modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="953e9-120">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="953e9-120">**Compress**</span></span>](compress-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="953e9-121">Metodo della classe che comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-121">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="953e9-122">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="953e9-122">**CompressEx**</span></span>](compressex-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="953e9-123">Metodo della classe che comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="953e9-124">**Copia**</span><span class="sxs-lookup"><span data-stu-id="953e9-124">**Copy**</span></span>](copy-method-in-class-win32-shortcutfile.md)                                               | <span data-ttu-id="953e9-125">Metodo della classe che copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="953e9-125">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="953e9-126">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="953e9-126">**CopyEx**</span></span>](copyex-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="953e9-127">Metodo della classe che copia il file o la directory logica specificata nel percorso dell'oggetto nella posizione specificata dal parametro *filename* .</span><span class="sxs-lookup"><span data-stu-id="953e9-127">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                |
| [<span data-ttu-id="953e9-128">**Delete**</span><span class="sxs-lookup"><span data-stu-id="953e9-128">**Delete**</span></span>](delete-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="953e9-129">Metodo della classe che elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-129">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="953e9-130">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="953e9-130">**DeleteEx**</span></span>](deleteex-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="953e9-131">Metodo della classe che elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="953e9-132">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="953e9-132">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | <span data-ttu-id="953e9-133">Metodo della classe che determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di autorizzazione non solo per l'oggetto file, ma sulla condivisione in cui risiede il file o la directory (se si trova in una condivisione).</span><span class="sxs-lookup"><span data-stu-id="953e9-133">Class method that determines whether the caller has the aggregated permissions specified by the Permission argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="953e9-134">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="953e9-134">**Rename**</span></span>](rename-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="953e9-135">Metodo della classe che rinomina il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-135">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="953e9-136">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="953e9-136">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-shortcutfile.md)                             | <span data-ttu-id="953e9-137">Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-137">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="953e9-138">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="953e9-138">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-shortcutfile.md)                         | <span data-ttu-id="953e9-139">Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="953e9-140">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="953e9-140">**Uncompress**</span></span>](uncompress-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="953e9-141">Metodo della classe che decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-141">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="953e9-142">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="953e9-142">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-shortcutfile.md)                               | <span data-ttu-id="953e9-143">Metodo della classe che decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="953e9-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="953e9-144">Properties</span></span>

<span data-ttu-id="953e9-145">La classe **Win32 \_ ShortcutFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="953e9-145">The **Win32\_ShortcutFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="953e9-146">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="953e9-146">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="953e9-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-149">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("diritti di accesso")</span><span class="sxs-lookup"><span data-stu-id="953e9-149">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-150">Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file.</span><span class="sxs-lookup"><span data-stu-id="953e9-150">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="953e9-151">Per i valori di bit, vedere [**costanti di diritti di accesso a file e directory**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-151">For bit values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="953e9-152">Nei volumi FAT viene invece restituito il valore di **\_ accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-152">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="953e9-153">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-153">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="953e9-154">**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="953e9-154">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="953e9-155">**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="953e9-155">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="953e9-156">**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)</span><span class="sxs-lookup"><span data-stu-id="953e9-156">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="953e9-157">**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="953e9-157">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="953e9-158">**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="953e9-158">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="953e9-159">**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="953e9-159">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="953e9-160">**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="953e9-160">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="953e9-161">**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="953e9-161">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="953e9-162">**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="953e9-162">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="953e9-163">**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="953e9-163">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="953e9-164">**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="953e9-164">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="953e9-165">**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="953e9-165">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="953e9-166">**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="953e9-166">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="953e9-167">**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="953e9-167">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="953e9-168">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="953e9-168">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-169">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="953e9-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-171">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("deve essere archiviato")</span><span class="sxs-lookup"><span data-stu-id="953e9-171">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-172">Se **true**, il file deve essere archiviato.</span><span class="sxs-lookup"><span data-stu-id="953e9-172">If **True**, the file should be archived.</span></span>

<span data-ttu-id="953e9-173">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-173">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-174">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="953e9-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-177">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="953e9-177">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-178">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-178">A short textual description of the object.</span></span>

<span data-ttu-id="953e9-179">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-180">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="953e9-180">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-181">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="953e9-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-183">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("compresso")</span><span class="sxs-lookup"><span data-stu-id="953e9-183">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-184">Se **true**, il file è compresso.</span><span class="sxs-lookup"><span data-stu-id="953e9-184">If **True**, the file is compressed.</span></span>

<span data-ttu-id="953e9-185">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-185">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-186">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="953e9-186">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-189">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("metodo di compressione")</span><span class="sxs-lookup"><span data-stu-id="953e9-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-190">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="953e9-190">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="953e9-191">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="953e9-191">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="953e9-192">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="953e9-192">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="953e9-193">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="953e9-193">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="953e9-194">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-194">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="953e9-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-198">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="953e9-198">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-199">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="953e9-199">Name of the class.</span></span>

<span data-ttu-id="953e9-200">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-200">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-201">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="953e9-201">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-202">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="953e9-202">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-204">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Data creazione")</span><span class="sxs-lookup"><span data-stu-id="953e9-204">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-205">Data e ora di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="953e9-205">Date and time of the file's creation.</span></span>

<span data-ttu-id="953e9-206">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-206">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-207">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="953e9-207">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-210">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="953e9-210">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-211">Classe del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="953e9-211">Class of the computer system.</span></span>

<span data-ttu-id="953e9-212">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-213">**CSName**</span><span class="sxs-lookup"><span data-stu-id="953e9-213">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-216">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="953e9-216">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-217">Nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="953e9-217">Name of the computer system.</span></span>

<span data-ttu-id="953e9-218">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-219">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="953e9-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-222">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="953e9-222">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-223">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-223">A textual description of the object.</span></span>

<span data-ttu-id="953e9-224">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-225">**Unità**</span><span class="sxs-lookup"><span data-stu-id="953e9-225">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-226">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-228">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("unità")</span><span class="sxs-lookup"><span data-stu-id="953e9-228">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-229">Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file.</span><span class="sxs-lookup"><span data-stu-id="953e9-229">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="953e9-230">Esempio: "c:"</span><span class="sxs-lookup"><span data-stu-id="953e9-230">Example: "c:"</span></span>

<span data-ttu-id="953e9-231">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-232">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="953e9-232">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-235">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("otto punto tre nome file")</span><span class="sxs-lookup"><span data-stu-id="953e9-235">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-236">Nome file in formato 8,3.</span><span class="sxs-lookup"><span data-stu-id="953e9-236">File name in 8.3 format.</span></span>

<span data-ttu-id="953e9-237">Esempio: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="953e9-237">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="953e9-238">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-238">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-239">**Crittografata**</span><span class="sxs-lookup"><span data-stu-id="953e9-239">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-240">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="953e9-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-242">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="953e9-242">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-243">Se **true**, il file è crittografato.</span><span class="sxs-lookup"><span data-stu-id="953e9-243">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="953e9-244">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-244">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-245">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="953e9-245">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-248">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("metodo di crittografia")</span><span class="sxs-lookup"><span data-stu-id="953e9-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-249">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="953e9-249">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="953e9-250">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="953e9-250">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="953e9-251">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="953e9-251">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="953e9-252">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="953e9-252">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="953e9-253">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-254">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="953e9-254">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-257">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("estensione di file")</span><span class="sxs-lookup"><span data-stu-id="953e9-257">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-258">Estensione del nome file senza il periodo precedente (punto).</span><span class="sxs-lookup"><span data-stu-id="953e9-258">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="953e9-259">Esempio: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="953e9-259">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="953e9-260">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-261">**FileName**</span><span class="sxs-lookup"><span data-stu-id="953e9-261">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-262">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-264">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome file")</span><span class="sxs-lookup"><span data-stu-id="953e9-264">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-265">Nome file senza l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="953e9-265">File name without the file name extension.</span></span>

<span data-ttu-id="953e9-266">Esempio: "DataFile"</span><span class="sxs-lookup"><span data-stu-id="953e9-266">Example: "MyDataFile"</span></span>

<span data-ttu-id="953e9-267">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-267">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-268">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="953e9-268">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-269">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="953e9-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-271">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("size"), [**unità**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="953e9-271">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-272">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="953e9-272">Size of the file, in bytes.</span></span>

<span data-ttu-id="953e9-273">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-273">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="953e9-274">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-274">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-275">**FileType**</span><span class="sxs-lookup"><span data-stu-id="953e9-275">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-278">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo di file")</span><span class="sxs-lookup"><span data-stu-id="953e9-278">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-279">Descrittore che rappresenta il tipo di file indicato dalla proprietà di **estensione** .</span><span class="sxs-lookup"><span data-stu-id="953e9-279">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="953e9-280">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-280">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="953e9-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-284">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe file System ")</span><span class="sxs-lookup"><span data-stu-id="953e9-284">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-285">Classe del file system.</span><span class="sxs-lookup"><span data-stu-id="953e9-285">Class of the file system.</span></span>

<span data-ttu-id="953e9-286">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-287">**FSName**</span><span class="sxs-lookup"><span data-stu-id="953e9-287">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-290">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome file System ")</span><span class="sxs-lookup"><span data-stu-id="953e9-290">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-291">Nome del file system.</span><span class="sxs-lookup"><span data-stu-id="953e9-291">Name of the file system.</span></span>

<span data-ttu-id="953e9-292">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-293">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="953e9-293">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-294">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="953e9-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-296">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("hidden")</span><span class="sxs-lookup"><span data-stu-id="953e9-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-297">Se **true**, il file è nascosto.</span><span class="sxs-lookup"><span data-stu-id="953e9-297">If **True**, the file is hidden.</span></span>

<span data-ttu-id="953e9-298">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-299">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="953e9-299">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-300">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="953e9-300">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-302">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="953e9-302">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-303">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="953e9-303">Indicates when the object was installed.</span></span> <span data-ttu-id="953e9-304">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="953e9-304">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="953e9-305">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-306">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="953e9-306">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-307">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="953e9-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-309">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("conteggio aperto file corrente")</span><span class="sxs-lookup"><span data-stu-id="953e9-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-310">Numero di "file aperti" attualmente attivi sul file.</span><span class="sxs-lookup"><span data-stu-id="953e9-310">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="953e9-311">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-311">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="953e9-312">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-312">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-313">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="953e9-313">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-314">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="953e9-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-316">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ultimo accesso")</span><span class="sxs-lookup"><span data-stu-id="953e9-316">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-317">Data e ora dell'ultimo accesso al file.</span><span class="sxs-lookup"><span data-stu-id="953e9-317">Date and time the file was last accessed.</span></span>

<span data-ttu-id="953e9-318">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-318">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-319">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="953e9-319">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-320">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="953e9-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-322">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Ultima modifica")</span><span class="sxs-lookup"><span data-stu-id="953e9-322">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-323">Data e ora dell'Ultima modifica apportata al file.</span><span class="sxs-lookup"><span data-stu-id="953e9-323">Date and time the file was last modified.</span></span>

<span data-ttu-id="953e9-324">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-324">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-325">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="953e9-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-328">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("produttore")</span><span class="sxs-lookup"><span data-stu-id="953e9-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-329">Stringa del produttore dalla risorsa della versione (se presente).</span><span class="sxs-lookup"><span data-stu-id="953e9-329">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="953e9-330">Questa proprietà viene ereditata da file di [**\_ DataFile CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-330">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-331">**Nome**</span><span class="sxs-lookup"><span data-stu-id="953e9-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-332">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-334">Qualificatori: [ **chiave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="953e9-334">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="953e9-335">La proprietà Name è una stringa che rappresenta il nome ereditato che funge da chiave di un'istanza di file logico all'interno di una file system.</span><span class="sxs-lookup"><span data-stu-id="953e9-335">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="953e9-336">È necessario specificare i nomi dei percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="953e9-336">Full path names should be provided.</span></span>

<span data-ttu-id="953e9-337">Esempio: C: \\ \\ sistema Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="953e9-337">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="953e9-338">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-339">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="953e9-339">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-342">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span><span class="sxs-lookup"><span data-stu-id="953e9-342">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-343">Percorso del file, incluse le barre rovesciate iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="953e9-343">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="953e9-344">Esempio: " \\ \\ sistema Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="953e9-344">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="953e9-345">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-345">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-346">**Leggibile**</span><span class="sxs-lookup"><span data-stu-id="953e9-346">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-347">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="953e9-347">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-349">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("leggibile")</span><span class="sxs-lookup"><span data-stu-id="953e9-349">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-350">Se **true**, il file può essere letto.</span><span class="sxs-lookup"><span data-stu-id="953e9-350">If **True**, the file can be read.</span></span>

<span data-ttu-id="953e9-351">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-352">**Status**</span><span class="sxs-lookup"><span data-stu-id="953e9-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-355">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="953e9-355">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-356">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="953e9-356">String that indicates the current status of the object.</span></span> <span data-ttu-id="953e9-357">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="953e9-357">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="953e9-358">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="953e9-358">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="953e9-359">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="953e9-359">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="953e9-360">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="953e9-360">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="953e9-361">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="953e9-361">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="953e9-362">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="953e9-362">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="953e9-363">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-363">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="953e9-364">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="953e9-364">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="953e9-365">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="953e9-365">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="953e9-366">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="953e9-366">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="953e9-367">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="953e9-367">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="953e9-368">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="953e9-368">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="953e9-369">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="953e9-369">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="953e9-370">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="953e9-370">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="953e9-371">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="953e9-371">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="953e9-372">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="953e9-372">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="953e9-373">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="953e9-373">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="953e9-374">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="953e9-374">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="953e9-375">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="953e9-375">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="953e9-376">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="953e9-376">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="953e9-377">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="953e9-377">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-378">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="953e9-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-380">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("file di sistema")</span><span class="sxs-lookup"><span data-stu-id="953e9-380">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-381">Se **true**, il file è un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="953e9-381">If **True**, the file is a system file.</span></span>

<span data-ttu-id="953e9-382">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-383">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="953e9-383">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-384">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-386">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| \_ beginthreadex")</span><span class="sxs-lookup"><span data-stu-id="953e9-386">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|\_beginthreadex")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-387">Nome dell'oggetto a cui è associato il collegamento.</span><span class="sxs-lookup"><span data-stu-id="953e9-387">Name of the object that this is a shortcut to.</span></span>

</dd> <dt>

<span data-ttu-id="953e9-388">**Versione**</span><span class="sxs-lookup"><span data-stu-id="953e9-388">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-389">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="953e9-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-391">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span><span class="sxs-lookup"><span data-stu-id="953e9-391">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-392">Stringa di versione dalla risorsa della versione (se presente).</span><span class="sxs-lookup"><span data-stu-id="953e9-392">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="953e9-393">Questa proprietà viene ereditata da file di [**\_ DataFile CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-393">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="953e9-394">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="953e9-394">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="953e9-395">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="953e9-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="953e9-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="953e9-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="953e9-397">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("scrivibile")</span><span class="sxs-lookup"><span data-stu-id="953e9-397">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="953e9-398">Se **true**, il file può essere scritto.</span><span class="sxs-lookup"><span data-stu-id="953e9-398">If **True**, the file can be written.</span></span>

<span data-ttu-id="953e9-399">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="953e9-400">Commenti</span><span class="sxs-lookup"><span data-stu-id="953e9-400">Remarks</span></span>

<span data-ttu-id="953e9-401">La classe **Win32 \_ ShortcutFile** è derivata da file di file [**CIM \_**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="953e9-401">The **Win32\_ShortcutFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="953e9-402">Requisiti</span><span class="sxs-lookup"><span data-stu-id="953e9-402">Requirements</span></span>



| <span data-ttu-id="953e9-403">Requisito</span><span class="sxs-lookup"><span data-stu-id="953e9-403">Requirement</span></span> | <span data-ttu-id="953e9-404">Valore</span><span class="sxs-lookup"><span data-stu-id="953e9-404">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="953e9-405">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="953e9-405">Minimum supported client</span></span><br/> | <span data-ttu-id="953e9-406">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="953e9-406">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="953e9-407">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="953e9-407">Minimum supported server</span></span><br/> | <span data-ttu-id="953e9-408">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="953e9-408">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="953e9-409">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="953e9-409">Namespace</span></span><br/>                | <span data-ttu-id="953e9-410">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="953e9-410">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="953e9-411">MOF</span><span class="sxs-lookup"><span data-stu-id="953e9-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="953e9-412"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="953e9-412"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="953e9-413">DLL</span><span class="sxs-lookup"><span data-stu-id="953e9-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="953e9-414"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="953e9-414"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="953e9-415">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="953e9-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953e9-416">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="953e9-416">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="953e9-417">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="953e9-417">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
