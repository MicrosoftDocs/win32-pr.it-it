---
description: La \_ classe CIM DeviceFile rappresenta un tipo di file logico, che rappresenta un dispositivo.
ms.assetid: b07f039c-8ab0-4e13-96d5-3621da19e66d
ms.tgt_platform: multiple
title: Classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile
- CIM_DeviceFile.AccessMask
- CIM_DeviceFile.Archive
- CIM_DeviceFile.Caption
- CIM_DeviceFile.Compressed
- CIM_DeviceFile.CompressionMethod
- CIM_DeviceFile.CreationClassName
- CIM_DeviceFile.CreationDate
- CIM_DeviceFile.CSCreationClassName
- CIM_DeviceFile.CSName
- CIM_DeviceFile.Description
- CIM_DeviceFile.Drive
- CIM_DeviceFile.EightDotThreeFileName
- CIM_DeviceFile.Encrypted
- CIM_DeviceFile.EncryptionMethod
- CIM_DeviceFile.Extension
- CIM_DeviceFile.FileName
- CIM_DeviceFile.FileSize
- CIM_DeviceFile.FileType
- CIM_DeviceFile.FSCreationClassName
- CIM_DeviceFile.FSName
- CIM_DeviceFile.Hidden
- CIM_DeviceFile.InstallDate
- CIM_DeviceFile.InUseCount
- CIM_DeviceFile.LastAccessed
- CIM_DeviceFile.LastModified
- CIM_DeviceFile.Name
- CIM_DeviceFile.Path
- CIM_DeviceFile.Readable
- CIM_DeviceFile.Status
- CIM_DeviceFile.System
- CIM_DeviceFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 476f0ecd212247e1fc96db3efedcc0c18a6a2e06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966230"
---
# <a name="cim_devicefile-class"></a><span data-ttu-id="65dcd-103">CIM \_ DeviceFile (classe)</span><span class="sxs-lookup"><span data-stu-id="65dcd-103">CIM\_DeviceFile class</span></span>

<span data-ttu-id="65dcd-104">La classe **CIM \_ DeviceFile** rappresenta un tipo di file logico, che rappresenta un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65dcd-104">The **CIM\_DeviceFile** class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="65dcd-105">Questa convenzione è utile per i sistemi operativi che gestiscono I dispositivi usando un modello di I/O del flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="65dcd-105">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="65dcd-106">Il dispositivo logico associato a questo file viene specificato utilizzando la relazione [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="65dcd-106">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65dcd-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="65dcd-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="65dcd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="65dcd-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="65dcd-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="65dcd-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="65dcd-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65dcd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65dcd-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{4333BD60-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceFile : CIM_LogicalFile
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

## <a name="members"></a><span data-ttu-id="65dcd-112">Members</span><span class="sxs-lookup"><span data-stu-id="65dcd-112">Members</span></span>

<span data-ttu-id="65dcd-113">La classe **CIM \_ DeviceFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="65dcd-113">The **CIM\_DeviceFile** class has these types of members:</span></span>

-   [<span data-ttu-id="65dcd-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="65dcd-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="65dcd-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="65dcd-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="65dcd-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="65dcd-116">Methods</span></span>

<span data-ttu-id="65dcd-117">La classe **CIM \_ DeviceFile** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="65dcd-117">The **CIM\_DeviceFile** class has these methods.</span></span>



| <span data-ttu-id="65dcd-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="65dcd-118">Method</span></span>                                                                                            | <span data-ttu-id="65dcd-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65dcd-119">Description</span></span>                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65dcd-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="65dcd-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)     | <span data-ttu-id="65dcd-121">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="65dcd-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-122">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="65dcd-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="65dcd-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | <span data-ttu-id="65dcd-124">Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="65dcd-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-125">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="65dcd-126">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="65dcd-126">**Compress**</span></span>](compress-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="65dcd-127">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-127">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65dcd-128">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-128">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="65dcd-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="65dcd-129">**CompressEx**</span></span>](compressex-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="65dcd-130">Comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65dcd-131">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-131">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="65dcd-132">**Copia**</span><span class="sxs-lookup"><span data-stu-id="65dcd-132">**Copy**</span></span>](copy-method-in-class-cim-devicefile.md)                                               | <span data-ttu-id="65dcd-133">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="65dcd-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="65dcd-134">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-134">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="65dcd-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="65dcd-135">**CopyEx**</span></span>](copyex-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="65dcd-136">Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="65dcd-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="65dcd-137">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-137">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="65dcd-138">**Delete**</span><span class="sxs-lookup"><span data-stu-id="65dcd-138">**Delete**</span></span>](delete-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="65dcd-139">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65dcd-140">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-140">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="65dcd-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="65dcd-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="65dcd-142">Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65dcd-143">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-143">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="65dcd-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="65dcd-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)           | <span data-ttu-id="65dcd-145">Determina se il chiamante dispone delle autorizzazioni aggregate specificate dall'argomento di **autorizzazione** .</span><span class="sxs-lookup"><span data-stu-id="65dcd-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="65dcd-146">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-146">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="65dcd-147">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="65dcd-147">**Rename**</span></span>](rename-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="65dcd-148">Rinomina il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65dcd-149">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-149">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="65dcd-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="65dcd-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-devicefile.md)                             | <span data-ttu-id="65dcd-151">Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="65dcd-152">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-152">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="65dcd-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="65dcd-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-devicefile.md)                         | <span data-ttu-id="65dcd-154">Ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="65dcd-155">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-155">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="65dcd-156">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="65dcd-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="65dcd-157">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65dcd-158">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-158">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="65dcd-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="65dcd-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-devicefile.md)                               | <span data-ttu-id="65dcd-160">Decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65dcd-161">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="65dcd-161">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="65dcd-162">Proprietà</span><span class="sxs-lookup"><span data-stu-id="65dcd-162">Properties</span></span>

<span data-ttu-id="65dcd-163">La classe **CIM \_ DeviceFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="65dcd-163">The **CIM\_DeviceFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65dcd-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="65dcd-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="65dcd-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-167">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("diritti di accesso")</span><span class="sxs-lookup"><span data-stu-id="65dcd-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-168">Matrice di bit che rappresenta i diritti di accesso al file o alla directory specificata dall'utente o dal gruppo per conto del quale viene restituita l'istanza.</span><span class="sxs-lookup"><span data-stu-id="65dcd-168">Bit array that represents the access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="65dcd-169">Nei volumi FAT viene **restituito \_ l'accesso completo** , che indica che non è stata impostata alcuna sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-169">On FAT volumes, **FULL\_ACCESS** is returned, which indicates that no security has been set on the object.</span></span>

<span data-ttu-id="65dcd-170">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-170">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="65dcd-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="65dcd-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-172">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-172">Grants the right to read data from the file.</span></span> <span data-ttu-id="65dcd-173">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="65dcd-173">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="65dcd-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="65dcd-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-175">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-175">Grants the right to write data to the file.</span></span> <span data-ttu-id="65dcd-176">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="65dcd-176">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="65dcd-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)</span><span class="sxs-lookup"><span data-stu-id="65dcd-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-178">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-178">Grants the right to append data to the file.</span></span> <span data-ttu-id="65dcd-179">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="65dcd-179">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="65dcd-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="65dcd-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-181">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="65dcd-181">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="65dcd-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="65dcd-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-183">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="65dcd-183">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="65dcd-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="65dcd-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-185">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-185">Grants the right to execute a file.</span></span> <span data-ttu-id="65dcd-186">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="65dcd-186">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="65dcd-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="65dcd-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-188">Concede il diritto di eliminare una directory e tutti i file in esso contenuti (elementi figlio), anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="65dcd-188">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="65dcd-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="65dcd-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-190">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-190">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="65dcd-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="65dcd-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-192">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-192">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="65dcd-193"><span id="DELETE"></span><span id="delete"></span>**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="65dcd-193"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-194">Concede l'accesso DELETE.</span><span class="sxs-lookup"><span data-stu-id="65dcd-194">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="65dcd-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="65dcd-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-196">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="65dcd-196">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="65dcd-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="65dcd-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-198">Concede l'accesso in scrittura all'ACL discrezionale.</span><span class="sxs-lookup"><span data-stu-id="65dcd-198">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="65dcd-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="65dcd-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-200">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="65dcd-200">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="65dcd-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="65dcd-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="65dcd-202">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="65dcd-202">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="65dcd-203">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="65dcd-203">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-204">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="65dcd-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-206">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve essere archiviato")</span><span class="sxs-lookup"><span data-stu-id="65dcd-206">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-207">Se **true**, il file deve essere archiviato.</span><span class="sxs-lookup"><span data-stu-id="65dcd-207">If **True**, the file should be archived.</span></span>

<span data-ttu-id="65dcd-208">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-209">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="65dcd-209">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-212">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="65dcd-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-213">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-213">Short textual description of the object.</span></span>

<span data-ttu-id="65dcd-214">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-215">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="65dcd-215">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-216">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="65dcd-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-218">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compresso")</span><span class="sxs-lookup"><span data-stu-id="65dcd-218">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-219">Se **true**, il file è compresso.</span><span class="sxs-lookup"><span data-stu-id="65dcd-219">If **True**, the file is compressed.</span></span>

<span data-ttu-id="65dcd-220">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-221">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="65dcd-221">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-224">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di compressione")</span><span class="sxs-lookup"><span data-stu-id="65dcd-224">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-225">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="65dcd-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="65dcd-226">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="65dcd-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="65dcd-227">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="65dcd-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="65dcd-228">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="65dcd-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="65dcd-229">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-229">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-230">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="65dcd-230">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-233">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="65dcd-233">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-234">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="65dcd-234">Name of the class.</span></span>

<span data-ttu-id="65dcd-235">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-235">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-236">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="65dcd-236">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-237">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65dcd-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-239">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data creazione")</span><span class="sxs-lookup"><span data-stu-id="65dcd-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-240">Data di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-240">File's creation date.</span></span>

<span data-ttu-id="65dcd-241">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-242">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="65dcd-242">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-245">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="65dcd-245">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-246">Classe del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="65dcd-246">Class of the computer system.</span></span>

<span data-ttu-id="65dcd-247">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-247">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-248">**CSName**</span><span class="sxs-lookup"><span data-stu-id="65dcd-248">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-251">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="65dcd-251">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-252">Nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="65dcd-252">Name of the computer system.</span></span>

<span data-ttu-id="65dcd-253">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-254">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="65dcd-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-257">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="65dcd-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-258">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-258">Textual description of the object.</span></span>

<span data-ttu-id="65dcd-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-260">**Unità**</span><span class="sxs-lookup"><span data-stu-id="65dcd-260">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-263">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("unità")</span><span class="sxs-lookup"><span data-stu-id="65dcd-263">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-264">Lettera di unità (inclusi i due punti che seguono la lettera di unità) del file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-264">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="65dcd-265">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65dcd-266">Esempio: "c:"</span><span class="sxs-lookup"><span data-stu-id="65dcd-266">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-267">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="65dcd-267">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-268">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-270">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("otto punto tre nome file")</span><span class="sxs-lookup"><span data-stu-id="65dcd-270">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-271">Nome file compatibile con DOS per il file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-271">DOS-compatible file name for the file.</span></span> <span data-ttu-id="65dcd-272">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65dcd-273">Esempio: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="65dcd-273">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-274">**Crittografata**</span><span class="sxs-lookup"><span data-stu-id="65dcd-274">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-275">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="65dcd-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-277">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="65dcd-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-278">Se **true**, il file è crittografato.</span><span class="sxs-lookup"><span data-stu-id="65dcd-278">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="65dcd-279">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-280">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="65dcd-280">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-283">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("metodo di crittografia")</span><span class="sxs-lookup"><span data-stu-id="65dcd-283">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-284">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="65dcd-284">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="65dcd-285">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="65dcd-285">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="65dcd-286">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="65dcd-286">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="65dcd-287">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="65dcd-287">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="65dcd-288">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-289">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="65dcd-289">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-290">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-292">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estensione di file")</span><span class="sxs-lookup"><span data-stu-id="65dcd-292">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-293">Estensione del nome file senza il periodo precedente (punto).</span><span class="sxs-lookup"><span data-stu-id="65dcd-293">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="65dcd-294">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65dcd-295">Esempio: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="65dcd-295">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-296">**FileName**</span><span class="sxs-lookup"><span data-stu-id="65dcd-296">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-299">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome file")</span><span class="sxs-lookup"><span data-stu-id="65dcd-299">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-300">Nome file senza l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-300">File name without the file name extension.</span></span>

<span data-ttu-id="65dcd-301">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65dcd-302">Esempio: "DataFile"</span><span class="sxs-lookup"><span data-stu-id="65dcd-302">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-303">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="65dcd-303">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-304">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65dcd-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-306">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="65dcd-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-307">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="65dcd-307">Size of the file, in bytes.</span></span>

<span data-ttu-id="65dcd-308">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65dcd-309">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="65dcd-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-310">**FileType**</span><span class="sxs-lookup"><span data-stu-id="65dcd-310">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-311">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-313">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di file")</span><span class="sxs-lookup"><span data-stu-id="65dcd-313">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-314">Descrittore che rappresenta il tipo di file (indicato dalla proprietà **Extension** ).</span><span class="sxs-lookup"><span data-stu-id="65dcd-314">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="65dcd-315">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-315">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-316">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="65dcd-316">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-319">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe file System ")</span><span class="sxs-lookup"><span data-stu-id="65dcd-319">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-320">Classe del file system.</span><span class="sxs-lookup"><span data-stu-id="65dcd-320">Class of the file system.</span></span>

<span data-ttu-id="65dcd-321">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-321">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-322">**FSName**</span><span class="sxs-lookup"><span data-stu-id="65dcd-322">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-323">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-325">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ file System CIM**](cim-filesystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome file System ")</span><span class="sxs-lookup"><span data-stu-id="65dcd-325">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-326">Nome del file system.</span><span class="sxs-lookup"><span data-stu-id="65dcd-326">Name of the file system.</span></span>

<span data-ttu-id="65dcd-327">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-328">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="65dcd-328">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-329">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="65dcd-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-331">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("hidden")</span><span class="sxs-lookup"><span data-stu-id="65dcd-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-332">Se **true**, il file è nascosto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-332">If **True**, the file is hidden.</span></span>

<span data-ttu-id="65dcd-333">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-333">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="65dcd-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-335">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65dcd-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="65dcd-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-338">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-338">Date and time when the object was installed.</span></span> <span data-ttu-id="65dcd-339">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="65dcd-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="65dcd-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-341">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="65dcd-341">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-342">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65dcd-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-344">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("conteggio aperto file corrente")</span><span class="sxs-lookup"><span data-stu-id="65dcd-344">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-345">Numero di "file aperti" attualmente attivi sul file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-345">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="65dcd-346">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-346">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65dcd-347">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="65dcd-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-348">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="65dcd-348">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-349">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65dcd-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-351">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ultimo accesso")</span><span class="sxs-lookup"><span data-stu-id="65dcd-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-352">Data e ora dell'ultimo accesso al file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-352">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="65dcd-353">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-354">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="65dcd-354">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-355">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65dcd-355">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-357">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Ultima modifica")</span><span class="sxs-lookup"><span data-stu-id="65dcd-357">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-358">Data e ora dell'Ultima modifica apportata al file.</span><span class="sxs-lookup"><span data-stu-id="65dcd-358">Date and time that the file was last modified.</span></span>

<span data-ttu-id="65dcd-359">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-359">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-360">**Nome**</span><span class="sxs-lookup"><span data-stu-id="65dcd-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-363">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65dcd-363">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-364">Nome ereditato che funge da chiave di un'istanza di file logica all'interno di un file system (fornire nomi di percorso completi).</span><span class="sxs-lookup"><span data-stu-id="65dcd-364">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="65dcd-365">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="65dcd-366">Esempio: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="65dcd-366">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-367">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="65dcd-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-368">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-370">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="65dcd-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-371">Percorso del file, incluse le barre rovesciate iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="65dcd-371">Path of the file including leading and trailing backslashes.</span></span> <span data-ttu-id="65dcd-372">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-372">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65dcd-373">Esempio: " \\ \\ sistema Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="65dcd-373">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-374">**Leggibile**</span><span class="sxs-lookup"><span data-stu-id="65dcd-374">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-375">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="65dcd-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-377">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("leggibile")</span><span class="sxs-lookup"><span data-stu-id="65dcd-377">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-378">Se **true**, il file può essere letto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-378">If **True**, the file can be read.</span></span>

<span data-ttu-id="65dcd-379">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-379">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-380">**Status**</span><span class="sxs-lookup"><span data-stu-id="65dcd-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="65dcd-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-383">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="65dcd-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-384">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="65dcd-385">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="65dcd-385">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="65dcd-386">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="65dcd-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="65dcd-387">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="65dcd-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="65dcd-388">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="65dcd-388">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="65dcd-389">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="65dcd-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="65dcd-390">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="65dcd-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="65dcd-391">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="65dcd-392">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="65dcd-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="65dcd-393">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="65dcd-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="65dcd-394">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="65dcd-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="65dcd-395">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="65dcd-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="65dcd-396">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="65dcd-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="65dcd-397">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="65dcd-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="65dcd-398">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="65dcd-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="65dcd-399">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="65dcd-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="65dcd-400">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="65dcd-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="65dcd-401">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="65dcd-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="65dcd-402">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="65dcd-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="65dcd-403">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="65dcd-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="65dcd-404">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="65dcd-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="65dcd-405">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="65dcd-405">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-406">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="65dcd-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-408">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file di sistema")</span><span class="sxs-lookup"><span data-stu-id="65dcd-408">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-409">Se **true**, il file è un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="65dcd-409">If **True**, the file is a system file.</span></span>

<span data-ttu-id="65dcd-410">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65dcd-411">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="65dcd-411">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dcd-412">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="65dcd-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="65dcd-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dcd-414">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("scrivibile")</span><span class="sxs-lookup"><span data-stu-id="65dcd-414">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="65dcd-415">Se **true**, il file può essere scritto.</span><span class="sxs-lookup"><span data-stu-id="65dcd-415">If **True**, the file can be written.</span></span>

<span data-ttu-id="65dcd-416">Questa proprietà viene ereditata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-416">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65dcd-417">Commenti</span><span class="sxs-lookup"><span data-stu-id="65dcd-417">Remarks</span></span>

<span data-ttu-id="65dcd-418">La classe **CIM \_ DeviceFile** è derivata da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65dcd-418">The **CIM\_DeviceFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65dcd-419">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="65dcd-419">WMI does not implement this class.</span></span>

<span data-ttu-id="65dcd-420">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="65dcd-420">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="65dcd-421">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="65dcd-421">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="65dcd-422">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65dcd-422">Requirements</span></span>



| <span data-ttu-id="65dcd-423">Requisito</span><span class="sxs-lookup"><span data-stu-id="65dcd-423">Requirement</span></span> | <span data-ttu-id="65dcd-424">Valore</span><span class="sxs-lookup"><span data-stu-id="65dcd-424">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65dcd-425">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65dcd-425">Minimum supported client</span></span><br/> | <span data-ttu-id="65dcd-426">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65dcd-426">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65dcd-427">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65dcd-427">Minimum supported server</span></span><br/> | <span data-ttu-id="65dcd-428">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65dcd-428">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65dcd-429">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="65dcd-429">Namespace</span></span><br/>                | <span data-ttu-id="65dcd-430">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="65dcd-430">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65dcd-431">MOF</span><span class="sxs-lookup"><span data-stu-id="65dcd-431">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65dcd-432"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65dcd-432"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65dcd-433">DLL</span><span class="sxs-lookup"><span data-stu-id="65dcd-433">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65dcd-434"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65dcd-434"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65dcd-435">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65dcd-435">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65dcd-436">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="65dcd-436">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

