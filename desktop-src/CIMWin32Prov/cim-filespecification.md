---
description: La \_ classe CIM Filespecification rappresenta un file che si trova in una posizione di sistema.
ms.assetid: 25d6cc79-1497-4615-9251-8e00524dff1b
ms.tgt_platform: multiple
title: Classe CIM_FileSpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification
- CIM_FileSpecification.CheckID
- CIM_FileSpecification.Caption
- CIM_FileSpecification.Description
- CIM_FileSpecification.CheckMode
- CIM_FileSpecification.TargetOperatingSystem
- CIM_FileSpecification.Version
- CIM_FileSpecification.SoftwareElementID
- CIM_FileSpecification.SoftwareElementState
- CIM_FileSpecification.Name
- CIM_FileSpecification.CheckSum
- CIM_FileSpecification.CRC1
- CIM_FileSpecification.CRC2
- CIM_FileSpecification.CreateTimeStamp
- CIM_FileSpecification.FileSize
- CIM_FileSpecification.MD5Checksum
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 503cf9678d2be7a3afb3f8c205f0d042b4bcaec2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304913"
---
# <a name="cim_filespecification-class"></a><span data-ttu-id="c0feb-103">CIM \_ Filespecification (classe)</span><span class="sxs-lookup"><span data-stu-id="c0feb-103">CIM\_FileSpecification class</span></span>

<span data-ttu-id="c0feb-104">La classe **CIM \_ filespecification** rappresenta un file che si trova in una posizione di sistema.</span><span class="sxs-lookup"><span data-stu-id="c0feb-104">The **CIM\_FileSpecification** class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="c0feb-105">Il file si trova nella directory identificata dall'associazione [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="c0feb-105">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="c0feb-106">Il metodo [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa le informazioni per verificare l'esistenza del file.</span><span class="sxs-lookup"><span data-stu-id="c0feb-106">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="c0feb-107">Si noti che le proprietà con un valore **null** non vengono controllate.</span><span class="sxs-lookup"><span data-stu-id="c0feb-107">Note that properties with a **Null** value are not checked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0feb-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c0feb-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c0feb-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c0feb-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c0feb-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c0feb-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c0feb-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c0feb-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0feb-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0feb-112">Syntax</span></span>

``` syntax
[UUID("{41F377B0-DB2A-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_FileSpecification : CIM_Check
{
  string   CheckID;
  string   Caption;
  string   Description;
  boolean  CheckMode;
  uint16   TargetOperatingSystem;
  string   Version;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Name;
  uint32   CheckSum;
  uint32   CRC1;
  uint32   CRC2;
  datetime CreateTimeStamp;
  uint64   FileSize;
  string   MD5Checksum;
};
```

## <a name="members"></a><span data-ttu-id="c0feb-113">Members</span><span class="sxs-lookup"><span data-stu-id="c0feb-113">Members</span></span>

<span data-ttu-id="c0feb-114">La classe **CIM \_ filespecification** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0feb-114">The **CIM\_FileSpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="c0feb-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0feb-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0feb-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0feb-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0feb-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0feb-117">Methods</span></span>

<span data-ttu-id="c0feb-118">La classe **CIM \_ filespecification** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c0feb-118">The **CIM\_FileSpecification** class has these methods.</span></span>



| <span data-ttu-id="c0feb-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="c0feb-119">Method</span></span>                                                         | <span data-ttu-id="c0feb-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0feb-120">Description</span></span>                                                      |
|:---------------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="c0feb-121">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="c0feb-121">**Invoke**</span></span>](invoke-method-in-class-cim-filespecification.md) | <span data-ttu-id="c0feb-122">Valuta un particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="c0feb-122">Evaluates a particular check.</span></span> <span data-ttu-id="c0feb-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="c0feb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c0feb-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0feb-124">Properties</span></span>

<span data-ttu-id="c0feb-125">La classe **CIM \_ filespecification** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c0feb-125">The **CIM\_FileSpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0feb-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c0feb-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0feb-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c0feb-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-130">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0feb-130">A short textual description of the subject.</span></span>

<span data-ttu-id="c0feb-131">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="c0feb-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0feb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-135">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c0feb-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-136">Identificatore utilizzato insieme ad altre chiavi per identificare in modo univoco il controllo.</span><span class="sxs-lookup"><span data-stu-id="c0feb-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="c0feb-137">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="c0feb-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c0feb-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-141">Se **true**, la condizione dovrebbe esistere nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="c0feb-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="c0feb-142">Un file, ad esempio, dovrebbe trovarsi in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="c0feb-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="c0feb-143">Se **false**, la condizione non è prevista.</span><span class="sxs-lookup"><span data-stu-id="c0feb-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="c0feb-144">Un file, ad esempio, non si trova in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="c0feb-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="c0feb-145">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-146">**CheckSum**</span><span class="sxs-lookup"><span data-stu-id="c0feb-146">**CheckSum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0feb-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-149">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Firma del software DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="c0feb-149">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-150">Valore calcolato come somma a 16 bit dei primi 32 byte del file.</span><span class="sxs-lookup"><span data-stu-id="c0feb-150">Value calculated as the 16-bit sum of the file's first 32 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-151">**CRC1**</span><span class="sxs-lookup"><span data-stu-id="c0feb-151">**CRC1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0feb-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-154">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Firma del software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="c0feb-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-155">Valore CRC calcolato con il medio 512 KB.</span><span class="sxs-lookup"><span data-stu-id="c0feb-155">CRC value calculated using the middle 512 KB.</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-156">**CRC2**</span><span class="sxs-lookup"><span data-stu-id="c0feb-156">**CRC2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0feb-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-159">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Firma del software DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="c0feb-159">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-160">Valore CRC per la media di 512 KB del file, modulo 3.</span><span class="sxs-lookup"><span data-stu-id="c0feb-160">CRC value for the middle 512 KB of the file, modulo 3.</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-161">**CreateTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="c0feb-161">**CreateTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-162">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c0feb-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-164">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0feb-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-165">Data e ora di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="c0feb-165">File creation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-166">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c0feb-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0feb-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-169">Descrizione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="c0feb-169">A description of the objects.</span></span>

<span data-ttu-id="c0feb-170">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-170">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-171">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="c0feb-171">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-172">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c0feb-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-174">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="c0feb-174">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-175">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="c0feb-175">Size of the file, in bytes.</span></span>

<span data-ttu-id="c0feb-176">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c0feb-176">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-177">**MD5Checksum**</span><span class="sxs-lookup"><span data-stu-id="c0feb-177">**MD5Checksum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0feb-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-180">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span><span class="sxs-lookup"><span data-stu-id="c0feb-180">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-181">Algoritmo per il calcolo di un checksum a 128 bit per qualsiasi file o oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0feb-181">Algorithm for computing a 128-bit checksum for any file or object.</span></span> <span data-ttu-id="c0feb-182">La probabilità di due file diversi che producono lo stesso checksum MD5 è molto piccola (circa 1 in 2 ^ 64) e il checksum MD5 di un file può essere usato per costruire un identificatore di contenuto affidabile che probabilmente identifichi il file in modo univoco.</span><span class="sxs-lookup"><span data-stu-id="c0feb-182">The likelihood of two different files producing the same MD5 checksum is very small (about 1 in 2^64), and the MD5 checksum of a file can be used to construct a reliable content identifier that is likely to uniquely identify the file.</span></span> <span data-ttu-id="c0feb-183">È anche vero il contrario.</span><span class="sxs-lookup"><span data-stu-id="c0feb-183">The reverse is also true.</span></span> <span data-ttu-id="c0feb-184">Se due file hanno lo stesso checksum MD5, è molto probabile che i file siano identici.</span><span class="sxs-lookup"><span data-stu-id="c0feb-184">If two files have the same MD5 checksum, it is very likely that the files are identical.</span></span> <span data-ttu-id="c0feb-185">Ai fini della specifica MOF della proprietà MD5, l'algoritmo MD5 genera sempre una stringa di 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c0feb-185">For purposes of MOF specification of the MD5 property, the MD5 algorithm always generates a 32-character string.</span></span> <span data-ttu-id="c0feb-186">Ad esempio, la stringa "abcdefghijklmnopqrstuvwxyz" genera la stringa "c3fcd3d76192e4007dfb496cca67e13b".</span><span class="sxs-lookup"><span data-stu-id="c0feb-186">For example, the string "abcdefghijklmnopqrstuvwxyz" generates the string "c3fcd3d76192e4007dfb496cca67e13b".</span></span> <span data-ttu-id="c0feb-187">Per ulteriori informazioni sull'implementazione dell'algoritmo MD5, vedere [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span><span class="sxs-lookup"><span data-stu-id="c0feb-187">For more information about implementing the MD5 algorithm, see [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-188">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c0feb-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0feb-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-191">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="c0feb-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-192">Nome del file o nome del file con prefisso di directory.</span><span class="sxs-lookup"><span data-stu-id="c0feb-192">Either the name of the file or the name of the file with a directory prefix.</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-193">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="c0feb-193">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0feb-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-196">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c0feb-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-197">Si tratta di un identificatore per questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="c0feb-197">This is an identifier for this software element.</span></span>

<span data-ttu-id="c0feb-198">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-198">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0feb-199">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="c0feb-199">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-200">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0feb-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-202">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0feb-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-203">Stato dell'elemento software di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="c0feb-203">The software element state of a software element.</span></span>

<span data-ttu-id="c0feb-204">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="c0feb-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="c0feb-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-206">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="c0feb-206">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="c0feb-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="c0feb-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-208">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="c0feb-208">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="c0feb-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="c0feb-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-210">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="c0feb-210">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="c0feb-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="c0feb-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-212">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="c0feb-212">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0feb-213">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="c0feb-213">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-214">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0feb-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-216">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="c0feb-216">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-217">Sistema operativo di destinazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="c0feb-217">Target operating system of the software element.</span></span>

<span data-ttu-id="c0feb-218">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-218">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0feb-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="c0feb-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0feb-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c0feb-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="c0feb-221"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="c0feb-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-222">Mac OS</span><span class="sxs-lookup"><span data-stu-id="c0feb-222">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="c0feb-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="c0feb-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-224">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="c0feb-224">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="c0feb-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="c0feb-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="c0feb-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="c0feb-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="c0feb-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="c0feb-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="c0feb-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="c0feb-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-229">Apri VM</span><span class="sxs-lookup"><span data-stu-id="c0feb-229">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="c0feb-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="c0feb-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-231">HP-UX</span><span class="sxs-lookup"><span data-stu-id="c0feb-231">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="c0feb-232"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="c0feb-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="c0feb-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="c0feb-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="c0feb-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="c0feb-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="c0feb-235"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="c0feb-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="c0feb-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="c0feb-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-237">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="c0feb-237">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="c0feb-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="c0feb-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="c0feb-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="c0feb-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-240">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="c0feb-240">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="c0feb-241"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="c0feb-241"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-242">Windows 95</span><span class="sxs-lookup"><span data-stu-id="c0feb-242">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="c0feb-243"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="c0feb-243"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-244">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c0feb-244">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="c0feb-245"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="c0feb-245"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-246">Windows NT</span><span class="sxs-lookup"><span data-stu-id="c0feb-246">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="c0feb-247"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="c0feb-247"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-248">Windows CE</span><span class="sxs-lookup"><span data-stu-id="c0feb-248">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="c0feb-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="c0feb-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-250">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="c0feb-250">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="c0feb-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="c0feb-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="c0feb-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="c0feb-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="c0feb-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="c0feb-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="c0feb-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="c0feb-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="c0feb-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="c0feb-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="c0feb-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="c0feb-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="c0feb-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="c0feb-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="c0feb-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="c0feb-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="c0feb-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="c0feb-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="c0feb-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="c0feb-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="c0feb-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="c0feb-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="c0feb-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="c0feb-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-263">Serie A</span><span class="sxs-lookup"><span data-stu-id="c0feb-263">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="c0feb-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="c0feb-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-265">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="c0feb-265">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="c0feb-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="c0feb-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-267">NT tandem</span><span class="sxs-lookup"><span data-stu-id="c0feb-267">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="c0feb-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="c0feb-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-269">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="c0feb-269">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="c0feb-270"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="c0feb-270"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="c0feb-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="c0feb-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="c0feb-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="c0feb-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="c0feb-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="c0feb-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="c0feb-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="c0feb-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="c0feb-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="c0feb-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-276">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="c0feb-276">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="c0feb-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="c0feb-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="c0feb-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="c0feb-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="c0feb-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="c0feb-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="c0feb-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="c0feb-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-281">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="c0feb-281">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="c0feb-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="c0feb-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="c0feb-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="c0feb-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="c0feb-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="c0feb-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="c0feb-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="c0feb-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="c0feb-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="c0feb-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="c0feb-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="c0feb-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="c0feb-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="c0feb-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="c0feb-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="c0feb-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="c0feb-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="c0feb-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="c0feb-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="c0feb-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="c0feb-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="c0feb-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="c0feb-293">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="c0feb-293">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="c0feb-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="c0feb-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="c0feb-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="c0feb-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="c0feb-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="c0feb-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="c0feb-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="c0feb-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="c0feb-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="c0feb-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0feb-299">**Versione**</span><span class="sxs-lookup"><span data-stu-id="c0feb-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0feb-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0feb-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0feb-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0feb-302">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="c0feb-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c0feb-303">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c0feb-303">Version of the operation.</span></span>

<span data-ttu-id="c0feb-304">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="c0feb-304">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="c0feb-305"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="c0feb-305"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="c0feb-306"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="c0feb-306"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="c0feb-307">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-307">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0feb-308">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0feb-308">Remarks</span></span>

<span data-ttu-id="c0feb-309">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c0feb-309">WMI does not implement this class.</span></span> <span data-ttu-id="c0feb-310">Per le classi derivate dalla **\_ specifica del filecim**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c0feb-310">For classes derived from **CIM\_FileSpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c0feb-311">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c0feb-311">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c0feb-312">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c0feb-312">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0feb-313">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0feb-313">Requirements</span></span>



| <span data-ttu-id="c0feb-314">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0feb-314">Requirement</span></span> | <span data-ttu-id="c0feb-315">Valore</span><span class="sxs-lookup"><span data-stu-id="c0feb-315">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0feb-316">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0feb-316">Minimum supported client</span></span><br/> | <span data-ttu-id="c0feb-317">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0feb-317">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0feb-318">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0feb-318">Minimum supported server</span></span><br/> | <span data-ttu-id="c0feb-319">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0feb-319">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0feb-320">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c0feb-320">Namespace</span></span><br/>                | <span data-ttu-id="c0feb-321">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c0feb-321">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0feb-322">MOF</span><span class="sxs-lookup"><span data-stu-id="c0feb-322">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0feb-323"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0feb-323"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0feb-324">DLL</span><span class="sxs-lookup"><span data-stu-id="c0feb-324">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0feb-325"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0feb-325"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0feb-326">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0feb-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0feb-327">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="c0feb-327">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

