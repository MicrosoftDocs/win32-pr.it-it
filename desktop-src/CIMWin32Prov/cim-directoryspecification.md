---
description: La \_ classe CIM DirectorySpecification acquisisce la struttura di directory principale di un elemento software. Questa classe viene utilizzata per organizzare i file di un elemento software in unità gestibili che possono essere rilocate in un sistema di computer.
ms.assetid: faeab356-e470-477b-97d2-1a19ce1d8d21
ms.tgt_platform: multiple
title: Classe CIM_DirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification
- CIM_DirectorySpecification.CheckID
- CIM_DirectorySpecification.Caption
- CIM_DirectorySpecification.Description
- CIM_DirectorySpecification.CheckMode
- CIM_DirectorySpecification.Name
- CIM_DirectorySpecification.TargetOperatingSystem
- CIM_DirectorySpecification.Version
- CIM_DirectorySpecification.SoftwareElementID
- CIM_DirectorySpecification.SoftwareElementState
- CIM_DirectorySpecification.DirectoryPath
- CIM_DirectorySpecification.DirectoryType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a7eb6ae627c8ed9b5639e573e1d2d89132698ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127186"
---
# <a name="cim_directoryspecification-class"></a><span data-ttu-id="6c05d-104">CIM \_ DirectorySpecification (classe)</span><span class="sxs-lookup"><span data-stu-id="6c05d-104">CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="6c05d-105">La classe **CIM \_ DirectorySpecification** acquisisce la struttura di directory principale di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="6c05d-105">The **CIM\_DirectorySpecification** class captures the major directory structure of a software element.</span></span> <span data-ttu-id="6c05d-106">Questa classe viene utilizzata per organizzare i file di un elemento software in unità gestibili che possono essere rilocate in un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="6c05d-106">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c05d-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6c05d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6c05d-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6c05d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6c05d-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6c05d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6c05d-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6c05d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c05d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c05d-111">Syntax</span></span>

``` syntax
[UUID("{A524EE6E-DB29-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_DirectorySpecification : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  string  DirectoryPath;
  uint16  DirectoryType;
};
```

## <a name="members"></a><span data-ttu-id="6c05d-112">Members</span><span class="sxs-lookup"><span data-stu-id="6c05d-112">Members</span></span>

<span data-ttu-id="6c05d-113">La classe **CIM \_ DirectorySpecification** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6c05d-113">The **CIM\_DirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="6c05d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="6c05d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6c05d-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c05d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6c05d-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="6c05d-116">Methods</span></span>

<span data-ttu-id="6c05d-117">La classe **CIM \_ DirectorySpecification** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6c05d-117">The **CIM\_DirectorySpecification** class has these methods.</span></span>



| <span data-ttu-id="6c05d-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="6c05d-118">Method</span></span>                                                              | <span data-ttu-id="6c05d-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c05d-119">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="6c05d-120">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="6c05d-120">**Invoke**</span></span>](invoke-method-in-class-cim-directoryspecification.md) | <span data-ttu-id="6c05d-121">Valuta un particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="6c05d-121">Evaluates a particular check.</span></span> <span data-ttu-id="6c05d-122">Questo metodo non è implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="6c05d-122">This method is not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6c05d-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c05d-123">Properties</span></span>

<span data-ttu-id="6c05d-124">La classe **CIM \_ DirectorySpecification** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6c05d-124">The **CIM\_DirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c05d-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6c05d-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6c05d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-128">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6c05d-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-129">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c05d-129">A short textual description of the subject.</span></span>

<span data-ttu-id="6c05d-130">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05d-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="6c05d-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6c05d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-134">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6c05d-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-135">Identificatore utilizzato insieme ad altre chiavi per identificare in modo univoco il controllo.</span><span class="sxs-lookup"><span data-stu-id="6c05d-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="6c05d-136">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05d-137">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="6c05d-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c05d-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-140">Se **true**, la condizione dovrebbe esistere nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="6c05d-140">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="6c05d-141">Un file, ad esempio, dovrebbe trovarsi in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="6c05d-141">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="6c05d-142">Se **false**, la condizione non è prevista.</span><span class="sxs-lookup"><span data-stu-id="6c05d-142">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="6c05d-143">Un file, ad esempio, non si trova in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="6c05d-143">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="6c05d-144">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05d-145">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6c05d-145">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6c05d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-148">Descrizione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="6c05d-148">A description of the objects.</span></span>

<span data-ttu-id="6c05d-149">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-149">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05d-150">**DirectoryPath**</span><span class="sxs-lookup"><span data-stu-id="6c05d-150">**DirectoryPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6c05d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-153">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="6c05d-153">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-154">Nome della directory.</span><span class="sxs-lookup"><span data-stu-id="6c05d-154">Directory name.</span></span> <span data-ttu-id="6c05d-155">Il valore fornito da un provider di applicazioni è un nome di percorso predefinito o consigliato.</span><span class="sxs-lookup"><span data-stu-id="6c05d-155">The value supplied by an application provider is a default or recommended path name.</span></span> <span data-ttu-id="6c05d-156">Il valore può essere modificato per un ambiente specifico.</span><span class="sxs-lookup"><span data-stu-id="6c05d-156">The value can be changed for a particular environment.</span></span>

</dd> <dt>

<span data-ttu-id="6c05d-157">**DirectoryType**</span><span class="sxs-lookup"><span data-stu-id="6c05d-157">**DirectoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-158">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c05d-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-160">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Percorso DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="6c05d-160">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Location\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-161">Tipo di directory da descrivere.</span><span class="sxs-lookup"><span data-stu-id="6c05d-161">Type of directory being described.</span></span>

<dt>

<span id="Product_base_directory"></span><span id="product_base_directory"></span><span id="PRODUCT_BASE_DIRECTORY"></span>

<span data-ttu-id="6c05d-162">**Directory di base del prodotto** (0)</span><span class="sxs-lookup"><span data-stu-id="6c05d-162">**Product base directory** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_executable_directory"></span><span id="product_executable_directory"></span><span id="PRODUCT_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="6c05d-163">**Directory eseguibile prodotto** (1)</span><span class="sxs-lookup"><span data-stu-id="6c05d-163">**Product executable directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_library_directory"></span><span id="product_library_directory"></span><span id="PRODUCT_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="6c05d-164">**Directory della raccolta di prodotti** (2)</span><span class="sxs-lookup"><span data-stu-id="6c05d-164">**Product library directory** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_configuration_directory"></span><span id="product_configuration_directory"></span><span id="PRODUCT_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="6c05d-165">**Directory di configurazione del prodotto** (3)</span><span class="sxs-lookup"><span data-stu-id="6c05d-165">**Product configuration directory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_include_directory"></span><span id="product_include_directory"></span><span id="PRODUCT_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="6c05d-166">**Directory di inclusione prodotto** (4)</span><span class="sxs-lookup"><span data-stu-id="6c05d-166">**Product include directory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_working_directory"></span><span id="product_working_directory"></span><span id="PRODUCT_WORKING_DIRECTORY"></span>

<span data-ttu-id="6c05d-167">**Directory di lavoro del prodotto** (5)</span><span class="sxs-lookup"><span data-stu-id="6c05d-167">**Product working directory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_log_directory"></span><span id="product_log_directory"></span><span id="PRODUCT_LOG_DIRECTORY"></span>

<span data-ttu-id="6c05d-168">**Directory log prodotto** (6)</span><span class="sxs-lookup"><span data-stu-id="6c05d-168">**Product log directory** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_base_directory"></span><span id="shared_base_directory"></span><span id="SHARED_BASE_DIRECTORY"></span>

<span data-ttu-id="6c05d-169">**Directory di base condivisa** (7)</span><span class="sxs-lookup"><span data-stu-id="6c05d-169">**Shared base directory** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_executable_directory"></span><span id="shared_executable_directory"></span><span id="SHARED_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="6c05d-170">**Directory eseguibile condivisa** (8)</span><span class="sxs-lookup"><span data-stu-id="6c05d-170">**Shared executable directory** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_library_directory"></span><span id="shared_library_directory"></span><span id="SHARED_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="6c05d-171">**Directory delle librerie condivise** (9)</span><span class="sxs-lookup"><span data-stu-id="6c05d-171">**Shared library directory** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_include_directory"></span><span id="shared_include_directory"></span><span id="SHARED_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="6c05d-172">**Directory di inclusione condivisa** (10)</span><span class="sxs-lookup"><span data-stu-id="6c05d-172">**Shared include directory** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="System_base_directory"></span><span id="system_base_directory"></span><span id="SYSTEM_BASE_DIRECTORY"></span>

<span data-ttu-id="6c05d-173">**Directory di base di sistema** (11)</span><span class="sxs-lookup"><span data-stu-id="6c05d-173">**System base directory** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="System_executable_directory"></span><span id="system_executable_directory"></span><span id="SYSTEM_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="6c05d-174">**Directory eseguibile di sistema** (12)</span><span class="sxs-lookup"><span data-stu-id="6c05d-174">**System executable directory** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="System_library_directory"></span><span id="system_library_directory"></span><span id="SYSTEM_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="6c05d-175">**Directory libreria di sistema** (13)</span><span class="sxs-lookup"><span data-stu-id="6c05d-175">**System library directory** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="System_configuration_directory"></span><span id="system_configuration_directory"></span><span id="SYSTEM_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="6c05d-176">**Directory di configurazione di sistema** (14)</span><span class="sxs-lookup"><span data-stu-id="6c05d-176">**System configuration directory** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="System_include_directory"></span><span id="system_include_directory"></span><span id="SYSTEM_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="6c05d-177">**Directory di inclusione sistema** (15)</span><span class="sxs-lookup"><span data-stu-id="6c05d-177">**System include directory** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="System_log_directory"></span><span id="system_log_directory"></span><span id="SYSTEM_LOG_DIRECTORY"></span>

<span data-ttu-id="6c05d-178">**Directory registro di sistema** (16)</span><span class="sxs-lookup"><span data-stu-id="6c05d-178">**System log directory** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c05d-179">**Altro** (17)</span><span class="sxs-lookup"><span data-stu-id="6c05d-179">**Other** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05d-180">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6c05d-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6c05d-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-183">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6c05d-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-184">Nome usato per identificare l'elemento software</span><span class="sxs-lookup"><span data-stu-id="6c05d-184">Name used to identify the software element</span></span>

<span data-ttu-id="6c05d-185">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05d-186">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="6c05d-186">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6c05d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-189">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6c05d-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-190">Si tratta di un identificatore per questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="6c05d-190">This is an identifier for this software element.</span></span>

<span data-ttu-id="6c05d-191">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05d-192">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="6c05d-192">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-193">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c05d-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-195">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c05d-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-196">Stato dell'elemento software di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="6c05d-196">The software element state of a software element.</span></span>

<span data-ttu-id="6c05d-197">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-197">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="6c05d-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="6c05d-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-199">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="6c05d-199">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="6c05d-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="6c05d-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-201">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="6c05d-201">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="6c05d-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="6c05d-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-203">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="6c05d-203">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="6c05d-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="6c05d-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-205">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="6c05d-205">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05d-206">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="6c05d-206">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-207">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c05d-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-209">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="6c05d-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-210">Sistema operativo di destinazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="6c05d-210">Target operating system of the software element.</span></span>

<span data-ttu-id="6c05d-211">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-211">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c05d-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6c05d-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c05d-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6c05d-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="6c05d-214"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="6c05d-214"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-215">Mac OS</span><span class="sxs-lookup"><span data-stu-id="6c05d-215">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="6c05d-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="6c05d-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-217">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="6c05d-217">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="6c05d-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="6c05d-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="6c05d-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="6c05d-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="6c05d-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="6c05d-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="6c05d-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="6c05d-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-222">Apri VM</span><span class="sxs-lookup"><span data-stu-id="6c05d-222">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="6c05d-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="6c05d-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-224">HP-UX</span><span class="sxs-lookup"><span data-stu-id="6c05d-224">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="6c05d-225"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="6c05d-225"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="6c05d-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="6c05d-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="6c05d-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="6c05d-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="6c05d-228"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="6c05d-228"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="6c05d-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="6c05d-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-230">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="6c05d-230">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="6c05d-231"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="6c05d-231"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="6c05d-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="6c05d-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-233">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="6c05d-233">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="6c05d-234"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="6c05d-234"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-235">Windows 95</span><span class="sxs-lookup"><span data-stu-id="6c05d-235">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="6c05d-236"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="6c05d-236"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-237">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6c05d-237">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="6c05d-238"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="6c05d-238"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-239">Windows NT</span><span class="sxs-lookup"><span data-stu-id="6c05d-239">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="6c05d-240"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="6c05d-240"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-241">Windows CE</span><span class="sxs-lookup"><span data-stu-id="6c05d-241">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="6c05d-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="6c05d-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-243">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="6c05d-243">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="6c05d-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="6c05d-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="6c05d-245"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="6c05d-245"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="6c05d-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="6c05d-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="6c05d-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="6c05d-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="6c05d-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="6c05d-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="6c05d-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="6c05d-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="6c05d-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="6c05d-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="6c05d-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="6c05d-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="6c05d-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="6c05d-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="6c05d-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="6c05d-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="6c05d-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="6c05d-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="6c05d-255"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="6c05d-255"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-256">Serie A</span><span class="sxs-lookup"><span data-stu-id="6c05d-256">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="6c05d-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="6c05d-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-258">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="6c05d-258">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="6c05d-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="6c05d-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-260">NT tandem</span><span class="sxs-lookup"><span data-stu-id="6c05d-260">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="6c05d-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="6c05d-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-262">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="6c05d-262">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="6c05d-263"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="6c05d-263"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="6c05d-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="6c05d-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="6c05d-265"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="6c05d-265"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="6c05d-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="6c05d-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="6c05d-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="6c05d-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="6c05d-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="6c05d-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-269">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="6c05d-269">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="6c05d-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="6c05d-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="6c05d-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="6c05d-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="6c05d-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="6c05d-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="6c05d-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="6c05d-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-274">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="6c05d-274">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="6c05d-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="6c05d-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="6c05d-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="6c05d-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="6c05d-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="6c05d-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="6c05d-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="6c05d-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="6c05d-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="6c05d-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="6c05d-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="6c05d-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="6c05d-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="6c05d-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="6c05d-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="6c05d-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="6c05d-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="6c05d-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="6c05d-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="6c05d-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="6c05d-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="6c05d-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="6c05d-286">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="6c05d-286">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="6c05d-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="6c05d-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="6c05d-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="6c05d-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="6c05d-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="6c05d-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="6c05d-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="6c05d-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="6c05d-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="6c05d-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05d-292">**Versione**</span><span class="sxs-lookup"><span data-stu-id="6c05d-292">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05d-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6c05d-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c05d-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05d-295">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="6c05d-295">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="6c05d-296">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6c05d-296">Version of the operation.</span></span>

<span data-ttu-id="6c05d-297">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="6c05d-297">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="6c05d-298"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="6c05d-298"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="6c05d-299"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="6c05d-299"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="6c05d-300">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-300">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c05d-301">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c05d-301">Remarks</span></span>

<span data-ttu-id="6c05d-302">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6c05d-302">WMI does not implement this class.</span></span> <span data-ttu-id="6c05d-303">Per le classi derivate da **CIM \_ DirectorySpecification**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-303">For classes derived from **CIM\_DirectorySpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6c05d-304">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6c05d-304">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6c05d-305">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6c05d-305">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c05d-306">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c05d-306">Requirements</span></span>



| <span data-ttu-id="6c05d-307">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c05d-307">Requirement</span></span> | <span data-ttu-id="6c05d-308">Valore</span><span class="sxs-lookup"><span data-stu-id="6c05d-308">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c05d-309">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c05d-309">Minimum supported client</span></span><br/> | <span data-ttu-id="6c05d-310">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c05d-310">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c05d-311">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c05d-311">Minimum supported server</span></span><br/> | <span data-ttu-id="6c05d-312">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c05d-312">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c05d-313">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6c05d-313">Namespace</span></span><br/>                | <span data-ttu-id="6c05d-314">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6c05d-314">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c05d-315">MOF</span><span class="sxs-lookup"><span data-stu-id="6c05d-315">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c05d-316"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c05d-316"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c05d-317">DLL</span><span class="sxs-lookup"><span data-stu-id="6c05d-317">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c05d-318"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c05d-318"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c05d-319">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c05d-319">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c05d-320">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="6c05d-320">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

