---
description: La \_ classe CIM filesystem rappresenta un file o un set di dati locale in un sistema di computer o montato in modalità remota da un file server.
ms.assetid: 5a54ab35-b9b6-49e6-96a8-cb2820b054eb
ms.tgt_platform: multiple
title: Classe CIM_FileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSystem
- CIM_FileSystem.Caption
- CIM_FileSystem.Description
- CIM_FileSystem.InstallDate
- CIM_FileSystem.Name
- CIM_FileSystem.Status
- CIM_FileSystem.AvailableSpace
- CIM_FileSystem.BlockSize
- CIM_FileSystem.CasePreserved
- CIM_FileSystem.CaseSensitive
- CIM_FileSystem.CodeSet
- CIM_FileSystem.CompressionMethod
- CIM_FileSystem.CreationClassName
- CIM_FileSystem.CSCreationClassName
- CIM_FileSystem.CSName
- CIM_FileSystem.EncryptionMethod
- CIM_FileSystem.FileSystemSize
- CIM_FileSystem.MaxFileNameLength
- CIM_FileSystem.ReadOnly
- CIM_FileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2795e76c686e8f2bb4079aee376dae397b36f510
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877898"
---
# <a name="cim_filesystem-class"></a><span data-ttu-id="2099f-103">\_Classe FileSystem CIM</span><span class="sxs-lookup"><span data-stu-id="2099f-103">CIM\_FileSystem class</span></span>

<span data-ttu-id="2099f-104">La classe **CIM \_ filesystem** rappresenta un file o un set di dati locale in un sistema di computer o montato in modalità remota da un file server.</span><span class="sxs-lookup"><span data-stu-id="2099f-104">The **CIM\_FileSystem** class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2099f-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2099f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2099f-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2099f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2099f-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2099f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2099f-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2099f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2099f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2099f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4DA18760-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_FileSystem : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="2099f-110">Members</span><span class="sxs-lookup"><span data-stu-id="2099f-110">Members</span></span>

<span data-ttu-id="2099f-111">La classe **CIM \_ filesystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2099f-111">The **CIM\_FileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="2099f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2099f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2099f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2099f-113">Properties</span></span>

<span data-ttu-id="2099f-114">La classe **CIM \_ filesystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2099f-114">The **CIM\_FileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2099f-115">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="2099f-115">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-116">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2099f-116">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-118">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Partition \| 002,4 "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="2099f-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-119">Quantità di spazio disponibile, in byte, per la file system.</span><span class="sxs-lookup"><span data-stu-id="2099f-119">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="2099f-120">Se è sconosciuto, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="2099f-120">If unknown, enter 0.</span></span>

<span data-ttu-id="2099f-121">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2099f-121">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2099f-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="2099f-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-123">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2099f-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-125">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="2099f-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-126">Dimensioni del blocco del file system per l'archiviazione e il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="2099f-126">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="2099f-127">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2099f-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2099f-128">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2099f-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-131">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2099f-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-132">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2099f-132">A short textual description of the object.</span></span>

<span data-ttu-id="2099f-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2099f-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2099f-134">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="2099f-134">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2099f-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2099f-137">Se **true**, la combinazione di maiuscole e minuscole dei nomi file viene mantenuta.</span><span class="sxs-lookup"><span data-stu-id="2099f-137">If **TRUE**, the case of file names are preserved.</span></span>

</dd> <dt>

<span data-ttu-id="2099f-138">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="2099f-138">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2099f-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2099f-141">Se **true**, i nomi di file con distinzione tra maiuscole e minuscole sono supportati.</span><span class="sxs-lookup"><span data-stu-id="2099f-141">If **TRUE**, case-sensitive file names are supported.</span></span>

</dd> <dt>

<span data-ttu-id="2099f-142">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="2099f-142">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-143">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2099f-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2099f-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2099f-145">Matrice che definisce i set di caratteri o la codifica supportati dal file system.</span><span class="sxs-lookup"><span data-stu-id="2099f-145">Array that defines the character sets or encoding supported by the file system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2099f-146">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2099f-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2099f-147">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2099f-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="2099f-148">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="2099f-148">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="2099f-149">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="2099f-149">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="2099f-150">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="2099f-150">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="2099f-151">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="2099f-151">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="2099f-152">**Codice UNIX esteso** (6)</span><span class="sxs-lookup"><span data-stu-id="2099f-152">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="2099f-153">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="2099f-153">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="2099f-154">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="2099f-154">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2099f-155">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="2099f-155">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-158">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| partizione \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="2099f-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-159">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="2099f-159">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="2099f-160">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="2099f-160">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="2099f-161">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="2099f-161">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="2099f-162">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="2099f-162">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="2099f-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2099f-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-166">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2099f-166">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2099f-167">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="2099f-167">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2099f-168">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="2099f-168">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="2099f-169">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2099f-169">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-172">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="2099f-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-173">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="2099f-173">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="2099f-174">**CSName**</span><span class="sxs-lookup"><span data-stu-id="2099f-174">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-177">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="2099f-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-178">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="2099f-178">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="2099f-179">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2099f-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-182">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2099f-182">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-183">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2099f-183">A textual description of the object.</span></span>

<span data-ttu-id="2099f-184">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2099f-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2099f-185">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="2099f-185">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-188">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| partizione \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="2099f-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-189">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="2099f-189">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="2099f-190">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="2099f-190">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="2099f-191">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="2099f-191">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="2099f-192">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="2099f-192">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="2099f-193">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="2099f-193">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-194">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2099f-194">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-196">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="2099f-196">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-197">Dimensioni del file system, in byte.</span><span class="sxs-lookup"><span data-stu-id="2099f-197">Size of the file system, in bytes.</span></span> <span data-ttu-id="2099f-198">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2099f-198">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="2099f-199">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2099f-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2099f-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2099f-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-201">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2099f-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-203">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="2099f-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-204">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="2099f-204">Indicates when the object was installed.</span></span> <span data-ttu-id="2099f-205">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="2099f-205">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2099f-206">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2099f-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2099f-207">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="2099f-207">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2099f-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2099f-210">Lunghezza massima del nome di un file all'interno del file system.</span><span class="sxs-lookup"><span data-stu-id="2099f-210">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="2099f-211">Il valore 0 (zero) indica che non esiste alcun limite alla lunghezza del nome file.</span><span class="sxs-lookup"><span data-stu-id="2099f-211">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

</dd> <dt>

<span data-ttu-id="2099f-212">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2099f-212">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-215">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2099f-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-216">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="2099f-216">Label by which the object is known.</span></span> <span data-ttu-id="2099f-217">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="2099f-217">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2099f-218">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2099f-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2099f-219">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="2099f-219">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-220">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2099f-220">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-222">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="2099f-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-223">Se **true**, il file System viene designato come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2099f-223">If **TRUE**, the file system is designated as read only.</span></span>

</dd> <dt>

<span data-ttu-id="2099f-224">**Radice**</span><span class="sxs-lookup"><span data-stu-id="2099f-224">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-227">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="2099f-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-228">Nome del percorso o altre informazioni che definiscono la radice del file system.</span><span class="sxs-lookup"><span data-stu-id="2099f-228">Path name or other information that defines the root of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="2099f-229">**Status**</span><span class="sxs-lookup"><span data-stu-id="2099f-229">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2099f-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2099f-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2099f-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2099f-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2099f-232">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2099f-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2099f-233">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2099f-233">String that indicates the current status of the object.</span></span> <span data-ttu-id="2099f-234">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="2099f-234">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2099f-235">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="2099f-235">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2099f-236">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="2099f-236">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2099f-237">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="2099f-237">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2099f-238">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="2099f-238">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2099f-239">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="2099f-239">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2099f-240">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2099f-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2099f-241">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2099f-241">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2099f-242">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2099f-242">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2099f-243">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="2099f-243">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2099f-244">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="2099f-244">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2099f-245">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2099f-245">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2099f-246">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="2099f-246">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2099f-247">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="2099f-247">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2099f-248">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="2099f-248">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2099f-249">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="2099f-249">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2099f-250">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="2099f-250">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2099f-251">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="2099f-251">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2099f-252">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="2099f-252">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2099f-253">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="2099f-253">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2099f-254"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2099f-254"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2099f-255">Commenti</span><span class="sxs-lookup"><span data-stu-id="2099f-255">Remarks</span></span>

<span data-ttu-id="2099f-256">La classe **CIM \_ filesystem** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2099f-256">The **CIM\_FileSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="2099f-257">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="2099f-257">WMI does not implement this class.</span></span>

<span data-ttu-id="2099f-258">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2099f-258">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2099f-259">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2099f-259">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2099f-260">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2099f-260">Requirements</span></span>



| <span data-ttu-id="2099f-261">Requisito</span><span class="sxs-lookup"><span data-stu-id="2099f-261">Requirement</span></span> | <span data-ttu-id="2099f-262">Valore</span><span class="sxs-lookup"><span data-stu-id="2099f-262">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2099f-263">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2099f-263">Minimum supported client</span></span><br/> | <span data-ttu-id="2099f-264">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2099f-264">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2099f-265">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2099f-265">Minimum supported server</span></span><br/> | <span data-ttu-id="2099f-266">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2099f-266">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2099f-267">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2099f-267">Namespace</span></span><br/>                | <span data-ttu-id="2099f-268">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2099f-268">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2099f-269">MOF</span><span class="sxs-lookup"><span data-stu-id="2099f-269">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2099f-270"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2099f-270"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2099f-271">DLL</span><span class="sxs-lookup"><span data-stu-id="2099f-271">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2099f-272"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2099f-272"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2099f-273">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2099f-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2099f-274">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="2099f-274">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

