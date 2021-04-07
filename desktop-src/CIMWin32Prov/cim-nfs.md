---
description: La \_ classe CIM NFS rappresenta una file system remota montata usando il protocollo di rete file System (NFS), da un sistema di computer.
ms.assetid: 24eba28f-fbd5-4aa3-a7c7-a611269d55ac
ms.tgt_platform: multiple
title: Classe CIM_NFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NFS
- CIM_NFS.AttributeCaching
- CIM_NFS.AttributeCachingForDirectoriesMax
- CIM_NFS.AttributeCachingForDirectoriesMin
- CIM_NFS.AttributeCachingForRegularFilesMax
- CIM_NFS.AttributeCachingForRegularFilesMin
- CIM_NFS.AvailableSpace
- CIM_NFS.BlockSize
- CIM_NFS.Caption
- CIM_NFS.CasePreserved
- CIM_NFS.CaseSensitive
- CIM_NFS.CodeSet
- CIM_NFS.CompressionMethod
- CIM_NFS.CreationClassName
- CIM_NFS.CSCreationClassName
- CIM_NFS.CSName
- CIM_NFS.Description
- CIM_NFS.EncryptionMethod
- CIM_NFS.FileSystemSize
- CIM_NFS.ForegroundMount
- CIM_NFS.HardMount
- CIM_NFS.InstallDate
- CIM_NFS.Interrupt
- CIM_NFS.MaxFileNameLength
- CIM_NFS.MountFailureRetries
- CIM_NFS.Name
- CIM_NFS.ReadBufferSize
- CIM_NFS.ReadOnly
- CIM_NFS.RetransmissionAttempts
- CIM_NFS.RetransmissionTimeout
- CIM_NFS.Root
- CIM_NFS.ServerCommunicationPort
- CIM_NFS.Status
- CIM_NFS.WriteBufferSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0dcfb44fdcd035ca47cbe3056da2a081ef2ae07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748586"
---
# <a name="cim_nfs-class"></a><span data-ttu-id="530cb-103">\_Classe CIM NFS</span><span class="sxs-lookup"><span data-stu-id="530cb-103">CIM\_NFS class</span></span>

<span data-ttu-id="530cb-104">La classe **CIM \_ NFS** rappresenta una file system remota montata usando il protocollo di rete file System (NFS), da un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="530cb-104">The **CIM\_NFS** class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span> <span data-ttu-id="530cb-105">Le proprietà dell'oggetto NFS corrispondono agli aspetti operativi del montaggio e rappresentano la configurazione sul lato client per l'accesso a NFS.</span><span class="sxs-lookup"><span data-stu-id="530cb-105">The properties of the NFS object correspond to the operational aspects of the mount and represent the client-side configuration for NFS access.</span></span> <span data-ttu-id="530cb-106">Il tipo di file system deve essere impostato in modo da indicare il tipo di file system visualizzato al client.</span><span class="sxs-lookup"><span data-stu-id="530cb-106">The file system type should be set to indicate the type of file system as it appears to the client.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="530cb-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="530cb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="530cb-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="530cb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="530cb-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="530cb-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="530cb-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="530cb-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="530cb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="530cb-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FB-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_NFS : CIM_RemoteFileSystem
{
  boolean  AttributeCaching;
  uint16   AttributeCachingForDirectoriesMax;
  uint16   AttributeCachingForDirectoriesMin;
  uint16   AttributeCachingForRegularFilesMax;
  uint16   AttributeCachingForRegularFilesMin;
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
  boolean  ForegroundMount;
  boolean  HardMount;
  datetime InstallDate;
  boolean  Interrupt;
  uint32   MaxFileNameLength;
  uint16   MountFailureRetries;
  string   Name;
  uint64   ReadBufferSize;
  boolean  ReadOnly;
  uint16   RetransmissionAttempts;
  uint32   RetransmissionTimeout;
  string   Root;
  uint32   ServerCommunicationPort;
  string   Status;
  uint64   WriteBufferSize;
};
```

## <a name="members"></a><span data-ttu-id="530cb-112">Members</span><span class="sxs-lookup"><span data-stu-id="530cb-112">Members</span></span>

<span data-ttu-id="530cb-113">La classe **CIM \_ NFS** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="530cb-113">The **CIM\_NFS** class has these types of members:</span></span>

-   [<span data-ttu-id="530cb-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="530cb-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="530cb-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="530cb-115">Properties</span></span>

<span data-ttu-id="530cb-116">La classe **CIM \_ NFS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="530cb-116">The **CIM\_NFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="530cb-117">**AttributeCaching**</span><span class="sxs-lookup"><span data-stu-id="530cb-117">**AttributeCaching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-118">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="530cb-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-120">Se **true**, la memorizzazione degli attributi di controllo è abilitata.</span><span class="sxs-lookup"><span data-stu-id="530cb-120">If **TRUE**, control attribute caching is enabled.</span></span> <span data-ttu-id="530cb-121">Se **false**, la memorizzazione nella cache degli attributi di controllo è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="530cb-121">If **FALSE**, control attribute caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-122">**AttributeCachingForDirectoriesMax**</span><span class="sxs-lookup"><span data-stu-id="530cb-122">**AttributeCachingForDirectoriesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-123">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="530cb-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-125">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="530cb-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-126">Numero massimo di secondi durante i quali gli attributi memorizzati nella cache vengono mantenuti dopo l'aggiornamento della directory.</span><span class="sxs-lookup"><span data-stu-id="530cb-126">Maximum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-127">**AttributeCachingForDirectoriesMin**</span><span class="sxs-lookup"><span data-stu-id="530cb-127">**AttributeCachingForDirectoriesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="530cb-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-130">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="530cb-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-131">Numero minimo di secondi durante i quali gli attributi memorizzati nella cache vengono mantenuti dopo l'aggiornamento della directory.</span><span class="sxs-lookup"><span data-stu-id="530cb-131">Minimum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-132">**AttributeCachingForRegularFilesMax**</span><span class="sxs-lookup"><span data-stu-id="530cb-132">**AttributeCachingForRegularFilesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="530cb-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-135">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="530cb-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-136">Numero massimo di secondi durante i quali gli attributi memorizzati nella cache vengono mantenuti dopo la modifica dei file.</span><span class="sxs-lookup"><span data-stu-id="530cb-136">Maximum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-137">**AttributeCachingForRegularFilesMin**</span><span class="sxs-lookup"><span data-stu-id="530cb-137">**AttributeCachingForRegularFilesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-138">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="530cb-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-140">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="530cb-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-141">Numero minimo di secondi durante i quali gli attributi memorizzati nella cache vengono mantenuti dopo la modifica dei file.</span><span class="sxs-lookup"><span data-stu-id="530cb-141">Minimum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-142">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="530cb-142">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="530cb-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-145">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Partition \| 002,4 "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="530cb-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-146">Quantità totale di spazio disponibile, in byte, per la file system.</span><span class="sxs-lookup"><span data-stu-id="530cb-146">Total amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="530cb-147">Se è sconosciuto, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="530cb-147">If unknown, enter 0.</span></span>

<span data-ttu-id="530cb-148">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-148">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="530cb-149">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="530cb-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-150">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="530cb-150">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-151">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="530cb-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-153">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="530cb-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-154">I file System possono leggere o scrivere dati in blocchi definiti indipendentemente dagli extent di archiviazione sottostanti.</span><span class="sxs-lookup"><span data-stu-id="530cb-154">File systems can read or write data in blocks that are defined independently of the underlying storage extents.</span></span> <span data-ttu-id="530cb-155">Questa proprietà acquisisce le dimensioni del blocco del file system per l'archiviazione e il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="530cb-155">This property captures the file system's block size for data storage and retrieval.</span></span>

<span data-ttu-id="530cb-156">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-156">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="530cb-157">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="530cb-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-158">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="530cb-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-161">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="530cb-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-162">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="530cb-162">Short textual description of the object.</span></span>

<span data-ttu-id="530cb-163">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-164">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="530cb-164">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-165">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="530cb-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-167">Se **true**, la combinazione di maiuscole e minuscole dei nomi file viene mantenuta.</span><span class="sxs-lookup"><span data-stu-id="530cb-167">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="530cb-168">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-168">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-169">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="530cb-169">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-170">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="530cb-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-172">Se **true**, i nomi di file con distinzione tra maiuscole e minuscole sono supportati.</span><span class="sxs-lookup"><span data-stu-id="530cb-172">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="530cb-173">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-174">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="530cb-174">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-175">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="530cb-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="530cb-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-177">Set di caratteri o codifica supportati dal file system.</span><span class="sxs-lookup"><span data-stu-id="530cb-177">Character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="530cb-178">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-178">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="530cb-179">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="530cb-179">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="530cb-180">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="530cb-180">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="530cb-181">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="530cb-181">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="530cb-182">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="530cb-182">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="530cb-183">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="530cb-183">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="530cb-184">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="530cb-184">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="530cb-185">**Codice UNIX esteso** (6)</span><span class="sxs-lookup"><span data-stu-id="530cb-185">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="530cb-186">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="530cb-186">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="530cb-187">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="530cb-187">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="530cb-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="530cb-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-191">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| partizione \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="530cb-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-192">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="530cb-192">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="530cb-193">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="530cb-193">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="530cb-194">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="530cb-194">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="530cb-195">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="530cb-195">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="530cb-196">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-196">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="530cb-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-200">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="530cb-200">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="530cb-201">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="530cb-201">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="530cb-202">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="530cb-202">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="530cb-203">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-203">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-204">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="530cb-204">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-207">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="530cb-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-208">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="530cb-208">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="530cb-209">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-209">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-210">**CSName**</span><span class="sxs-lookup"><span data-stu-id="530cb-210">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-213">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="530cb-213">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-214">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="530cb-214">Scoping computer system's name.</span></span>

<span data-ttu-id="530cb-215">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-215">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-216">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="530cb-216">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-219">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="530cb-219">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-220">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="530cb-220">Textual description of the object.</span></span>

<span data-ttu-id="530cb-221">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-222">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="530cb-222">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-225">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| partizione \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="530cb-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-226">Stringa in formato libero che identifica l'algoritmo o lo strumento utilizzato per crittografare un file logico.</span><span class="sxs-lookup"><span data-stu-id="530cb-226">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="530cb-227">Se lo schema di crittografia non è adatto (per motivi di sicurezza, ad esempio), usare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="530cb-227">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="530cb-228">Se il file è crittografato, ma lo schema di crittografia è sconosciuto o non è stato divulgato, usare "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="530cb-228">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="530cb-229">Se il file logico non è crittografato, utilizzare "non crittografato".</span><span class="sxs-lookup"><span data-stu-id="530cb-229">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="530cb-230">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-230">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-231">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="530cb-231">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-232">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="530cb-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-234">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="530cb-234">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-235">Dimensioni totali del file system, in byte.</span><span class="sxs-lookup"><span data-stu-id="530cb-235">Total size of the file system, in bytes.</span></span> <span data-ttu-id="530cb-236">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="530cb-236">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="530cb-237">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-237">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="530cb-238">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="530cb-238">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-239">**ForegroundMount**</span><span class="sxs-lookup"><span data-stu-id="530cb-239">**ForegroundMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-240">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="530cb-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-242">Se **true**, i tentativi vengono eseguiti in primo piano.</span><span class="sxs-lookup"><span data-stu-id="530cb-242">If **TRUE**, retries are performed in the foreground.</span></span> <span data-ttu-id="530cb-243">Se **false** e il primo tentativo di montaggio ha esito negativo, i tentativi vengono eseguiti in background.</span><span class="sxs-lookup"><span data-stu-id="530cb-243">If **FALSE**, and the first mount attempt fails, retries are performed in the background.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-244">**HardMount**</span><span class="sxs-lookup"><span data-stu-id="530cb-244">**HardMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-245">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="530cb-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-247">Se **true**, dopo l'installazione del file System, le richieste NFS vengono ritentate fino a quando il sistema host non risponde.</span><span class="sxs-lookup"><span data-stu-id="530cb-247">If **TRUE**, after the file system is mounted, NFS requests are retried until the hosting system responds.</span></span> <span data-ttu-id="530cb-248">Se **false**, dopo che il file System è stato montato, viene restituito un errore se il sistema host non risponde.</span><span class="sxs-lookup"><span data-stu-id="530cb-248">If **FALSE**, after the file system is mounted, an error is returned if the hosting system does not respond.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="530cb-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-250">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="530cb-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-252">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="530cb-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-253">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="530cb-253">Date and time the object was installed.</span></span> <span data-ttu-id="530cb-254">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="530cb-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="530cb-255">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-256">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="530cb-256">**Interrupt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-257">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="530cb-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-259">Se **true**, gli interrupt sono consentiti per i montaggi reali.</span><span class="sxs-lookup"><span data-stu-id="530cb-259">If **TRUE**, interrupts are permitted for hard mounts.</span></span> <span data-ttu-id="530cb-260">Se **false**, gli interrupt vengono ignorati per i montaggi reali.</span><span class="sxs-lookup"><span data-stu-id="530cb-260">If **FALSE**, interrupts are ignored for hard mounts.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-261">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="530cb-261">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-262">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="530cb-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-264">Lunghezza massima del nome di un file all'interno del file system.</span><span class="sxs-lookup"><span data-stu-id="530cb-264">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="530cb-265">Il valore 0 (zero) indica che non esiste alcun limite per la lunghezza del nome file.</span><span class="sxs-lookup"><span data-stu-id="530cb-265">A value of 0 (zero)indicates that there is no limit for file name length.</span></span>

<span data-ttu-id="530cb-266">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-266">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-267">**MountFailureRetries**</span><span class="sxs-lookup"><span data-stu-id="530cb-267">**MountFailureRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-268">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="530cb-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-270">Numero massimo di tentativi di errore di montaggio consentiti.</span><span class="sxs-lookup"><span data-stu-id="530cb-270">Maximum number of mount failure retries that are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-271">**Nome**</span><span class="sxs-lookup"><span data-stu-id="530cb-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-272">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-274">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="530cb-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-275">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="530cb-275">Label by which the object is known.</span></span> <span data-ttu-id="530cb-276">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="530cb-276">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="530cb-277">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-277">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-278">**ReadBufferSize**</span><span class="sxs-lookup"><span data-stu-id="530cb-278">**ReadBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-279">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="530cb-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-281">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="530cb-281">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-282">Dimensioni del buffer di lettura, in byte.</span><span class="sxs-lookup"><span data-stu-id="530cb-282">Read buffer size, in bytes.</span></span>

<span data-ttu-id="530cb-283">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="530cb-283">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-284">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="530cb-284">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-285">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="530cb-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-287">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="530cb-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-288">Se **true**, il file System viene designato come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="530cb-288">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="530cb-289">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-289">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-290">**RetransmissionAttempts**</span><span class="sxs-lookup"><span data-stu-id="530cb-290">**RetransmissionAttempts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-291">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="530cb-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-293">Numero massimo di ritrasmissioni NFS consentite.</span><span class="sxs-lookup"><span data-stu-id="530cb-293">Maximum number of NFS retransmissions allowed.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-294">**RetransmissionTimeout**</span><span class="sxs-lookup"><span data-stu-id="530cb-294">**RetransmissionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-295">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="530cb-295">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-297">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("decimi di secondi")</span><span class="sxs-lookup"><span data-stu-id="530cb-297">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of seconds")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-298">Timeout NFS, in decimi di secondo.</span><span class="sxs-lookup"><span data-stu-id="530cb-298">NFS time-out, in tenths of a second.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-299">**Radice**</span><span class="sxs-lookup"><span data-stu-id="530cb-299">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-302">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="530cb-302">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-303">Nome del percorso o altre informazioni che definiscono la radice del file system.</span><span class="sxs-lookup"><span data-stu-id="530cb-303">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="530cb-304">Questa proprietà viene ereditata [**dal \_ file System CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-304">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="530cb-305">**ServerCommunicationPort**</span><span class="sxs-lookup"><span data-stu-id="530cb-305">**ServerCommunicationPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-306">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="530cb-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="530cb-308">Numero di porta UDP del sistema del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="530cb-308">Remote computer system's UDP port number.</span></span>

</dd> <dt>

<span data-ttu-id="530cb-309">**Status**</span><span class="sxs-lookup"><span data-stu-id="530cb-309">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cb-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-312">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="530cb-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-313">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="530cb-313">Current status of the object.</span></span>

<span data-ttu-id="530cb-314">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="530cb-315">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="530cb-315">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="530cb-316">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="530cb-316">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="530cb-317">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="530cb-317">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="530cb-318">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="530cb-318">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="530cb-319">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="530cb-319">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="530cb-320">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="530cb-320">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="530cb-321">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="530cb-321">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="530cb-322">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="530cb-322">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="530cb-323">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="530cb-323">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="530cb-324">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="530cb-324">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="530cb-325">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="530cb-325">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="530cb-326">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="530cb-326">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="530cb-327">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="530cb-327">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="530cb-328">**WriteBufferSize**</span><span class="sxs-lookup"><span data-stu-id="530cb-328">**WriteBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cb-329">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="530cb-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="530cb-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cb-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cb-331">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="530cb-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="530cb-332">Dimensioni del buffer di scrittura, in byte.</span><span class="sxs-lookup"><span data-stu-id="530cb-332">Write buffer size, in bytes.</span></span>

<span data-ttu-id="530cb-333">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="530cb-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="530cb-334">Commenti</span><span class="sxs-lookup"><span data-stu-id="530cb-334">Remarks</span></span>

<span data-ttu-id="530cb-335">La classe **CIM \_ NFS** è derivata da [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md).</span><span class="sxs-lookup"><span data-stu-id="530cb-335">The **CIM\_NFS** class is derived from [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md).</span></span>

<span data-ttu-id="530cb-336">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="530cb-336">WMI does not implement this class.</span></span>

<span data-ttu-id="530cb-337">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="530cb-337">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="530cb-338">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="530cb-338">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="530cb-339">Requisiti</span><span class="sxs-lookup"><span data-stu-id="530cb-339">Requirements</span></span>



| <span data-ttu-id="530cb-340">Requisito</span><span class="sxs-lookup"><span data-stu-id="530cb-340">Requirement</span></span> | <span data-ttu-id="530cb-341">Valore</span><span class="sxs-lookup"><span data-stu-id="530cb-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="530cb-342">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="530cb-342">Minimum supported client</span></span><br/> | <span data-ttu-id="530cb-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="530cb-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="530cb-344">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="530cb-344">Minimum supported server</span></span><br/> | <span data-ttu-id="530cb-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="530cb-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="530cb-346">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="530cb-346">Namespace</span></span><br/>                | <span data-ttu-id="530cb-347">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="530cb-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="530cb-348">MOF</span><span class="sxs-lookup"><span data-stu-id="530cb-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="530cb-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="530cb-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="530cb-350">DLL</span><span class="sxs-lookup"><span data-stu-id="530cb-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="530cb-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="530cb-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530cb-352">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="530cb-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530cb-353">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="530cb-353">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> </dl>

 

