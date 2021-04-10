---
description: La \_ classe CIM RemoteFileSystem rappresenta una file system remota a cui si accede tramite un servizio correlato alla rete. In questo caso, l'archivio file è ospitato da un computer che funge da file server.
ms.assetid: 932970a8-0ab3-45d8-912d-c4ba7cf433b5
ms.tgt_platform: multiple
title: Classe CIM_RemoteFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoteFileSystem
- CIM_RemoteFileSystem.AvailableSpace
- CIM_RemoteFileSystem.BlockSize
- CIM_RemoteFileSystem.Caption
- CIM_RemoteFileSystem.CasePreserved
- CIM_RemoteFileSystem.CaseSensitive
- CIM_RemoteFileSystem.CodeSet
- CIM_RemoteFileSystem.CompressionMethod
- CIM_RemoteFileSystem.CreationClassName
- CIM_RemoteFileSystem.CSCreationClassName
- CIM_RemoteFileSystem.CSName
- CIM_RemoteFileSystem.Description
- CIM_RemoteFileSystem.EncryptionMethod
- CIM_RemoteFileSystem.FileSystemSize
- CIM_RemoteFileSystem.InstallDate
- CIM_RemoteFileSystem.MaxFileNameLength
- CIM_RemoteFileSystem.Name
- CIM_RemoteFileSystem.ReadOnly
- CIM_RemoteFileSystem.Root
- CIM_RemoteFileSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c29e0212ba55b37abd734fb149d118ccc693908
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126135"
---
# <a name="cim_remotefilesystem-class"></a><span data-ttu-id="e2785-104">CIM \_ RemoteFileSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="e2785-104">CIM\_RemoteFileSystem class</span></span>

<span data-ttu-id="e2785-105">La classe **CIM \_ RemoteFileSystem** rappresenta una file system remota a cui si accede tramite un servizio correlato alla rete.</span><span class="sxs-lookup"><span data-stu-id="e2785-105">The **CIM\_RemoteFileSystem** class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="e2785-106">In questo caso, l'archivio file è ospitato da un computer che funge da file server.</span><span class="sxs-lookup"><span data-stu-id="e2785-106">In this case, the file store is hosted by a computer, which acts as a file server.</span></span> <span data-ttu-id="e2785-107">L'archivio file per un file system NFS, ad esempio, non è in genere presente nei supporti controllati localmente da un computer, né accede direttamente tramite un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2785-107">For example, the file store for an NFS file system is typically not on a computer system's locally controlled media, nor is it directly accessed through a device driver.</span></span> <span data-ttu-id="e2785-108">Le sottoclassi di **\_ RemoteFileSystem CIM** contengono informazioni di configurazione sul lato client correlate all'accesso del file System.</span><span class="sxs-lookup"><span data-stu-id="e2785-108">Subclasses of **CIM\_RemoteFileSystem** contain client-side configuration information related to the access of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2785-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e2785-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e2785-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e2785-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e2785-111">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e2785-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e2785-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e2785-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2785-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2785-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F9-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_RemoteFileSystem : CIM_FileSystem
{
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  datetime InstallDate;
  uint32   MaxFileNameLength;
  string   Name;
  boolean  ReadOnly;
  string   Root;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="e2785-114">Members</span><span class="sxs-lookup"><span data-stu-id="e2785-114">Members</span></span>

<span data-ttu-id="e2785-115">La classe **CIM \_ RemoteFileSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e2785-115">The **CIM\_RemoteFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="e2785-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2785-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2785-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2785-117">Properties</span></span>

<span data-ttu-id="e2785-118">La classe **CIM \_ RemoteFileSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e2785-118">The **CIM\_RemoteFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2785-119">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="e2785-119">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-120">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2785-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-122">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Partition \| 002,4 "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="e2785-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-123">Quantità di spazio libero per il file system, in byte.</span><span class="sxs-lookup"><span data-stu-id="e2785-123">Amount of free space for the file system, in bytes.</span></span> <span data-ttu-id="e2785-124">Se è sconosciuto, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="e2785-124">If unknown, enter 0.</span></span>

<span data-ttu-id="e2785-125">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-125">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="e2785-126">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e2785-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-127">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="e2785-127">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2785-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-130">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="e2785-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-131">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e2785-131">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="e2785-132">Se è sconosciuto o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="e2785-132">If unknown, or if a block concept is not valid, (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="e2785-133">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-133">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="e2785-134">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e2785-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-135">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e2785-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-138">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e2785-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-139">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2785-139">Textual description of the object.</span></span>

<span data-ttu-id="e2785-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-141">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="e2785-141">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2785-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2785-144">Se **true**, la combinazione di maiuscole e minuscole dei nomi file viene mantenuta.</span><span class="sxs-lookup"><span data-stu-id="e2785-144">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="e2785-145">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-145">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-146">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="e2785-146">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-147">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2785-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2785-149">Se **true**, i nomi di file con distinzione tra maiuscole e minuscole sono supportati.</span><span class="sxs-lookup"><span data-stu-id="e2785-149">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="e2785-150">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-150">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-151">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="e2785-151">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-152">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2785-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2785-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2785-154">Set di caratteri o codifica supportati dal file system.</span><span class="sxs-lookup"><span data-stu-id="e2785-154">Character sets or encoding supported by the file system.</span></span> <span data-ttu-id="e2785-155">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-155">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2785-156">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e2785-156">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e2785-157">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e2785-157">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="e2785-158">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="e2785-158">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="e2785-159">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="e2785-159">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="e2785-160">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="e2785-160">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="e2785-161">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="e2785-161">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="e2785-162">**Codice UNIX esteso** (6)</span><span class="sxs-lookup"><span data-stu-id="e2785-162">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="e2785-163">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="e2785-163">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="e2785-164">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="e2785-164">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2785-165">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="e2785-165">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-168">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| partizione \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="e2785-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-169">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="e2785-169">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="e2785-170">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="e2785-170">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="e2785-171">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="e2785-171">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="e2785-172">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="e2785-172">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="e2785-173">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-174">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2785-174">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-177">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e2785-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e2785-178">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="e2785-178">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e2785-179">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="e2785-179">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e2785-180">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-180">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-181">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2785-181">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-184">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="e2785-184">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-185">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="e2785-185">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="e2785-186">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-186">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-187">**CSName**</span><span class="sxs-lookup"><span data-stu-id="e2785-187">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-190">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="e2785-190">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-191">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="e2785-191">Scoping computer system's name.</span></span>

<span data-ttu-id="e2785-192">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-192">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-193">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e2785-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-196">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e2785-196">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-197">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2785-197">Textual description of the object.</span></span>

<span data-ttu-id="e2785-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-199">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="e2785-199">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-202">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| partizione \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="e2785-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-203">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="e2785-203">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="e2785-204">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="e2785-204">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="e2785-205">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="e2785-205">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="e2785-206">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="e2785-206">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="e2785-207">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-207">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-208">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="e2785-208">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-209">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2785-209">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-211">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="e2785-211">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-212">Dimensioni totali del file system, in byte.</span><span class="sxs-lookup"><span data-stu-id="e2785-212">Total size of the file system, in bytes.</span></span> <span data-ttu-id="e2785-213">Se è sconosciuto, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="e2785-213">If unknown, enter 0.</span></span>

<span data-ttu-id="e2785-214">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-214">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="e2785-215">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e2785-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-216">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2785-216">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-217">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2785-217">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-219">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="e2785-219">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-220">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2785-220">Date and time the object was installed.</span></span> <span data-ttu-id="e2785-221">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="e2785-221">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e2785-222">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-223">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="e2785-223">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-224">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2785-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2785-226">Lunghezza massima del nome di un file all'interno del file system.</span><span class="sxs-lookup"><span data-stu-id="e2785-226">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="e2785-227">Il valore 0 indica che la lunghezza del nome file è illimitata.</span><span class="sxs-lookup"><span data-stu-id="e2785-227">A value of 0 indicates that file name length is unlimited.</span></span>

<span data-ttu-id="e2785-228">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-228">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-229">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e2785-229">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-232">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e2785-232">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-233">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="e2785-233">Label by which the object is known.</span></span> <span data-ttu-id="e2785-234">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="e2785-234">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e2785-235">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-236">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="e2785-236">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-237">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2785-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-239">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="e2785-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-240">Se **true**, il file System viene designato come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e2785-240">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="e2785-241">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-241">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-242">**Radice**</span><span class="sxs-lookup"><span data-stu-id="e2785-242">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-245">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="e2785-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-246">Nome del percorso o altre informazioni che definiscono la radice del file system.</span><span class="sxs-lookup"><span data-stu-id="e2785-246">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="e2785-247">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-247">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2785-248">**Status**</span><span class="sxs-lookup"><span data-stu-id="e2785-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2785-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2785-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2785-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2785-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2785-251">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e2785-251">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e2785-252">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2785-252">Current status of the object.</span></span>

<span data-ttu-id="e2785-253">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e2785-254">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2785-254">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e2785-255">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e2785-255">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e2785-256">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="e2785-256">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e2785-257">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="e2785-257">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2785-258">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e2785-258">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e2785-259">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="e2785-259">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e2785-260">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="e2785-260">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e2785-261">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="e2785-261">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e2785-262">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="e2785-262">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e2785-263">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="e2785-263">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e2785-264">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="e2785-264">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e2785-265">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="e2785-265">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e2785-266">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="e2785-266">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="e2785-267"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e2785-267"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e2785-268">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2785-268">Remarks</span></span>

<span data-ttu-id="e2785-269">La classe **CIM \_ RemoteFileSystem** è derivata dal [**\_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="e2785-269">The **CIM\_RemoteFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="e2785-270">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="e2785-270">WMI does not implement this class.</span></span>

<span data-ttu-id="e2785-271">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="e2785-271">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e2785-272">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="e2785-272">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2785-273">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2785-273">Requirements</span></span>



| <span data-ttu-id="e2785-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2785-274">Requirement</span></span> | <span data-ttu-id="e2785-275">Valore</span><span class="sxs-lookup"><span data-stu-id="e2785-275">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2785-276">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2785-276">Minimum supported client</span></span><br/> | <span data-ttu-id="e2785-277">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2785-277">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2785-278">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2785-278">Minimum supported server</span></span><br/> | <span data-ttu-id="e2785-279">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2785-279">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2785-280">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e2785-280">Namespace</span></span><br/>                | <span data-ttu-id="e2785-281">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e2785-281">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2785-282">MOF</span><span class="sxs-lookup"><span data-stu-id="e2785-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2785-283"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2785-283"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2785-284">DLL</span><span class="sxs-lookup"><span data-stu-id="e2785-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2785-285"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2785-285"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2785-286">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2785-286">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2785-287">**\_File System CIM**</span><span class="sxs-lookup"><span data-stu-id="e2785-287">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

