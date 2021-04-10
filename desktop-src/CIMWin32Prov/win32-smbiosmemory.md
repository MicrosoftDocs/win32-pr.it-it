---
description: La \_ classe WMI astratta Win32 SMBIOSMemory rappresenta le proprietà di una memoria di sistema del computer come illustrato nell'interfaccia SMBIOS (System Management BIOS).
ms.assetid: 2f609fc6-f0f5-45a5-9f9a-3873da034d49
ms.tgt_platform: multiple
title: Classe Win32_SMBIOSMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SMBIOSMemory
- Win32_SMBIOSMemory.Reset
- Win32_SMBIOSMemory.SetPowerState
- Win32_SMBIOSMemory.Access
- Win32_SMBIOSMemory.AdditionalErrorData
- Win32_SMBIOSMemory.Availability
- Win32_SMBIOSMemory.BlockSize
- Win32_SMBIOSMemory.Caption
- Win32_SMBIOSMemory.ConfigManagerErrorCode
- Win32_SMBIOSMemory.ConfigManagerUserConfig
- Win32_SMBIOSMemory.CorrectableError
- Win32_SMBIOSMemory.CreationClassName
- Win32_SMBIOSMemory.Description
- Win32_SMBIOSMemory.DeviceID
- Win32_SMBIOSMemory.EndingAddress
- Win32_SMBIOSMemory.ErrorAccess
- Win32_SMBIOSMemory.ErrorAddress
- Win32_SMBIOSMemory.ErrorCleared
- Win32_SMBIOSMemory.ErrorData
- Win32_SMBIOSMemory.ErrorDataOrder
- Win32_SMBIOSMemory.ErrorDescription
- Win32_SMBIOSMemory.ErrorInfo
- Win32_SMBIOSMemory.ErrorMethodology
- Win32_SMBIOSMemory.ErrorResolution
- Win32_SMBIOSMemory.ErrorTime
- Win32_SMBIOSMemory.ErrorTransferSize
- Win32_SMBIOSMemory.InstallDate
- Win32_SMBIOSMemory.LastErrorCode
- Win32_SMBIOSMemory.Name
- Win32_SMBIOSMemory.NumberOfBlocks
- Win32_SMBIOSMemory.OtherErrorDescription
- Win32_SMBIOSMemory.PNPDeviceID
- Win32_SMBIOSMemory.PowerManagementCapabilities
- Win32_SMBIOSMemory.PowerManagementSupported
- Win32_SMBIOSMemory.Purpose
- Win32_SMBIOSMemory.StartingAddress
- Win32_SMBIOSMemory.Status
- Win32_SMBIOSMemory.StatusInfo
- Win32_SMBIOSMemory.SystemCreationClassName
- Win32_SMBIOSMemory.SystemLevelAddress
- Win32_SMBIOSMemory.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4dc7a42732dfb00d965f79045254878f690309fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127454"
---
# <a name="win32_smbiosmemory-class"></a><span data-ttu-id="94a80-103">Win32 \_ SMBIOSMemory (classe)</span><span class="sxs-lookup"><span data-stu-id="94a80-103">Win32\_SMBIOSMemory class</span></span>

<span data-ttu-id="94a80-104">La [classe WMI](../wmisdk/retrieving-a-class.md) astratta **Win32 \_ SMBIOSMemory** rappresenta le proprietà di una memoria di sistema del computer come illustrato nell'interfaccia SMBIOS (System Management BIOS).</span><span class="sxs-lookup"><span data-stu-id="94a80-104">The **Win32\_SMBIOSMemory** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a computer system memory as seen through the system management BIOS (SMBIOS) interface.</span></span> <span data-ttu-id="94a80-105">L'interfaccia SMBIOS non distingue tra le memorie non volatili, volatili e Flash.</span><span class="sxs-lookup"><span data-stu-id="94a80-105">The SMBIOS interface does not distinguish between nonvolatile, volatile, and flash memories.</span></span> <span data-ttu-id="94a80-106">La classe [**CIM \_ Memory**](cim-memory.md) è la classe padre di tutti i tipi di memoria.</span><span class="sxs-lookup"><span data-stu-id="94a80-106">The [**CIM\_Memory**](cim-memory.md) class is the parent class of all types of memory.</span></span>

<span data-ttu-id="94a80-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="94a80-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="94a80-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="94a80-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a80-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94a80-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FECB095B-F0FA-11d2-8617-0000F8102E5F}"), AMENDMENT]
class Win32_SMBIOSMemory : CIM_StorageExtent
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16e  StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="94a80-110">Members</span><span class="sxs-lookup"><span data-stu-id="94a80-110">Members</span></span>

<span data-ttu-id="94a80-111">La classe **Win32 \_ SMBIOSMemory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="94a80-111">The **Win32\_SMBIOSMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="94a80-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="94a80-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="94a80-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94a80-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="94a80-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="94a80-114">Methods</span></span>

<span data-ttu-id="94a80-115">La classe **Win32 \_ SMBIOSMemory** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="94a80-115">The **Win32\_SMBIOSMemory** class has these methods.</span></span>



| <span data-ttu-id="94a80-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="94a80-116">Method</span></span>            | <span data-ttu-id="94a80-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94a80-117">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a80-118">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="94a80-118">**Reset**</span></span>         | <span data-ttu-id="94a80-119">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="94a80-119">Not implemented.</span></span> <span data-ttu-id="94a80-120">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/>                 |
| <span data-ttu-id="94a80-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="94a80-121">**SetPowerState**</span></span> | <span data-ttu-id="94a80-122">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="94a80-122">Not implemented.</span></span> <span data-ttu-id="94a80-123">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="94a80-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94a80-124">Properties</span></span>

<span data-ttu-id="94a80-125">La classe **Win32 \_ SMBIOSMemory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="94a80-125">The **Win32\_SMBIOSMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94a80-126">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="94a80-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94a80-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a80-129">Tipo di accesso.</span><span class="sxs-lookup"><span data-stu-id="94a80-129">Type of access.</span></span>

<span data-ttu-id="94a80-130">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="94a80-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="94a80-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="94a80-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="94a80-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="94a80-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-134">Scrivibile</span><span class="sxs-lookup"><span data-stu-id="94a80-134">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="94a80-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="94a80-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="94a80-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="94a80-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-137">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="94a80-137">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-138">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="94a80-138">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="94a80-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-140">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 18 \| 32-bit memory Error Information Error \| Syndrome"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="94a80-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="94a80-141">Matrice di ottetti che contengono informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="94a80-141">Array of octets that hold additional error information.</span></span> <span data-ttu-id="94a80-142">Un esempio è la sindrome di controllo degli errori e correzione (ECC) oppure la restituzione dei bit di controllo se viene utilizzata una metodologia di errore basata su CRC.</span><span class="sxs-lookup"><span data-stu-id="94a80-142">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="94a80-143">In quest'ultimo caso, se viene riconosciuto un errore di bit singolo e l'algoritmo CRC (Ciclic ridondance check) è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="94a80-143">In the latter case, if a single bit error is recognized and the cyclical redundancy check (CRC) algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="94a80-144">Questo tipo di dati (sindrome ECC, dati di controllo bit o bit di parità o altre informazioni fornite dal fornitore) è incluso in questo campo.</span><span class="sxs-lookup"><span data-stu-id="94a80-144">This type of data (ECC Syndrome, Check Bit or Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="94a80-145">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-145">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="94a80-146">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="94a80-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-147">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94a80-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-149">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="94a80-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-150">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-150">Availability and status of the device.</span></span>

<span data-ttu-id="94a80-151">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="94a80-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="94a80-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="94a80-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="94a80-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="94a80-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-155">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="94a80-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="94a80-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="94a80-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="94a80-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="94a80-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="94a80-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="94a80-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="94a80-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="94a80-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="94a80-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="94a80-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="94a80-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="94a80-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="94a80-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="94a80-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="94a80-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="94a80-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="94a80-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="94a80-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="94a80-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="94a80-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-166">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="94a80-166">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="94a80-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="94a80-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-168">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="94a80-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="94a80-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="94a80-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-170">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="94a80-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="94a80-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="94a80-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="94a80-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="94a80-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-173">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="94a80-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="94a80-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="94a80-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-175">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="94a80-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="94a80-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="94a80-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-177">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="94a80-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="94a80-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="94a80-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-179">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="94a80-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="94a80-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="94a80-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-181">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="94a80-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="94a80-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-183">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94a80-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-185">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](../wmisdk/standard-qualifiers.md) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="94a80-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-186">Dimensioni in byte dei blocchi che formano questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="94a80-186">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="94a80-187">Se è sconosciuto o se un concetto di blocco non è valido (ad esempio per extent di aggregazione, memoria o dischi logici), immettere 1.</span><span class="sxs-lookup"><span data-stu-id="94a80-187">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="94a80-188">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="94a80-189">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-190">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="94a80-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-193">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="94a80-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-194">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="94a80-194">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="94a80-195">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-196">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="94a80-196">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-197">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94a80-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-199">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="94a80-199">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-200">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="94a80-200">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="94a80-201">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-201">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="94a80-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="94a80-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="94a80-203"> (0)</span><span class="sxs-lookup"><span data-stu-id="94a80-203">(0)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-204">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="94a80-204">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="94a80-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="94a80-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="94a80-206">(1)</span><span class="sxs-lookup"><span data-stu-id="94a80-206">(1)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-207">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="94a80-207">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="94a80-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="94a80-209">(2)</span><span class="sxs-lookup"><span data-stu-id="94a80-209">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="94a80-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="94a80-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="94a80-211">(3)</span><span class="sxs-lookup"><span data-stu-id="94a80-211">(3)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-212">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="94a80-212">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="94a80-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="94a80-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="94a80-214">(4)</span><span class="sxs-lookup"><span data-stu-id="94a80-214">(4)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-215">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="94a80-215">Device is not working properly.</span></span> <span data-ttu-id="94a80-216">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="94a80-216">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="94a80-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="94a80-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="94a80-218">(5)</span><span class="sxs-lookup"><span data-stu-id="94a80-218">(5)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-219">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="94a80-219">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="94a80-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="94a80-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="94a80-221"> (6)</span><span class="sxs-lookup"><span data-stu-id="94a80-221">(6)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-222">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="94a80-222">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="94a80-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="94a80-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="94a80-224">(7)</span><span class="sxs-lookup"><span data-stu-id="94a80-224">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="94a80-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="94a80-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="94a80-226">(8)</span><span class="sxs-lookup"><span data-stu-id="94a80-226">(8)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-227">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="94a80-227">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="94a80-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="94a80-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="94a80-229">(9)</span><span class="sxs-lookup"><span data-stu-id="94a80-229">(9)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-230">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="94a80-230">Device is not working properly.</span></span> <span data-ttu-id="94a80-231">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-231">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="94a80-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="94a80-233">(10)</span><span class="sxs-lookup"><span data-stu-id="94a80-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-234">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="94a80-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="94a80-236">(11)</span><span class="sxs-lookup"><span data-stu-id="94a80-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-237">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="94a80-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="94a80-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="94a80-239">12</span><span class="sxs-lookup"><span data-stu-id="94a80-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-240">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="94a80-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="94a80-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="94a80-242">(13)</span><span class="sxs-lookup"><span data-stu-id="94a80-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-243">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="94a80-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="94a80-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="94a80-245">(14)</span><span class="sxs-lookup"><span data-stu-id="94a80-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-246">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="94a80-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="94a80-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="94a80-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="94a80-248">(15)</span><span class="sxs-lookup"><span data-stu-id="94a80-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-249">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="94a80-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="94a80-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="94a80-251">(16)</span><span class="sxs-lookup"><span data-stu-id="94a80-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-252">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="94a80-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="94a80-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="94a80-254">(17)</span><span class="sxs-lookup"><span data-stu-id="94a80-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-255">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="94a80-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="94a80-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="94a80-257">(18)</span><span class="sxs-lookup"><span data-stu-id="94a80-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-258">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="94a80-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="94a80-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="94a80-260">(19)</span><span class="sxs-lookup"><span data-stu-id="94a80-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="94a80-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="94a80-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="94a80-262">(20)</span><span class="sxs-lookup"><span data-stu-id="94a80-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-263">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="94a80-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="94a80-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="94a80-265">(21)</span><span class="sxs-lookup"><span data-stu-id="94a80-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-266">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="94a80-266">System failure.</span></span> <span data-ttu-id="94a80-267">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="94a80-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="94a80-268">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="94a80-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="94a80-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="94a80-270">(22)</span><span class="sxs-lookup"><span data-stu-id="94a80-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-271">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="94a80-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="94a80-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="94a80-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="94a80-273">(23)</span><span class="sxs-lookup"><span data-stu-id="94a80-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-274">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="94a80-274">System failure.</span></span> <span data-ttu-id="94a80-275">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="94a80-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="94a80-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="94a80-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="94a80-277">(24)</span><span class="sxs-lookup"><span data-stu-id="94a80-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-278">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="94a80-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="94a80-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="94a80-280">(25)</span><span class="sxs-lookup"><span data-stu-id="94a80-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-281">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="94a80-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="94a80-283">(26)</span><span class="sxs-lookup"><span data-stu-id="94a80-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-284">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="94a80-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="94a80-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="94a80-286">(27)</span><span class="sxs-lookup"><span data-stu-id="94a80-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-287">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="94a80-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="94a80-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="94a80-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="94a80-289">(28)</span><span class="sxs-lookup"><span data-stu-id="94a80-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-290">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="94a80-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="94a80-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="94a80-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="94a80-292">(29)</span><span class="sxs-lookup"><span data-stu-id="94a80-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-293">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="94a80-293">Device is disabled.</span></span> <span data-ttu-id="94a80-294">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="94a80-294">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="94a80-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="94a80-296">(30)</span><span class="sxs-lookup"><span data-stu-id="94a80-296">(30)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-297">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94a80-297">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="94a80-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94a80-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="94a80-299">31</span><span class="sxs-lookup"><span data-stu-id="94a80-299">(31)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-300">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="94a80-300">Device is not working properly.</span></span> <span data-ttu-id="94a80-301">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="94a80-301">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-302">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="94a80-302">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-303">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="94a80-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-305">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="94a80-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-306">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="94a80-306">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="94a80-307">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-308">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="94a80-308">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-309">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="94a80-309">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-311">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="94a80-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-312">Se **true**, l'errore più recente è correggibile.</span><span class="sxs-lookup"><span data-stu-id="94a80-312">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="94a80-313">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-313">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="94a80-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="94a80-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-317">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="94a80-317">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="94a80-318">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="94a80-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="94a80-319">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="94a80-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="94a80-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-321">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="94a80-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-324">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="94a80-324">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-325">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94a80-325">Description of the object.</span></span>

<span data-ttu-id="94a80-326">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="94a80-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-330">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="94a80-330">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="94a80-331">Identificatore univoco del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="94a80-331">Unique identifier of the logical device.</span></span>

<span data-ttu-id="94a80-332">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-333">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="94a80-333">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-334">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94a80-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-336">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| tipo 19 \| indirizzi con mapping del dispositivo di memoria che \| terminano l'indirizzo")</span><span class="sxs-lookup"><span data-stu-id="94a80-336">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-337">Indirizzo finale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="94a80-337">Ending address, referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="94a80-338">L'indirizzo finale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="94a80-338">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="94a80-339">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-339">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-340">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="94a80-340">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-341">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94a80-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-343">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| di tipo \| 32 18-operazione di errore informazioni errore memoria bit \| ")</span><span class="sxs-lookup"><span data-stu-id="94a80-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-344">Operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="94a80-344">Memory access operation that caused the last error.</span></span> <span data-ttu-id="94a80-345">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="94a80-345">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="94a80-346">Se **errorInfo** è uguale a 3 (OK), questa proprietà non ha significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-346">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="94a80-347">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="94a80-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-348">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="94a80-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="94a80-349">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="94a80-349">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="94a80-350">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="94a80-350">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="94a80-351">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="94a80-351">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-352">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="94a80-352">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-353">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94a80-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-355">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="94a80-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-356">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="94a80-356">Address of the last memory error.</span></span> <span data-ttu-id="94a80-357">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="94a80-357">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="94a80-358">Se **errorInfo** è uguale a 3 (OK), questa proprietà non ha significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-358">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="94a80-359">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-359">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-360">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="94a80-360">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-361">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="94a80-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a80-363">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="94a80-363">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="94a80-364">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-365">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="94a80-365">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-366">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="94a80-366">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="94a80-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-368">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="94a80-368">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="94a80-369">Matrice di dati acquisiti durante l'ultimo accesso errato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="94a80-369">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="94a80-370">I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="94a80-370">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="94a80-371">Se **ErrorTransferSize** è 0 (zero), questa proprietà non ha significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-371">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="94a80-372">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="94a80-372">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-373">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94a80-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-375">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="94a80-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-376">Ordinamento dei dati archiviati nella proprietà **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="94a80-376">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="94a80-377">Se **ErrorTransferSize** è 0 (zero), questa proprietà non ha significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-377">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-378">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="94a80-378">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="94a80-379">**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="94a80-379">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="94a80-380">**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="94a80-380">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="94a80-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a80-384">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="94a80-384">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="94a80-385">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="94a80-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-387">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94a80-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-389">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS \| Type 18 \| 32-bit Error Information Error Information \| Type ")</span><span class="sxs-lookup"><span data-stu-id="94a80-389">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-390">Tipo di errore che si è verificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="94a80-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="94a80-391">I valori da 12 a 14 sono inutilizzati.</span><span class="sxs-lookup"><span data-stu-id="94a80-391">The values 12 through 14 are unused.</span></span> <span data-ttu-id="94a80-392">La possibilità di correggere è indicata nella proprietà **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="94a80-392">The ability to be corrected is indicated in the property **CorrectableError**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="94a80-393">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="94a80-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-394">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="94a80-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="94a80-395">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="94a80-395">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="94a80-396">**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="94a80-396">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="94a80-397">**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="94a80-397">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="94a80-398">**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="94a80-398">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="94a80-399">**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="94a80-399">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="94a80-400">**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="94a80-400">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="94a80-401">**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="94a80-401">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="94a80-402">**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="94a80-402">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="94a80-403">**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="94a80-403">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="94a80-404">**Correzione di un errore a bit singolo** (12)</span><span class="sxs-lookup"><span data-stu-id="94a80-404">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="94a80-405">**Errore corretto** (13)</span><span class="sxs-lookup"><span data-stu-id="94a80-405">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="94a80-406">**Errore non correggibile** (14)</span><span class="sxs-lookup"><span data-stu-id="94a80-406">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-407">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="94a80-407">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-408">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-410">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 16 memoria \| fisica matrice \| errore di memoria")</span><span class="sxs-lookup"><span data-stu-id="94a80-410">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-411">Informazioni dettagliate sugli algoritmi di parità o CRC, ECC o altri meccanismi utilizzati.</span><span class="sxs-lookup"><span data-stu-id="94a80-411">Details on the parity or CRC algorithms, ECC or other mechanisms used.</span></span>

<span data-ttu-id="94a80-412">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-412">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="94a80-413">**Altro** ("altro")</span><span class="sxs-lookup"><span data-stu-id="94a80-413">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-414">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="94a80-414">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="94a80-415">**None** ("None")</span><span class="sxs-lookup"><span data-stu-id="94a80-415">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="94a80-416">**Parità** ("parità")</span><span class="sxs-lookup"><span data-stu-id="94a80-416">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="94a80-417">**Ecc a bit singolo** ("ecc a bit singolo")</span><span class="sxs-lookup"><span data-stu-id="94a80-417">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="94a80-418">**Ecc a più bit** ("ecc a più bit")</span><span class="sxs-lookup"><span data-stu-id="94a80-418">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="94a80-419">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="94a80-419">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-420">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="94a80-420">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-421">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94a80-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-423">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32-bit informazioni errore di memoria errore \| "), [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="94a80-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-424">Intervallo, in byte, in cui è possibile risolvere l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="94a80-424">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="94a80-425">Se, ad esempio, gli indirizzi di errore vengono risolti in bit 11, ovvero in base a una tipica pagina, gli errori possono essere risolti in limiti di 4 KB e questa proprietà è impostata su 4000.</span><span class="sxs-lookup"><span data-stu-id="94a80-425">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="94a80-426">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-426">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="94a80-427">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-427">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-428">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="94a80-428">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-429">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94a80-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-431">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="94a80-431">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-432">Ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="94a80-432">Time that the last memory error occurred.</span></span> <span data-ttu-id="94a80-433">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="94a80-433">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="94a80-434">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-434">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="94a80-435">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="94a80-435">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-436">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94a80-436">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-438">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**unità**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="94a80-438">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-439">Dimensioni del trasferimento dati in bit che hanno causato l'ultimo errore: 0 (zero) indica che non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="94a80-439">Size of the data transfer in bits that caused the last error—0 (zero) indicates no error.</span></span> <span data-ttu-id="94a80-440">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="94a80-440">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-441">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="94a80-441">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-442">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94a80-442">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-444">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="94a80-444">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-445">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94a80-445">Date and time the object was installed.</span></span> <span data-ttu-id="94a80-446">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="94a80-446">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="94a80-447">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-448">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="94a80-448">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-449">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94a80-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a80-451">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="94a80-451">Last error code reported by the logical device.</span></span>

<span data-ttu-id="94a80-452">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-453">**Nome**</span><span class="sxs-lookup"><span data-stu-id="94a80-453">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-454">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-456">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="94a80-456">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-457">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="94a80-457">Label by which the object is known.</span></span> <span data-ttu-id="94a80-458">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="94a80-458">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="94a80-459">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-459">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-460">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="94a80-460">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-461">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94a80-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-462">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-463">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="94a80-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-464">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="94a80-464">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="94a80-465">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="94a80-465">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="94a80-466">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="94a80-466">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="94a80-467">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-467">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="94a80-468">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-468">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-469">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="94a80-469">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-470">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-470">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-471">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-472">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="94a80-472">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-473">Stringa in formato libero che fornisce ulteriori informazioni se la proprietà **ErrorType** è impostata su 1. in caso contrario, questa stringa non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-473">Free-form string that provides more information if the **ErrorType** property is set to 1; otherwise, this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="94a80-474">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="94a80-474">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-475">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-476">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-477">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="94a80-477">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-478">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="94a80-478">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="94a80-479">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="94a80-479">Example: "\*PNP030b"</span></span>

<span data-ttu-id="94a80-480">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-481">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="94a80-481">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-482">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94a80-482">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="94a80-483">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a80-484">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="94a80-484">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="94a80-485">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="94a80-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="94a80-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="94a80-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="94a80-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="94a80-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="94a80-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="94a80-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-490">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="94a80-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="94a80-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="94a80-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-492">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="94a80-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="94a80-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="94a80-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-494">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="94a80-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="94a80-495">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="94a80-495">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="94a80-496">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-496">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="94a80-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="94a80-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-498">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="94a80-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="94a80-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="94a80-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="94a80-500">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="94a80-500">Timed Power-On Supported</span></span>

<span data-ttu-id="94a80-501">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="94a80-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="94a80-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-503">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="94a80-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-504">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a80-505">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="94a80-505">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="94a80-506">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="94a80-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="94a80-507">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-508">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="94a80-508">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-509">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-509">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-510">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a80-511">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="94a80-511">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="94a80-512">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-512">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-513">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="94a80-513">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-514">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94a80-514">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-515">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-516">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 19 \| Memory Device mapping \| Address Starting Address")</span><span class="sxs-lookup"><span data-stu-id="94a80-516">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-517">Indirizzo iniziale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="94a80-517">Beginning address that is referenced by an application or operating system, and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="94a80-518">L'indirizzo iniziale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="94a80-518">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="94a80-519">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-519">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-520">**Status**</span><span class="sxs-lookup"><span data-stu-id="94a80-520">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-521">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-522">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-523">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="94a80-523">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-524">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94a80-524">Current status of the object.</span></span> <span data-ttu-id="94a80-525">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="94a80-525">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="94a80-526">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="94a80-526">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="94a80-527">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="94a80-527">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="94a80-528">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="94a80-528">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="94a80-529">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="94a80-529">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="94a80-530">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-530">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="94a80-531">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="94a80-531">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="94a80-532">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="94a80-532">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="94a80-533">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="94a80-533">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="94a80-534">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="94a80-534">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-535">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="94a80-535">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="94a80-536">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="94a80-536">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="94a80-537">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="94a80-537">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="94a80-538">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="94a80-538">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="94a80-539">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="94a80-539">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="94a80-540">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="94a80-540">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="94a80-541">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="94a80-541">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="94a80-542">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="94a80-542">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="94a80-543">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="94a80-543">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-544">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="94a80-544">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-545">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94a80-545">Data type: **uint16e**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-546">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-547">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="94a80-547">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-548">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="94a80-548">State of the logical device.</span></span> <span data-ttu-id="94a80-549">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="94a80-549">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="94a80-550">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="94a80-551">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="94a80-551">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94a80-552">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="94a80-552">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="94a80-553">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="94a80-553">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="94a80-554">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="94a80-554">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="94a80-555">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="94a80-555">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94a80-556">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="94a80-556">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-557">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-558">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-559">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="94a80-559">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="94a80-560">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="94a80-560">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="94a80-561">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-561">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a80-562">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="94a80-562">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-563">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="94a80-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-564">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-565">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="94a80-565">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="94a80-566">Se **true**, le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="94a80-566">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="94a80-567">Se **false**, si tratta di un indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="94a80-567">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="94a80-568">Se la proprietà **errorInfo** è uguale a 3 (OK), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="94a80-568">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="94a80-569">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="94a80-569">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a80-570">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a80-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a80-571">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a80-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a80-572">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="94a80-572">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="94a80-573">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="94a80-573">Name of the scoping system.</span></span>

<span data-ttu-id="94a80-574">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-574">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94a80-575">Commenti</span><span class="sxs-lookup"><span data-stu-id="94a80-575">Remarks</span></span>

<span data-ttu-id="94a80-576">La classe **Win32 \_ SMBIOSMemory** è derivata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94a80-576">The **Win32\_SMBIOSMemory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94a80-577">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94a80-577">Requirements</span></span>



| <span data-ttu-id="94a80-578">Requisito</span><span class="sxs-lookup"><span data-stu-id="94a80-578">Requirement</span></span> | <span data-ttu-id="94a80-579">Valore</span><span class="sxs-lookup"><span data-stu-id="94a80-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94a80-580">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94a80-580">Minimum supported client</span></span><br/> | <span data-ttu-id="94a80-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94a80-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94a80-582">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94a80-582">Minimum supported server</span></span><br/> | <span data-ttu-id="94a80-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94a80-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94a80-584">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94a80-584">Namespace</span></span><br/>                | <span data-ttu-id="94a80-585">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="94a80-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94a80-586">MOF</span><span class="sxs-lookup"><span data-stu-id="94a80-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94a80-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94a80-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94a80-588">DLL</span><span class="sxs-lookup"><span data-stu-id="94a80-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94a80-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94a80-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94a80-590">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94a80-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a80-591">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="94a80-591">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="94a80-592">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="94a80-592">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
