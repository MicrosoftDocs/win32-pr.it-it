---
description: Win32 \_ CacheMemory&\# 32; La classe WMI rappresenta la memoria cache interna ed esterna in un sistema di computer.
ms.assetid: 9cfb992d-fbac-4e56-b4f3-61c0c93f5852
ms.tgt_platform: multiple
title: Classe Win32_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CacheMemory
- Win32_CacheMemory.Reset
- Win32_CacheMemory.SetPowerState
- Win32_CacheMemory.Access
- Win32_CacheMemory.AdditionalErrorData
- Win32_CacheMemory.Associativity
- Win32_CacheMemory.Availability
- Win32_CacheMemory.BlockSize
- Win32_CacheMemory.CacheSpeed
- Win32_CacheMemory.CacheType
- Win32_CacheMemory.Caption
- Win32_CacheMemory.ConfigManagerErrorCode
- Win32_CacheMemory.ConfigManagerUserConfig
- Win32_CacheMemory.CorrectableError
- Win32_CacheMemory.CreationClassName
- Win32_CacheMemory.CurrentSRAM
- Win32_CacheMemory.Description
- Win32_CacheMemory.DeviceID
- Win32_CacheMemory.EndingAddress
- Win32_CacheMemory.ErrorAccess
- Win32_CacheMemory.ErrorAddress
- Win32_CacheMemory.ErrorCleared
- Win32_CacheMemory.ErrorCorrectType
- Win32_CacheMemory.ErrorData
- Win32_CacheMemory.ErrorDataOrder
- Win32_CacheMemory.ErrorDescription
- Win32_CacheMemory.ErrorInfo
- Win32_CacheMemory.ErrorMethodology
- Win32_CacheMemory.ErrorResolution
- Win32_CacheMemory.ErrorTime
- Win32_CacheMemory.ErrorTransferSize
- Win32_CacheMemory.FlushTimer
- Win32_CacheMemory.InstallDate
- Win32_CacheMemory.InstalledSize
- Win32_CacheMemory.LastErrorCode
- Win32_CacheMemory.Level
- Win32_CacheMemory.LineSize
- Win32_CacheMemory.Location
- Win32_CacheMemory.MaxCacheSize
- Win32_CacheMemory.Name
- Win32_CacheMemory.NumberOfBlocks
- Win32_CacheMemory.OtherErrorDescription
- Win32_CacheMemory.PNPDeviceID
- Win32_CacheMemory.PowerManagementCapabilities
- Win32_CacheMemory.PowerManagementSupported
- Win32_CacheMemory.Purpose
- Win32_CacheMemory.ReadPolicy
- Win32_CacheMemory.ReplacementPolicy
- Win32_CacheMemory.StartingAddress
- Win32_CacheMemory.Status
- Win32_CacheMemory.StatusInfo
- Win32_CacheMemory.SupportedSRAM
- Win32_CacheMemory.SystemCreationClassName
- Win32_CacheMemory.SystemLevelAddress
- Win32_CacheMemory.SystemName
- Win32_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83a8fefbe1104f24f208d232b8f6bc134efefd83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878165"
---
# <a name="win32_cachememory-class"></a><span data-ttu-id="20f15-103">Win32 \_ CacheMemory (classe)</span><span class="sxs-lookup"><span data-stu-id="20f15-103">Win32\_CacheMemory class</span></span>

<span data-ttu-id="20f15-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CacheMemory Win32** rappresenta la memoria cache interna ed esterna in un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="20f15-104">The **Win32\_CacheMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents internal and external cache memory on a computer system.</span></span>

<span data-ttu-id="20f15-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="20f15-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="20f15-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="20f15-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f15-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20f15-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B97-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_CacheMemory : CIM_CacheMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Associativity;
  uint16   Availability;
  uint64   BlockSize;
  uint32   CacheSpeed;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  uint16   CurrentSRAM[];
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint16   ErrorCorrectType;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  uint32   FlushTimer;
  datetime InstallDate;
  uint32   InstalledSize;
  uint32   LastErrorCode;
  uint16   Level;
  uint32   LineSize;
  uint16   Location;
  uint32   MaxCacheSize;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  uint16   SupportedSRAM[];
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="20f15-108">Members</span><span class="sxs-lookup"><span data-stu-id="20f15-108">Members</span></span>

<span data-ttu-id="20f15-109">La classe **Win32 \_ CacheMemory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="20f15-109">The **Win32\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="20f15-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="20f15-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="20f15-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20f15-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20f15-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="20f15-112">Methods</span></span>

<span data-ttu-id="20f15-113">La classe **Win32 \_ CacheMemory** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="20f15-113">The **Win32\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="20f15-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="20f15-114">Method</span></span>            | <span data-ttu-id="20f15-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20f15-115">Description</span></span>                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f15-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="20f15-116">**Reset**</span></span>         | <span data-ttu-id="20f15-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="20f15-117">Not implemented.</span></span> <span data-ttu-id="20f15-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ CacheMemory**](cim-cachememory.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="20f15-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="20f15-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="20f15-119">**SetPowerState**</span></span> | <span data-ttu-id="20f15-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="20f15-120">Not implemented.</span></span> <span data-ttu-id="20f15-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ CacheMemory**](cim-cachememory.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="20f15-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="20f15-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20f15-122">Properties</span></span>

<span data-ttu-id="20f15-123">La classe **Win32 \_ CacheMemory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="20f15-123">The **Win32\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20f15-124">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="20f15-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-127">Tipo di accesso.</span><span class="sxs-lookup"><span data-stu-id="20f15-127">Type of access.</span></span>

<span data-ttu-id="20f15-128">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="20f15-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="20f15-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="20f15-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-132">Scrivibile</span><span class="sxs-lookup"><span data-stu-id="20f15-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="20f15-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="20f15-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="20f15-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-136">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="20f15-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="20f15-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,18 "," MIF. DMTF \| array di memoria fisica \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="20f15-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="20f15-139">Matrice di ottetti che contengono informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="20f15-139">Array of octets that hold additional error information.</span></span> <span data-ttu-id="20f15-140">Un esempio è la sindrome ECC o il ritorno dei bit di controllo se viene usata una metodologia di errore basata su CRC.</span><span class="sxs-lookup"><span data-stu-id="20f15-140">An example is ECC Syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="20f15-141">Nel secondo caso, se viene riconosciuto un errore a bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="20f15-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="20f15-142">Questo tipo di dati (sindrome ECC, bit check, dati bit di parità o altre informazioni fornite dal fornitore) è incluso in questo campo.</span><span class="sxs-lookup"><span data-stu-id="20f15-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="20f15-143">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-143">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="20f15-144">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-144">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-145">**Associatività**</span><span class="sxs-lookup"><span data-stu-id="20f15-145">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-146">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,15 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-149">Enumerazione Integer che definisce l'associatività della cache di sistema.</span><span class="sxs-lookup"><span data-stu-id="20f15-149">An integer enumeration that defines the system cache associativity.</span></span>

<span data-ttu-id="20f15-150">Questo valore deriva dal membro di **associatività** della struttura di **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-150">This value comes from the **Associativity** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="20f15-151">Questa proprietà viene ereditata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-151">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-152">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-152">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-153">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-153">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="20f15-154">Con **mapping diretto** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-154">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="20f15-155">**set bidirezionale-associativo** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-155">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="20f15-156">**set-associativo a 4 vie** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-156">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="20f15-157">**Completamente associativo** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-157">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="20f15-158">**set a 8 vie-associativo** (7)</span><span class="sxs-lookup"><span data-stu-id="20f15-158">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="20f15-159">**set-associativo a 16 vie** (8)</span><span class="sxs-lookup"><span data-stu-id="20f15-159">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-160">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="20f15-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-163">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="20f15-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-164">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-164">Availability and status of the device.</span></span>

<span data-ttu-id="20f15-165">Questo valore deriva dal membro di **configurazione** della cache della struttura delle **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-165">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="20f15-166">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-166">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="20f15-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-170">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="20f15-170">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="20f15-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="20f15-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="20f15-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="20f15-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="20f15-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="20f15-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="20f15-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="20f15-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="20f15-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="20f15-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="20f15-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="20f15-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="20f15-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="20f15-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="20f15-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="20f15-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="20f15-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-181">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="20f15-181">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="20f15-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="20f15-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-183">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="20f15-183">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="20f15-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="20f15-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-185">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="20f15-185">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="20f15-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="20f15-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="20f15-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="20f15-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-188">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="20f15-188">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="20f15-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="20f15-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-190">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="20f15-190">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="20f15-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="20f15-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-192">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="20f15-192">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="20f15-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="20f15-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-194">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="20f15-194">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="20f15-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="20f15-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-196">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="20f15-196">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-197">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="20f15-197">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-198">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20f15-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-200">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="20f15-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-201">Dimensioni in byte dei blocchi che formano questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="20f15-201">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="20f15-202">Se è sconosciuto o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1.</span><span class="sxs-lookup"><span data-stu-id="20f15-202">If unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="20f15-203">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-203">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="20f15-204">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="20f15-204">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-205">**CacheSpeed**</span><span class="sxs-lookup"><span data-stu-id="20f15-205">**CacheSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-206">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20f15-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-208">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| velocità della cache di tipo SMBIOS 7"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanosecondi")</span><span class="sxs-lookup"><span data-stu-id="20f15-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Cache Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-209">Velocità della cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-209">Speed of the cache.</span></span>

<span data-ttu-id="20f15-210">Questo valore deriva dal membro della **velocità della cache** della struttura delle informazioni della **cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-210">This value comes from the **Cache Speed** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="20f15-211">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="20f15-211">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-212">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-214">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-215">Tipo di cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-215">Type of cache.</span></span>

<span data-ttu-id="20f15-216">Questo valore deriva dal membro di **tipo cache di sistema** della struttura di **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-216">This value comes from the **System Cache Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="20f15-217">Questa proprietà viene ereditata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-217">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-218">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-218">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-219">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-219">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="20f15-220">**Istruzione** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-220">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="20f15-221">**Dati** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-221">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="20f15-222">**Unificato** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-222">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-223">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="20f15-223">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-226">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="20f15-226">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-227">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="20f15-227">Short description of the object a one-line string.</span></span>

<span data-ttu-id="20f15-228">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-229">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="20f15-229">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-230">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20f15-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-232">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20f15-232">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-233">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="20f15-233">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="20f15-234">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-234">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="20f15-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="20f15-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="20f15-236"> (0)</span><span class="sxs-lookup"><span data-stu-id="20f15-236">(0)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-237">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="20f15-237">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="20f15-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="20f15-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="20f15-239">(1)</span><span class="sxs-lookup"><span data-stu-id="20f15-239">(1)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-240">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="20f15-240">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20f15-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="20f15-242">(2)</span><span class="sxs-lookup"><span data-stu-id="20f15-242">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="20f15-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="20f15-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="20f15-244">(3)</span><span class="sxs-lookup"><span data-stu-id="20f15-244">(3)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-245">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="20f15-245">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="20f15-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="20f15-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="20f15-247">(4)</span><span class="sxs-lookup"><span data-stu-id="20f15-247">(4)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-248">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="20f15-248">Device is not working properly.</span></span> <span data-ttu-id="20f15-249">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="20f15-249">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="20f15-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="20f15-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="20f15-251">(5)</span><span class="sxs-lookup"><span data-stu-id="20f15-251">(5)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-252">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="20f15-252">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="20f15-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="20f15-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="20f15-254"> (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-254">(6)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-255">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="20f15-255">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="20f15-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="20f15-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="20f15-257">(7)</span><span class="sxs-lookup"><span data-stu-id="20f15-257">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="20f15-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="20f15-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="20f15-259">(8)</span><span class="sxs-lookup"><span data-stu-id="20f15-259">(8)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-260">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="20f15-260">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="20f15-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="20f15-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="20f15-262">(9)</span><span class="sxs-lookup"><span data-stu-id="20f15-262">(9)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-263">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="20f15-263">Device is not working properly.</span></span> <span data-ttu-id="20f15-264">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-264">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="20f15-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="20f15-266">(10)</span><span class="sxs-lookup"><span data-stu-id="20f15-266">(10)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-267">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-267">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="20f15-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="20f15-269">(11)</span><span class="sxs-lookup"><span data-stu-id="20f15-269">(11)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-270">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-270">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="20f15-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="20f15-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="20f15-272">12</span><span class="sxs-lookup"><span data-stu-id="20f15-272">(12)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-273">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="20f15-273">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="20f15-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="20f15-275">(13)</span><span class="sxs-lookup"><span data-stu-id="20f15-275">(13)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-276">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-276">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="20f15-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="20f15-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="20f15-278">(14)</span><span class="sxs-lookup"><span data-stu-id="20f15-278">(14)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-279">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="20f15-279">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="20f15-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="20f15-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="20f15-281">(15)</span><span class="sxs-lookup"><span data-stu-id="20f15-281">(15)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-282">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="20f15-282">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="20f15-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="20f15-284">(16)</span><span class="sxs-lookup"><span data-stu-id="20f15-284">(16)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-285">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-285">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="20f15-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="20f15-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="20f15-287">(17)</span><span class="sxs-lookup"><span data-stu-id="20f15-287">(17)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-288">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="20f15-288">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20f15-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="20f15-290">(18)</span><span class="sxs-lookup"><span data-stu-id="20f15-290">(18)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-291">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-291">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="20f15-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="20f15-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="20f15-293">(19)</span><span class="sxs-lookup"><span data-stu-id="20f15-293">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="20f15-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="20f15-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="20f15-295">(20)</span><span class="sxs-lookup"><span data-stu-id="20f15-295">(20)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-296">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="20f15-296">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="20f15-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="20f15-298">(21)</span><span class="sxs-lookup"><span data-stu-id="20f15-298">(21)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-299">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="20f15-299">System failure.</span></span> <span data-ttu-id="20f15-300">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="20f15-300">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="20f15-301">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-301">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="20f15-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="20f15-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="20f15-303">(22)</span><span class="sxs-lookup"><span data-stu-id="20f15-303">(22)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-304">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="20f15-304">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="20f15-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="20f15-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="20f15-306">(23)</span><span class="sxs-lookup"><span data-stu-id="20f15-306">(23)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-307">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="20f15-307">System failure.</span></span> <span data-ttu-id="20f15-308">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="20f15-308">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="20f15-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="20f15-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="20f15-310">(24)</span><span class="sxs-lookup"><span data-stu-id="20f15-310">(24)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-311">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="20f15-311">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="20f15-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="20f15-313">(25)</span><span class="sxs-lookup"><span data-stu-id="20f15-313">(25)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-314">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-314">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="20f15-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="20f15-316">(26)</span><span class="sxs-lookup"><span data-stu-id="20f15-316">(26)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-317">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-317">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="20f15-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="20f15-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="20f15-319">(27)</span><span class="sxs-lookup"><span data-stu-id="20f15-319">(27)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-320">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="20f15-320">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="20f15-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="20f15-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="20f15-322">(28)</span><span class="sxs-lookup"><span data-stu-id="20f15-322">(28)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-323">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="20f15-323">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="20f15-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="20f15-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="20f15-325">(29)</span><span class="sxs-lookup"><span data-stu-id="20f15-325">(29)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-326">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="20f15-326">Device is disabled.</span></span> <span data-ttu-id="20f15-327">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="20f15-327">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="20f15-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="20f15-329">(30)</span><span class="sxs-lookup"><span data-stu-id="20f15-329">(30)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-330">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20f15-330">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20f15-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20f15-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="20f15-332">31</span><span class="sxs-lookup"><span data-stu-id="20f15-332">(31)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-333">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="20f15-333">Device is not working properly.</span></span> <span data-ttu-id="20f15-334">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="20f15-334">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-335">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="20f15-335">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-336">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="20f15-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-338">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20f15-338">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-339">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="20f15-339">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="20f15-340">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-341">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="20f15-341">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-342">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="20f15-342">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-344">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. DMTF \| matrice di memoria fisica \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-345">Se **true**, l'errore più recente è correggibile.</span><span class="sxs-lookup"><span data-stu-id="20f15-345">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="20f15-346">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-346">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="20f15-347">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-347">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-348">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20f15-348">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-351">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20f15-351">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20f15-352">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="20f15-352">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="20f15-353">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="20f15-353">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="20f15-354">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-355">**CurrentSRAM**</span><span class="sxs-lookup"><span data-stu-id="20f15-355">**CurrentSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-356">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-356">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20f15-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-358">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| Current SRAM Type")</span><span class="sxs-lookup"><span data-stu-id="20f15-358">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Current SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-359">Matrice di tipi di memoria statica ad accesso casuale (SRAM) utilizzata per la memoria cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-359">Array of types of Static Random Access Memory (SRAM) being used for the cache memory.</span></span>

<span data-ttu-id="20f15-360">Questo valore deriva dal membro di **tipo SRAM corrente** della struttura di **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-360">This value comes from the **Current SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-361">**Altro** (0)</span><span class="sxs-lookup"><span data-stu-id="20f15-361">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-362">**Sconosciuto** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-362">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="20f15-363">**Non in sequenza** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-363">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="20f15-364">**Sequenza** di espansione (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-364">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="20f15-365">**Impulso della pipeline** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-365">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="20f15-366">**Sincrona** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-366">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="20f15-367">**Asincrono** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-367">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-368">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="20f15-368">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-369">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-371">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="20f15-371">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-372">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="20f15-372">Description of the object.</span></span>

<span data-ttu-id="20f15-373">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-374">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="20f15-374">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-375">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-377">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="20f15-377">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-378">Identificatore univoco della cache rappresentata da un'istanza di **Win32 \_ CacheMemory**.</span><span class="sxs-lookup"><span data-stu-id="20f15-378">Unique identifier of the cache represented by an instance of **Win32\_CacheMemory**.</span></span>

<span data-ttu-id="20f15-379">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="20f15-380">Esempio: "cache memory 1"</span><span class="sxs-lookup"><span data-stu-id="20f15-380">Example: "Cache Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="20f15-381">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="20f15-381">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-382">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20f15-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-384">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,4 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="20f15-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-385">Indirizzo finale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria, per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="20f15-385">Ending address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="20f15-386">L'indirizzo finale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="20f15-386">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="20f15-387">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-387">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="20f15-388">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="20f15-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-389">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="20f15-389">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-390">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-392">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,15 "," MIF. DMTF \| matrice di memoria fisica \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-393">Operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="20f15-393">Memory access operation that caused the last error.</span></span> <span data-ttu-id="20f15-394">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="20f15-394">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="20f15-395">Se **errorInfo** è uguale a 3 (OK), questa proprietà non ha significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-395">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="20f15-396">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-396">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-397">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-398">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="20f15-399">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-399">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="20f15-400">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-400">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="20f15-401">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-401">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-402">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="20f15-402">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-403">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20f15-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-405">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. DMTF \| matrice di memoria fisica \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-406">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="20f15-406">Address of the last memory error.</span></span> <span data-ttu-id="20f15-407">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="20f15-407">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="20f15-408">Se **errorInfo** è uguale a 3 (OK), questa proprietà non ha significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-408">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="20f15-409">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-409">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="20f15-410">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="20f15-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-411">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="20f15-411">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-412">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="20f15-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-414">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="20f15-414">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="20f15-415">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-416">**ErrorCorrectType**</span><span class="sxs-lookup"><span data-stu-id="20f15-416">**ErrorCorrectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-417">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-419">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo di \| correzione degli errori di tipo 7 SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="20f15-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Error Correction Type")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-420">Metodo di correzione degli errori utilizzato dalla memoria cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-420">Error correction method used by the cache memory.</span></span>

<span data-ttu-id="20f15-421">Questo valore deriva dal membro del **tipo di correzione degli errori** della struttura di informazioni della **cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-421">This value comes from the **Error Correction Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="20f15-422">**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="20f15-422">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-423">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-423">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-424">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-424">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="20f15-425">**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-425">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="20f15-426">**Parità** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-426">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="20f15-427">**Ecc a bit singolo** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-427">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="20f15-428">**Ecc a più bit** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-428">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-429">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="20f15-429">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-430">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="20f15-430">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="20f15-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-432">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. DMTF \| array di memoria fisica \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="20f15-432">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="20f15-433">Matrice di dati acquisiti durante l'ultimo accesso errato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="20f15-433">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="20f15-434">I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="20f15-434">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="20f15-435">Se **ErrorTransferSize** è 0 (zero), questa proprietà non ha significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-435">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="20f15-436">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-436">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-437">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="20f15-437">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-438">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-440">Ordinamento dei dati archiviati nella proprietà **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="20f15-440">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="20f15-441">Se **ErrorTransferSize** è 0 (zero), questa proprietà non ha significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-441">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="20f15-442">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-443">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="20f15-443">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="20f15-444">**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-444">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="20f15-445">**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-445">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-446">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="20f15-446">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-447">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-449">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="20f15-449">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="20f15-450">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-451">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="20f15-451">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-452">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-454">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Matrice di memoria fisica DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="20f15-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-455">Tipo di errore che si è verificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="20f15-455">Type of error that occurred most recently.</span></span> <span data-ttu-id="20f15-456">I valori 12-14 non sono definiti nello schema CIM perché in DMI combinano la semantica del tipo di errore e se sono stati corretti o meno.</span><span class="sxs-lookup"><span data-stu-id="20f15-456">The values 12-14 are undefined in the CIM schema because in DMI they mix the semantics of the type of error and whether it was correctable or not.</span></span> <span data-ttu-id="20f15-457">Quest'ultimo è indicato nella proprietà **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="20f15-457">The latter is indicated in the property **CorrectableError**.</span></span>

<span data-ttu-id="20f15-458">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-459">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-460">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-460">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="20f15-461">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-461">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="20f15-462">**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-462">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="20f15-463">**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-463">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="20f15-464">**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-464">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="20f15-465">**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="20f15-465">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="20f15-466">**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="20f15-466">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="20f15-467">**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="20f15-467">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="20f15-468">**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="20f15-468">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="20f15-469">**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="20f15-469">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="20f15-470">Non **definito** (12)</span><span class="sxs-lookup"><span data-stu-id="20f15-470">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="20f15-471">Non **definito** (13)</span><span class="sxs-lookup"><span data-stu-id="20f15-471">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="20f15-472">Non **definito** (14)</span><span class="sxs-lookup"><span data-stu-id="20f15-472">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-473">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="20f15-473">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-476">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-476">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-477">Informazioni dettagliate sugli algoritmi di parità o CRC, ECC o altri meccanismi utilizzati.</span><span class="sxs-lookup"><span data-stu-id="20f15-477">Details on the parity or CRC algorithms, ECC, or other mechanisms used.</span></span>

<span data-ttu-id="20f15-478">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-478">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-479">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="20f15-479">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-480">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20f15-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-482">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,21 "," MIF. DMTF \| array di memoria fisica \| 001,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="20f15-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-483">Intervallo, in byte, in cui è possibile risolvere l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="20f15-483">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="20f15-484">Se, ad esempio, gli indirizzi di errore vengono risolti in bit 11, ovvero in base a una tipica pagina, gli errori possono essere risolti in limiti di 4 KB e questa proprietà è impostata su 4000.</span><span class="sxs-lookup"><span data-stu-id="20f15-484">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="20f15-485">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-485">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="20f15-486">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-486">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="20f15-487">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="20f15-487">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-488">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="20f15-488">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-489">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20f15-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-490">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-491">Ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="20f15-491">Time that the last memory error occurred.</span></span> <span data-ttu-id="20f15-492">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="20f15-492">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="20f15-493">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-493">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="20f15-494">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-494">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-495">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="20f15-495">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-496">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20f15-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-497">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-498">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,16 "," MIF. DMTF \| array di memoria fisica \| 001,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="20f15-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-499">Dimensioni del trasferimento dei dati in bit che hanno causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="20f15-499">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="20f15-500">0 (zero) indica che non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="20f15-500">0 (zero) indicates no error.</span></span> <span data-ttu-id="20f15-501">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="20f15-501">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="20f15-502">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-502">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-503">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="20f15-503">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-504">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20f15-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-505">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-506">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache \| di sistema 003,14 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" secondi ")</span><span class="sxs-lookup"><span data-stu-id="20f15-506">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-507">Quantità massima di tempo, in secondi, per cui è possibile che le righe o i bucket sporchi rimangano nella cache prima che vengano scaricati.</span><span class="sxs-lookup"><span data-stu-id="20f15-507">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="20f15-508">Il valore 0 (zero) indica che uno scaricamento della cache non è controllato da un timer di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="20f15-508">A value of 0 (zero) indicates that a cache flush is not controlled by a flushing timer.</span></span>

<span data-ttu-id="20f15-509">Questa proprietà viene ereditata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-509">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="20f15-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-511">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20f15-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-512">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-513">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="20f15-513">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-514">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="20f15-514">Date and time the object was installed.</span></span> <span data-ttu-id="20f15-515">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="20f15-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="20f15-516">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-517">**InstalledSize**</span><span class="sxs-lookup"><span data-stu-id="20f15-517">**InstalledSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-518">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20f15-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-520">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| installato size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="20f15-520">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Installed Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-521">Dimensioni correnti della memoria cache installata.</span><span class="sxs-lookup"><span data-stu-id="20f15-521">Current size of the installed cache memory.</span></span>

<span data-ttu-id="20f15-522">Questo valore deriva dal membro **size installato** della struttura di **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-522">This value comes from the **Installed Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="20f15-523">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="20f15-523">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-524">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20f15-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-525">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-526">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="20f15-526">Last error code reported by the logical device.</span></span>

<span data-ttu-id="20f15-527">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-528">**Level**</span><span class="sxs-lookup"><span data-stu-id="20f15-528">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-529">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-529">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-530">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-531">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-531">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-532">Livello della cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-532">Level of the cache.</span></span>

<span data-ttu-id="20f15-533">Questo valore deriva dal membro di **configurazione** della cache della struttura delle **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-533">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="20f15-534">Questa proprietà viene ereditata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-534">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="20f15-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primario** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="20f15-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondario** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="20f15-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terziario** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="20f15-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-541">**LineSize**</span><span class="sxs-lookup"><span data-stu-id="20f15-541">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-542">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20f15-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-543">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-544">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Cache \| 003,10 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="20f15-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-545">Dimensione, in byte, di un singolo bucket o riga della cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-545">Size, in bytes, of a single cache bucket or line.</span></span>

<span data-ttu-id="20f15-546">Questa proprietà viene ereditata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-546">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-547">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="20f15-547">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-548">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-548">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-549">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-550">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 7 \| location")</span><span class="sxs-lookup"><span data-stu-id="20f15-550">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-551">Posizione fisica della memoria cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-551">Physical location of the cache memory.</span></span>

<span data-ttu-id="20f15-552">Questo valore deriva dal membro di **configurazione** della cache della struttura delle **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-552">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="20f15-553">**Interno** (0)</span><span class="sxs-lookup"><span data-stu-id="20f15-553">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

<span data-ttu-id="20f15-554">**Esterno** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-554">**External** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="20f15-555">**Riservato** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-555">**Reserved** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-556">**Sconosciuto** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-556">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-557">**MaxCacheSize**</span><span class="sxs-lookup"><span data-stu-id="20f15-557">**MaxCacheSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-558">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20f15-558">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-559">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-560">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 7 \| dimensione massima cache"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="20f15-560">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Maximum Cache Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-561">Dimensioni massime della cache installabili in questa particolare memoria cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-561">Maximum cache size installable to this particular cache memory.</span></span>

<span data-ttu-id="20f15-562">Questo valore deriva dal membro **dimensione massima della cache** della struttura delle **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-562">This value comes from the **Maximum Cache Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="20f15-563">**Nome**</span><span class="sxs-lookup"><span data-stu-id="20f15-563">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-564">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-564">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-565">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-565">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-566">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="20f15-566">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-567">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="20f15-567">Label by which the object is known.</span></span> <span data-ttu-id="20f15-568">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="20f15-568">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="20f15-569">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-569">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-570">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="20f15-570">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-571">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20f15-571">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-572">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-573">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="20f15-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-574">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="20f15-574">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="20f15-575">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="20f15-575">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="20f15-576">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="20f15-576">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="20f15-577">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-577">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="20f15-578">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="20f15-578">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-579">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="20f15-579">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-580">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-581">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-582">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="20f15-582">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-583">Stringa in formato libero che fornisce ulteriori informazioni se la proprietà **ErrorType** è impostata su 1, other.</span><span class="sxs-lookup"><span data-stu-id="20f15-583">Free-form string providing more information if the **ErrorType** property is set to 1, Other.</span></span> <span data-ttu-id="20f15-584">In caso contrario, questa stringa non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-584">Otherwise, this string has no meaning.</span></span>

<span data-ttu-id="20f15-585">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-585">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-586">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="20f15-586">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-587">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-588">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-589">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20f15-589">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-590">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="20f15-590">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="20f15-591">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="20f15-592">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="20f15-592">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="20f15-593">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="20f15-593">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-594">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-594">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20f15-595">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-595">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-596">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="20f15-596">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="20f15-597">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="20f15-597">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="20f15-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="20f15-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="20f15-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="20f15-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-602">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="20f15-602">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="20f15-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-604">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="20f15-604">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="20f15-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-606">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="20f15-606">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="20f15-607">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="20f15-607">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="20f15-608">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="20f15-608">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="20f15-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-610">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="20f15-610">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="20f15-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="20f15-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="20f15-612">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="20f15-612">Timed Power-On Supported</span></span>

<span data-ttu-id="20f15-613">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="20f15-613">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-614">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="20f15-614">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-615">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="20f15-615">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-616">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-616">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-617">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="20f15-617">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="20f15-618">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="20f15-618">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="20f15-619">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-619">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-620">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="20f15-620">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-621">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-621">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-622">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-623">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="20f15-623">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="20f15-624">Questo valore deriva dal membro della **designazione del socket** della struttura di **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-624">This value comes from the **Socket Designation** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="20f15-625">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-625">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-626">**Disporre**</span><span class="sxs-lookup"><span data-stu-id="20f15-626">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-627">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-627">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-628">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-629">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-629">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-630">Criteri che verranno utilizzati dalla cache per gestire le richieste di lettura.</span><span class="sxs-lookup"><span data-stu-id="20f15-630">Policy that shall be employed by the cache for handling read requests.</span></span>

<span data-ttu-id="20f15-631">Questa proprietà viene ereditata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-631">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-632">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-632">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-633">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-633">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="20f15-634">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-634">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="20f15-635">**Read-Ahead** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-635">**Read-Ahead** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="20f15-636">**Lettura e Read-Ahead** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-636">**Read and Read-Ahead** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="20f15-637">**Determinazione per I/O** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-637">**Determination Per I/O** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-638">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="20f15-638">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-639">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-639">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-640">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-640">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-641">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,12 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-641">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-642">Algoritmo per determinare le righe o i bucket della cache da riutilizzare.</span><span class="sxs-lookup"><span data-stu-id="20f15-642">Algorithm to determine which cache lines or buckets should be reused.</span></span>

<span data-ttu-id="20f15-643">Questa proprietà viene ereditata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-643">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-644">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-644">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-645">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-645">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="20f15-646">**Utilizzato meno di recente (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-646">**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="20f15-647">**FIFO (First in First out)** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-647">**First In First Out (FIFO)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="20f15-648">**LIFO (Last in First out)** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-648">**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="20f15-649">**Uso meno frequente (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-649">**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="20f15-650">**Uso più frequente (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="20f15-650">**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="20f15-651">**Più algoritmi dipendenti dai dati** (8)</span><span class="sxs-lookup"><span data-stu-id="20f15-651">**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-652">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="20f15-652">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-653">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20f15-653">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-654">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-654">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-655">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,3 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="20f15-655">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-656">Indirizzo iniziale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria, per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="20f15-656">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="20f15-657">L'indirizzo iniziale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="20f15-657">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="20f15-658">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-658">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="20f15-659">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="20f15-659">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-660">**Status**</span><span class="sxs-lookup"><span data-stu-id="20f15-660">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-661">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-662">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-663">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="20f15-663">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-664">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="20f15-664">Current status of the object.</span></span> <span data-ttu-id="20f15-665">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="20f15-665">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="20f15-666">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="20f15-666">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="20f15-667">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="20f15-667">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="20f15-668">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="20f15-668">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="20f15-669">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="20f15-669">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="20f15-670">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-670">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="20f15-671">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="20f15-671">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="20f15-672">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="20f15-672">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="20f15-673">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="20f15-673">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="20f15-674">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="20f15-674">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-675">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="20f15-675">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="20f15-676">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="20f15-676">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="20f15-677">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="20f15-677">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="20f15-678">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="20f15-678">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="20f15-679">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="20f15-679">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="20f15-680">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="20f15-680">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="20f15-681">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="20f15-681">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="20f15-682">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="20f15-682">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="20f15-683">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="20f15-683">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-684">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="20f15-684">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-685">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-685">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-686">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-687">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-687">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-688">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="20f15-688">State of the logical device.</span></span> <span data-ttu-id="20f15-689">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="20f15-689">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="20f15-690">Questo valore deriva dal membro di **configurazione** della cache della struttura delle **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-690">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="20f15-691">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-691">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-692">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-692">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-693">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-693">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="20f15-694">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-694">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="20f15-695">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-695">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="20f15-696">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-696">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-697">**SupportedSRAM**</span><span class="sxs-lookup"><span data-stu-id="20f15-697">**SupportedSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-698">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-698">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20f15-699">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-700">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| supported SRAM Type")</span><span class="sxs-lookup"><span data-stu-id="20f15-700">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Supported SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-701">Matrice di tipi supportati di memoria statica ad accesso casuale (SRAM) che possono essere usati per la memoria cache.</span><span class="sxs-lookup"><span data-stu-id="20f15-701">Array of supported types of Static Random Access Memory (SRAM) that can be used for the cache memory.</span></span>

<span data-ttu-id="20f15-702">Questo valore deriva dal membro di **tipo SRAM supportato** della struttura di **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-702">This value comes from the **Supported SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-703">**Altro** (0)</span><span class="sxs-lookup"><span data-stu-id="20f15-703">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-704">**Sconosciuto** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-704">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="20f15-705">**Non in sequenza** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-705">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="20f15-706">**Sequenza** di espansione (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-706">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="20f15-707">**Impulso della pipeline** (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-707">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="20f15-708">**Sincrona** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-708">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="20f15-709">**Asincrono** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-709">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20f15-710">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20f15-710">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-711">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-711">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-712">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-713">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20f15-713">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20f15-714">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="20f15-714">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="20f15-715">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-715">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-716">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="20f15-716">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-717">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="20f15-717">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-718">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-718">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20f15-719">Se **true**, le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="20f15-719">If **True**, the address information in the property **ErrorAddress** is a system-level address.</span></span> <span data-ttu-id="20f15-720">Se **false**, si tratta di un indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="20f15-720">If **False**, it is a physical address.</span></span> <span data-ttu-id="20f15-721">Se la proprietà **errorInfo** è uguale a 3, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="20f15-721">If the **ErrorInfo** property is equal to 3, then this property has no meaning.</span></span>

<span data-ttu-id="20f15-722">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-722">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-723">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="20f15-723">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-724">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20f15-724">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-725">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-726">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20f15-726">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20f15-727">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="20f15-727">Name of the scoping system.</span></span>

<span data-ttu-id="20f15-728">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-728">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20f15-729">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="20f15-729">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20f15-730">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20f15-730">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20f15-731">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20f15-731">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20f15-732">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,5 ")</span><span class="sxs-lookup"><span data-stu-id="20f15-732">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="20f15-733">Definizione dei criteri di scrittura.</span><span class="sxs-lookup"><span data-stu-id="20f15-733">Write policy definition.</span></span>

<span data-ttu-id="20f15-734">Questo valore deriva dal membro di **configurazione** della cache della struttura delle **informazioni della cache** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="20f15-734">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="20f15-735">Questa proprietà viene ereditata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-735">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20f15-736">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20f15-736">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20f15-737">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="20f15-737">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="20f15-738">**Write back** (3)</span><span class="sxs-lookup"><span data-stu-id="20f15-738">**Write Back** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="20f15-739">**Scrivi fino** a (4)</span><span class="sxs-lookup"><span data-stu-id="20f15-739">**Write Through** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="20f15-740">**Varia in base all'indirizzo** (5)</span><span class="sxs-lookup"><span data-stu-id="20f15-740">**Varies with Address** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="20f15-741">**Determinazione per I/O** (6)</span><span class="sxs-lookup"><span data-stu-id="20f15-741">**Determination Per I/O** (6)</span></span>


<span data-ttu-id="20f15-742"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="20f15-742"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="20f15-743">Commenti</span><span class="sxs-lookup"><span data-stu-id="20f15-743">Remarks</span></span>

<span data-ttu-id="20f15-744">La classe **Win32 \_ CacheMemory** è derivata da [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="20f15-744">The **Win32\_CacheMemory** class is derived from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20f15-745">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20f15-745">Requirements</span></span>



| <span data-ttu-id="20f15-746">Requisito</span><span class="sxs-lookup"><span data-stu-id="20f15-746">Requirement</span></span> | <span data-ttu-id="20f15-747">Valore</span><span class="sxs-lookup"><span data-stu-id="20f15-747">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20f15-748">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20f15-748">Minimum supported client</span></span><br/> | <span data-ttu-id="20f15-749">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20f15-749">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20f15-750">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20f15-750">Minimum supported server</span></span><br/> | <span data-ttu-id="20f15-751">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20f15-751">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20f15-752">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="20f15-752">Namespace</span></span><br/>                | <span data-ttu-id="20f15-753">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="20f15-753">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20f15-754">MOF</span><span class="sxs-lookup"><span data-stu-id="20f15-754">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20f15-755"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20f15-755"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20f15-756">DLL</span><span class="sxs-lookup"><span data-stu-id="20f15-756">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20f15-757"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20f15-757"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f15-758">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20f15-758">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f15-759">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="20f15-759">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="20f15-760">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="20f15-760">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

