---
description: La \_ classe CIM LocalFileSystem rappresenta l'archivio file controllato da un sistema di computer tramite mezzi locali, ad esempio l'accesso diretto ai driver di dispositivo.
ms.assetid: eab52a25-ca24-4a69-b030-091603d3582c
ms.tgt_platform: multiple
title: Classe CIM_LocalFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LocalFileSystem
- CIM_LocalFileSystem.Caption
- CIM_LocalFileSystem.Description
- CIM_LocalFileSystem.InstallDate
- CIM_LocalFileSystem.Name
- CIM_LocalFileSystem.Status
- CIM_LocalFileSystem.AvailableSpace
- CIM_LocalFileSystem.BlockSize
- CIM_LocalFileSystem.CasePreserved
- CIM_LocalFileSystem.CaseSensitive
- CIM_LocalFileSystem.CodeSet
- CIM_LocalFileSystem.CompressionMethod
- CIM_LocalFileSystem.CreationClassName
- CIM_LocalFileSystem.CSCreationClassName
- CIM_LocalFileSystem.CSName
- CIM_LocalFileSystem.EncryptionMethod
- CIM_LocalFileSystem.FileSystemSize
- CIM_LocalFileSystem.MaxFileNameLength
- CIM_LocalFileSystem.ReadOnly
- CIM_LocalFileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a4a45541a651c92b45baba70828ba99c911d59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877881"
---
# <a name="cim_localfilesystem-class"></a><span data-ttu-id="cf5a1-103">CIM \_ LocalFileSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-103">CIM\_LocalFileSystem class</span></span>

<span data-ttu-id="cf5a1-104">La classe **CIM \_ LocalFileSystem** rappresenta l'archivio file controllato da un sistema di computer tramite mezzi locali, ad esempio l'accesso diretto ai driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-104">The **CIM\_LocalFileSystem** class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="cf5a1-105">L'archivio file può essere gestito direttamente dal computer, senza la necessità che un altro computer funga da file server.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-105">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="cf5a1-106">Per un file system cluster, tuttavia, il file system è locale e, di conseguenza, rinvia al cluster.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-106">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf5a1-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cf5a1-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cf5a1-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cf5a1-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf5a1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf5a1-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{5B6C820A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LocalFileSystem : CIM_FileSystem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint64   AvailableSpace;
  uint64   BlockSize;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  uint32   MaxFileNameLength;
  boolean  ReadOnly;
  string   Root;
};
```

## <a name="members"></a><span data-ttu-id="cf5a1-112">Members</span><span class="sxs-lookup"><span data-stu-id="cf5a1-112">Members</span></span>

<span data-ttu-id="cf5a1-113">La classe **CIM \_ LocalFileSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cf5a1-113">The **CIM\_LocalFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="cf5a1-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cf5a1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf5a1-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cf5a1-115">Properties</span></span>

<span data-ttu-id="cf5a1-116">La classe **CIM \_ LocalFileSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-116">The **CIM\_LocalFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf5a1-117">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-117">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-118">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-120">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Partition \| 002,4 "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-121">Quantità di spazio disponibile, in byte, per la file system.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-121">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="cf5a1-122">Se è sconosciuto, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-122">If unknown, enter 0.</span></span>

<span data-ttu-id="cf5a1-123">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-123">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="cf5a1-124">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-124">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-125">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-125">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-128">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-129">Dimensioni del blocco del file system per l'archiviazione e il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-129">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="cf5a1-130">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="cf5a1-131">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-131">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-132">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-132">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-135">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-136">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-136">A short textual description of the object.</span></span>

<span data-ttu-id="cf5a1-137">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-138">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-138">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-141">Se **true**, la combinazione di maiuscole e minuscole dei nomi file viene mantenuta.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-141">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="cf5a1-142">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-142">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-143">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-143">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-144">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-146">Se **true**, i nomi di file con distinzione tra maiuscole e minuscole sono supportati.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-146">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="cf5a1-147">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-147">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-148">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-148">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-149">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-151">Matrice che definisce i set di caratteri o la codifica supportati dal file system.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-151">Array that defines the character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="cf5a1-152">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-152">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cf5a1-153">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cf5a1-154">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="cf5a1-155">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-155">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="cf5a1-156">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-156">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="cf5a1-157">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-157">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="cf5a1-158">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-158">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="cf5a1-159">**Codice UNIX esteso** (6)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-159">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="cf5a1-160">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-160">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="cf5a1-161">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-161">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cf5a1-162">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-162">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-165">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| partizione \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-166">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-166">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="cf5a1-167">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="cf5a1-167">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="cf5a1-168">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="cf5a1-168">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="cf5a1-169">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="cf5a1-169">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="cf5a1-170">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-170">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-174">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-174">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-175">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-175">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cf5a1-176">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-176">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cf5a1-177">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-177">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-178">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-178">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-181">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-182">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-182">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="cf5a1-183">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-183">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-184">**CSName**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-184">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-187">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-187">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-188">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-188">Scoping computer system's name.</span></span>

<span data-ttu-id="cf5a1-189">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-189">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-190">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-190">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-193">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-194">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-194">A textual description of the object.</span></span>

<span data-ttu-id="cf5a1-195">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-196">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-196">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-199">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| partizione \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-200">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-200">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="cf5a1-201">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="cf5a1-201">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="cf5a1-202">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="cf5a1-202">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="cf5a1-203">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="cf5a1-203">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="cf5a1-204">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-204">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-205">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-205">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-206">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-206">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-208">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-208">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-209">Dimensioni del file system, in byte.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-209">Size of the file system, in bytes.</span></span> <span data-ttu-id="cf5a1-210">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-210">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="cf5a1-211">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-211">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="cf5a1-212">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-212">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-213">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-213">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-214">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-214">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-216">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-217">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-217">Indicates when the object was installed.</span></span> <span data-ttu-id="cf5a1-218">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-218">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cf5a1-219">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-219">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-220">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-220">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-221">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-223">Lunghezza massima del nome di un file all'interno del file system.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-223">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="cf5a1-224">Il valore 0 (zero) indica che non esiste alcun limite alla lunghezza del nome file.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-224">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

<span data-ttu-id="cf5a1-225">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-225">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-226">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-229">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-229">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-230">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-230">Label by which the object is known.</span></span> <span data-ttu-id="cf5a1-231">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-231">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cf5a1-232">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-233">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-233">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-234">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-236">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-236">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-237">Se **true**, il file System viene designato come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-237">If **TRUE**, the file system is designated as read only.</span></span>

<span data-ttu-id="cf5a1-238">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-238">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-239">**Radice**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-239">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-242">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-242">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-243">Nome del percorso o altre informazioni che definiscono la radice del file system.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-243">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="cf5a1-244">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-244">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5a1-245">**Status**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-245">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5a1-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf5a1-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5a1-248">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cf5a1-249">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-249">String that indicates the current status of the object.</span></span> <span data-ttu-id="cf5a1-250">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-250">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cf5a1-251">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="cf5a1-251">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cf5a1-252">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-252">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cf5a1-253">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="cf5a1-253">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cf5a1-254">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-254">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cf5a1-255">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-255">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cf5a1-256">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cf5a1-257">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf5a1-257">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cf5a1-258">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-258">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cf5a1-259">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-259">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cf5a1-260">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="cf5a1-260">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cf5a1-261">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-261">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cf5a1-262">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-262">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cf5a1-263">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-263">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cf5a1-264">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-264">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cf5a1-265">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-265">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cf5a1-266">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="cf5a1-266">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cf5a1-267">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-267">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cf5a1-268">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-268">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cf5a1-269">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-269">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="cf5a1-270"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cf5a1-270"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cf5a1-271">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf5a1-271">Remarks</span></span>

<span data-ttu-id="cf5a1-272">La classe **CIM \_ LocalFileSystem** è derivata dal [**\_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a1-272">The **CIM\_LocalFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="cf5a1-273">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-273">WMI does not implement this class.</span></span>

<span data-ttu-id="cf5a1-274">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-274">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cf5a1-275">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-275">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf5a1-276">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf5a1-276">Requirements</span></span>



| <span data-ttu-id="cf5a1-277">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf5a1-277">Requirement</span></span> | <span data-ttu-id="cf5a1-278">Valore</span><span class="sxs-lookup"><span data-stu-id="cf5a1-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf5a1-279">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf5a1-279">Minimum supported client</span></span><br/> | <span data-ttu-id="cf5a1-280">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf5a1-280">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf5a1-281">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf5a1-281">Minimum supported server</span></span><br/> | <span data-ttu-id="cf5a1-282">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf5a1-282">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf5a1-283">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cf5a1-283">Namespace</span></span><br/>                | <span data-ttu-id="cf5a1-284">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cf5a1-284">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf5a1-285">MOF</span><span class="sxs-lookup"><span data-stu-id="cf5a1-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf5a1-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf5a1-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf5a1-287">DLL</span><span class="sxs-lookup"><span data-stu-id="cf5a1-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf5a1-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf5a1-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf5a1-289">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf5a1-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf5a1-290">**\_File System CIM**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-290">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

