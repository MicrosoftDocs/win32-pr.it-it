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
# <a name="cim_directory-class"></a><span data-ttu-id="aab52-103">\_Classe Directory CIM</span><span class="sxs-lookup"><span data-stu-id="aab52-103">CIM\_Directory class</span></span>

<span data-ttu-id="aab52-104">La classe **CIM \_ directory** rappresenta un tipo di file che raggruppa logicamente i file di dati che contiene e fornisce informazioni sul percorso per i file raggruppati.</span><span class="sxs-lookup"><span data-stu-id="aab52-104">The **CIM\_Directory** class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aab52-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aab52-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aab52-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aab52-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="aab52-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aab52-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="aab52-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aab52-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aab52-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="aab52-110">Members</span><span class="sxs-lookup"><span data-stu-id="aab52-110">Members</span></span>

<span data-ttu-id="aab52-111">La classe **CIM \_ directory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aab52-111">The **CIM\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="aab52-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="aab52-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="aab52-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aab52-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aab52-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="aab52-114">Methods</span></span>

<span data-ttu-id="aab52-115">La classe **CIM \_ directory** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="aab52-115">The **CIM\_Directory** class has these methods.</span></span>



| <span data-ttu-id="aab52-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="aab52-116">Method</span></span>                                                                                           | <span data-ttu-id="aab52-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aab52-117">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aab52-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="aab52-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)     | <span data-ttu-id="aab52-119">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="aab52-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="aab52-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="aab52-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md) | <span data-ttu-id="aab52-122">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="aab52-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="aab52-124">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="aab52-124">**Compress**</span></span>](compress-method-in-class-cim-directory.md)                                       | <span data-ttu-id="aab52-125">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="aab52-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="aab52-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="aab52-127">**CompressEx**</span></span>](compressex-method-in-class-cim-directory.md)                                   | <span data-ttu-id="aab52-128">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="aab52-129">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="aab52-130">**Copia**</span><span class="sxs-lookup"><span data-stu-id="aab52-130">**Copy**</span></span>](copy-method-in-class-cim-directory.md)                                               | <span data-ttu-id="aab52-131">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="aab52-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="aab52-132">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="aab52-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="aab52-133">**CopyEx**</span></span>](copyex-method-in-class-cim-directory.md)                                           | <span data-ttu-id="aab52-134">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="aab52-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="aab52-135">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="aab52-136">**Delete**</span><span class="sxs-lookup"><span data-stu-id="aab52-136">**Delete**</span></span>](delete-method-in-class-cim-directory.md)                                           | <span data-ttu-id="aab52-137">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="aab52-138">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="aab52-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="aab52-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-directory.md)                                       | <span data-ttu-id="aab52-140">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="aab52-141">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="aab52-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="aab52-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)           | <span data-ttu-id="aab52-143">Determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di **autorizzazione** .</span><span class="sxs-lookup"><span data-stu-id="aab52-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="aab52-144">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="aab52-145">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="aab52-145">**Rename**</span></span>](rename-method-in-class-cim-directory.md)                                           | <span data-ttu-id="aab52-146">Rinomina il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="aab52-147">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="aab52-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="aab52-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-directory.md)                             | <span data-ttu-id="aab52-149">Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-149">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="aab52-150">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-150">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="aab52-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="aab52-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-directory.md)                         | <span data-ttu-id="aab52-152">Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-152">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="aab52-153">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-153">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="aab52-154">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="aab52-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-directory.md)                                   | <span data-ttu-id="aab52-155">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="aab52-156">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="aab52-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="aab52-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-directory.md)                               | <span data-ttu-id="aab52-158">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="aab52-159">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aab52-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="aab52-160">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aab52-160">Properties</span></span>

<span data-ttu-id="aab52-161">La classe di **\_ directory CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="aab52-161">The **CIM\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aab52-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="aab52-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aab52-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-165">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("diritti di accesso")</span><span class="sxs-lookup"><span data-stu-id="aab52-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-166">Maschera di maschera che rappresenta i diritti di accesso necessari per accedere o eseguire operazioni specifiche sulla directory.</span><span class="sxs-lookup"><span data-stu-id="aab52-166">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="aab52-167">Per i valori, vedere [**costanti di diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="aab52-167">For values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="aab52-168">Nei volumi FAT viene invece restituito il valore di **\_ accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="aab52-169">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-169">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="aab52-170">**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="aab52-170">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="aab52-171">**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="aab52-171">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="aab52-172">**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)</span><span class="sxs-lookup"><span data-stu-id="aab52-172">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="aab52-173">**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="aab52-173">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="aab52-174">**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="aab52-174">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="aab52-175">**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="aab52-175">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="aab52-176">**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="aab52-176">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="aab52-177">**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="aab52-177">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="aab52-178">**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="aab52-178">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="aab52-179">**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="aab52-179">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="aab52-180">**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="aab52-180">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="aab52-181">**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="aab52-181">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="aab52-182">**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="aab52-182">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="aab52-183">**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="aab52-183">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aab52-184">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="aab52-184">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-185">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aab52-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-187">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve essere archiviato")</span><span class="sxs-lookup"><span data-stu-id="aab52-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-188">Se **true**, il file deve essere archiviato.</span><span class="sxs-lookup"><span data-stu-id="aab52-188">If **True**, the file should be archived.</span></span>

<span data-ttu-id="aab52-189">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-189">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-190">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="aab52-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-193">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aab52-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-194">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-194">Short textual description of the object.</span></span>

<span data-ttu-id="aab52-195">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-196">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="aab52-196">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-197">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aab52-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-199">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compresso")</span><span class="sxs-lookup"><span data-stu-id="aab52-199">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-200">Se **true**, il file è compresso.</span><span class="sxs-lookup"><span data-stu-id="aab52-200">If **True**, the file is compressed.</span></span>

<span data-ttu-id="aab52-201">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-202">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="aab52-202">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-205">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di compressione")</span><span class="sxs-lookup"><span data-stu-id="aab52-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-206">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="aab52-206">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="aab52-207">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="aab52-207">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="aab52-208">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="aab52-208">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="aab52-209">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="aab52-209">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="aab52-210">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-210">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-211">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aab52-211">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-212">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-214">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="aab52-214">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-215">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="aab52-215">Name of the class.</span></span>

<span data-ttu-id="aab52-216">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-216">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-217">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="aab52-217">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-218">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aab52-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-220">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data creazione")</span><span class="sxs-lookup"><span data-stu-id="aab52-220">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-221">Data e ora di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="aab52-221">Date and time that the file was created.</span></span>

<span data-ttu-id="aab52-222">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-222">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-223">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aab52-223">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-226">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="aab52-226">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-227">Classe del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="aab52-227">Class of the computer system.</span></span>

<span data-ttu-id="aab52-228">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-228">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-229">**CSName**</span><span class="sxs-lookup"><span data-stu-id="aab52-229">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-232">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="aab52-232">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-233">Nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="aab52-233">Name of the computer system.</span></span>

<span data-ttu-id="aab52-234">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-235">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="aab52-235">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-238">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="aab52-238">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-239">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-239">Textual description of the object.</span></span>

<span data-ttu-id="aab52-240">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-241">**Unità**</span><span class="sxs-lookup"><span data-stu-id="aab52-241">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-244">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("unità")</span><span class="sxs-lookup"><span data-stu-id="aab52-244">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-245">Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file.</span><span class="sxs-lookup"><span data-stu-id="aab52-245">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="aab52-246">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="aab52-247">Esempio: "c:"</span><span class="sxs-lookup"><span data-stu-id="aab52-247">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="aab52-248">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="aab52-248">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-251">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("otto punto tre nome file")</span><span class="sxs-lookup"><span data-stu-id="aab52-251">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-252">Nome file compatibile con DOS.</span><span class="sxs-lookup"><span data-stu-id="aab52-252">DOS-compatible file name.</span></span> <span data-ttu-id="aab52-253">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="aab52-254">Esempio: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="aab52-254">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="aab52-255">**Crittografata**</span><span class="sxs-lookup"><span data-stu-id="aab52-255">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-256">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aab52-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-258">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="aab52-258">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-259">Se **true**, il file è crittografato.</span><span class="sxs-lookup"><span data-stu-id="aab52-259">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="aab52-260">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-261">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="aab52-261">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-262">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-264">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di crittografia")</span><span class="sxs-lookup"><span data-stu-id="aab52-264">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-265">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="aab52-265">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="aab52-266">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="aab52-266">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="aab52-267">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="aab52-267">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="aab52-268">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="aab52-268">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="aab52-269">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-270">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="aab52-270">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-271">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-273">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estensione di file")</span><span class="sxs-lookup"><span data-stu-id="aab52-273">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-274">Estensione del nome file senza il periodo precedente (punto).</span><span class="sxs-lookup"><span data-stu-id="aab52-274">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="aab52-275">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="aab52-276">Esempio: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="aab52-276">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="aab52-277">**FileName**</span><span class="sxs-lookup"><span data-stu-id="aab52-277">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-280">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")</span><span class="sxs-lookup"><span data-stu-id="aab52-280">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-281">Nome file senza l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="aab52-281">File name without the file name extension.</span></span>

<span data-ttu-id="aab52-282">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="aab52-283">Esempio: "DataFile"</span><span class="sxs-lookup"><span data-stu-id="aab52-283">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="aab52-284">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="aab52-284">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-285">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aab52-285">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-287">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="aab52-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-288">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="aab52-288">Size of the file, in bytes.</span></span>

<span data-ttu-id="aab52-289">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-289">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="aab52-290">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aab52-290">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-291">**FileType**</span><span class="sxs-lookup"><span data-stu-id="aab52-291">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-294">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di file")</span><span class="sxs-lookup"><span data-stu-id="aab52-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-295">Descrittore che rappresenta il tipo di file (indicato dalla proprietà **Extension** ).</span><span class="sxs-lookup"><span data-stu-id="aab52-295">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="aab52-296">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-296">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-297">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aab52-297">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-300">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe file System ")</span><span class="sxs-lookup"><span data-stu-id="aab52-300">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-301">Classe del file system.</span><span class="sxs-lookup"><span data-stu-id="aab52-301">Class of the file system.</span></span>

<span data-ttu-id="aab52-302">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-303">**FSName**</span><span class="sxs-lookup"><span data-stu-id="aab52-303">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-306">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome file System ")</span><span class="sxs-lookup"><span data-stu-id="aab52-306">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-307">Nome del file system.</span><span class="sxs-lookup"><span data-stu-id="aab52-307">Name of the file system.</span></span>

<span data-ttu-id="aab52-308">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-309">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="aab52-309">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-310">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aab52-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-312">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("hidden")</span><span class="sxs-lookup"><span data-stu-id="aab52-312">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-313">Se **true**, il file è nascosto.</span><span class="sxs-lookup"><span data-stu-id="aab52-313">If **True**, the file is hidden.</span></span>

<span data-ttu-id="aab52-314">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-314">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-315">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aab52-315">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-316">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aab52-316">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-318">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="aab52-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-319">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-319">Date and time when the object was installed.</span></span> <span data-ttu-id="aab52-320">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="aab52-320">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aab52-321">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-322">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="aab52-322">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-323">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aab52-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-325">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggio aperto file corrente")</span><span class="sxs-lookup"><span data-stu-id="aab52-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-326">Numero di "file aperti" attualmente attivi sul file.</span><span class="sxs-lookup"><span data-stu-id="aab52-326">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="aab52-327">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="aab52-328">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aab52-328">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-329">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="aab52-329">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-330">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aab52-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-332">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ultimo accesso")</span><span class="sxs-lookup"><span data-stu-id="aab52-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-333">Data e ora dell'ultimo accesso al file.</span><span class="sxs-lookup"><span data-stu-id="aab52-333">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="aab52-334">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-334">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-335">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="aab52-335">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-336">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aab52-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-338">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultima modifica")</span><span class="sxs-lookup"><span data-stu-id="aab52-338">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-339">Data e ora dell'Ultima modifica apportata al file.</span><span class="sxs-lookup"><span data-stu-id="aab52-339">Date and time that the file was last modified.</span></span>

<span data-ttu-id="aab52-340">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-340">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-341">**Nome**</span><span class="sxs-lookup"><span data-stu-id="aab52-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-344">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aab52-344">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aab52-345">Nome ereditato che funge da chiave di un'istanza di file logica all'interno di un file system (fornire nomi di percorso completi).</span><span class="sxs-lookup"><span data-stu-id="aab52-345">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="aab52-346">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aab52-347">Esempio: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="aab52-347">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="aab52-348">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="aab52-348">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-351">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="aab52-351">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-352">Percorso del file, incluse le barre rovesciate iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="aab52-352">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="aab52-353">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="aab52-354">Esempio: " \\ \\ sistema Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="aab52-354">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="aab52-355">**Leggibile**</span><span class="sxs-lookup"><span data-stu-id="aab52-355">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-356">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aab52-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-358">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("leggibile")</span><span class="sxs-lookup"><span data-stu-id="aab52-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-359">Se **true**, il file può essere letto.</span><span class="sxs-lookup"><span data-stu-id="aab52-359">If **True**, the file can be read.</span></span>

<span data-ttu-id="aab52-360">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-360">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-361">**Status**</span><span class="sxs-lookup"><span data-stu-id="aab52-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-362">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aab52-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-364">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="aab52-364">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-365">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aab52-365">String that indicates the current status of the object.</span></span>

<span data-ttu-id="aab52-366">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aab52-367">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="aab52-367">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aab52-368">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="aab52-368">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aab52-369">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="aab52-369">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aab52-370">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="aab52-370">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aab52-371">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="aab52-371">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aab52-372">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="aab52-372">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aab52-373">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="aab52-373">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aab52-374">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="aab52-374">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aab52-375">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="aab52-375">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aab52-376">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="aab52-376">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aab52-377">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="aab52-377">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aab52-378">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="aab52-378">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aab52-379">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="aab52-379">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aab52-380">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="aab52-380">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-381">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aab52-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-383">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file di sistema")</span><span class="sxs-lookup"><span data-stu-id="aab52-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-384">Se **true**, il file è un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="aab52-384">If **True**, the file is a system file.</span></span>

<span data-ttu-id="aab52-385">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-385">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aab52-386">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="aab52-386">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aab52-387">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aab52-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aab52-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aab52-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aab52-389">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("scrivibile")</span><span class="sxs-lookup"><span data-stu-id="aab52-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="aab52-390">Se **true**, il file può essere scritto.</span><span class="sxs-lookup"><span data-stu-id="aab52-390">If **True**, the file can be written.</span></span>

<span data-ttu-id="aab52-391">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-391">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aab52-392">Commenti</span><span class="sxs-lookup"><span data-stu-id="aab52-392">Remarks</span></span>

<span data-ttu-id="aab52-393">La classe **CIM \_ directory** è derivata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-393">The **CIM\_Directory** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="aab52-394">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="aab52-394">WMI does not implement this class.</span></span> <span data-ttu-id="aab52-395">Per ulteriori informazioni sulle classi derivate dalla **\_ directory CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aab52-395">For more information about classes derived from **CIM\_Directory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="aab52-396">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="aab52-396">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aab52-397">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="aab52-397">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab52-398">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aab52-398">Requirements</span></span>



| <span data-ttu-id="aab52-399">Requisito</span><span class="sxs-lookup"><span data-stu-id="aab52-399">Requirement</span></span> | <span data-ttu-id="aab52-400">Valore</span><span class="sxs-lookup"><span data-stu-id="aab52-400">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aab52-401">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aab52-401">Minimum supported client</span></span><br/> | <span data-ttu-id="aab52-402">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aab52-402">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aab52-403">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aab52-403">Minimum supported server</span></span><br/> | <span data-ttu-id="aab52-404">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aab52-404">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aab52-405">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aab52-405">Namespace</span></span><br/>                | <span data-ttu-id="aab52-406">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aab52-406">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aab52-407">MOF</span><span class="sxs-lookup"><span data-stu-id="aab52-407">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aab52-408"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aab52-408"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aab52-409">DLL</span><span class="sxs-lookup"><span data-stu-id="aab52-409">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aab52-410"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aab52-410"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab52-411">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aab52-411">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab52-412">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="aab52-412">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

