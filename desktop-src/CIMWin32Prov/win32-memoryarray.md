---
description: La \_ classe WMI MemoryArray Win32 rappresenta le proprietà della matrice di memoria di sistema del computer e degli indirizzi mappati.
ms.assetid: 56ff6960-cde3-4e34-b4df-d2993bafaa62
ms.tgt_platform: multiple
title: Classe Win32_MemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArray
- Win32_MemoryArray.Reset
- Win32_MemoryArray.SetPowerState
- Win32_MemoryArray.Access
- Win32_MemoryArray.AdditionalErrorData
- Win32_MemoryArray.Availability
- Win32_MemoryArray.BlockSize
- Win32_MemoryArray.Caption
- Win32_MemoryArray.ConfigManagerErrorCode
- Win32_MemoryArray.ConfigManagerUserConfig
- Win32_MemoryArray.CorrectableError
- Win32_MemoryArray.CreationClassName
- Win32_MemoryArray.Description
- Win32_MemoryArray.DeviceID
- Win32_MemoryArray.EndingAddress
- Win32_MemoryArray.ErrorAccess
- Win32_MemoryArray.ErrorAddress
- Win32_MemoryArray.ErrorCleared
- Win32_MemoryArray.ErrorData
- Win32_MemoryArray.ErrorDataOrder
- Win32_MemoryArray.ErrorDescription
- Win32_MemoryArray.ErrorGranularity
- Win32_MemoryArray.ErrorInfo
- Win32_MemoryArray.ErrorMethodology
- Win32_MemoryArray.ErrorResolution
- Win32_MemoryArray.ErrorTime
- Win32_MemoryArray.ErrorTransferSize
- Win32_MemoryArray.InstallDate
- Win32_MemoryArray.LastErrorCode
- Win32_MemoryArray.Name
- Win32_MemoryArray.NumberOfBlocks
- Win32_MemoryArray.OtherErrorDescription
- Win32_MemoryArray.PNPDeviceID
- Win32_MemoryArray.PowerManagementCapabilities
- Win32_MemoryArray.PowerManagementSupported
- Win32_MemoryArray.Purpose
- Win32_MemoryArray.StartingAddress
- Win32_MemoryArray.Status
- Win32_MemoryArray.StatusInfo
- Win32_MemoryArray.SystemCreationClassName
- Win32_MemoryArray.SystemLevelAddress
- Win32_MemoryArray.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c102d383502bec4808b26a87eb2f6d8445b6c2a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225768"
---
# <a name="win32_memoryarray-class"></a><span data-ttu-id="0fe8f-103">Win32 \_ MemoryArray (classe)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-103">Win32\_MemoryArray class</span></span>

<span data-ttu-id="0fe8f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryArray Win32** rappresenta le proprietà della matrice di memoria di sistema del computer e degli indirizzi mappati.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-104">The **Win32\_MemoryArray** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of the computer system memory array and mapped addresses.</span></span>

<span data-ttu-id="0fe8f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0fe8f-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe8f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fe8f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryArray : Win32_SMBIOSMemory
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
  uint16   ErrorGranularity;
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
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="0fe8f-108">Members</span><span class="sxs-lookup"><span data-stu-id="0fe8f-108">Members</span></span>

<span data-ttu-id="0fe8f-109">La classe **Win32 \_ MemoryArray** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0fe8f-109">The **Win32\_MemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="0fe8f-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0fe8f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0fe8f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0fe8f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0fe8f-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0fe8f-112">Methods</span></span>

<span data-ttu-id="0fe8f-113">La classe **Win32 \_ MemoryArray** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-113">The **Win32\_MemoryArray** class has these methods.</span></span>



| <span data-ttu-id="0fe8f-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="0fe8f-114">Method</span></span>            | <span data-ttu-id="0fe8f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fe8f-115">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe8f-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-116">**Reset**</span></span>         | <span data-ttu-id="0fe8f-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-117">Not implemented.</span></span> <span data-ttu-id="0fe8f-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="0fe8f-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-119">**SetPowerState**</span></span> | <span data-ttu-id="0fe8f-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-120">Not implemented.</span></span> <span data-ttu-id="0fe8f-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0fe8f-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0fe8f-122">Properties</span></span>

<span data-ttu-id="0fe8f-123">La classe **Win32 \_ MemoryArray** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-123">The **Win32\_MemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fe8f-124">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-127">Tipo di accesso ai supporti disponibile.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-127">Type of media access available.</span></span>

<span data-ttu-id="0fe8f-128">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="0fe8f-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="0fe8f-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-132">Scrivibile</span><span class="sxs-lookup"><span data-stu-id="0fe8f-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="0fe8f-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="0fe8f-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-136">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 18 \| 32-bit memory Error Information Error \| Syndrome"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-139">Matrice di informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-139">Array of additional error information.</span></span> <span data-ttu-id="0fe8f-140">Un esempio è la sindrome di controllo degli errori e correzione (ECC) o la restituzione dei bit di controllo se viene usato un valore **ErrorMethodology** basato sul controllo di ridondanza ciclico (CRC).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based **ErrorMethodology** value is used.</span></span> <span data-ttu-id="0fe8f-141">Nel secondo caso, se viene riconosciuto un errore a bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="0fe8f-142">In questo campo sono inclusi questo tipo di dati (sindrome ECC, bit check, dati di bit di parità o altre informazioni fornite dal fornitore).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="0fe8f-143">Questa proprietà viene utilizzata solo quando la proprietà **errorInfo** è diversa da 3.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="0fe8f-144">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-145">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-146">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-149">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-149">Availability and status of the device.</span></span>

<span data-ttu-id="0fe8f-150">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0fe8f-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0fe8f-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-154">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="0fe8f-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0fe8f-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0fe8f-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0fe8f-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0fe8f-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="0fe8f-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0fe8f-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="0fe8f-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0fe8f-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0fe8f-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0fe8f-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0fe8f-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0fe8f-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-165">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0fe8f-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-167">Il dispositivo è in uno stato di risparmio energia, ma è ancora funzionante e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-167">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0fe8f-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-169">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0fe8f-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0fe8f-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-172">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0fe8f-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-174">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0fe8f-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-176">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0fe8f-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-178">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0fe8f-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-180">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-182">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-184">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-185">Dimensioni in byte dei blocchi che formano questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="0fe8f-186">Se è sconosciuto o se un concetto di blocco non è valido (ad esempio per extent di aggregazione, memoria o dischi logici), immettere 1.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="0fe8f-187">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0fe8f-188">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-189">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-192">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-193">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="0fe8f-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-196">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-198">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-199">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="0fe8f-200">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0fe8f-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0fe8f-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-203">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0fe8f-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0fe8f-205">(1)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-206">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0fe8f-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0fe8f-208">(2)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0fe8f-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0fe8f-210">(3)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-211">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0fe8f-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0fe8f-213">(4)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-214">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-214">Device is not working properly.</span></span> <span data-ttu-id="0fe8f-215">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0fe8f-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0fe8f-217">(5)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-218">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0fe8f-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0fe8f-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-221">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0fe8f-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0fe8f-223">(7)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0fe8f-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0fe8f-225">(8)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-226">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0fe8f-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0fe8f-228">(9)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-229">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-229">Device is not working properly.</span></span> <span data-ttu-id="0fe8f-230">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0fe8f-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0fe8f-232">(10)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-233">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0fe8f-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0fe8f-235">(11)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-236">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0fe8f-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0fe8f-238">12</span><span class="sxs-lookup"><span data-stu-id="0fe8f-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-239">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0fe8f-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0fe8f-241">(13)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-242">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0fe8f-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0fe8f-244">(14)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-245">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0fe8f-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0fe8f-247">(15)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-248">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0fe8f-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0fe8f-250">(16)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-251">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0fe8f-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0fe8f-253">(17)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-254">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0fe8f-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0fe8f-256">(18)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-257">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0fe8f-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0fe8f-259">(19)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0fe8f-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0fe8f-261">(20)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-262">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0fe8f-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0fe8f-264">(21)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-265">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-265">System failure.</span></span> <span data-ttu-id="0fe8f-266">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0fe8f-267">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0fe8f-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0fe8f-269">(22)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-270">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0fe8f-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0fe8f-272">(23)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-273">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-273">System failure.</span></span> <span data-ttu-id="0fe8f-274">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0fe8f-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0fe8f-276">(24)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-277">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0fe8f-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0fe8f-279">(25)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-280">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0fe8f-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0fe8f-282">(26)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-283">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0fe8f-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0fe8f-285">(27)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-286">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0fe8f-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0fe8f-288">(28)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-289">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0fe8f-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0fe8f-291">(29)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-292">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-292">Device is disabled.</span></span> <span data-ttu-id="0fe8f-293">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0fe8f-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0fe8f-295">(30)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-296">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0fe8f-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0fe8f-298">31</span><span class="sxs-lookup"><span data-stu-id="0fe8f-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-299">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-299">Device is not working properly.</span></span> <span data-ttu-id="0fe8f-300">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-302">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-304">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-305">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0fe8f-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-308">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-310">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-311">Se **true**, l'errore più recente è correggibile.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="0fe8f-312">Questa proprietà non viene utilizzata se **errorInfo** è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="0fe8f-313">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-317">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-318">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0fe8f-319">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="0fe8f-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-321">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-324">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-325">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-325">Description of the object.</span></span>

<span data-ttu-id="0fe8f-326">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-330">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-331">Identificatore univoco della matrice di memoria.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-331">Unique identifier of the memory array.</span></span>

<span data-ttu-id="0fe8f-332">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0fe8f-333">Esempio: "Memory Array 1"</span><span class="sxs-lookup"><span data-stu-id="0fe8f-333">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-335">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| tipo 19 \| indirizzi con mapping del dispositivo di memoria che \| terminano l'indirizzo")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-338">Indirizzo finale a cui fa riferimento un'applicazione o un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="0fe8f-339">Questo indirizzo di memoria è mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="0fe8f-340">Questo valore deriva dalla struttura dell' **indirizzo mappato della matrice di memoria** nelle informazioni sulla versione di SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-340">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="0fe8f-341">Per SMBIOS versioni da 2,1 a 2,6, il valore deriva dal membro dell' **indirizzo finale** .</span><span class="sxs-lookup"><span data-stu-id="0fe8f-341">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Ending Address** member.</span></span> <span data-ttu-id="0fe8f-342">Per SMBIOS versione 2.7 + il valore deriva dal membro dell' **indirizzo finale esteso** .</span><span class="sxs-lookup"><span data-stu-id="0fe8f-342">For SMBIOS version 2.7+ the value comes from the **Extended Ending Address** member.</span></span>

<span data-ttu-id="0fe8f-343">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-343">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="0fe8f-344">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-345">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-345">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-346">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-348">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| di tipo \| 32 18-operazione di errore informazioni errore memoria bit \| ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-348">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-349">Tipo di operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-349">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="0fe8f-350">Questa proprietà è valida solo se **errorInfo** non è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-350">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="0fe8f-351">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-351">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0fe8f-352">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-352">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-353">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-353">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="0fe8f-354">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-354">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="0fe8f-355">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-355">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="0fe8f-356">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-356">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-357">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-357">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-358">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-360">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-361">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-361">Address of the last memory error.</span></span> <span data-ttu-id="0fe8f-362">Questa proprietà viene utilizzata solo se **errorInfo** non è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-362">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="0fe8f-363">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-363">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="0fe8f-364">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-366">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-368">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-368">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="0fe8f-369">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-370">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-371">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-373">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-374">Matrice di dati acquisiti dall'ultimo accesso alla memoria con un errore.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-374">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="0fe8f-375">I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="0fe8f-375">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="0fe8f-376">Se **ErrorTransferSize** è 0 (zero), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-376">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="0fe8f-377">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-377">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-379">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-381">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-382">Ordinamento dei dati archiviati nella proprietà **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="0fe8f-382">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="0fe8f-383">Questa proprietà viene utilizzata solo quando **ErrorTransferSize** è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-383">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="0fe8f-384">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-384">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-385">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-385">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="0fe8f-386">**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-386">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="0fe8f-387">**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-387">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-388">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-388">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-389">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-391">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-391">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="0fe8f-392">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-393">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-393">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-394">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-396">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| errore granularità")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-397">Livello in cui è possibile risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-397">Level where the error can be resolved.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="0fe8f-398">**1** (altro)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-398">**1** (Other)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="0fe8f-399">**2** (sconosciuto)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-399">**2** (Unknown)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="0fe8f-400">**3** (a livello di dispositivo)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-400">**3** (Device level)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="0fe8f-401">**4** (livello partizione di memoria)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-401">**4** (Memory partition level)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-402">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-402">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-403">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-405">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| Type 18 \| 32-bit Error Information Error Information \| Type ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-405">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-406">Tipo di errore che si è verificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-406">Type of error that occurred most recently.</span></span> <span data-ttu-id="0fe8f-407">I valori 12-14, che indicano se un errore è correggibile, non vengono utilizzati con questa proprietà, ma queste informazioni si trovano nella proprietà **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="0fe8f-407">The values 12-14, which indicate whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="0fe8f-408">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-408">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0fe8f-409">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-410">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0fe8f-411">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-411">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="0fe8f-412">**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-412">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="0fe8f-413">**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-413">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="0fe8f-414">**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-414">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="0fe8f-415">**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-415">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="0fe8f-416">**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-416">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="0fe8f-417">**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-417">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="0fe8f-418">**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-418">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="0fe8f-419">**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-419">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="0fe8f-420">**Correzione di un errore a bit singolo** (12)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-420">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="0fe8f-421">**Errore corretto** (13)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-421">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="0fe8f-422">**Errore non correggibile** (14)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-422">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-423">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-423">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-426">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 16 memoria \| fisica matrice \| errore di memoria")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-427">Tipi di controllo degli errori utilizzati dall'hardware di memoria.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-427">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="0fe8f-428">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="0fe8f-429">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="0fe8f-429">The values are:</span></span>

<dl> <dd><span data-ttu-id="0fe8f-430">Altri</span><span class="sxs-lookup"><span data-stu-id="0fe8f-430">"Other"</span></span></dd> <dd><span data-ttu-id="0fe8f-431">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="0fe8f-431">"Unknown"</span></span></dd> <dd><span data-ttu-id="0fe8f-432">"None"</span><span class="sxs-lookup"><span data-stu-id="0fe8f-432">"None"</span></span></dd> <dd><span data-ttu-id="0fe8f-433">Parità</span><span class="sxs-lookup"><span data-stu-id="0fe8f-433">"Parity"</span></span></dd> <dd><span data-ttu-id="0fe8f-434">"ECC a bit singolo"</span><span class="sxs-lookup"><span data-stu-id="0fe8f-434">"Single-bit ECC"</span></span></dd> <dd><span data-ttu-id="0fe8f-435">"ECC a più bit"</span><span class="sxs-lookup"><span data-stu-id="0fe8f-435">"Multi-bit ECC"</span></span></dd> <dd><span data-ttu-id="0fe8f-436">CRC</span><span class="sxs-lookup"><span data-stu-id="0fe8f-436">"CRC"</span></span></dd> </dl>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0fe8f-437">**Altro** ("altro")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-437">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-438">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-438">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="0fe8f-439">**None** ("None")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-439">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="0fe8f-440">**Parità** ("parità")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-440">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="0fe8f-441">**Ecc a bit singolo** ("ecc a bit singolo")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-441">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="0fe8f-442">**Ecc a più bit** ("ecc a più bit")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-442">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="0fe8f-443">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-443">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-444">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-444">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-445">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-447">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit informazioni errore di memoria errore \| "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-447">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-448">Quantità di dati effettivamente determinata per causare l'errore.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-448">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="0fe8f-449">Questa proprietà non viene utilizzata quando la proprietà **errorInfo** è impostata su 3.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-449">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="0fe8f-450">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-450">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="0fe8f-451">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-451">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-452">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-452">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-453">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-454">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-455">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-455">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-456">Ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-456">Time that the last memory error occurred.</span></span> <span data-ttu-id="0fe8f-457">Questa proprietà è valida solo se **errorInfo** non è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-457">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="0fe8f-458">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-458">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-459">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-459">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-460">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-460">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-461">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-462">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-463">Dimensione dei dati (contenente l'ultimo errore) trasferiti.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-463">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="0fe8f-464">Questa proprietà è impostata su 0 (zero) se non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-464">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="0fe8f-465">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-465">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-466">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-466">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-467">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-467">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-469">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-470">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-470">Date and time the object was installed.</span></span> <span data-ttu-id="0fe8f-471">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-471">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0fe8f-472">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-472">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-473">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-473">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-474">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-474">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-476">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-476">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0fe8f-477">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-478">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-478">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-479">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-480">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-481">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-481">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-482">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-482">Label by which the object is known.</span></span> <span data-ttu-id="0fe8f-483">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-483">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0fe8f-484">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-484">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-485">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-485">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-486">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-488">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-489">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-489">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="0fe8f-490">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-490">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="0fe8f-491">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-491">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="0fe8f-492">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-492">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0fe8f-493">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-493">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-494">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-494">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-495">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-496">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-497">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-498">Ulteriori informazioni quando la proprietà **errorInfo** è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-498">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="0fe8f-499">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-499">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-501">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-502">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-503">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-504">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-504">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0fe8f-505">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0fe8f-506">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0fe8f-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-508">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-509">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-510">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0fe8f-511">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0fe8f-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0fe8f-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0fe8f-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-516">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0fe8f-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-518">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0fe8f-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-520">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0fe8f-521">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0fe8f-522">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0fe8f-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-524">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0fe8f-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0fe8f-526">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="0fe8f-526">Timed Power-On Supported</span></span>

<span data-ttu-id="0fe8f-527">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-527">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-528">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-528">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-529">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-530">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-531">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-531">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="0fe8f-532">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-532">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="0fe8f-533">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-533">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-534">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-534">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-535">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-536">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-537">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-537">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="0fe8f-538">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-538">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-539">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-539">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-540">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-540">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-541">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-542">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 19 \| Memory Device mapping \| Address Starting Address")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-542">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-543">Indirizzo iniziale a cui fa riferimento un'applicazione o il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-543">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="0fe8f-544">Questo indirizzo di memoria è mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-544">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="0fe8f-545">Questo valore deriva dalla struttura dell' **indirizzo mappato della matrice di memoria** nelle informazioni sulla versione di SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-545">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="0fe8f-546">Per SMBIOS versioni da 2,1 a 2,6, il valore deriva dal membro dell' **indirizzo iniziale** .</span><span class="sxs-lookup"><span data-stu-id="0fe8f-546">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Starting Address** member.</span></span> <span data-ttu-id="0fe8f-547">Per SMBIOS versione 2.7 + il valore deriva dal membro dell' **indirizzo iniziale esteso** .</span><span class="sxs-lookup"><span data-stu-id="0fe8f-547">For SMBIOS version 2.7+ the value comes from the **Extended Starting Address** member.</span></span>

<span data-ttu-id="0fe8f-548">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-548">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="0fe8f-549">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-549">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-550">**Status**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-550">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-551">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-552">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-553">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-553">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-554">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-554">Current status of the object.</span></span> <span data-ttu-id="0fe8f-555">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-555">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0fe8f-556">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-556">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0fe8f-557">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="0fe8f-557">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0fe8f-558">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-558">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0fe8f-559">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-559">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0fe8f-560">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-560">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0fe8f-561">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0fe8f-561">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0fe8f-562">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-562">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0fe8f-563">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-563">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0fe8f-564">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="0fe8f-564">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-565">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-565">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0fe8f-566">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-566">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0fe8f-567">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-567">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0fe8f-568">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-568">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0fe8f-569">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-569">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0fe8f-570">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-570">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0fe8f-571">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-571">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0fe8f-572">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-572">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0fe8f-573">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-573">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-574">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-574">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-575">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-576">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-577">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-577">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-578">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-578">State of the logical device.</span></span> <span data-ttu-id="0fe8f-579">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-579">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0fe8f-580">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-580">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0fe8f-581">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-581">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fe8f-582">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-582">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0fe8f-583">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-583">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0fe8f-584">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-584">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0fe8f-585">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-585">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe8f-586">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-586">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-587">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-588">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-589">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-589">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-590">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-590">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="0fe8f-591">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-592">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-592">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-593">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-593">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-594">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-594">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-595">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="0fe8f-595">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-596">Se **true**, le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-596">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="0fe8f-597">Se **false**, si tratta di un indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-597">If **False**, it is a physical address.</span></span> <span data-ttu-id="0fe8f-598">Questa proprietà viene utilizzata solo se **errorInfo** non è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-598">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="0fe8f-599">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-599">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe8f-600">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-600">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe8f-601">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-602">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe8f-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe8f-603">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0fe8f-603">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0fe8f-604">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="0fe8f-604">Name of the scoping system.</span></span>

<span data-ttu-id="0fe8f-605">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-605">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fe8f-606">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fe8f-606">Remarks</span></span>

<span data-ttu-id="0fe8f-607">La classe **Win32 \_ MemoryArray** è derivata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fe8f-607">The **Win32\_MemoryArray** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe8f-608">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fe8f-608">Requirements</span></span>



| <span data-ttu-id="0fe8f-609">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fe8f-609">Requirement</span></span> | <span data-ttu-id="0fe8f-610">Valore</span><span class="sxs-lookup"><span data-stu-id="0fe8f-610">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe8f-611">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fe8f-611">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe8f-612">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fe8f-612">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fe8f-613">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fe8f-613">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe8f-614">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fe8f-614">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fe8f-615">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0fe8f-615">Namespace</span></span><br/>                | <span data-ttu-id="0fe8f-616">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0fe8f-616">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0fe8f-617">MOF</span><span class="sxs-lookup"><span data-stu-id="0fe8f-617">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fe8f-618"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fe8f-618"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fe8f-619">DLL</span><span class="sxs-lookup"><span data-stu-id="0fe8f-619">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fe8f-620"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fe8f-620"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fe8f-621">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fe8f-621">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe8f-622">**\_SMBIOSMemory Win32**</span><span class="sxs-lookup"><span data-stu-id="0fe8f-622">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="0fe8f-623">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="0fe8f-623">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

