---
description: La \_ classe CIM CacheMemory definisce le funzionalità e la gestione della memoria cache.
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: Classe CIM_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b7a7add96c523dae6b683d597ba36953c605d28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878006"
---
# <a name="cim_cachememory-class"></a><span data-ttu-id="fa460-103">CIM \_ CacheMemory (classe)</span><span class="sxs-lookup"><span data-stu-id="fa460-103">CIM\_CacheMemory class</span></span>

<span data-ttu-id="fa460-104">La classe **CIM \_ CacheMemory** definisce le funzionalità e la gestione della memoria cache.</span><span class="sxs-lookup"><span data-stu-id="fa460-104">The **CIM\_CacheMemory** class defines the capabilities and management of cache memory.</span></span>

<span data-ttu-id="fa460-105">Memoria cache è la RAM dedicata o allocata in cui un processore cerca i dati.</span><span class="sxs-lookup"><span data-stu-id="fa460-105">Cache memory is the dedicated or allocated RAM where a processor first searches for data.</span></span> <span data-ttu-id="fa460-106">I dati nella memoria cache vengono recapitati rapidamente al processore e vengono in genere descritti in prossimità del processore, ad esempio la cache primaria o secondaria.</span><span class="sxs-lookup"><span data-stu-id="fa460-106">Data in cache memory is quickly delivered to the processor and is usually described by its proximity to the processor (for example, primary or secondary cache).</span></span> <span data-ttu-id="fa460-107">Anche un'unità disco che include RAM allocata per contenere i dati letti o adiacenti del disco più recenti (per velocizzare il recupero) viene modellata come memoria della cache.</span><span class="sxs-lookup"><span data-stu-id="fa460-107">A disk drive that includes RAM allocated for holding the disk's most recently read or adjacent data (to speed up retrieval) is also modeled as cache memory.</span></span>

> [!Note]  
> <span data-ttu-id="fa460-108">La memoria cache non è un buffer a livello di sistema operativo o di applicazione. si tratta di una RAM allocata per la memorizzazione nella cache dei dati del processore.</span><span class="sxs-lookup"><span data-stu-id="fa460-108">Cache memory is not an operating-system or application-level buffer; it is RAM that has been allocated for caching processor data.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="fa460-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="fa460-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fa460-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fa460-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fa460-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fa460-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fa460-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fa460-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa460-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa460-113">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="fa460-114">Members</span><span class="sxs-lookup"><span data-stu-id="fa460-114">Members</span></span>

<span data-ttu-id="fa460-115">La classe **CIM \_ CacheMemory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fa460-115">The **CIM\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="fa460-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="fa460-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="fa460-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa460-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fa460-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="fa460-118">Methods</span></span>

<span data-ttu-id="fa460-119">La classe **CIM \_ CacheMemory** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fa460-119">The **CIM\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="fa460-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="fa460-120">Method</span></span>                                                                 | <span data-ttu-id="fa460-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa460-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa460-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="fa460-122">**Reset**</span></span>](reset-method-in-class-cim-cachememory.md)                 | <span data-ttu-id="fa460-123">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="fa460-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="fa460-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="fa460-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="fa460-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fa460-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cachememory.md) | <span data-ttu-id="fa460-126">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="fa460-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="fa460-127">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="fa460-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fa460-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa460-128">Properties</span></span>

<span data-ttu-id="fa460-129">La classe **CIM \_ CacheMemory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fa460-129">The **CIM\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa460-130">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="fa460-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-133">Descrive le proprietà di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="fa460-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="fa460-134">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-135">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="fa460-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="fa460-136">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="fa460-137">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="fa460-138">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="fa460-139">**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="fa460-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-141">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fa460-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fa460-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-143">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,18 "," MIF. DMTF \| array di memoria fisica \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="fa460-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fa460-144">Matrice di ottetti che contengono informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="fa460-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="fa460-145">Un esempio è la sindrome di controllo degli errori e correzione (ECC) oppure la restituzione dei bit di controllo se viene utilizzata una metodologia di errore basata su CRC.</span><span class="sxs-lookup"><span data-stu-id="fa460-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="fa460-146">Nel secondo caso, se viene riconosciuto un errore a bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="fa460-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="fa460-147">In questo campo sono inclusi questo tipo di dati (la sindrome ECC, i dati di controllo o di bit di parità o altre informazioni fornite dal fornitore).</span><span class="sxs-lookup"><span data-stu-id="fa460-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="fa460-148">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="fa460-149">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-150">**Associatività**</span><span class="sxs-lookup"><span data-stu-id="fa460-150">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-153">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,15 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-154">Enumerazione che definisce l'associatività della cache di sistema.</span><span class="sxs-lookup"><span data-stu-id="fa460-154">Enumeration that defines the system cache associativity.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-155">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-156">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-156">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="fa460-157">Con **mapping diretto** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-157">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="fa460-158">**set bidirezionale-associativo** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-158">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="fa460-159">**set-associativo a 4 vie** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-159">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="fa460-160">**Completamente associativo** (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-160">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="fa460-161">**set a 8 vie-associativo** (7)</span><span class="sxs-lookup"><span data-stu-id="fa460-161">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="fa460-162">**set-associativo a 16 vie** (8)</span><span class="sxs-lookup"><span data-stu-id="fa460-162">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-163">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="fa460-163">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-164">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-166">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="fa460-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-167">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa460-167">Availability and status of the device.</span></span>

<span data-ttu-id="fa460-168">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-168">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="fa460-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="fa460-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="fa460-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fa460-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="fa460-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="fa460-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="fa460-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="fa460-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="fa460-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="fa460-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fa460-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="fa460-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="fa460-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="fa460-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="fa460-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="fa460-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="fa460-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="fa460-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-182">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fa460-182">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="fa460-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="fa460-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-184">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="fa460-184">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="fa460-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="fa460-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-186">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="fa460-186">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="fa460-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="fa460-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="fa460-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="fa460-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-189">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="fa460-189">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="fa460-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="fa460-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-191">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="fa460-191">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="fa460-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="fa460-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-193">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="fa460-193">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="fa460-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="fa460-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-195">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="fa460-195">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="fa460-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="fa460-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-197">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="fa460-197">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-198">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="fa460-198">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-199">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fa460-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-201">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="fa460-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-202">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fa460-202">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="fa460-203">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="fa460-203">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="fa460-204">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="fa460-204">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="fa460-205">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fa460-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fa460-206">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-207">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="fa460-207">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-210">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-211">Specifica la memorizzazione nella cache delle istruzioni, la memorizzazione dei dati o entrambe.</span><span class="sxs-lookup"><span data-stu-id="fa460-211">Specifies instruction caching, data caching, or both.</span></span> <span data-ttu-id="fa460-212">È possibile definire anche "other" e "Unknown".</span><span class="sxs-lookup"><span data-stu-id="fa460-212">"Other" and "Unknown" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-213">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-213">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-214">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-214">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="fa460-215">**Istruzione** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-215">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="fa460-216">**Dati** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-216">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="fa460-217">**Unificato** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-217">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-218">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="fa460-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-221">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="fa460-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-222">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa460-222">A short textual description of the object.</span></span>

<span data-ttu-id="fa460-223">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fa460-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-225">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa460-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-227">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fa460-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-228">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fa460-228">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="fa460-229">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="fa460-230">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="fa460-230">**This device is working properly.**</span></span> <span data-ttu-id="fa460-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="fa460-231">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="fa460-232">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="fa460-232">**This device is not configured correctly.**</span></span> <span data-ttu-id="fa460-233">(1)</span><span class="sxs-lookup"><span data-stu-id="fa460-233">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fa460-234">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-234">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="fa460-235">(2)</span><span class="sxs-lookup"><span data-stu-id="fa460-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="fa460-236">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="fa460-236">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="fa460-237">(3)</span><span class="sxs-lookup"><span data-stu-id="fa460-237">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fa460-238">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="fa460-238">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="fa460-239">(4)</span><span class="sxs-lookup"><span data-stu-id="fa460-239">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="fa460-240">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="fa460-240">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="fa460-241">(5)</span><span class="sxs-lookup"><span data-stu-id="fa460-241">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="fa460-242">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="fa460-242">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="fa460-243"> (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-243">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="fa460-244">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="fa460-244">**Cannot filter.**</span></span> <span data-ttu-id="fa460-245">(7)</span><span class="sxs-lookup"><span data-stu-id="fa460-245">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="fa460-246">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="fa460-246">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="fa460-247">(8)</span><span class="sxs-lookup"><span data-stu-id="fa460-247">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="fa460-248">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="fa460-248">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="fa460-249">(9)</span><span class="sxs-lookup"><span data-stu-id="fa460-249">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="fa460-250">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-250">**This device cannot start.**</span></span> <span data-ttu-id="fa460-251">(10)</span><span class="sxs-lookup"><span data-stu-id="fa460-251">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="fa460-252">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-252">**This device failed.**</span></span> <span data-ttu-id="fa460-253">(11)</span><span class="sxs-lookup"><span data-stu-id="fa460-253">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="fa460-254">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="fa460-254">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="fa460-255">12</span><span class="sxs-lookup"><span data-stu-id="fa460-255">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="fa460-256">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-256">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="fa460-257">(13)</span><span class="sxs-lookup"><span data-stu-id="fa460-257">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="fa460-258">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="fa460-258">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="fa460-259">(14)</span><span class="sxs-lookup"><span data-stu-id="fa460-259">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="fa460-260">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="fa460-260">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="fa460-261">(15)</span><span class="sxs-lookup"><span data-stu-id="fa460-261">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="fa460-262">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-262">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="fa460-263">(16)</span><span class="sxs-lookup"><span data-stu-id="fa460-263">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="fa460-264">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="fa460-264">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="fa460-265">(17)</span><span class="sxs-lookup"><span data-stu-id="fa460-265">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fa460-266">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-266">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="fa460-267">(18)</span><span class="sxs-lookup"><span data-stu-id="fa460-267">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="fa460-268">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="fa460-268">**Failure using the VxD loader.**</span></span> <span data-ttu-id="fa460-269">(19)</span><span class="sxs-lookup"><span data-stu-id="fa460-269">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fa460-270">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="fa460-270">**Your registry might be corrupted.**</span></span> <span data-ttu-id="fa460-271">(20)</span><span class="sxs-lookup"><span data-stu-id="fa460-271">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="fa460-272">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-272">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="fa460-273">(21)</span><span class="sxs-lookup"><span data-stu-id="fa460-273">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="fa460-274">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="fa460-274">**This device is disabled.**</span></span> <span data-ttu-id="fa460-275">(22)</span><span class="sxs-lookup"><span data-stu-id="fa460-275">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="fa460-276">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="fa460-276">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="fa460-277">(23)</span><span class="sxs-lookup"><span data-stu-id="fa460-277">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="fa460-278">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="fa460-278">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="fa460-279">(24)</span><span class="sxs-lookup"><span data-stu-id="fa460-279">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fa460-280">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-280">**Windows is still setting up this device.**</span></span> <span data-ttu-id="fa460-281">(25)</span><span class="sxs-lookup"><span data-stu-id="fa460-281">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fa460-282">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-282">**Windows is still setting up this device.**</span></span> <span data-ttu-id="fa460-283">(26)</span><span class="sxs-lookup"><span data-stu-id="fa460-283">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="fa460-284">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="fa460-284">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="fa460-285">(27)</span><span class="sxs-lookup"><span data-stu-id="fa460-285">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="fa460-286">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="fa460-286">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="fa460-287">(28)</span><span class="sxs-lookup"><span data-stu-id="fa460-287">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="fa460-288">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="fa460-288">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="fa460-289">(29)</span><span class="sxs-lookup"><span data-stu-id="fa460-289">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="fa460-290">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-290">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="fa460-291">(30)</span><span class="sxs-lookup"><span data-stu-id="fa460-291">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fa460-292">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa460-292">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="fa460-293">31</span><span class="sxs-lookup"><span data-stu-id="fa460-293">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="fa460-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-295">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa460-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-297">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fa460-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-298">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="fa460-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="fa460-299">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-300">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="fa460-300">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-301">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa460-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-303">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. DMTF \| matrice di memoria fisica \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-304">Se **true**, l'errore più recente è correggibile.</span><span class="sxs-lookup"><span data-stu-id="fa460-304">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="fa460-305">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-305">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="fa460-306">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-306">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fa460-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-310">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa460-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa460-311">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="fa460-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fa460-312">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="fa460-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="fa460-313">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-314">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fa460-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-317">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="fa460-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-318">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa460-318">A textual description of the object.</span></span>

<span data-ttu-id="fa460-319">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="fa460-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-323">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa460-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa460-324">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="fa460-324">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="fa460-325">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-326">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="fa460-326">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-327">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fa460-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-329">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,4 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="fa460-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-330">Indirizzo finale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="fa460-330">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="fa460-331">L'indirizzo finale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="fa460-331">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="fa460-332">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fa460-332">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fa460-333">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-333">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-334">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="fa460-334">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-335">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,15 "," MIF. DMTF \| matrice di memoria fisica \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-338">Operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="fa460-338">Memory access operation that caused the last error.</span></span> <span data-ttu-id="fa460-339">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="fa460-339">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="fa460-340">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-340">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="fa460-341">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-342">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-343">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="fa460-344">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-344">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="fa460-345">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-345">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="fa460-346">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-346">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-347">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="fa460-347">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-348">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fa460-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-350">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. DMTF \| matrice di memoria fisica \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-350">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-351">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="fa460-351">Address of the last memory error.</span></span> <span data-ttu-id="fa460-352">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="fa460-352">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="fa460-353">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-353">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="fa460-354">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fa460-354">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fa460-355">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-355">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="fa460-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-357">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa460-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-359">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="fa460-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="fa460-360">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-361">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="fa460-361">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-362">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fa460-362">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fa460-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-364">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. DMTF \| array di memoria fisica \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="fa460-364">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fa460-365">Dati acquisiti durante l'ultimo accesso errato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="fa460-365">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="fa460-366">I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="fa460-366">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="fa460-367">Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-367">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="fa460-368">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-368">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-369">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="fa460-369">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-370">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-372">Ordine dei dati archiviati nella proprietà **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="fa460-372">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="fa460-373">Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-373">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="fa460-374">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-374">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="fa460-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-376">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fa460-376">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="fa460-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-378">Byte meno significativo per primo.</span><span class="sxs-lookup"><span data-stu-id="fa460-378">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="fa460-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-380">Primo byte significativo.</span><span class="sxs-lookup"><span data-stu-id="fa460-380">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fa460-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-384">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="fa460-384">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="fa460-385">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fa460-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-387">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-389">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Matrice di memoria fisica DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="fa460-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-390">Tipo di errore che si è verificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="fa460-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="fa460-391">I valori da 12 a 14 non sono definiti nello schema CIM perché DMI combina la semantica del tipo di errore e se è correggibile.</span><span class="sxs-lookup"><span data-stu-id="fa460-391">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="fa460-392">Se un errore è correggibile è indicato nella proprietà **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="fa460-392">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<span data-ttu-id="fa460-393">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-395">Altro.</span><span class="sxs-lookup"><span data-stu-id="fa460-395">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-397">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fa460-397">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fa460-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-399">OK.</span><span class="sxs-lookup"><span data-stu-id="fa460-399">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="fa460-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-401">Lettura non valida.</span><span class="sxs-lookup"><span data-stu-id="fa460-401">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="fa460-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-403">Errore di parità.</span><span class="sxs-lookup"><span data-stu-id="fa460-403">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="fa460-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-405">Errore a bit singolo.</span><span class="sxs-lookup"><span data-stu-id="fa460-405">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="fa460-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="fa460-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-407">Errore a doppio bit.</span><span class="sxs-lookup"><span data-stu-id="fa460-407">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="fa460-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="fa460-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-409">Errore a più bit.</span><span class="sxs-lookup"><span data-stu-id="fa460-409">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="fa460-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="fa460-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-411">Errore di bocconcino.</span><span class="sxs-lookup"><span data-stu-id="fa460-411">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="fa460-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="fa460-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-413">Errore di checksum.</span><span class="sxs-lookup"><span data-stu-id="fa460-413">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="fa460-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="fa460-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-415">Errore CRC.</span><span class="sxs-lookup"><span data-stu-id="fa460-415">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="fa460-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (12)</span><span class="sxs-lookup"><span data-stu-id="fa460-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-417">Non definito.</span><span class="sxs-lookup"><span data-stu-id="fa460-417">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="fa460-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (13)</span><span class="sxs-lookup"><span data-stu-id="fa460-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-419">Non definito.</span><span class="sxs-lookup"><span data-stu-id="fa460-419">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="fa460-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (14)</span><span class="sxs-lookup"><span data-stu-id="fa460-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-421">Non definito.</span><span class="sxs-lookup"><span data-stu-id="fa460-421">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-422">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="fa460-422">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-423">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-425">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-426">Indica se vengono utilizzati algoritmi di parità o CRC, ECC o altri meccanismi.</span><span class="sxs-lookup"><span data-stu-id="fa460-426">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="fa460-427">È anche possibile specificare i dettagli sull'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="fa460-427">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="fa460-428">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-428">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-429">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="fa460-429">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-430">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fa460-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-432">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,21 "," MIF. DMTF \| array di memoria fisica \| 001,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="fa460-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-433">Specifica l'intervallo, in byte, in cui è possibile risolvere l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="fa460-433">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="fa460-434">Se, ad esempio, gli indirizzi di errore vengono risolti in bit 11, ovvero in base a una tipica pagina, gli errori possono essere risolti in limiti di 4 KB e questa proprietà è impostata su 4000.</span><span class="sxs-lookup"><span data-stu-id="fa460-434">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="fa460-435">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-435">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="fa460-436">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fa460-436">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fa460-437">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-437">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-438">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="fa460-438">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-439">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fa460-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-441">Data e ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="fa460-441">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="fa460-442">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="fa460-442">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="fa460-443">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-443">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="fa460-444">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-444">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-445">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="fa460-445">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-446">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa460-446">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-448">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,16 "," MIF. DMTF \| array di memoria fisica \| 001,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="fa460-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-449">Dimensioni del trasferimento dei dati, in bit, che hanno causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="fa460-449">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="fa460-450">Il valore 0 indica che non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="fa460-450">A value of 0 indicates no error.</span></span> <span data-ttu-id="fa460-451">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="fa460-451">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

<span data-ttu-id="fa460-452">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-452">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-453">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="fa460-453">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-454">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa460-454">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-456">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache \| di sistema 003,14 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" secondi ")</span><span class="sxs-lookup"><span data-stu-id="fa460-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-457">Quantità massima di tempo, in secondi, per cui è possibile che le righe o i bucket sporchi rimangano nella cache prima che vengano scaricati.</span><span class="sxs-lookup"><span data-stu-id="fa460-457">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="fa460-458">Il valore 0 indica che uno scaricamento della cache non è controllato da un timer di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="fa460-458">A value of 0 indicates that a cache flush is not controlled by a flushing timer.</span></span>

</dd> <dt>

<span data-ttu-id="fa460-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fa460-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-460">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fa460-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-461">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-462">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="fa460-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-463">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="fa460-463">Indicates when the object was installed.</span></span> <span data-ttu-id="fa460-464">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="fa460-464">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fa460-465">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-466">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fa460-466">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-467">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa460-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-469">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="fa460-469">Last error code reported by the logical device.</span></span>

<span data-ttu-id="fa460-470">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-471">**Level**</span><span class="sxs-lookup"><span data-stu-id="fa460-471">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-472">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-473">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-474">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-475">Specifica se si tratta della cache primaria, secondaria o terziaria.</span><span class="sxs-lookup"><span data-stu-id="fa460-475">Specifies whether this is the primary, secondary or tertiary cache.</span></span> <span data-ttu-id="fa460-476">È possibile definire anche "other", "Unknown" e "not applicabile".</span><span class="sxs-lookup"><span data-stu-id="fa460-476">"Other", "Unknown", and "Not Applicable" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-478">Altro.</span><span class="sxs-lookup"><span data-stu-id="fa460-478">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-480">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fa460-480">Unknown.</span></span>

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="fa460-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primario** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-482">Primario.</span><span class="sxs-lookup"><span data-stu-id="fa460-482">Primary.</span></span>

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="fa460-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondario** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-484">Secondario.</span><span class="sxs-lookup"><span data-stu-id="fa460-484">Secondary.</span></span>

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="fa460-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terziario** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-486">Terziario.</span><span class="sxs-lookup"><span data-stu-id="fa460-486">Tertiary.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fa460-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-488">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="fa460-488">Not applicable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-489">**LineSize**</span><span class="sxs-lookup"><span data-stu-id="fa460-489">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-490">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa460-490">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-491">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-492">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Cache \| 003,10 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="fa460-492">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-493">Dimensione, in byte, di un singolo bucket o riga della cache.</span><span class="sxs-lookup"><span data-stu-id="fa460-493">Size, in bytes, of a single cache bucket or line.</span></span>

</dd> <dt>

<span data-ttu-id="fa460-494">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fa460-494">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-495">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-496">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-497">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fa460-497">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-498">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="fa460-498">Label by which the object is known.</span></span> <span data-ttu-id="fa460-499">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="fa460-499">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fa460-500">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-500">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-501">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="fa460-501">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-502">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fa460-502">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-503">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-504">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="fa460-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-505">Numero di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fa460-505">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="fa460-506">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="fa460-506">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="fa460-507">Se il valore di **blockSize** è 1 (uno), questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fa460-507">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="fa460-508">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fa460-508">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fa460-509">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-509">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-510">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fa460-510">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-511">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-512">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-513">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="fa460-513">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-514">Stringa in formato libero che fornisce informazioni se la proprietà **ErrorType** è impostata su 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="fa460-514">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="fa460-515">Se non è impostato su 1, questa stringa non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-515">If it is not set to 1, then this string has no meaning.</span></span>

<span data-ttu-id="fa460-516">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-516">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-517">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="fa460-517">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-518">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-520">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fa460-520">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-521">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="fa460-521">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="fa460-522">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="fa460-522">Example: "\*PNP030b"</span></span>

<span data-ttu-id="fa460-523">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-524">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fa460-524">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-525">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-525">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa460-526">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-527">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="fa460-527">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="fa460-528">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="fa460-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-530">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="fa460-530">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="fa460-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-532">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa460-532">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fa460-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-534">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="fa460-534">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fa460-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-536">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="fa460-536">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="fa460-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-538">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="fa460-538">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="fa460-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-540">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="fa460-540">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="fa460-541">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="fa460-541">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="fa460-542">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="fa460-542">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="fa460-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-544">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="fa460-544">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="fa460-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="fa460-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-546">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="fa460-546">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-547">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="fa460-547">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-548">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa460-548">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-549">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-550">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="fa460-550">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="fa460-551">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="fa460-551">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="fa460-552">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="fa460-552">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="fa460-553">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="fa460-553">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="fa460-554">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-554">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-555">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="fa460-555">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-556">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-557">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-557">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-558">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="fa460-558">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="fa460-559">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-559">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-560">**Disporre**</span><span class="sxs-lookup"><span data-stu-id="fa460-560">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-561">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-562">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-563">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-563">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-564">Criteri utilizzati dalla cache per gestire le richieste di lettura.</span><span class="sxs-lookup"><span data-stu-id="fa460-564">Policy employed by the cache for handling read requests.</span></span> <span data-ttu-id="fa460-565">Se i criteri di lettura vengono determinati singolarmente, ovvero per ogni richiesta, è necessario specificare il valore 6 ("determinazione per I/O").</span><span class="sxs-lookup"><span data-stu-id="fa460-565">If the read policy is determined individually, that is, for each request, then the value 6 ("Determination per I/O") should be specified.</span></span> <span data-ttu-id="fa460-566">Anche "other" e "Unknown" sono valori validi.</span><span class="sxs-lookup"><span data-stu-id="fa460-566">"Other" and "Unknown" are also valid values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-568">Altro.</span><span class="sxs-lookup"><span data-stu-id="fa460-568">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-570">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fa460-570">Unknown.</span></span>

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="fa460-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-572">Lettura.</span><span class="sxs-lookup"><span data-stu-id="fa460-572">Read.</span></span>

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="fa460-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-574">Read-ahead.</span><span class="sxs-lookup"><span data-stu-id="fa460-574">Read-ahead.</span></span>

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="fa460-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Lettura e Read-Ahead** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Read and Read-Ahead** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-576">Lettura e Read-ahead.</span><span class="sxs-lookup"><span data-stu-id="fa460-576">Read and read-ahead.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="fa460-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinazione per I/O** (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-578">Determinazione per I/O.</span><span class="sxs-lookup"><span data-stu-id="fa460-578">Determination per I/O.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-579">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="fa460-579">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-580">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-580">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-581">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-582">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,12 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-583">Enumerazione Integer che descrive l'algoritmo che determina quali righe o bucket della cache deve essere riutilizzato.</span><span class="sxs-lookup"><span data-stu-id="fa460-583">Integer enumeration describing the algorithm that determines which cache lines or buckets should be re-used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-585">Altro.</span><span class="sxs-lookup"><span data-stu-id="fa460-585">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-587">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fa460-587">Unknown.</span></span>

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="fa460-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Utilizzato meno di recente (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-589">Utilizzato meno di recente (LRU).</span><span class="sxs-lookup"><span data-stu-id="fa460-589">Least recently used (LRU).</span></span>

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="fa460-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**FIFO (First in First out)** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First In First Out (FIFO)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-591">FIFO (First-in, First-out).</span><span class="sxs-lookup"><span data-stu-id="fa460-591">First-in, first-out (FIFO).</span></span>

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="fa460-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**LIFO (Last in First out)** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-593">LIFO (Last-in, First-out).</span><span class="sxs-lookup"><span data-stu-id="fa460-593">Last-in, first-out (LIFO).</span></span>

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="fa460-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Uso meno frequente (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-595">Uso meno frequente (LFU)</span><span class="sxs-lookup"><span data-stu-id="fa460-595">Least frequently used (LFU.)</span></span>

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="fa460-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Uso più frequente (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="fa460-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-597">Utilizzato più di frequente (MFU).</span><span class="sxs-lookup"><span data-stu-id="fa460-597">Most frequently used (MFU).</span></span>

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="fa460-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Più algoritmi dipendenti dai dati** (8)</span><span class="sxs-lookup"><span data-stu-id="fa460-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-599">Più algoritmi dipendenti dai dati.</span><span class="sxs-lookup"><span data-stu-id="fa460-599">Data-dependent multiple algorithms.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-600">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="fa460-600">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-601">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fa460-601">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-602">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-603">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,3 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="fa460-603">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-604">Indirizzo iniziale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria, per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="fa460-604">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="fa460-605">L'indirizzo iniziale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="fa460-605">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="fa460-606">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fa460-606">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fa460-607">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-607">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-608">**Status**</span><span class="sxs-lookup"><span data-stu-id="fa460-608">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-609">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-609">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-610">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-610">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-611">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="fa460-611">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-612">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa460-612">String that indicates the current status of the object.</span></span> <span data-ttu-id="fa460-613">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="fa460-613">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fa460-614">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="fa460-614">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fa460-615">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="fa460-615">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fa460-616">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="fa460-616">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fa460-617">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="fa460-617">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fa460-618">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="fa460-618">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fa460-619">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-619">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fa460-620">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa460-620">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fa460-621">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="fa460-621">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fa460-622">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="fa460-622">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fa460-623">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="fa460-623">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-624">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="fa460-624">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fa460-625">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="fa460-625">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fa460-626">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="fa460-626">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fa460-627">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="fa460-627">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fa460-628">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="fa460-628">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fa460-629">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="fa460-629">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fa460-630">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="fa460-630">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fa460-631">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="fa460-631">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fa460-632">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="fa460-632">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-633">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="fa460-633">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-634">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-634">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-635">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-636">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-637">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="fa460-637">State of the logical device.</span></span> <span data-ttu-id="fa460-638">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="fa460-638">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="fa460-639">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-640">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-640">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-641">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-641">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fa460-642">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-642">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fa460-643">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-643">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fa460-644">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-644">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa460-645">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fa460-645">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-646">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-647">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-648">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa460-648">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa460-649">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="fa460-649">The scoping system's creation class name.</span></span>

<span data-ttu-id="fa460-650">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-650">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-651">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="fa460-651">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-652">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa460-652">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-653">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-653">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa460-654">Indica se le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema (**true**) o un indirizzo fisico (**false**).</span><span class="sxs-lookup"><span data-stu-id="fa460-654">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="fa460-655">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="fa460-655">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="fa460-656">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-656">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-657">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fa460-657">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-658">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa460-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-659">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-659">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-660">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa460-660">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa460-661">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="fa460-661">The scoping system's name.</span></span>

<span data-ttu-id="fa460-662">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-662">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa460-663">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="fa460-663">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa460-664">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa460-664">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa460-665">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa460-665">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa460-666">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,5 ")</span><span class="sxs-lookup"><span data-stu-id="fa460-666">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="fa460-667">Definisce se la cache è write-back o Write-through o se le informazioni "variano in base all'indirizzo" o se sono definite singolarmente per ogni input/output.</span><span class="sxs-lookup"><span data-stu-id="fa460-667">Defines whether the cache is write-back or write-through, or whether the information "Varies with Address" or is defined individually for each input/output.</span></span> <span data-ttu-id="fa460-668">È possibile specificare anche "other" e "Unknown".</span><span class="sxs-lookup"><span data-stu-id="fa460-668">"Other" and "Unknown" also can be specified.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa460-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa460-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-670">Altro.</span><span class="sxs-lookup"><span data-stu-id="fa460-670">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa460-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa460-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-672">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fa460-672">Unknown.</span></span>

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="fa460-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write back** (3)</span><span class="sxs-lookup"><span data-stu-id="fa460-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write Back** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-674">Write back.</span><span class="sxs-lookup"><span data-stu-id="fa460-674">Write back.</span></span>

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="fa460-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Scrivi fino** a (4)</span><span class="sxs-lookup"><span data-stu-id="fa460-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Write Through** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-676">Scrivere.</span><span class="sxs-lookup"><span data-stu-id="fa460-676">Write through.</span></span>

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="fa460-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varia in base all'indirizzo** (5)</span><span class="sxs-lookup"><span data-stu-id="fa460-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varies with Address** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-678">Varia in base all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="fa460-678">Varies with address.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="fa460-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinazione per I/O** (6)</span><span class="sxs-lookup"><span data-stu-id="fa460-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fa460-680">Determinazione per I/O.</span><span class="sxs-lookup"><span data-stu-id="fa460-680">Determination per I/O.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa460-681">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa460-681">Remarks</span></span>

<span data-ttu-id="fa460-682">La classe **CIM \_ CacheMemory** è derivata dalla [**\_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-682">The **CIM\_CacheMemory** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="fa460-683">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="fa460-683">WMI does not implement this class.</span></span> <span data-ttu-id="fa460-684">Per ulteriori informazioni sulle classi derivate da **CIM \_ CacheMemory**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fa460-684">For more information about classes derived from **CIM\_CacheMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fa460-685">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="fa460-685">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fa460-686">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="fa460-686">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa460-687">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa460-687">Requirements</span></span>



| <span data-ttu-id="fa460-688">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa460-688">Requirement</span></span> | <span data-ttu-id="fa460-689">Valore</span><span class="sxs-lookup"><span data-stu-id="fa460-689">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa460-690">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa460-690">Minimum supported client</span></span><br/> | <span data-ttu-id="fa460-691">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa460-691">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa460-692">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa460-692">Minimum supported server</span></span><br/> | <span data-ttu-id="fa460-693">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa460-693">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa460-694">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa460-694">Namespace</span></span><br/>                | <span data-ttu-id="fa460-695">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fa460-695">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa460-696">MOF</span><span class="sxs-lookup"><span data-stu-id="fa460-696">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa460-697"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa460-697"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa460-698">DLL</span><span class="sxs-lookup"><span data-stu-id="fa460-698">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa460-699"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa460-699"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa460-700">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa460-700">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa460-701">**\_Memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="fa460-701">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

