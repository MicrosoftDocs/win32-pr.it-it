---
description: La \_ directory Win32&\# 32; La classe WMI rappresenta una voce di directory in un computer che esegue Windows.
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225740"
---
# <a name="win32_directory-class"></a><span data-ttu-id="6db04-103">\_Classe directory Win32</span><span class="sxs-lookup"><span data-stu-id="6db04-103">Win32\_Directory class</span></span>

<span data-ttu-id="6db04-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) della **\_ directory Win32** rappresenta una voce di directory in un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="6db04-104">The **Win32\_Directory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a directory entry on a computer system running Windows.</span></span> <span data-ttu-id="6db04-105">Una directory è un tipo di file che raggruppa logicamente i file di dati e fornisce informazioni sul percorso per i file raggruppati.</span><span class="sxs-lookup"><span data-stu-id="6db04-105">A directory is a type of file that logically groups data files and provides path information for the grouped files.</span></span> <span data-ttu-id="6db04-106">Esempio: C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="6db04-106">Example: C:\\TEMP.</span></span> <span data-ttu-id="6db04-107">**Win32 \_ La directory** non include directory di unità di rete.</span><span class="sxs-lookup"><span data-stu-id="6db04-107">**Win32\_Directory** does not include directories of network drives.</span></span>

<span data-ttu-id="6db04-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6db04-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6db04-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6db04-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db04-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6db04-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
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

## <a name="members"></a><span data-ttu-id="6db04-111">Members</span><span class="sxs-lookup"><span data-stu-id="6db04-111">Members</span></span>

<span data-ttu-id="6db04-112">La classe di **\_ directory Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6db04-112">The **Win32\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="6db04-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="6db04-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="6db04-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6db04-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6db04-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="6db04-115">Methods</span></span>

<span data-ttu-id="6db04-116">La classe di **\_ directory Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6db04-116">The **Win32\_Directory** class has these methods.</span></span>



| <span data-ttu-id="6db04-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="6db04-117">Method</span></span>                                                                                             | <span data-ttu-id="6db04-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6db04-118">Description</span></span>                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6db04-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="6db04-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-directory.md)     | <span data-ttu-id="6db04-120">Metodo della classe che modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-120">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="6db04-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="6db04-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-directory.md) | <span data-ttu-id="6db04-122">Metodo della classe che modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-122">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="6db04-123">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="6db04-123">**Compress**</span></span>](compress-method-in-class-win32-directory.md)                                       | <span data-ttu-id="6db04-124">Metodo della classe che comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-124">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="6db04-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="6db04-125">**CompressEx**</span></span>](compressex-method-in-class-win32-directory.md)                                   | <span data-ttu-id="6db04-126">Metodo della classe che comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-126">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="6db04-127">**Copia**</span><span class="sxs-lookup"><span data-stu-id="6db04-127">**Copy**</span></span>](copy-method-in-class-win32-directory.md)                                               | <span data-ttu-id="6db04-128">Metodo della classe che copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="6db04-128">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                        |
| [<span data-ttu-id="6db04-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="6db04-129">**CopyEx**</span></span>](copyex-method-in-class-win32-directory.md)                                           | <span data-ttu-id="6db04-130">Metodo della classe che copia il file o la directory logica specificata nel percorso dell'oggetto nella posizione specificata dal parametro *filename* .</span><span class="sxs-lookup"><span data-stu-id="6db04-130">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                   |
| [<span data-ttu-id="6db04-131">**Delete**</span><span class="sxs-lookup"><span data-stu-id="6db04-131">**Delete**</span></span>](delete-method-in-class-win32-directory.md)                                           | <span data-ttu-id="6db04-132">Metodo della classe che elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-132">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="6db04-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="6db04-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-directory.md)                                       | <span data-ttu-id="6db04-134">Metodo della classe che elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-134">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="6db04-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="6db04-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-directory.md)           | <span data-ttu-id="6db04-136">Metodo della classe che determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento *delle autorizzazioni* non solo per l'oggetto file, ma sulla condivisione in cui risiede il file o la directory (se si trova in una condivisione).</span><span class="sxs-lookup"><span data-stu-id="6db04-136">Class method that determines whether the caller has the aggregated permissions specified by the *Permissions* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="6db04-137">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="6db04-137">**Rename**</span></span>](rename-method-in-class-win32-directory.md)                                           | <span data-ttu-id="6db04-138">Metodo della classe che rinomina il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="6db04-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="6db04-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-directory.md)                             | <span data-ttu-id="6db04-140">Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-140">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="6db04-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="6db04-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-directory.md)                         | <span data-ttu-id="6db04-142">Metodo della classe che ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="6db04-143">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="6db04-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)                                   | <span data-ttu-id="6db04-144">Metodo della classe che decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-144">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="6db04-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="6db04-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-directory.md)                               | <span data-ttu-id="6db04-146">Metodo della classe che decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-146">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="6db04-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6db04-147">Properties</span></span>

<span data-ttu-id="6db04-148">La classe di **\_ directory Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6db04-148">The **Win32\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6db04-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="6db04-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6db04-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-152">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("diritti di accesso")</span><span class="sxs-lookup"><span data-stu-id="6db04-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-153">Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sulla directory.</span><span class="sxs-lookup"><span data-stu-id="6db04-153">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="6db04-154">Per i valori di bit, vedere [**costanti di diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="6db04-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="6db04-155">Nei volumi FAT viene invece restituito il valore di **\_ accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="6db04-156">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6db04-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="6db04-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-158">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="6db04-158">Grants the right to read data from the file.</span></span> <span data-ttu-id="6db04-159">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="6db04-159">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="6db04-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="6db04-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-161">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="6db04-161">Grants the right to write data to the file.</span></span> <span data-ttu-id="6db04-162">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="6db04-162">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="6db04-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory** (4)</span><span class="sxs-lookup"><span data-stu-id="6db04-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-164">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="6db04-164">Grants the right to append data to the file.</span></span> <span data-ttu-id="6db04-165">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="6db04-165">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="6db04-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="6db04-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-167">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="6db04-167">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="6db04-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="6db04-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-169">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="6db04-169">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="6db04-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="6db04-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-171">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="6db04-171">Grants the right to execute a file.</span></span> <span data-ttu-id="6db04-172">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="6db04-172">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="6db04-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="6db04-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-174">Concede il diritto di eliminare una directory e tutti i file in esso contenuti (elementi figlio), anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6db04-174">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="6db04-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="6db04-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-176">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="6db04-176">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="6db04-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="6db04-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-178">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="6db04-178">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="6db04-179"><span id="DELETE"></span><span id="delete"></span>**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="6db04-179"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-180">Concede l'accesso DELETE.</span><span class="sxs-lookup"><span data-stu-id="6db04-180">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="6db04-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="6db04-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-182">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="6db04-182">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="6db04-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="6db04-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-184">Concede l'accesso in scrittura all'ACL discrezionale.</span><span class="sxs-lookup"><span data-stu-id="6db04-184">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="6db04-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="6db04-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-186">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="6db04-186">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="6db04-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="6db04-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-188">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="6db04-188">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span data-ttu-id="6db04-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Accesso \_ a \_Sicurezza del sistema** (18809343)</span><span class="sxs-lookup"><span data-stu-id="6db04-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**ACCESS\_SYSTEM\_SECURITY** (18809343)</span></span>


</dt> <dd>

<span data-ttu-id="6db04-190">Controlla la possibilità di ottenere o impostare l'elenco SACL nel descrittore di sicurezza di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-190">Controls the ability to get or set the SACL in an object's security descriptor.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6db04-191">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="6db04-191">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-192">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6db04-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-194">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve essere archiviato")</span><span class="sxs-lookup"><span data-stu-id="6db04-194">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-195">Indica se è stato impostato il bit di archiviazione nella cartella.</span><span class="sxs-lookup"><span data-stu-id="6db04-195">Indicates whether the archive bit on the folder has been set.</span></span> <span data-ttu-id="6db04-196">Il bit di archiviazione viene usato dai programmi di backup per identificare i file di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="6db04-196">The archive bit is used by backup programs to identify files that should be backed up.</span></span> <span data-ttu-id="6db04-197">Se **true**, il file deve essere archiviato.</span><span class="sxs-lookup"><span data-stu-id="6db04-197">If **True**, the file should be archived.</span></span>

<span data-ttu-id="6db04-198">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-198">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-199">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6db04-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-202">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6db04-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-203">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-203">A short textual description of the object.</span></span>

<span data-ttu-id="6db04-204">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-205">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="6db04-205">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-206">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6db04-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-208">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compresso")</span><span class="sxs-lookup"><span data-stu-id="6db04-208">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-209">Indica se la cartella è stata compressa.</span><span class="sxs-lookup"><span data-stu-id="6db04-209">Indicates whether or not the folder has been compressed.</span></span> <span data-ttu-id="6db04-210">WMI riconosce le cartelle compresse mediante WMI o l'interfaccia utente grafica; Tuttavia, non riconosce. File ZIP compressi.</span><span class="sxs-lookup"><span data-stu-id="6db04-210">WMI recognizes folders compressed using WMI itself or using the graphical user interface; it does not, however, recognize .ZIP files as being compressed.</span></span> <span data-ttu-id="6db04-211">Se **true**, il file è compresso.</span><span class="sxs-lookup"><span data-stu-id="6db04-211">If **True**, the file is compressed.</span></span>

<span data-ttu-id="6db04-212">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-213">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="6db04-213">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-216">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di compressione")</span><span class="sxs-lookup"><span data-stu-id="6db04-216">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-217">Algoritmo o strumento (in genere un metodo) usato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="6db04-217">Algorithm or tool (usually a method) used to compress the logical file.</span></span> <span data-ttu-id="6db04-218">Se non è possibile (o non si desidera) descrivere lo schema di compressione (probabilmente perché non è noto), utilizzare le parole seguenti: "Unknown" per indicare che non è noto se il file logico è compresso; "Compresso" per indicare che il file è compresso, ma lo schema di compressione non è noto o non è stato divulgato; e "non compressi" per indicare che il file logico non è compresso.</span><span class="sxs-lookup"><span data-stu-id="6db04-218">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed; "Compressed" to represent that the file is compressed, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="6db04-219">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-220">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6db04-220">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-223">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="6db04-223">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-224">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="6db04-224">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="6db04-225">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="6db04-225">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6db04-226">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-226">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-227">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="6db04-227">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-228">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6db04-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-230">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data creazione")</span><span class="sxs-lookup"><span data-stu-id="6db04-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-231">Data di creazione dell'oggetto file system.</span><span class="sxs-lookup"><span data-stu-id="6db04-231">Date that the file system object was created.</span></span> <span data-ttu-id="6db04-232">Per ulteriori informazioni sull'utilizzo dei formati di data e ora WMI, vedere [attività WMI: date e ore](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="6db04-232">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="6db04-233">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-234">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6db04-234">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-237">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="6db04-237">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-238">Nome della classe di creazione del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="6db04-238">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="6db04-239">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-239">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-240">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6db04-240">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-243">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="6db04-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-244">Nome del computer in cui è archiviato l'oggetto file system.</span><span class="sxs-lookup"><span data-stu-id="6db04-244">Name of the computer where the file system object is stored.</span></span>

<span data-ttu-id="6db04-245">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-245">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-246">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6db04-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-249">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6db04-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-250">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-250">A textual description of the object.</span></span>

<span data-ttu-id="6db04-251">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-252">**Unità**</span><span class="sxs-lookup"><span data-stu-id="6db04-252">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-253">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-255">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("unità")</span><span class="sxs-lookup"><span data-stu-id="6db04-255">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-256">Lettera di unità dell'unità (inclusi i due punti) in cui è archiviato l'oggetto file system.</span><span class="sxs-lookup"><span data-stu-id="6db04-256">Drive letter of the drive (including colon) where the file system object is stored.</span></span>

<span data-ttu-id="6db04-257">Esempio: "c:"</span><span class="sxs-lookup"><span data-stu-id="6db04-257">Example: "c:"</span></span>

<span data-ttu-id="6db04-258">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-258">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-259">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="6db04-259">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-262">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("otto punto tre nome file")</span><span class="sxs-lookup"><span data-stu-id="6db04-262">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-263">Nome compatibile con MS-DOS per la cartella.</span><span class="sxs-lookup"><span data-stu-id="6db04-263">MS-DOS -compatible name for the folder.</span></span>

<span data-ttu-id="6db04-264">Esempio: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="6db04-264">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="6db04-265">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-266">**Crittografata**</span><span class="sxs-lookup"><span data-stu-id="6db04-266">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-267">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6db04-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-269">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="6db04-269">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-270">Indica se la cartella è stata crittografata o meno.</span><span class="sxs-lookup"><span data-stu-id="6db04-270">Indicates whether or not the folder has been encrypted.</span></span> <span data-ttu-id="6db04-271">Se **true**, la cartella è crittografata.</span><span class="sxs-lookup"><span data-stu-id="6db04-271">If **True**, the folder is encrypted.</span></span>

<span data-ttu-id="6db04-272">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-273">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="6db04-273">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-276">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di crittografia")</span><span class="sxs-lookup"><span data-stu-id="6db04-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-277">Algoritmo o strumento utilizzato per crittografare il file logico.</span><span class="sxs-lookup"><span data-stu-id="6db04-277">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="6db04-278">Se non è possibile (o non si desidera) descrivere lo schema di crittografia (ad esempio per motivi di sicurezza), utilizzare le parole seguenti: "Unknown" per indicare che non è noto se il file logico è crittografato; "Encrypted" per indicare che il file è crittografato, ma lo schema di crittografia non è noto o non è stato divulgato; e "non crittografato" per indicare che il file logico non è crittografato.</span><span class="sxs-lookup"><span data-stu-id="6db04-278">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted; "Encrypted" to represent that the file is encrypted, but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="6db04-279">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-280">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="6db04-280">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-283">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estensione di file")</span><span class="sxs-lookup"><span data-stu-id="6db04-283">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-284">Estensione del nome file per l'oggetto file system, escluso il punto (.) che separa l'estensione dal nome del file.</span><span class="sxs-lookup"><span data-stu-id="6db04-284">File name extension for the file system object, not including the dot (.) that separates the extension from the file name.</span></span>

<span data-ttu-id="6db04-285">Esempi: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="6db04-285">Examples: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="6db04-286">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-287">**FileName**</span><span class="sxs-lookup"><span data-stu-id="6db04-287">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-290">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")</span><span class="sxs-lookup"><span data-stu-id="6db04-290">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-291">Nome file (senza il punto o l'estensione) del file.</span><span class="sxs-lookup"><span data-stu-id="6db04-291">File name (without the dot or extension) of the file.</span></span>

<span data-ttu-id="6db04-292">Esempio: "Autoexec"</span><span class="sxs-lookup"><span data-stu-id="6db04-292">Example: "autoexec"</span></span>

<span data-ttu-id="6db04-293">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-293">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-294">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="6db04-294">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-295">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6db04-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-297">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6db04-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-298">Dimensioni dell'oggetto file system, in byte.</span><span class="sxs-lookup"><span data-stu-id="6db04-298">Size of the file system object, in bytes.</span></span> <span data-ttu-id="6db04-299">Sebbene le cartelle dispongano di una proprietà **Filesize** , viene sempre restituito il valore 0.</span><span class="sxs-lookup"><span data-stu-id="6db04-299">Although folders possess a **FileSize** property, the value 0 is always returned.</span></span> <span data-ttu-id="6db04-300">Per determinare le dimensioni di una cartella, utilizzare FileSystemObject o sommare le dimensioni di tutti i file archiviati nella cartella.</span><span class="sxs-lookup"><span data-stu-id="6db04-300">To determine the size of a folder, use the FileSystemObject or add up the size of all the files stored in the folder.</span></span>

<span data-ttu-id="6db04-301">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6db04-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6db04-302">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-303">**FileType**</span><span class="sxs-lookup"><span data-stu-id="6db04-303">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-306">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di file")</span><span class="sxs-lookup"><span data-stu-id="6db04-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-307">Tipo di file (indicato dalla proprietà **Extension** ).</span><span class="sxs-lookup"><span data-stu-id="6db04-307">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="6db04-308">Ad esempio, è probabile che un file con estensione mdb abbia il tipo di file applicazione Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6db04-308">For example, an .mdb file is likely to have the file type Microsoft Access Application.</span></span> <span data-ttu-id="6db04-309">È probabile che un file ASP includa il documento HTML di tipo file.</span><span class="sxs-lookup"><span data-stu-id="6db04-309">An .asp file likely has the file type HTML Document.</span></span> <span data-ttu-id="6db04-310">Le cartelle vengono in genere segnalate semplicemente come cartella.</span><span class="sxs-lookup"><span data-stu-id="6db04-310">Folders are typically reported simply as Folder.</span></span>

<span data-ttu-id="6db04-311">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-311">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-312">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6db04-312">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-315">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe file System ")</span><span class="sxs-lookup"><span data-stu-id="6db04-315">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-316">Classe del file system.</span><span class="sxs-lookup"><span data-stu-id="6db04-316">Class of the file system.</span></span>

<span data-ttu-id="6db04-317">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-317">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-318">**FSName**</span><span class="sxs-lookup"><span data-stu-id="6db04-318">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-321">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome file System ")</span><span class="sxs-lookup"><span data-stu-id="6db04-321">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-322">Tipo di file system (NTFS, FAT, FAT32) installato nell'unità in cui si trova il file o la cartella.</span><span class="sxs-lookup"><span data-stu-id="6db04-322">Type of file system (NTFS, FAT, FAT32) installed on the drive where the file or folder is located.</span></span>

<span data-ttu-id="6db04-323">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-324">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="6db04-324">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-325">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6db04-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-327">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("hidden")</span><span class="sxs-lookup"><span data-stu-id="6db04-327">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-328">Indica se l'oggetto file system è nascosto.</span><span class="sxs-lookup"><span data-stu-id="6db04-328">Indicates whether the file system object is hidden.</span></span> <span data-ttu-id="6db04-329">Se **true**, il file è nascosto.</span><span class="sxs-lookup"><span data-stu-id="6db04-329">If **True**, the file is hidden.</span></span>

<span data-ttu-id="6db04-330">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-331">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6db04-331">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-332">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6db04-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-334">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="6db04-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-335">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="6db04-335">Indicates when the object was installed.</span></span> <span data-ttu-id="6db04-336">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="6db04-336">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6db04-337">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-338">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="6db04-338">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-339">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6db04-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-341">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggio aperto file corrente")</span><span class="sxs-lookup"><span data-stu-id="6db04-341">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-342">Numero di "file aperti" attualmente attivi sul file.</span><span class="sxs-lookup"><span data-stu-id="6db04-342">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="6db04-343">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-343">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="6db04-344">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6db04-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-345">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="6db04-345">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-346">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6db04-346">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-348">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ultimo accesso")</span><span class="sxs-lookup"><span data-stu-id="6db04-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-349">Data dell'ultimo accesso al file.</span><span class="sxs-lookup"><span data-stu-id="6db04-349">Date the file was last accessed.</span></span> <span data-ttu-id="6db04-350">Per ulteriori informazioni sull'utilizzo dei formati di data e ora WMI, vedere [attività WMI: date e ore](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="6db04-350">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="6db04-351">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-352">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="6db04-352">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-353">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6db04-353">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-355">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultima modifica")</span><span class="sxs-lookup"><span data-stu-id="6db04-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-356">Data dell'Ultima modifica del file.</span><span class="sxs-lookup"><span data-stu-id="6db04-356">Date the file was last modified.</span></span> <span data-ttu-id="6db04-357">Per ulteriori informazioni sull'utilizzo dei formati di data e ora WMI, vedere [attività WMI: date e ore](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="6db04-357">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="6db04-358">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-358">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-359">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6db04-359">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-360">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-362">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6db04-362">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6db04-363">La proprietà Name è una stringa che rappresenta il nome ereditato che funge da chiave di un'istanza di file logico all'interno di una file system.</span><span class="sxs-lookup"><span data-stu-id="6db04-363">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="6db04-364">È necessario specificare i nomi dei percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="6db04-364">Full path names should be provided.</span></span> <span data-ttu-id="6db04-365">Esempio: C: \\ \\ sistema Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="6db04-365">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="6db04-366">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-366">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-367">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="6db04-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-368">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-370">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="6db04-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-371">Percorso del file.</span><span class="sxs-lookup"><span data-stu-id="6db04-371">Path for the file.</span></span> <span data-ttu-id="6db04-372">Il percorso include le barre rovesciate iniziali e finali, ma non la lettera di unità o il nome della cartella.</span><span class="sxs-lookup"><span data-stu-id="6db04-372">The path includes the leading and trailing backslashes, but not the drive letter or the folder name.</span></span>

<span data-ttu-id="6db04-373">Per la cartella c: \\ Windows \\ system32 \\ WBEM, il percorso è \\ Windows \\ system32 \\ .</span><span class="sxs-lookup"><span data-stu-id="6db04-373">For the folder c:\\windows\\system32\\wbem, the path is \\windows\\system32\\.</span></span> <span data-ttu-id="6db04-374">Per la cartella c: \\ Scripts, il percorso è \\ .</span><span class="sxs-lookup"><span data-stu-id="6db04-374">For the folder c:\\scripts, the path is \\.</span></span>

<span data-ttu-id="6db04-375">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-375">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-376">**Leggibile**</span><span class="sxs-lookup"><span data-stu-id="6db04-376">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-377">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6db04-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-379">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("leggibile")</span><span class="sxs-lookup"><span data-stu-id="6db04-379">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-380">Indica se è possibile leggere gli elementi nella cartella.</span><span class="sxs-lookup"><span data-stu-id="6db04-380">Indicates whether you can read items in the folder.</span></span> <span data-ttu-id="6db04-381">Se **true**, il file può essere letto.</span><span class="sxs-lookup"><span data-stu-id="6db04-381">If **True**, the file can be read.</span></span>

<span data-ttu-id="6db04-382">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-383">**Status**</span><span class="sxs-lookup"><span data-stu-id="6db04-383">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-384">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6db04-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-386">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6db04-386">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-387">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6db04-387">String that indicates the current status of the object.</span></span>

<span data-ttu-id="6db04-388">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6db04-389">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6db04-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6db04-390">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6db04-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6db04-391">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="6db04-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6db04-392">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="6db04-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6db04-393">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="6db04-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6db04-394">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="6db04-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6db04-395">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="6db04-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6db04-396">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="6db04-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6db04-397">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="6db04-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6db04-398">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="6db04-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6db04-399">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="6db04-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6db04-400">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="6db04-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6db04-401">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="6db04-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6db04-402">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="6db04-402">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-403">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6db04-403">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-405">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file di sistema")</span><span class="sxs-lookup"><span data-stu-id="6db04-405">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-406">Indica se l'oggetto è un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="6db04-406">Indicates whether the object is a system file.</span></span> <span data-ttu-id="6db04-407">Se **true**, il file è un file di sistema</span><span class="sxs-lookup"><span data-stu-id="6db04-407">If **True**, the file is a system file</span></span>

<span data-ttu-id="6db04-408">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-408">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db04-409">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="6db04-409">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db04-410">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6db04-410">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db04-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6db04-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db04-412">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("scrivibile")</span><span class="sxs-lookup"><span data-stu-id="6db04-412">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="6db04-413">Se **true**, il file può essere scritto.</span><span class="sxs-lookup"><span data-stu-id="6db04-413">If **True**, the file can be written.</span></span>

<span data-ttu-id="6db04-414">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-414">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6db04-415">Commenti</span><span class="sxs-lookup"><span data-stu-id="6db04-415">Remarks</span></span>

<span data-ttu-id="6db04-416">La **classe \_ directory Win32** è derivata dalla [**\_ directory CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="6db04-416">The **Win32\_Directory** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

<span data-ttu-id="6db04-417">**Overview**</span><span class="sxs-lookup"><span data-stu-id="6db04-417">**Overview**</span></span>

<span data-ttu-id="6db04-418">Le cartelle sono file system oggetti progettati per contenere altri oggetti file system.</span><span class="sxs-lookup"><span data-stu-id="6db04-418">Folders are file system objects designed to contain other file system objects.</span></span> <span data-ttu-id="6db04-419">Ciò non significa che tutte le cartelle sono comunque simili.</span><span class="sxs-lookup"><span data-stu-id="6db04-419">This does not mean that all folders are alike, however.</span></span> <span data-ttu-id="6db04-420">Le cartelle possono invece variare in modo significativo.</span><span class="sxs-lookup"><span data-stu-id="6db04-420">Instead, folders can vary considerably.</span></span> <span data-ttu-id="6db04-421">Alcune cartelle sono cartelle del sistema operativo, che in genere non devono essere modificate da uno script.</span><span class="sxs-lookup"><span data-stu-id="6db04-421">Some folders are operating system folders, which generally should not be modified by a script.</span></span> <span data-ttu-id="6db04-422">Alcune cartelle sono di sola lettura, il che significa che gli utenti possono accedere al contenuto della cartella, ma non possono aggiungere, eliminare o modificare tali contenuti.</span><span class="sxs-lookup"><span data-stu-id="6db04-422">Some folders are read-only, which means that users can access the contents of that folder but cannot add to, delete from, or modify those contents.</span></span> <span data-ttu-id="6db04-423">Alcune cartelle vengono compresse per l'archiviazione ottimale, mentre altre sono nascoste e non sono visibili agli utenti.</span><span class="sxs-lookup"><span data-stu-id="6db04-423">Some folders are compressed for optimal storage, while others are hidden and not visible to users.</span></span>

<span data-ttu-id="6db04-424">WMI utilizza la **classe \_ directory Win32** per gestire le cartelle.</span><span class="sxs-lookup"><span data-stu-id="6db04-424">WMI uses the **Win32\_Directory** class to manage folders.</span></span> <span data-ttu-id="6db04-425">In modo significativo, le proprietà e i metodi disponibili in questa classe sono identici alle proprietà e ai metodi disponibili nella classe [**CIM \_ DataFile**](cim-datafile.md) , la classe usata per gestire i file.</span><span class="sxs-lookup"><span data-stu-id="6db04-425">Significantly, the properties and methods available in this class are identical to the properties and methods available in the [**CIM\_DataFile**](cim-datafile.md) class, the class used to manage files.</span></span> <span data-ttu-id="6db04-426">Ciò significa che, dopo aver appreso come gestire le cartelle tramite WMI, si saprà anche come gestire i file, senza alcuna attività aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="6db04-426">This means that after you have learned how to manage folders using WMI, you will, without any extra work, also know how to manage files.</span></span>

<span data-ttu-id="6db04-427">La classe di associazione della [**\_ sottodirectory Win32**](win32-subdirectory.md) viene utilizzata anche per gestire file e cartelle.</span><span class="sxs-lookup"><span data-stu-id="6db04-427">The [**Win32\_Subdirectory**](win32-subdirectory.md) association class is also used to manage files and folders.</span></span> <span data-ttu-id="6db04-428">La classe della **\_ sottodirectory Win32** mette in correlazione una cartella e le relative sottocartelle immediate.</span><span class="sxs-lookup"><span data-stu-id="6db04-428">The **Win32\_Subdirectory** class relates a folder and its immediate subfolders.</span></span> <span data-ttu-id="6db04-429">Ad esempio, nella struttura di cartelle C: \\ log Scripts \\ , logs è una sottocartella di script e Scripts è una sottocartella della cartella radice c: \\ .</span><span class="sxs-lookup"><span data-stu-id="6db04-429">For example, in the folder structure C:\\Scripts\\Logs, Logs is a subfolder of Scripts, and Scripts is a subfolder of the root folder C:\\.</span></span> <span data-ttu-id="6db04-430">Tuttavia, i log non vengono considerati sottocartelle di C: \\ .</span><span class="sxs-lookup"><span data-stu-id="6db04-430">However, Logs is not considered a subfolder of C:\\.</span></span>

<span data-ttu-id="6db04-431">È possibile recuperare le proprietà di qualsiasi cartella nella file system usando la classe **di \_ directory Win32** .</span><span class="sxs-lookup"><span data-stu-id="6db04-431">You can retrieve the properties of any folder in the file system using the **Win32\_Directory** class.</span></span> <span data-ttu-id="6db04-432">Le proprietà disponibili con questa classe sono illustrate nella tabella 11,1.</span><span class="sxs-lookup"><span data-stu-id="6db04-432">The properties available using this class are shown in Table 11.1.</span></span> <span data-ttu-id="6db04-433">Per recuperare le proprietà di una singola cartella, creare una query WQL (Windows Query Language) per la classe di **\_ directory Win32** , assicurandosi di includere il nome della cartella.</span><span class="sxs-lookup"><span data-stu-id="6db04-433">To retrieve the properties for a single folder, construct a Windows Query Language (WQL) query for the **Win32\_Directory** class, making sure that you include the name of the folder.</span></span> <span data-ttu-id="6db04-434">Ad esempio, questa query viene associata alla cartella D: \\ Archive:</span><span class="sxs-lookup"><span data-stu-id="6db04-434">For example, this query binds to the folder D:\\Archive:</span></span>

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

<span data-ttu-id="6db04-435">Quando si specifica un nome di file o cartella in una query WQL, assicurarsi di utilizzare due barre rovesciate ( \\ \\ ) per separare i componenti del percorso.</span><span class="sxs-lookup"><span data-stu-id="6db04-435">When specifying a file or folder name in a WQL query, be sure you use two backslashes (\\\\) to separate path components.</span></span>

<span data-ttu-id="6db04-436">Se si vuole limitare il recupero dei dati a una singola unità disco, includere una clausola WHERE che specifichi la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="6db04-436">If you want to limit data retrieval to a single disk drive, include a Where clause specifying the drive letter.</span></span> <span data-ttu-id="6db04-437">Ad esempio, questa query restituisce un elenco di tutte le cartelle nell'unità C:</span><span class="sxs-lookup"><span data-stu-id="6db04-437">For example, this query returns a list of all the folders on drive C:</span></span>

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

<span data-ttu-id="6db04-438">Se è necessario enumerare tutte le cartelle in un computer, tenere presente che questa query può richiedere un tempo prolungato per il completamento.</span><span class="sxs-lookup"><span data-stu-id="6db04-438">If you need to enumerate all the folders on a computer, be aware that this query can take an extended time to complete.</span></span>

## <a name="examples"></a><span data-ttu-id="6db04-439">Esempio</span><span class="sxs-lookup"><span data-stu-id="6db04-439">Examples</span></span>

<span data-ttu-id="6db04-440">Nell'esempio VBScript seguente vengono recuperate le proprietà per la cartella C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="6db04-440">The following VBScript sample retrieves properties for the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



<span data-ttu-id="6db04-441">Nell'esempio VBScript seguente viene restituito un elenco di tutte le cartelle nascoste in un computer.</span><span class="sxs-lookup"><span data-stu-id="6db04-441">The following VBScript sample returns a list of all the hidden folders on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="6db04-442">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6db04-442">Requirements</span></span>



| <span data-ttu-id="6db04-443">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db04-443">Requirement</span></span> | <span data-ttu-id="6db04-444">Valore</span><span class="sxs-lookup"><span data-stu-id="6db04-444">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6db04-445">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6db04-445">Minimum supported client</span></span><br/> | <span data-ttu-id="6db04-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6db04-446">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6db04-447">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6db04-447">Minimum supported server</span></span><br/> | <span data-ttu-id="6db04-448">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6db04-448">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6db04-449">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6db04-449">Namespace</span></span><br/>                | <span data-ttu-id="6db04-450">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6db04-450">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6db04-451">MOF</span><span class="sxs-lookup"><span data-stu-id="6db04-451">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6db04-452"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6db04-452"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6db04-453">DLL</span><span class="sxs-lookup"><span data-stu-id="6db04-453">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6db04-454"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6db04-454"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db04-455">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6db04-455">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db04-456">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="6db04-456">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dt>

<span data-ttu-id="6db04-457">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6db04-457">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

