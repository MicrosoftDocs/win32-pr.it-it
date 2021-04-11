---
description: La \_ classe CIM Memory rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.
ms.assetid: ddc72aad-5687-4bc1-b402-e27b27eca9be
ms.tgt_platform: multiple
title: Classe CIM_Memory (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Caption
- CIM_Memory.Description
- CIM_Memory.InstallDate
- CIM_Memory.Name
- CIM_Memory.Status
- CIM_Memory.Availability
- CIM_Memory.ConfigManagerErrorCode
- CIM_Memory.ConfigManagerUserConfig
- CIM_Memory.CreationClassName
- CIM_Memory.DeviceID
- CIM_Memory.PowerManagementCapabilities
- CIM_Memory.ErrorCleared
- CIM_Memory.ErrorDescription
- CIM_Memory.LastErrorCode
- CIM_Memory.PNPDeviceID
- CIM_Memory.PowerManagementSupported
- CIM_Memory.StatusInfo
- CIM_Memory.SystemCreationClassName
- CIM_Memory.SystemName
- CIM_Memory.Access
- CIM_Memory.BlockSize
- CIM_Memory.NumberOfBlocks
- CIM_Memory.Purpose
- CIM_Memory.ErrorMethodology
- CIM_Memory.AdditionalErrorData
- CIM_Memory.CorrectableError
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorAddress
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorInfo
- CIM_Memory.ErrorResolution
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorTransferSize
- CIM_Memory.OtherErrorDescription
- CIM_Memory.StartingAddress
- CIM_Memory.SystemLevelAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35fbb8467337da1ceab044a42533a6ca8628cf63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127178"
---
# <a name="cim_memory-class-cimwin32-wmi-providers"></a><span data-ttu-id="cdd97-103">Classe CIM_Memory (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cdd97-103">CIM_Memory class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cdd97-104">La classe **CIM \_ Memory** rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.</span><span class="sxs-lookup"><span data-stu-id="cdd97-104">The **CIM\_Memory** class represents the capabilities and management of memory-related logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdd97-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="cdd97-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cdd97-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cdd97-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cdd97-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cdd97-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cdd97-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cdd97-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd97-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdd97-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B64-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
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
};
```

## <a name="members"></a><span data-ttu-id="cdd97-110">Members</span><span class="sxs-lookup"><span data-stu-id="cdd97-110">Members</span></span>

<span data-ttu-id="cdd97-111">La classe **CIM \_ Memory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cdd97-111">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="cdd97-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="cdd97-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cdd97-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cdd97-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cdd97-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="cdd97-114">Methods</span></span>

<span data-ttu-id="cdd97-115">La classe **CIM \_ Memory** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cdd97-115">The **CIM\_Memory** class has these methods.</span></span>



| <span data-ttu-id="cdd97-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="cdd97-116">Method</span></span>                                                            | <span data-ttu-id="cdd97-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdd97-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdd97-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="cdd97-118">**Reset**</span></span>](reset-method-in-class-cim-memory.md)                 | <span data-ttu-id="cdd97-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cdd97-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="cdd97-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="cdd97-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="cdd97-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cdd97-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-memory.md) | <span data-ttu-id="cdd97-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="cdd97-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="cdd97-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cdd97-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cdd97-124">Properties</span></span>

<span data-ttu-id="cdd97-125">La classe di **\_ memoria CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cdd97-125">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdd97-126">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="cdd97-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdd97-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-129">Descrive le proprietà di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-129">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="cdd97-130">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdd97-131">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="cdd97-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="cdd97-132">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="cdd97-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="cdd97-133">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="cdd97-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="cdd97-134">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="cdd97-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="cdd97-135">**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="cdd97-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="cdd97-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-137">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cdd97-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,18 "," MIF. DMTF \| array di memoria fisica \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cdd97-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-140">Matrice di ottetti che contengono informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="cdd97-140">Array of octets that hold additional error information.</span></span> <span data-ttu-id="cdd97-141">Un esempio è la sindrome di controllo degli errori e correzione (ECC) oppure la restituzione dei bit di controllo se viene utilizzata una metodologia di errore basata su CRC.</span><span class="sxs-lookup"><span data-stu-id="cdd97-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="cdd97-142">Nel secondo caso, se viene riconosciuto un errore a bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="cdd97-143">In questo campo sono inclusi questo tipo di dati (la sindrome ECC, i dati di controllo o di bit di parità o altre informazioni fornite dal fornitore).</span><span class="sxs-lookup"><span data-stu-id="cdd97-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="cdd97-144">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-145">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="cdd97-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-146">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdd97-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-149">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-149">Availability and status of the device.</span></span>

<span data-ttu-id="cdd97-150">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cdd97-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="cdd97-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdd97-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="cdd97-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="cdd97-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="cdd97-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="cdd97-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="cdd97-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="cdd97-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="cdd97-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cdd97-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="cdd97-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="cdd97-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="cdd97-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="cdd97-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="cdd97-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="cdd97-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="cdd97-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cdd97-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="cdd97-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="cdd97-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="cdd97-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="cdd97-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="cdd97-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="cdd97-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="cdd97-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-164">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-164">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="cdd97-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="cdd97-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-166">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="cdd97-166">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="cdd97-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="cdd97-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-168">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="cdd97-168">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="cdd97-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="cdd97-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="cdd97-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="cdd97-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-171">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="cdd97-171">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="cdd97-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="cdd97-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-173">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="cdd97-173">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="cdd97-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="cdd97-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-175">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-175">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="cdd97-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="cdd97-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-177">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-177">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="cdd97-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="cdd97-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-179">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="cdd97-179">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-180">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="cdd97-180">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-181">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd97-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-183">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-184">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdd97-184">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="cdd97-185">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="cdd97-185">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="cdd97-186">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="cdd97-186">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="cdd97-187">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cdd97-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="cdd97-188">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-188">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-189">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="cdd97-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-192">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cdd97-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-193">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-193">A short textual description of the object.</span></span>

<span data-ttu-id="cdd97-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cdd97-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-196">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdd97-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-198">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cdd97-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-199">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cdd97-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="cdd97-200">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="cdd97-201">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-201">**This device is working properly.**</span></span> <span data-ttu-id="cdd97-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="cdd97-202">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="cdd97-203">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-203">**This device is not configured correctly.**</span></span> <span data-ttu-id="cdd97-204">(1)</span><span class="sxs-lookup"><span data-stu-id="cdd97-204">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cdd97-205">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-205">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="cdd97-206">(2)</span><span class="sxs-lookup"><span data-stu-id="cdd97-206">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="cdd97-207">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-207">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="cdd97-208">(3)</span><span class="sxs-lookup"><span data-stu-id="cdd97-208">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cdd97-209">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-209">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="cdd97-210">(4)</span><span class="sxs-lookup"><span data-stu-id="cdd97-210">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="cdd97-211">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-211">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="cdd97-212">(5)</span><span class="sxs-lookup"><span data-stu-id="cdd97-212">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="cdd97-213">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-213">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="cdd97-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="cdd97-214">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="cdd97-215">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-215">**Cannot filter.**</span></span> <span data-ttu-id="cdd97-216">(7)</span><span class="sxs-lookup"><span data-stu-id="cdd97-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="cdd97-217">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-217">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="cdd97-218">(8)</span><span class="sxs-lookup"><span data-stu-id="cdd97-218">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="cdd97-219">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-219">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="cdd97-220">(9)</span><span class="sxs-lookup"><span data-stu-id="cdd97-220">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="cdd97-221">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-221">**This device cannot start.**</span></span> <span data-ttu-id="cdd97-222">(10)</span><span class="sxs-lookup"><span data-stu-id="cdd97-222">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="cdd97-223">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-223">**This device failed.**</span></span> <span data-ttu-id="cdd97-224">(11)</span><span class="sxs-lookup"><span data-stu-id="cdd97-224">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="cdd97-225">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-225">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="cdd97-226">12</span><span class="sxs-lookup"><span data-stu-id="cdd97-226">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="cdd97-227">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-227">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="cdd97-228">(13)</span><span class="sxs-lookup"><span data-stu-id="cdd97-228">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="cdd97-229">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-229">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="cdd97-230">(14)</span><span class="sxs-lookup"><span data-stu-id="cdd97-230">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="cdd97-231">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-231">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="cdd97-232">(15)</span><span class="sxs-lookup"><span data-stu-id="cdd97-232">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="cdd97-233">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-233">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="cdd97-234">(16)</span><span class="sxs-lookup"><span data-stu-id="cdd97-234">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="cdd97-235">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-235">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="cdd97-236">(17)</span><span class="sxs-lookup"><span data-stu-id="cdd97-236">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cdd97-237">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-237">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="cdd97-238">(18)</span><span class="sxs-lookup"><span data-stu-id="cdd97-238">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="cdd97-239">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-239">**Failure using the VxD loader.**</span></span> <span data-ttu-id="cdd97-240">(19)</span><span class="sxs-lookup"><span data-stu-id="cdd97-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cdd97-241">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-241">**Your registry might be corrupted.**</span></span> <span data-ttu-id="cdd97-242">(20)</span><span class="sxs-lookup"><span data-stu-id="cdd97-242">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="cdd97-243">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-243">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="cdd97-244">(21)</span><span class="sxs-lookup"><span data-stu-id="cdd97-244">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="cdd97-245">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-245">**This device is disabled.**</span></span> <span data-ttu-id="cdd97-246">(22)</span><span class="sxs-lookup"><span data-stu-id="cdd97-246">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="cdd97-247">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-247">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="cdd97-248">(23)</span><span class="sxs-lookup"><span data-stu-id="cdd97-248">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="cdd97-249">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-249">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="cdd97-250">(24)</span><span class="sxs-lookup"><span data-stu-id="cdd97-250">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cdd97-251">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-251">**Windows is still setting up this device.**</span></span> <span data-ttu-id="cdd97-252">(25)</span><span class="sxs-lookup"><span data-stu-id="cdd97-252">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cdd97-253">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-253">**Windows is still setting up this device.**</span></span> <span data-ttu-id="cdd97-254">(26)</span><span class="sxs-lookup"><span data-stu-id="cdd97-254">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="cdd97-255">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-255">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="cdd97-256">(27)</span><span class="sxs-lookup"><span data-stu-id="cdd97-256">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="cdd97-257">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-257">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="cdd97-258">(28)</span><span class="sxs-lookup"><span data-stu-id="cdd97-258">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="cdd97-259">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-259">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="cdd97-260">(29)</span><span class="sxs-lookup"><span data-stu-id="cdd97-260">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="cdd97-261">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-261">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="cdd97-262">(30)</span><span class="sxs-lookup"><span data-stu-id="cdd97-262">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cdd97-263">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cdd97-263">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="cdd97-264">31</span><span class="sxs-lookup"><span data-stu-id="cdd97-264">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-265">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="cdd97-265">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-266">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cdd97-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-268">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cdd97-268">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-269">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="cdd97-269">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="cdd97-270">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-271">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="cdd97-271">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-272">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cdd97-272">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-274">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. DMTF \| matrice di memoria fisica \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-274">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-275">Se **true**, l'errore più recente è correggibile.</span><span class="sxs-lookup"><span data-stu-id="cdd97-275">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="cdd97-276">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-276">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-277">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cdd97-277">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-280">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cdd97-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-281">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="cdd97-281">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cdd97-282">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="cdd97-282">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cdd97-283">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-284">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cdd97-284">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-287">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cdd97-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-288">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-288">A textual description of the object.</span></span>

<span data-ttu-id="cdd97-289">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-289">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-290">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cdd97-290">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-291">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-293">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cdd97-293">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-294">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cdd97-294">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="cdd97-295">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-296">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="cdd97-296">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-297">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd97-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-299">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,4 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-300">Indirizzo finale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="cdd97-300">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="cdd97-301">L'indirizzo finale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="cdd97-301">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="cdd97-302">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cdd97-302">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-303">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="cdd97-303">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-304">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdd97-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-306">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,15 "," MIF. DMTF \| matrice di memoria fisica \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-306">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-307">Operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="cdd97-307">Memory access operation that caused the last error.</span></span> <span data-ttu-id="cdd97-308">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="cdd97-308">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="cdd97-309">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-309">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cdd97-310">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="cdd97-310">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdd97-311">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="cdd97-311">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="cdd97-312">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="cdd97-312">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="cdd97-313">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="cdd97-313">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="cdd97-314">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="cdd97-314">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-315">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="cdd97-315">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-316">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd97-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-318">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. DMTF \| matrice di memoria fisica \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-319">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="cdd97-319">Address of the last memory error.</span></span> <span data-ttu-id="cdd97-320">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="cdd97-320">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="cdd97-321">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-321">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="cdd97-322">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cdd97-322">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="cdd97-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-324">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cdd97-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-326">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="cdd97-327">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-328">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="cdd97-328">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-329">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cdd97-329">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-331">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. DMTF \| array di memoria fisica \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cdd97-331">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-332">Dati acquisiti durante l'ultimo accesso errato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="cdd97-332">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="cdd97-333">I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="cdd97-333">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="cdd97-334">Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-334">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-335">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="cdd97-335">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-336">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdd97-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-338">Ordine dei dati archiviati nella proprietà **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="cdd97-338">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="cdd97-339">Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-339">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdd97-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="cdd97-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-341">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-341">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="cdd97-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="cdd97-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-343">Byte meno significativo per primo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-343">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="cdd97-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="cdd97-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-345">Primo byte significativo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-345">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-346">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cdd97-346">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-349">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="cdd97-349">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="cdd97-350">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-351">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="cdd97-351">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-352">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdd97-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-354">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Matrice di memoria fisica DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="cdd97-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-355">Tipo di errore che si è verificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="cdd97-355">Type of error that occurred most recently.</span></span> <span data-ttu-id="cdd97-356">I valori da 12 a 14 non sono definiti nello schema CIM perché DMI combina la semantica del tipo di errore e se è correggibile.</span><span class="sxs-lookup"><span data-stu-id="cdd97-356">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="cdd97-357">Se un errore è correggibile è indicato nella proprietà **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="cdd97-357">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cdd97-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="cdd97-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-359">Altro.</span><span class="sxs-lookup"><span data-stu-id="cdd97-359">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdd97-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="cdd97-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-361">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-361">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cdd97-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="cdd97-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-363">OK.</span><span class="sxs-lookup"><span data-stu-id="cdd97-363">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="cdd97-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="cdd97-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-365">Lettura non valida.</span><span class="sxs-lookup"><span data-stu-id="cdd97-365">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="cdd97-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="cdd97-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-367">Errore di parità.</span><span class="sxs-lookup"><span data-stu-id="cdd97-367">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="cdd97-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="cdd97-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-369">Errore a bit singolo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-369">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="cdd97-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="cdd97-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-371">Errore a doppio bit.</span><span class="sxs-lookup"><span data-stu-id="cdd97-371">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="cdd97-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="cdd97-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-373">Errore a più bit.</span><span class="sxs-lookup"><span data-stu-id="cdd97-373">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="cdd97-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="cdd97-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-375">Errore di bocconcino.</span><span class="sxs-lookup"><span data-stu-id="cdd97-375">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="cdd97-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="cdd97-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-377">Errore di checksum.</span><span class="sxs-lookup"><span data-stu-id="cdd97-377">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="cdd97-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="cdd97-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-379">Errore CRC.</span><span class="sxs-lookup"><span data-stu-id="cdd97-379">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="cdd97-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (12)</span><span class="sxs-lookup"><span data-stu-id="cdd97-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-381">Non definito.</span><span class="sxs-lookup"><span data-stu-id="cdd97-381">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="cdd97-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (13)</span><span class="sxs-lookup"><span data-stu-id="cdd97-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-383">Non definito.</span><span class="sxs-lookup"><span data-stu-id="cdd97-383">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="cdd97-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (14)</span><span class="sxs-lookup"><span data-stu-id="cdd97-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-385">Non definito.</span><span class="sxs-lookup"><span data-stu-id="cdd97-385">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-386">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="cdd97-386">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-389">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-390">Indica se vengono utilizzati algoritmi di parità o CRC, ECC o altri meccanismi.</span><span class="sxs-lookup"><span data-stu-id="cdd97-390">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="cdd97-391">È anche possibile specificare i dettagli sull'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-391">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-392">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="cdd97-392">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-393">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd97-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-395">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,21 "," MIF. DMTF \| array di memoria fisica \| 001,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-396">Specifica l'intervallo, in byte, in cui è possibile risolvere l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="cdd97-396">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="cdd97-397">Se, ad esempio, gli indirizzi di errore vengono risolti in bit 11, ovvero in base a una tipica pagina, gli errori possono essere risolti in limiti di 4 KB e questa proprietà è impostata su 4000.</span><span class="sxs-lookup"><span data-stu-id="cdd97-397">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="cdd97-398">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-398">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="cdd97-399">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cdd97-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-400">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="cdd97-400">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-401">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cdd97-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-403">Data e ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="cdd97-403">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="cdd97-404">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="cdd97-404">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="cdd97-405">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-405">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-406">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="cdd97-406">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-407">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdd97-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-409">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,16 "," MIF. DMTF \| array di memoria fisica \| 001,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-409">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-410">Dimensioni del trasferimento dei dati, in bit, che hanno causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="cdd97-410">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="cdd97-411">Il valore 0 indica che non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="cdd97-411">A value of 0 indicates no error.</span></span> <span data-ttu-id="cdd97-412">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="cdd97-412">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-413">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cdd97-413">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-414">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cdd97-414">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-416">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-417">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-417">Indicates when the object was installed.</span></span> <span data-ttu-id="cdd97-418">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-418">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cdd97-419">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-419">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-420">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cdd97-420">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-421">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdd97-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-423">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cdd97-423">Last error code reported by the logical device.</span></span>

<span data-ttu-id="cdd97-424">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-425">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cdd97-425">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-426">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-427">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-428">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cdd97-428">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-429">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-429">Label by which the object is known.</span></span> <span data-ttu-id="cdd97-430">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="cdd97-430">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cdd97-431">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-431">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-432">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="cdd97-432">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-433">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd97-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-435">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-436">Numero di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdd97-436">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="cdd97-437">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cdd97-437">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="cdd97-438">Se il valore di **blockSize** è 1 (uno), questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdd97-438">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="cdd97-439">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cdd97-439">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="cdd97-440">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-440">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-441">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cdd97-441">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-442">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-444">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="cdd97-444">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-445">Stringa in formato libero che fornisce informazioni se la proprietà **ErrorType** è impostata su 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="cdd97-445">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="cdd97-446">Se non è impostato su 1, questa stringa non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-446">If it is not set to 1, then this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-447">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cdd97-447">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-448">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-450">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cdd97-450">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-451">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cdd97-451">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="cdd97-452">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="cdd97-452">Example: "\*PNP030b"</span></span>

<span data-ttu-id="cdd97-453">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-454">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="cdd97-454">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-455">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdd97-455">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-456">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-457">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cdd97-457">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="cdd97-458">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdd97-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="cdd97-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-460">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="cdd97-460">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="cdd97-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="cdd97-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-462">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-462">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cdd97-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="cdd97-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-464">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="cdd97-464">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cdd97-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="cdd97-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-466">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="cdd97-466">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="cdd97-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="cdd97-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-468">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="cdd97-468">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="cdd97-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="cdd97-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-470">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-470">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="cdd97-471">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-471">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="cdd97-472">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="cdd97-472">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="cdd97-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="cdd97-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-474">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="cdd97-474">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="cdd97-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="cdd97-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cdd97-476">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="cdd97-476">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-477">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="cdd97-477">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-478">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cdd97-478">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-479">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-480">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="cdd97-480">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="cdd97-481">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cdd97-481">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="cdd97-482">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="cdd97-482">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="cdd97-483">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cdd97-483">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="cdd97-484">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-485">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="cdd97-485">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-486">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-486">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-488">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-488">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="cdd97-489">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-490">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="cdd97-490">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-491">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd97-491">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-492">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-493">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,3 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-493">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-494">Indirizzo iniziale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria, per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="cdd97-494">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="cdd97-495">L'indirizzo iniziale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="cdd97-495">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="cdd97-496">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cdd97-496">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-497">**Status**</span><span class="sxs-lookup"><span data-stu-id="cdd97-497">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-498">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-499">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-500">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cdd97-500">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-501">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdd97-501">String that indicates the current status of the object.</span></span> <span data-ttu-id="cdd97-502">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="cdd97-502">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cdd97-503">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="cdd97-503">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cdd97-504">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="cdd97-504">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cdd97-505">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="cdd97-505">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cdd97-506">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="cdd97-506">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cdd97-507">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="cdd97-507">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cdd97-508">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-508">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cdd97-509">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cdd97-509">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cdd97-510">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cdd97-510">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cdd97-511">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="cdd97-511">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cdd97-512">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="cdd97-512">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdd97-513">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="cdd97-513">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cdd97-514">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="cdd97-514">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cdd97-515">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="cdd97-515">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cdd97-516">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="cdd97-516">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cdd97-517">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="cdd97-517">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cdd97-518">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="cdd97-518">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cdd97-519">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="cdd97-519">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cdd97-520">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="cdd97-520">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cdd97-521">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="cdd97-521">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-522">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cdd97-522">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-523">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cdd97-523">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-525">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="cdd97-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-526">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cdd97-526">State of the logical device.</span></span> <span data-ttu-id="cdd97-527">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="cdd97-527">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="cdd97-528">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cdd97-529">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="cdd97-529">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cdd97-530">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="cdd97-530">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cdd97-531">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="cdd97-531">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cdd97-532">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="cdd97-532">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cdd97-533">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="cdd97-533">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cdd97-534">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cdd97-534">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-535">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-536">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-537">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cdd97-537">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-538">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="cdd97-538">The scoping system's creation class name.</span></span>

<span data-ttu-id="cdd97-539">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-539">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-540">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="cdd97-540">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-541">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cdd97-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-542">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-543">Indica se le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema (**true**) o un indirizzo fisico (**false**).</span><span class="sxs-lookup"><span data-stu-id="cdd97-543">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="cdd97-544">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="cdd97-544">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="cdd97-545">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cdd97-545">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd97-546">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cdd97-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-547">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdd97-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd97-548">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cdd97-548">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cdd97-549">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="cdd97-549">The scoping system's name.</span></span>

<span data-ttu-id="cdd97-550">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdd97-551">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdd97-551">Remarks</span></span>

<span data-ttu-id="cdd97-552">La classe **CIM \_ Memory** è derivata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-552">The **CIM\_Memory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="cdd97-553">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="cdd97-553">WMI does not implement this class.</span></span> <span data-ttu-id="cdd97-554">Per le classi derivate **dalla \_ memoria CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cdd97-554">For classes that are derived from **CIM\_Memory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cdd97-555">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="cdd97-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cdd97-556">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="cdd97-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd97-557">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdd97-557">Requirements</span></span>



| <span data-ttu-id="cdd97-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdd97-558">Requirement</span></span> | <span data-ttu-id="cdd97-559">Valore</span><span class="sxs-lookup"><span data-stu-id="cdd97-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd97-560">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdd97-560">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd97-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdd97-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cdd97-562">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdd97-562">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd97-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdd97-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cdd97-564">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cdd97-564">Namespace</span></span><br/>                | <span data-ttu-id="cdd97-565">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cdd97-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cdd97-566">MOF</span><span class="sxs-lookup"><span data-stu-id="cdd97-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdd97-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdd97-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdd97-568">DLL</span><span class="sxs-lookup"><span data-stu-id="cdd97-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdd97-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdd97-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd97-570">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdd97-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd97-571">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="cdd97-571">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

