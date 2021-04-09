---
description: La \_ classe WMI MemoryDevice Win32 rappresenta le proprietà di un dispositivo di memoria di sistema del computer e degli indirizzi mappati associati.
ms.assetid: d609dca5-2f5f-4f23-8fcc-bcc197d6c24b
ms.tgt_platform: multiple
title: Classe Win32_MemoryDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDevice
- Win32_MemoryDevice.Reset
- Win32_MemoryDevice.SetPowerState
- Win32_MemoryDevice.Access
- Win32_MemoryDevice.AdditionalErrorData
- Win32_MemoryDevice.Availability
- Win32_MemoryDevice.BlockSize
- Win32_MemoryDevice.Caption
- Win32_MemoryDevice.ConfigManagerErrorCode
- Win32_MemoryDevice.ConfigManagerUserConfig
- Win32_MemoryDevice.CorrectableError
- Win32_MemoryDevice.CreationClassName
- Win32_MemoryDevice.Description
- Win32_MemoryDevice.DeviceID
- Win32_MemoryDevice.EndingAddress
- Win32_MemoryDevice.ErrorAccess
- Win32_MemoryDevice.ErrorAddress
- Win32_MemoryDevice.ErrorCleared
- Win32_MemoryDevice.ErrorData
- Win32_MemoryDevice.ErrorDataOrder
- Win32_MemoryDevice.ErrorDescription
- Win32_MemoryDevice.ErrorGranularity
- Win32_MemoryDevice.ErrorInfo
- Win32_MemoryDevice.ErrorMethodology
- Win32_MemoryDevice.ErrorResolution
- Win32_MemoryDevice.ErrorTime
- Win32_MemoryDevice.ErrorTransferSize
- Win32_MemoryDevice.InstallDate
- Win32_MemoryDevice.LastErrorCode
- Win32_MemoryDevice.Name
- Win32_MemoryDevice.NumberOfBlocks
- Win32_MemoryDevice.OtherErrorDescription
- Win32_MemoryDevice.PNPDeviceID
- Win32_MemoryDevice.PowerManagementCapabilities
- Win32_MemoryDevice.PowerManagementSupported
- Win32_MemoryDevice.Purpose
- Win32_MemoryDevice.StartingAddress
- Win32_MemoryDevice.Status
- Win32_MemoryDevice.StatusInfo
- Win32_MemoryDevice.SystemCreationClassName
- Win32_MemoryDevice.SystemLevelAddress
- Win32_MemoryDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 277b868f1b92b9f7c6a0c520c77ab76fac6b544d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965984"
---
# <a name="win32_memorydevice-class"></a><span data-ttu-id="af983-103">Win32 \_ MemoryDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="af983-103">Win32\_MemoryDevice class</span></span>

<span data-ttu-id="af983-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryDevice Win32** rappresenta le proprietà di un dispositivo di memoria di sistema del computer e degli indirizzi mappati associati.</span><span class="sxs-lookup"><span data-stu-id="af983-104">The **Win32\_MemoryDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a computer system memory device and its associated mapped addresses.</span></span>

<span data-ttu-id="af983-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="af983-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="af983-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="af983-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af983-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af983-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDevice : Win32_SMBIOSMemory
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

## <a name="members"></a><span data-ttu-id="af983-108">Members</span><span class="sxs-lookup"><span data-stu-id="af983-108">Members</span></span>

<span data-ttu-id="af983-109">La classe **Win32 \_ MemoryDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af983-109">The **Win32\_MemoryDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="af983-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="af983-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="af983-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af983-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="af983-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="af983-112">Methods</span></span>

<span data-ttu-id="af983-113">La classe **Win32 \_ MemoryDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="af983-113">The **Win32\_MemoryDevice** class has these methods.</span></span>



| <span data-ttu-id="af983-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="af983-114">Method</span></span>            | <span data-ttu-id="af983-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af983-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af983-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="af983-116">**Reset**</span></span>         | <span data-ttu-id="af983-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="af983-117">Not implemented.</span></span> <span data-ttu-id="af983-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/>                 |
| <span data-ttu-id="af983-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="af983-119">**SetPowerState**</span></span> | <span data-ttu-id="af983-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="af983-120">Not implemented.</span></span> <span data-ttu-id="af983-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="af983-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af983-122">Properties</span></span>

<span data-ttu-id="af983-123">La classe **Win32 \_ MemoryDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af983-123">The **Win32\_MemoryDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af983-124">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="af983-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af983-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af983-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af983-127">Accesso ai supporti disponibile.</span><span class="sxs-lookup"><span data-stu-id="af983-127">Media access available.</span></span>

<span data-ttu-id="af983-128">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af983-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af983-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="af983-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="af983-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="af983-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="af983-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="af983-132">Scrivibile</span><span class="sxs-lookup"><span data-stu-id="af983-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="af983-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="af983-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="af983-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="af983-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="af983-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-136">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="af983-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="af983-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 18 \| 32-bit memory Error Information Error \| Syndrome"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="af983-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="af983-139">Matrice di informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="af983-139">Array of additional error information.</span></span> <span data-ttu-id="af983-140">Un esempio è la sindrome di controllo degli errori e correzione (ECC) o la restituzione dei bit di controllo se viene usata una metodologia di errore basata su un controllo di ridondanza ciclico (CRC).</span><span class="sxs-lookup"><span data-stu-id="af983-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based error methodology is used.</span></span> <span data-ttu-id="af983-141">Nel secondo caso, se viene riconosciuto un errore a bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="af983-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="af983-142">In questo campo sono inclusi questo tipo di dati (sindrome ECC, bit check, dati di bit di parità o altre informazioni fornite dal fornitore).</span><span class="sxs-lookup"><span data-stu-id="af983-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="af983-143">Questa proprietà viene utilizzata solo quando la proprietà **errorInfo** è diversa da 3.</span><span class="sxs-lookup"><span data-stu-id="af983-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="af983-144">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-145">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="af983-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-146">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af983-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af983-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="af983-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="af983-149">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-149">Availability and status of the device.</span></span>

<span data-ttu-id="af983-150">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af983-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af983-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="af983-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="af983-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="af983-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af983-154">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="af983-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="af983-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="af983-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="af983-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="af983-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="af983-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="af983-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="af983-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="af983-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="af983-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="af983-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="af983-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="af983-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="af983-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="af983-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="af983-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="af983-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="af983-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="af983-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="af983-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="af983-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="af983-165">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="af983-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="af983-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="af983-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="af983-167">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="af983-167">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="af983-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="af983-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="af983-169">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="af983-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="af983-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="af983-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="af983-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="af983-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="af983-172">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="af983-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="af983-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="af983-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="af983-174">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="af983-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="af983-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="af983-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="af983-176">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="af983-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="af983-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="af983-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="af983-178">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="af983-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="af983-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="af983-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="af983-180">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="af983-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="af983-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-182">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af983-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af983-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-184">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="af983-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="af983-185">Dimensioni in byte dei blocchi che formano questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="af983-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="af983-186">Se è sconosciuto o se un concetto di blocco non è valido (ad esempio per extent di aggregazione, memoria o dischi logici), immettere 1.</span><span class="sxs-lookup"><span data-stu-id="af983-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="af983-187">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af983-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="af983-188">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af983-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af983-189">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="af983-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-192">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="af983-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="af983-193">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="af983-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="af983-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af983-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="af983-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-196">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af983-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af983-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-198">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af983-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af983-199">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="af983-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="af983-200">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="af983-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="af983-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="af983-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="af983-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="af983-203">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="af983-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="af983-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="af983-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="af983-205">(1)</span><span class="sxs-lookup"><span data-stu-id="af983-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="af983-206">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="af983-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af983-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="af983-208">(2)</span><span class="sxs-lookup"><span data-stu-id="af983-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="af983-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="af983-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="af983-210">(3)</span><span class="sxs-lookup"><span data-stu-id="af983-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="af983-211">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="af983-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="af983-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="af983-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="af983-213">(4)</span><span class="sxs-lookup"><span data-stu-id="af983-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="af983-214">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="af983-214">Device is not working properly.</span></span> <span data-ttu-id="af983-215">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="af983-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="af983-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="af983-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="af983-217">(5)</span><span class="sxs-lookup"><span data-stu-id="af983-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="af983-218">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="af983-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="af983-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="af983-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="af983-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="af983-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="af983-221">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="af983-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="af983-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="af983-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="af983-223">(7)</span><span class="sxs-lookup"><span data-stu-id="af983-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="af983-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="af983-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="af983-225">(8)</span><span class="sxs-lookup"><span data-stu-id="af983-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="af983-226">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="af983-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="af983-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="af983-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="af983-228">(9)</span><span class="sxs-lookup"><span data-stu-id="af983-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="af983-229">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="af983-229">Device is not working properly.</span></span> <span data-ttu-id="af983-230">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="af983-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="af983-232">(10)</span><span class="sxs-lookup"><span data-stu-id="af983-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="af983-233">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="af983-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="af983-235">(11)</span><span class="sxs-lookup"><span data-stu-id="af983-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="af983-236">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="af983-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="af983-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="af983-238">12</span><span class="sxs-lookup"><span data-stu-id="af983-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="af983-239">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="af983-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="af983-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="af983-241">(13)</span><span class="sxs-lookup"><span data-stu-id="af983-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="af983-242">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="af983-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="af983-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="af983-244">(14)</span><span class="sxs-lookup"><span data-stu-id="af983-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="af983-245">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="af983-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="af983-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="af983-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="af983-247">(15)</span><span class="sxs-lookup"><span data-stu-id="af983-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="af983-248">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="af983-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="af983-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="af983-250">(16)</span><span class="sxs-lookup"><span data-stu-id="af983-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="af983-251">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="af983-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="af983-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="af983-253">(17)</span><span class="sxs-lookup"><span data-stu-id="af983-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="af983-254">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="af983-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af983-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="af983-256">(18)</span><span class="sxs-lookup"><span data-stu-id="af983-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="af983-257">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="af983-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="af983-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="af983-259">(19)</span><span class="sxs-lookup"><span data-stu-id="af983-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="af983-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="af983-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="af983-261">(20)</span><span class="sxs-lookup"><span data-stu-id="af983-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="af983-262">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="af983-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="af983-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="af983-264">(21)</span><span class="sxs-lookup"><span data-stu-id="af983-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="af983-265">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="af983-265">System failure.</span></span> <span data-ttu-id="af983-266">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="af983-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="af983-267">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="af983-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="af983-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="af983-269">(22)</span><span class="sxs-lookup"><span data-stu-id="af983-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="af983-270">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="af983-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="af983-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="af983-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="af983-272">(23)</span><span class="sxs-lookup"><span data-stu-id="af983-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="af983-273">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="af983-273">System failure.</span></span> <span data-ttu-id="af983-274">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="af983-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="af983-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="af983-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="af983-276">(24)</span><span class="sxs-lookup"><span data-stu-id="af983-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="af983-277">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="af983-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="af983-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="af983-279">(25)</span><span class="sxs-lookup"><span data-stu-id="af983-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="af983-280">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="af983-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="af983-282">(26)</span><span class="sxs-lookup"><span data-stu-id="af983-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="af983-283">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="af983-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="af983-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="af983-285">(27)</span><span class="sxs-lookup"><span data-stu-id="af983-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="af983-286">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="af983-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="af983-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="af983-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="af983-288">(28)</span><span class="sxs-lookup"><span data-stu-id="af983-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="af983-289">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="af983-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="af983-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="af983-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="af983-291">(29)</span><span class="sxs-lookup"><span data-stu-id="af983-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="af983-292">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="af983-292">Device is disabled.</span></span> <span data-ttu-id="af983-293">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="af983-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="af983-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="af983-295">(30)</span><span class="sxs-lookup"><span data-stu-id="af983-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="af983-296">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af983-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af983-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af983-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="af983-298">31</span><span class="sxs-lookup"><span data-stu-id="af983-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="af983-299">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="af983-299">Device is not working properly.</span></span> <span data-ttu-id="af983-300">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="af983-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="af983-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-302">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af983-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af983-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-304">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af983-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af983-305">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="af983-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="af983-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="af983-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-308">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af983-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af983-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-310">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="af983-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="af983-311">Se **true**, l'errore più recente è correggibile.</span><span class="sxs-lookup"><span data-stu-id="af983-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="af983-312">Questa proprietà non viene utilizzata se **errorInfo** è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="af983-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="af983-313">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="af983-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-317">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af983-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af983-318">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="af983-318">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="af983-319">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="af983-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="af983-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-321">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="af983-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-324">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="af983-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="af983-325">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af983-325">Description of the object.</span></span>

<span data-ttu-id="af983-326">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af983-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="af983-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-330">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="af983-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="af983-331">Identificatore univoco del dispositivo di memoria.</span><span class="sxs-lookup"><span data-stu-id="af983-331">Unique identifier of the memory device.</span></span>

<span data-ttu-id="af983-332">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="af983-333">Esempio: "dispositivo di memoria 1"</span><span class="sxs-lookup"><span data-stu-id="af983-333">Example: "Memory Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="af983-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="af983-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-335">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af983-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af983-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| tipo 19 \| indirizzi con mapping del dispositivo di memoria che \| terminano l'indirizzo")</span><span class="sxs-lookup"><span data-stu-id="af983-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="af983-338">Indirizzo finale a cui fa riferimento un'applicazione o un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="af983-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="af983-339">Questo indirizzo di memoria è mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="af983-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="af983-340">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-340">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="af983-341">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af983-341">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af983-342">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="af983-342">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-343">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af983-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af983-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-345">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| di tipo \| 32 18-operazione di errore informazioni errore memoria bit \| ")</span><span class="sxs-lookup"><span data-stu-id="af983-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="af983-346">Tipo di operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="af983-346">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="af983-347">Questa proprietà è valida solo se **errorInfo** non è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="af983-347">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="af983-348">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-348">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af983-349">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af983-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-350">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="af983-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="af983-351">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="af983-351">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="af983-352">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="af983-352">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="af983-353">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="af983-353">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-354">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="af983-354">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-355">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af983-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af983-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-357">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="af983-357">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="af983-358">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="af983-358">Address of the last memory error.</span></span> <span data-ttu-id="af983-359">Questa proprietà viene utilizzata solo se **errorInfo** non è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="af983-359">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="af983-360">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-360">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="af983-361">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af983-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af983-362">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="af983-362">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-363">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af983-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af983-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af983-365">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="af983-365">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="af983-366">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-367">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="af983-367">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-368">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="af983-368">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="af983-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-370">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="af983-370">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="af983-371">Matrice di dati acquisiti dall'ultimo accesso alla memoria con un errore.</span><span class="sxs-lookup"><span data-stu-id="af983-371">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="af983-372">I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="af983-372">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="af983-373">Se **ErrorTransferSize** è 0 (zero), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="af983-373">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="af983-374">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-374">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-375">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="af983-375">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-376">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af983-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af983-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-378">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="af983-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="af983-379">Ordinamento dei dati archiviati nella proprietà **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="af983-379">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="af983-380">Questa proprietà viene utilizzata solo quando **ErrorTransferSize** è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="af983-380">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="af983-381">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-381">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-382">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af983-382">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="af983-383">**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="af983-383">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="af983-384">**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="af983-384">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-385">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="af983-385">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-386">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af983-388">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="af983-388">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="af983-389">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-390">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="af983-390">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-391">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af983-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af983-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-393">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| errore granularità")</span><span class="sxs-lookup"><span data-stu-id="af983-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="af983-394">Livello in cui è possibile risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="af983-394">Level where the error can be resolved.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af983-395">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af983-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-396">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="af983-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_level"></span><span id="device_level"></span><span id="DEVICE_LEVEL"></span>

<span data-ttu-id="af983-397">**Livello dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="af983-397">**Device level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_partition_level"></span><span id="memory_partition_level"></span><span id="MEMORY_PARTITION_LEVEL"></span>

<span data-ttu-id="af983-398">**Livello partizione di memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="af983-398">**Memory partition level** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-399">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="af983-399">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-400">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af983-400">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af983-401">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-402">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| Type 18 \| 32-bit Error Information Error Information \| Type ")</span><span class="sxs-lookup"><span data-stu-id="af983-402">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="af983-403">Tipo di errore che si è verificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="af983-403">Type of error that occurred most recently.</span></span> <span data-ttu-id="af983-404">I valori 12-14, che indicano se un errore è correggibile, non vengono utilizzati con questa proprietà, ma queste informazioni si trovano nella proprietà **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="af983-404">The values 12-14, indicating whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="af983-405">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-405">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af983-406">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af983-406">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-407">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="af983-407">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="af983-408">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="af983-408">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="af983-409">**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="af983-409">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="af983-410">**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="af983-410">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="af983-411">**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="af983-411">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="af983-412">**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="af983-412">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="af983-413">**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="af983-413">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="af983-414">**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="af983-414">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="af983-415">**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="af983-415">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="af983-416">**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="af983-416">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="af983-417">**Correzione di un errore a bit singolo** (12)</span><span class="sxs-lookup"><span data-stu-id="af983-417">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="af983-418">**Errore corretto** (13)</span><span class="sxs-lookup"><span data-stu-id="af983-418">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="af983-419">**Errore non correggibile** (14)</span><span class="sxs-lookup"><span data-stu-id="af983-419">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-420">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="af983-420">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-423">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 16 memoria \| fisica matrice \| errore di memoria")</span><span class="sxs-lookup"><span data-stu-id="af983-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="af983-424">Tipi di controllo degli errori utilizzati dall'hardware di memoria.</span><span class="sxs-lookup"><span data-stu-id="af983-424">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="af983-425">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af983-425">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="af983-426">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="af983-426">The values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af983-427">**Altro** ("altro")</span><span class="sxs-lookup"><span data-stu-id="af983-427">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-428">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="af983-428">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="af983-429">**Parità** ("parità")</span><span class="sxs-lookup"><span data-stu-id="af983-429">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="af983-430">**Ecc a bit singolo** ("ecc a bit singolo")</span><span class="sxs-lookup"><span data-stu-id="af983-430">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="af983-431">**Ecc a più bit** ("ecc a più bit")</span><span class="sxs-lookup"><span data-stu-id="af983-431">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="af983-432">**None** ("None")</span><span class="sxs-lookup"><span data-stu-id="af983-432">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="af983-433">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="af983-433">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-434">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="af983-434">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-435">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af983-435">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af983-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-437">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit informazioni errore di memoria errore \| "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="af983-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="af983-438">Quantità di dati effettivamente determinata per causare l'errore.</span><span class="sxs-lookup"><span data-stu-id="af983-438">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="af983-439">Questa proprietà non viene utilizzata quando la proprietà **errorInfo** è impostata su 3.</span><span class="sxs-lookup"><span data-stu-id="af983-439">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="af983-440">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-440">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="af983-441">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af983-441">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af983-442">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="af983-442">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-443">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="af983-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="af983-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-445">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="af983-445">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="af983-446">Ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="af983-446">Time that the last memory error occurred.</span></span> <span data-ttu-id="af983-447">Questa proprietà è valida solo se **errorInfo** non è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="af983-447">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="af983-448">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-448">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-449">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="af983-449">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-450">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af983-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af983-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-452">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="af983-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="af983-453">Dimensione dei dati (contenente l'ultimo errore) trasferiti.</span><span class="sxs-lookup"><span data-stu-id="af983-453">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="af983-454">Questa proprietà è impostata su 0 (zero) se non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="af983-454">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="af983-455">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-455">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-456">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="af983-456">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-457">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="af983-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="af983-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-459">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="af983-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="af983-460">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af983-460">Date and time the object was installed.</span></span> <span data-ttu-id="af983-461">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="af983-461">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="af983-462">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af983-462">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-463">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="af983-463">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-464">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af983-464">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af983-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af983-466">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af983-466">Last error code reported by the logical device.</span></span>

<span data-ttu-id="af983-467">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-468">**Nome**</span><span class="sxs-lookup"><span data-stu-id="af983-468">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-471">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="af983-471">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="af983-472">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="af983-472">Label by which the object is known.</span></span> <span data-ttu-id="af983-473">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="af983-473">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="af983-474">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af983-474">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-475">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="af983-475">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-476">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af983-476">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af983-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-478">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="af983-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="af983-479">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="af983-479">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="af983-480">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="af983-480">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="af983-481">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="af983-481">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="af983-482">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af983-482">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="af983-483">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af983-483">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af983-484">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="af983-484">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-485">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-486">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-487">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="af983-487">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="af983-488">Ulteriori informazioni quando la proprietà **errorInfo** è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="af983-488">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="af983-489">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-489">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-490">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="af983-490">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-491">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-492">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-493">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af983-493">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af983-494">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af983-494">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="af983-495">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="af983-496">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="af983-496">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="af983-497">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="af983-497">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-498">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af983-498">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af983-499">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af983-500">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af983-500">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="af983-501">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="af983-501">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af983-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="af983-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="af983-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="af983-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="af983-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="af983-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="af983-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af983-506">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="af983-506">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="af983-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="af983-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="af983-508">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="af983-508">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="af983-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="af983-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="af983-510">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="af983-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="af983-511">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="af983-511">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="af983-512">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="af983-512">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="af983-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="af983-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="af983-514">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="af983-514">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="af983-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="af983-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="af983-516">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="af983-516">Timed Power-On Supported</span></span>

<span data-ttu-id="af983-517">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="af983-517">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-518">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="af983-518">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-519">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af983-519">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af983-520">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-520">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af983-521">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="af983-521">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="af983-522">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="af983-522">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="af983-523">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-524">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="af983-524">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-525">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-526">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af983-527">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="af983-527">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="af983-528">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af983-528">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-529">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="af983-529">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-530">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af983-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af983-531">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-532">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 19 \| Memory Device mapping \| Address Starting Address")</span><span class="sxs-lookup"><span data-stu-id="af983-532">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="af983-533">Indirizzo iniziale a cui fa riferimento un'applicazione o il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="af983-533">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="af983-534">Questo indirizzo di memoria è mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="af983-534">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="af983-535">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-535">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="af983-536">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af983-536">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af983-537">**Status**</span><span class="sxs-lookup"><span data-stu-id="af983-537">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-538">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-539">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-540">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="af983-540">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="af983-541">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af983-541">Current status of the object.</span></span> <span data-ttu-id="af983-542">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="af983-542">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="af983-543">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="af983-543">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="af983-544">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="af983-544">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="af983-545">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="af983-545">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="af983-546">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="af983-546">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="af983-547">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af983-547">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="af983-548">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="af983-548">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="af983-549">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="af983-549">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="af983-550">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="af983-550">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="af983-551">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="af983-551">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-552">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="af983-552">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="af983-553">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="af983-553">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="af983-554">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="af983-554">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="af983-555">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="af983-555">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="af983-556">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="af983-556">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="af983-557">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="af983-557">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="af983-558">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="af983-558">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="af983-559">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="af983-559">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="af983-560">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="af983-560">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-561">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="af983-561">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-562">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af983-562">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af983-563">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-563">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-564">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="af983-564">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="af983-565">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af983-565">State of the logical device.</span></span> <span data-ttu-id="af983-566">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="af983-566">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="af983-567">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-567">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af983-568">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af983-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af983-569">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="af983-569">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="af983-570">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="af983-570">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="af983-571">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="af983-571">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="af983-572">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="af983-572">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af983-573">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="af983-573">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-574">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-575">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-575">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-576">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af983-576">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af983-577">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="af983-577">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="af983-578">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-578">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-579">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="af983-579">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-580">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af983-580">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af983-581">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-582">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 18 \| 32-bit errore informazioni errore di memoria \| ")</span><span class="sxs-lookup"><span data-stu-id="af983-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="af983-583">Se **true**, le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="af983-583">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="af983-584">Se **false**, si tratta di un indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="af983-584">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="af983-585">Questa proprietà viene utilizzata solo se **errorInfo** non è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="af983-585">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="af983-586">Questa proprietà viene ereditata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-586">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af983-587">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="af983-587">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af983-588">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af983-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af983-589">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af983-589">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af983-590">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af983-590">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af983-591">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="af983-591">Name of the scoping system.</span></span>

<span data-ttu-id="af983-592">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af983-592">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af983-593">Commenti</span><span class="sxs-lookup"><span data-stu-id="af983-593">Remarks</span></span>

<span data-ttu-id="af983-594">La classe **Win32 \_ MemoryDevice** è derivata da [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="af983-594">The **Win32\_MemoryDevice** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="af983-595">Esempio</span><span class="sxs-lookup"><span data-stu-id="af983-595">Examples</span></span>

<span data-ttu-id="af983-596">L'esempio [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl restituisce gli indirizzi iniziale e finale per tutti i dispositivi di memoria installati in un computer.</span><span class="sxs-lookup"><span data-stu-id="af983-596">The [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl sample returns starting and ending addresses for all memory devices installed on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="af983-597">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af983-597">Requirements</span></span>



| <span data-ttu-id="af983-598">Requisito</span><span class="sxs-lookup"><span data-stu-id="af983-598">Requirement</span></span> | <span data-ttu-id="af983-599">Valore</span><span class="sxs-lookup"><span data-stu-id="af983-599">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af983-600">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af983-600">Minimum supported client</span></span><br/> | <span data-ttu-id="af983-601">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af983-601">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af983-602">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af983-602">Minimum supported server</span></span><br/> | <span data-ttu-id="af983-603">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af983-603">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af983-604">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af983-604">Namespace</span></span><br/>                | <span data-ttu-id="af983-605">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="af983-605">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af983-606">MOF</span><span class="sxs-lookup"><span data-stu-id="af983-606">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af983-607"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af983-607"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af983-608">DLL</span><span class="sxs-lookup"><span data-stu-id="af983-608">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af983-609"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af983-609"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af983-610">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af983-610">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af983-611">**\_SMBIOSMemory Win32**</span><span class="sxs-lookup"><span data-stu-id="af983-611">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="af983-612">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="af983-612">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

