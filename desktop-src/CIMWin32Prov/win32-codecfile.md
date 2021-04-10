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
# <a name="win32_codecfile-class"></a><span data-ttu-id="70b1d-103">\_Classe codecfile Win32</span><span class="sxs-lookup"><span data-stu-id="70b1d-103">Win32\_CodecFile class</span></span>

<span data-ttu-id="70b1d-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ codecfile Win32** rappresenta il codec audio o video installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="70b1d-104">The **Win32\_CodecFile** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the audio or video codec installed on the computer system.</span></span> <span data-ttu-id="70b1d-105">I codec convertono un tipo di formato multimediale in un altro, in genere un formato compresso in un formato non compresso.</span><span class="sxs-lookup"><span data-stu-id="70b1d-105">Codecs convert one media format type to another, typically a compressed format to an uncompressed format.</span></span> <span data-ttu-id="70b1d-106">Il nome "codec" deriva da una combinazione di comprimere e decomprimere.</span><span class="sxs-lookup"><span data-stu-id="70b1d-106">The name "codec" is derived from a combination of compress and decompress.</span></span> <span data-ttu-id="70b1d-107">Un codec, ad esempio, può convertire un formato compresso, ad esempio MS-ADPCM, in un formato non compresso, ad esempio PCM, che può essere riprodotto direttamente dalla maggior parte dell'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="70b1d-107">For example, a codec can convert a compressed format, such as MS-ADPCM, to an uncompressed format such as PCM, which most audio hardware can play directly.</span></span>

<span data-ttu-id="70b1d-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="70b1d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="70b1d-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="70b1d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b1d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70b1d-110">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="70b1d-111">Members</span><span class="sxs-lookup"><span data-stu-id="70b1d-111">Members</span></span>

<span data-ttu-id="70b1d-112">La classe **Win32 \_ codecfile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="70b1d-112">The **Win32\_CodecFile** class has these types of members:</span></span>

-   [<span data-ttu-id="70b1d-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="70b1d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="70b1d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="70b1d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70b1d-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="70b1d-115">Methods</span></span>

<span data-ttu-id="70b1d-116">La classe **Win32 \_ codecfile** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="70b1d-116">The **Win32\_CodecFile** class has these methods.</span></span>



| <span data-ttu-id="70b1d-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="70b1d-117">Method</span></span>                                                                                             | <span data-ttu-id="70b1d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70b1d-118">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70b1d-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="70b1d-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-codecfile.md)     | <span data-ttu-id="70b1d-120">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-120">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="70b1d-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="70b1d-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | <span data-ttu-id="70b1d-122">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-122">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="70b1d-123">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="70b1d-123">**Compress**</span></span>](compress-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="70b1d-124">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-124">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="70b1d-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="70b1d-125">**CompressEx**</span></span>](compressex-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="70b1d-126">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-126">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="70b1d-127">**Copia**</span><span class="sxs-lookup"><span data-stu-id="70b1d-127">**Copy**</span></span>](copy-method-in-class-win32-codecfile.md)                                               | <span data-ttu-id="70b1d-128">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="70b1d-128">Copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                         |
| [<span data-ttu-id="70b1d-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="70b1d-129">**CopyEx**</span></span>](copyex-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="70b1d-130">Metodo della classe che copia il file o la directory logica specificata nel percorso dell'oggetto nella posizione specificata dal parametro FileName.</span><span class="sxs-lookup"><span data-stu-id="70b1d-130">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                    |
| [<span data-ttu-id="70b1d-131">**Delete**</span><span class="sxs-lookup"><span data-stu-id="70b1d-131">**Delete**</span></span>](delete-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="70b1d-132">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-132">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="70b1d-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="70b1d-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="70b1d-134">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-134">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="70b1d-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="70b1d-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-codecfile.md)           | <span data-ttu-id="70b1d-136">Determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di **autorizzazione** non solo per l'oggetto file, ma sulla condivisione in cui risiede il file o la directory (se si trova in una condivisione).</span><span class="sxs-lookup"><span data-stu-id="70b1d-136">Determines whether the caller has the aggregated permissions specified by the **permission** argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="70b1d-137">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="70b1d-137">**Rename**</span></span>](rename-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="70b1d-138">Metodo della classe che rinomina il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="70b1d-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="70b1d-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-codecfile.md)                             | <span data-ttu-id="70b1d-140">Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-140">Obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="70b1d-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="70b1d-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-codecfile.md)                         | <span data-ttu-id="70b1d-142">Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="70b1d-143">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="70b1d-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="70b1d-144">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-144">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="70b1d-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="70b1d-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-codecfile.md)                               | <span data-ttu-id="70b1d-146">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-146">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="70b1d-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="70b1d-147">Properties</span></span>

<span data-ttu-id="70b1d-148">La classe **Win32 \_ codecfile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="70b1d-148">The **Win32\_CodecFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70b1d-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="70b1d-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70b1d-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-152">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("diritti di accesso")</span><span class="sxs-lookup"><span data-stu-id="70b1d-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-153">Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sul file di codec.</span><span class="sxs-lookup"><span data-stu-id="70b1d-153">Bitmask that represents the access rights required to access or perform specific operations on the codec file.</span></span> <span data-ttu-id="70b1d-154">Per i valori di bit, vedere [**costanti di diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="70b1d-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="70b1d-155">Nei volumi FAT viene invece restituito il valore di **\_ accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="70b1d-156">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="70b1d-157">**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="70b1d-157">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="70b1d-158">**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="70b1d-158">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="70b1d-159">**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)</span><span class="sxs-lookup"><span data-stu-id="70b1d-159">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="70b1d-160">**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="70b1d-160">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="70b1d-161">**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="70b1d-161">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="70b1d-162">**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="70b1d-162">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="70b1d-163">**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="70b1d-163">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="70b1d-164">**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="70b1d-164">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="70b1d-165">**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="70b1d-165">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="70b1d-166">**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="70b1d-166">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="70b1d-167">**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="70b1d-167">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="70b1d-168">**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="70b1d-168">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="70b1d-169">**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="70b1d-169">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="70b1d-170">**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="70b1d-170">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="70b1d-171">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="70b1d-171">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-172">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70b1d-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-174">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve essere archiviato")</span><span class="sxs-lookup"><span data-stu-id="70b1d-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-175">Se **true**, il file deve essere archiviato.</span><span class="sxs-lookup"><span data-stu-id="70b1d-175">If **True**, the file should be archived.</span></span>

<span data-ttu-id="70b1d-176">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-176">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-177">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="70b1d-177">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-180">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="70b1d-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-181">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-181">Short description of the object.</span></span>

<span data-ttu-id="70b1d-182">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-183">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="70b1d-183">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70b1d-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-186">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compresso")</span><span class="sxs-lookup"><span data-stu-id="70b1d-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-187">Se **true**, il file è compresso.</span><span class="sxs-lookup"><span data-stu-id="70b1d-187">If **True**, the file is compressed.</span></span>

<span data-ttu-id="70b1d-188">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-188">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-189">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="70b1d-189">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-192">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di compressione")</span><span class="sxs-lookup"><span data-stu-id="70b1d-192">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-193">Algoritmo o strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="70b1d-193">Algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="70b1d-194">Se non è possibile (o non si desidera) descrivere lo schema di compressione (probabilmente perché non è noto), utilizzare le parole seguenti: "Unknown" per indicare che non è noto se il file logico è compresso o meno. "Compresso" per indicare che il file è compresso, ma lo schema di compressione non è noto o non è stato divulgato; e "non compressi" per indicare che il file logico non è compresso.</span><span class="sxs-lookup"><span data-stu-id="70b1d-194">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed or not; "Compressed" to represent that the file is compressed but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="70b1d-195">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70b1d-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-199">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="70b1d-199">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-200">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="70b1d-200">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="70b1d-201">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="70b1d-201">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="70b1d-202">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-202">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-203">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="70b1d-203">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-204">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70b1d-204">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-206">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data creazione")</span><span class="sxs-lookup"><span data-stu-id="70b1d-206">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-207">Data di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="70b1d-207">File creation date.</span></span>

<span data-ttu-id="70b1d-208">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-209">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70b1d-209">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-212">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="70b1d-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-213">Classe del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="70b1d-213">Class of the computer system.</span></span>

<span data-ttu-id="70b1d-214">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-214">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-215">**CSName**</span><span class="sxs-lookup"><span data-stu-id="70b1d-215">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-218">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="70b1d-218">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-219">Stringa che rappresenta il nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="70b1d-219">String representing the name of the computer system.</span></span>

<span data-ttu-id="70b1d-220">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-221">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="70b1d-221">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-224">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (descrizione), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ MediaResources \\ \\ ICM \| Description")</span><span class="sxs-lookup"><span data-stu-id="70b1d-224">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\icm\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-225">Nome completo del driver del codec.</span><span class="sxs-lookup"><span data-stu-id="70b1d-225">Full name of the codec driver.</span></span> <span data-ttu-id="70b1d-226">Questa stringa deve essere visualizzata in spazi di grandi dimensioni (descrittivi).</span><span class="sxs-lookup"><span data-stu-id="70b1d-226">This string is intended to be displayed in large (descriptive) spaces.</span></span>

<span data-ttu-id="70b1d-227">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="70b1d-228">Esempio: "convertitore Microsoft PCM"</span><span class="sxs-lookup"><span data-stu-id="70b1d-228">Example: "Microsoft PCM Converter"</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-229">**Unità**</span><span class="sxs-lookup"><span data-stu-id="70b1d-229">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-232">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("unità")</span><span class="sxs-lookup"><span data-stu-id="70b1d-232">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-233">Lettera di unità (inclusi i due punti) del file.</span><span class="sxs-lookup"><span data-stu-id="70b1d-233">Drive letter (including colon) of the file.</span></span>

<span data-ttu-id="70b1d-234">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="70b1d-235">Esempio: "c:"</span><span class="sxs-lookup"><span data-stu-id="70b1d-235">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-236">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="70b1d-236">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-239">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("otto punto tre nome file")</span><span class="sxs-lookup"><span data-stu-id="70b1d-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-240">Nome file compatibile con DOS per questo file.</span><span class="sxs-lookup"><span data-stu-id="70b1d-240">DOS-compatible file name for this file.</span></span>

<span data-ttu-id="70b1d-241">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="70b1d-242">Esempio: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="70b1d-242">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-243">**Crittografata**</span><span class="sxs-lookup"><span data-stu-id="70b1d-243">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-244">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70b1d-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-246">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="70b1d-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-247">Se **true**, il file è crittografato.</span><span class="sxs-lookup"><span data-stu-id="70b1d-247">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="70b1d-248">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-248">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-249">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="70b1d-249">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-252">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di crittografia")</span><span class="sxs-lookup"><span data-stu-id="70b1d-252">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-253">Algoritmo o strumento utilizzato per crittografare il file logico.</span><span class="sxs-lookup"><span data-stu-id="70b1d-253">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="70b1d-254">Se non è possibile (o non si desidera) descrivere lo schema di crittografia (ad esempio per motivi di sicurezza), utilizzare le parole seguenti: "Unknown" per indicare che non è noto se il file logico è crittografato o meno. "Encrypted" per indicare che il file è crittografato, ma lo schema di crittografia non è noto o non è stato divulgato; e "non crittografato" per indicare che il file logico non è crittografato.</span><span class="sxs-lookup"><span data-stu-id="70b1d-254">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted or not; "Encrypted" to represent that the file is encrypted but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="70b1d-255">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-256">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="70b1d-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-259">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estensione di file")</span><span class="sxs-lookup"><span data-stu-id="70b1d-259">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-260">Estensione del nome file (senza il punto).</span><span class="sxs-lookup"><span data-stu-id="70b1d-260">File name extension (without the dot).</span></span>

<span data-ttu-id="70b1d-261">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-261">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="70b1d-262">Esempi: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="70b1d-262">Examples: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="70b1d-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-266">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")</span><span class="sxs-lookup"><span data-stu-id="70b1d-266">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-267">Nome (senza estensione) del file.</span><span class="sxs-lookup"><span data-stu-id="70b1d-267">Name (without the extension) of the file.</span></span>

<span data-ttu-id="70b1d-268">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-268">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="70b1d-269">Esempio: "Autoexec"</span><span class="sxs-lookup"><span data-stu-id="70b1d-269">Example: "autoexec"</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="70b1d-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-271">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70b1d-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-273">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="70b1d-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-274">Dimensioni del file (in byte).</span><span class="sxs-lookup"><span data-stu-id="70b1d-274">Size of the file (in bytes).</span></span>

<span data-ttu-id="70b1d-275">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="70b1d-276">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="70b1d-276">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="70b1d-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-280">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di file")</span><span class="sxs-lookup"><span data-stu-id="70b1d-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-281">Tipo di file (indicato dalla proprietà **Extension** ).</span><span class="sxs-lookup"><span data-stu-id="70b1d-281">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="70b1d-282">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-283">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70b1d-283">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-286">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe file System ")</span><span class="sxs-lookup"><span data-stu-id="70b1d-286">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-287">Classe del file system.</span><span class="sxs-lookup"><span data-stu-id="70b1d-287">Class of the file system.</span></span>

<span data-ttu-id="70b1d-288">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-289">**FSName**</span><span class="sxs-lookup"><span data-stu-id="70b1d-289">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-290">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-292">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome file System ")</span><span class="sxs-lookup"><span data-stu-id="70b1d-292">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-293">Nome del file system.</span><span class="sxs-lookup"><span data-stu-id="70b1d-293">Name of the file system.</span></span>

<span data-ttu-id="70b1d-294">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-295">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="70b1d-295">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-298">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ drivers. desc")</span><span class="sxs-lookup"><span data-stu-id="70b1d-298">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\drivers.desc")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-299">Codec rappresentato da questa classe.</span><span class="sxs-lookup"><span data-stu-id="70b1d-299">Codec represented by this class.</span></span>

<span data-ttu-id="70b1d-300">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="70b1d-300">The values are:</span></span>

<dl> <dd><span data-ttu-id="70b1d-301">Audio</span><span class="sxs-lookup"><span data-stu-id="70b1d-301">"Audio"</span></span></dd> <dd><span data-ttu-id="70b1d-302">Video</span><span class="sxs-lookup"><span data-stu-id="70b1d-302">"Video"</span></span></dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

<span data-ttu-id="70b1d-303">**Audio** ("audio")</span><span class="sxs-lookup"><span data-stu-id="70b1d-303">**Audio** ("Audio")</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="70b1d-304">**Video** ("video")</span><span class="sxs-lookup"><span data-stu-id="70b1d-304">**Video** ("Video")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="70b1d-305">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="70b1d-305">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-306">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70b1d-306">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-308">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("hidden")</span><span class="sxs-lookup"><span data-stu-id="70b1d-308">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-309">Se **true**, il file è nascosto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-309">If **True**, the file is hidden.</span></span>

<span data-ttu-id="70b1d-310">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="70b1d-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-312">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70b1d-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-314">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="70b1d-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-315">L'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="70b1d-315">Object was installed.</span></span> <span data-ttu-id="70b1d-316">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="70b1d-316">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="70b1d-317">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-318">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="70b1d-318">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-319">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70b1d-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-321">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggio aperto file corrente")</span><span class="sxs-lookup"><span data-stu-id="70b1d-321">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-322">Numero di "file aperti" attualmente attivi sul file.</span><span class="sxs-lookup"><span data-stu-id="70b1d-322">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="70b1d-323">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="70b1d-324">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="70b1d-324">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-325">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="70b1d-325">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-326">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70b1d-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-328">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ultimo accesso")</span><span class="sxs-lookup"><span data-stu-id="70b1d-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-329">Ultimo accesso al file.</span><span class="sxs-lookup"><span data-stu-id="70b1d-329">File was last accessed.</span></span>

<span data-ttu-id="70b1d-330">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-331">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="70b1d-331">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-332">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70b1d-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-334">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultima modifica")</span><span class="sxs-lookup"><span data-stu-id="70b1d-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-335">Data dell'Ultima modifica del file.</span><span class="sxs-lookup"><span data-stu-id="70b1d-335">File was last modified.</span></span>

<span data-ttu-id="70b1d-336">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-337">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="70b1d-337">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-338">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-340">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("produttore")</span><span class="sxs-lookup"><span data-stu-id="70b1d-340">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-341">Stringa del produttore dalla risorsa di versione, se presente.</span><span class="sxs-lookup"><span data-stu-id="70b1d-341">Manufacturer string from version resource, if one is present.</span></span>

<span data-ttu-id="70b1d-342">Questa proprietà viene ereditata da file di [**\_ DataFile CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-342">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-343">**Nome**</span><span class="sxs-lookup"><span data-stu-id="70b1d-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-344">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-346">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70b1d-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-347">Nome ereditato che funge da chiave di un'istanza di file logica all'interno di una file system.</span><span class="sxs-lookup"><span data-stu-id="70b1d-347">Inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="70b1d-348">È necessario specificare i nomi dei percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="70b1d-348">Full path names should be provided.</span></span>

<span data-ttu-id="70b1d-349">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="70b1d-350">Esempio: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="70b1d-350">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-351">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="70b1d-351">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-354">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="70b1d-354">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-355">Percorso del file.</span><span class="sxs-lookup"><span data-stu-id="70b1d-355">Path of the file.</span></span> <span data-ttu-id="70b1d-356">Sono incluse le barre rovesciate iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="70b1d-356">This includes leading and trailing backslashes.</span></span>

<span data-ttu-id="70b1d-357">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-357">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="70b1d-358">Esempio: " \\ \\ sistema Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="70b1d-358">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-359">**Leggibile**</span><span class="sxs-lookup"><span data-stu-id="70b1d-359">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-360">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70b1d-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-362">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("leggibile")</span><span class="sxs-lookup"><span data-stu-id="70b1d-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-363">Il file può essere letto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-363">File can be read.</span></span>

<span data-ttu-id="70b1d-364">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-364">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="70b1d-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-366">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-368">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="70b1d-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-369">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-369">Current status of the object.</span></span> <span data-ttu-id="70b1d-370">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="70b1d-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="70b1d-371">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="70b1d-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="70b1d-372">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="70b1d-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="70b1d-373">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="70b1d-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="70b1d-374">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="70b1d-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="70b1d-375">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="70b1d-376">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="70b1d-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="70b1d-377">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="70b1d-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="70b1d-378">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="70b1d-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="70b1d-379">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="70b1d-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="70b1d-380">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="70b1d-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="70b1d-381">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="70b1d-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="70b1d-382">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="70b1d-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="70b1d-383">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="70b1d-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="70b1d-384">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="70b1d-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="70b1d-385">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="70b1d-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="70b1d-386">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="70b1d-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="70b1d-387">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="70b1d-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="70b1d-388">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="70b1d-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="70b1d-389">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="70b1d-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-390">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70b1d-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-392">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file di sistema")</span><span class="sxs-lookup"><span data-stu-id="70b1d-392">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-393">Se **true**, il file è un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="70b1d-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="70b1d-394">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-395">**Versione**</span><span class="sxs-lookup"><span data-stu-id="70b1d-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-396">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70b1d-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-398">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span><span class="sxs-lookup"><span data-stu-id="70b1d-398">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-399">Stringa di versione dalla risorsa di versione, se presente.</span><span class="sxs-lookup"><span data-stu-id="70b1d-399">Version string from version resource, if one is present.</span></span>

<span data-ttu-id="70b1d-400">Questa proprietà viene ereditata da file di [**\_ DataFile CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="70b1d-401">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="70b1d-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b1d-402">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="70b1d-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70b1d-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70b1d-404">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("scrivibile")</span><span class="sxs-lookup"><span data-stu-id="70b1d-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="70b1d-405">Se **true**, il file può essere scritto.</span><span class="sxs-lookup"><span data-stu-id="70b1d-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="70b1d-406">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70b1d-407">Commenti</span><span class="sxs-lookup"><span data-stu-id="70b1d-407">Remarks</span></span>

<span data-ttu-id="70b1d-408">La classe **Win32 \_ codecfile** è derivata da file di [**\_ DataFile CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="70b1d-408">The **Win32\_CodecFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70b1d-409">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70b1d-409">Requirements</span></span>



| <span data-ttu-id="70b1d-410">Requisito</span><span class="sxs-lookup"><span data-stu-id="70b1d-410">Requirement</span></span> | <span data-ttu-id="70b1d-411">Valore</span><span class="sxs-lookup"><span data-stu-id="70b1d-411">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70b1d-412">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70b1d-412">Minimum supported client</span></span><br/> | <span data-ttu-id="70b1d-413">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70b1d-413">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70b1d-414">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70b1d-414">Minimum supported server</span></span><br/> | <span data-ttu-id="70b1d-415">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70b1d-415">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70b1d-416">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70b1d-416">Namespace</span></span><br/>                | <span data-ttu-id="70b1d-417">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="70b1d-417">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="70b1d-418">MOF</span><span class="sxs-lookup"><span data-stu-id="70b1d-418">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70b1d-419"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70b1d-419"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="70b1d-420">DLL</span><span class="sxs-lookup"><span data-stu-id="70b1d-420">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b1d-421"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70b1d-421"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70b1d-422">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70b1d-422">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b1d-423">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="70b1d-423">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

<span data-ttu-id="70b1d-424">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70b1d-424">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

