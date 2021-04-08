---
description: La \_ classe CIM VolatileStorage rappresenta le funzionalità e la gestione dell'archiviazione volatile.
ms.assetid: c2f7e11e-d7e4-4709-be55-1c94a0b14010
ms.tgt_platform: multiple
title: Classe CIM_VolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolatileStorage
- CIM_VolatileStorage.Access
- CIM_VolatileStorage.AdditionalErrorData
- CIM_VolatileStorage.Availability
- CIM_VolatileStorage.BlockSize
- CIM_VolatileStorage.Cacheable
- CIM_VolatileStorage.CacheType
- CIM_VolatileStorage.Caption
- CIM_VolatileStorage.ConfigManagerErrorCode
- CIM_VolatileStorage.ConfigManagerUserConfig
- CIM_VolatileStorage.CorrectableError
- CIM_VolatileStorage.CreationClassName
- CIM_VolatileStorage.Description
- CIM_VolatileStorage.DeviceID
- CIM_VolatileStorage.EndingAddress
- CIM_VolatileStorage.ErrorAccess
- CIM_VolatileStorage.ErrorAddress
- CIM_VolatileStorage.ErrorCleared
- CIM_VolatileStorage.ErrorData
- CIM_VolatileStorage.ErrorDataOrder
- CIM_VolatileStorage.ErrorDescription
- CIM_VolatileStorage.ErrorInfo
- CIM_VolatileStorage.ErrorMethodology
- CIM_VolatileStorage.ErrorResolution
- CIM_VolatileStorage.ErrorTime
- CIM_VolatileStorage.ErrorTransferSize
- CIM_VolatileStorage.InstallDate
- CIM_VolatileStorage.LastErrorCode
- CIM_VolatileStorage.Name
- CIM_VolatileStorage.NumberOfBlocks
- CIM_VolatileStorage.OtherErrorDescription
- CIM_VolatileStorage.PNPDeviceID
- CIM_VolatileStorage.PowerManagementCapabilities
- CIM_VolatileStorage.PowerManagementSupported
- CIM_VolatileStorage.Purpose
- CIM_VolatileStorage.StartingAddress
- CIM_VolatileStorage.Status
- CIM_VolatileStorage.StatusInfo
- CIM_VolatileStorage.SystemCreationClassName
- CIM_VolatileStorage.SystemLevelAddress
- CIM_VolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99add7401d92d82385a4182e466de8b28ad4fc09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877381"
---
# <a name="cim_volatilestorage-class"></a><span data-ttu-id="2a4fe-103">CIM \_ VolatileStorage (classe)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-103">CIM\_VolatileStorage class</span></span>

<span data-ttu-id="2a4fe-104">La classe **CIM \_ VolatileStorage** rappresenta le funzionalità e la gestione dell'archiviazione volatile.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-104">The **CIM\_VolatileStorage** class represents the capabilities and management of volatile storage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a4fe-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2a4fe-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2a4fe-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2a4fe-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a4fe-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a4fe-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36851DFE-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_VolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  boolean  Cacheable;
  uint16   CacheType;
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
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="2a4fe-110">Members</span><span class="sxs-lookup"><span data-stu-id="2a4fe-110">Members</span></span>

<span data-ttu-id="2a4fe-111">La classe **CIM \_ VolatileStorage** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a4fe-111">The **CIM\_VolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="2a4fe-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a4fe-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2a4fe-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a4fe-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2a4fe-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a4fe-114">Methods</span></span>

<span data-ttu-id="2a4fe-115">La classe **CIM \_ VolatileStorage** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-115">The **CIM\_VolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="2a4fe-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="2a4fe-116">Method</span></span>                                                                     | <span data-ttu-id="2a4fe-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a4fe-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a4fe-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-118">**Reset**</span></span>](reset-method-in-class-cim-volatilestorage.md)                 | <span data-ttu-id="2a4fe-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="2a4fe-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="2a4fe-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volatilestorage.md) | <span data-ttu-id="2a4fe-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="2a4fe-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2a4fe-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a4fe-124">Properties</span></span>

<span data-ttu-id="2a4fe-125">La classe **CIM \_ VolatileStorage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-125">The **CIM\_VolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a4fe-126">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-129">Proprietà di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-129">Read/write properties of the media.</span></span>

<span data-ttu-id="2a4fe-130">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-131">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="2a4fe-132">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="2a4fe-133">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="2a4fe-134">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="2a4fe-135">**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-137">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,18 "," MIF. DMTF \| array di memoria fisica \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-140">Informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-140">Additional error information.</span></span> <span data-ttu-id="2a4fe-141">Un esempio è la sindrome di controllo degli errori e correzione (ECC) oppure la restituzione dei bit di controllo se viene utilizzata una metodologia di errore basata su CRC.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="2a4fe-142">Nel secondo caso, se viene riconosciuto un errore a bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="2a4fe-143">In questo campo sono inclusi questo tipo di dati (la sindrome ECC, i dati di controllo o di bit di parità o altre informazioni fornite dal fornitore).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="2a4fe-144">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-145">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-145">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-146">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-147">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-149">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-150">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-150">Availability and status of the device.</span></span>

<span data-ttu-id="2a4fe-151">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a4fe-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2a4fe-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-155">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="2a4fe-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2a4fe-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2a4fe-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2a4fe-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2a4fe-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="2a4fe-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2a4fe-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="2a4fe-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2a4fe-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2a4fe-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2a4fe-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2a4fe-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2a4fe-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-166">Il dispositivo è noto come in modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-166">The device is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2a4fe-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-168">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2a4fe-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-170">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2a4fe-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2a4fe-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-173">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2a4fe-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-175">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2a4fe-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-177">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2a4fe-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-179">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2a4fe-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-181">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-183">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-185">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-186">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-186">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="2a4fe-187">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-187">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="2a4fe-188">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-188">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="2a4fe-189">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="2a4fe-190">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-190">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-191">**Inseribile nella cache**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-191">**Cacheable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-192">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-194">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni sulla memoria risorse di sistema \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-195">Se **true**, la memoria può essere memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-195">If **TRUE**, this memory can be cached.</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-196">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-196">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-197">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-199">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni sulla memoria risorse di sistema \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-200">Tipo di cache compatibile con la memoria.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-200">Cache type that is compatible with the memory.</span></span> <span data-ttu-id="2a4fe-201">Se la proprietà **memorizzabile nella cache** è impostata su **false**, questa proprietà non ha significato e deve essere impostata su 4 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="2a4fe-201">If the **Cacheable** property is set to **FALSE**, then this property does not have meaning and should be set to 4 ("Not Applicable").</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a4fe-202">**Altro** (0)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-202">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-203">**Sconosciuto** (1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-203">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Back"></span><span id="write-back"></span><span id="WRITE-BACK"></span>

<span data-ttu-id="2a4fe-204">**Write-back** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-204">**Write-Back** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Through"></span><span id="write-through"></span><span id="WRITE-THROUGH"></span>

<span data-ttu-id="2a4fe-205">**Write-through** (3)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-205">**Write-Through** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2a4fe-206">**Non applicabile** (4)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-206">**Not Applicable** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-207">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-210">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-211">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-211">Short textual description of the object.</span></span>

<span data-ttu-id="2a4fe-212">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-214">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-216">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-217">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="2a4fe-218">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2a4fe-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2a4fe-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-221">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2a4fe-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2a4fe-223">(1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-224">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2a4fe-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2a4fe-226">(2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2a4fe-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2a4fe-228">(3)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-229">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2a4fe-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2a4fe-231">(4)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-232">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-232">Device is not working properly.</span></span> <span data-ttu-id="2a4fe-233">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2a4fe-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2a4fe-235">(5)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-236">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2a4fe-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2a4fe-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-239">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2a4fe-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2a4fe-241">(7)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2a4fe-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2a4fe-243">(8)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-244">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2a4fe-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2a4fe-246">(9)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-247">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-247">Device is not working properly.</span></span> <span data-ttu-id="2a4fe-248">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2a4fe-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2a4fe-250">(10)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-251">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2a4fe-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2a4fe-253">(11)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-254">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2a4fe-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2a4fe-256">12</span><span class="sxs-lookup"><span data-stu-id="2a4fe-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-257">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2a4fe-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2a4fe-259">(13)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-260">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2a4fe-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2a4fe-262">(14)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-263">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2a4fe-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2a4fe-265">(15)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-266">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2a4fe-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2a4fe-268">(16)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-269">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2a4fe-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2a4fe-271">(17)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-272">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2a4fe-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2a4fe-274">(18)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-275">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2a4fe-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2a4fe-277">(19)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2a4fe-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2a4fe-279">(20)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-280">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2a4fe-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2a4fe-282">(21)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-283">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-283">System failure.</span></span> <span data-ttu-id="2a4fe-284">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2a4fe-285">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2a4fe-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2a4fe-287">(22)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-288">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2a4fe-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2a4fe-290">(23)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-291">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-291">System failure.</span></span> <span data-ttu-id="2a4fe-292">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2a4fe-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2a4fe-294">(24)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-295">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2a4fe-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2a4fe-297">(25)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-298">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2a4fe-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2a4fe-300">(26)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-301">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2a4fe-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2a4fe-303">(27)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-304">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2a4fe-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2a4fe-306">(28)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-307">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2a4fe-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2a4fe-309">(29)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-310">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-310">Device is disabled.</span></span> <span data-ttu-id="2a4fe-311">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2a4fe-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2a4fe-313">(30)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-314">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2a4fe-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2a4fe-316">31</span><span class="sxs-lookup"><span data-stu-id="2a4fe-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-317">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-317">Device is not working properly.</span></span> <span data-ttu-id="2a4fe-318">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-320">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-322">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-323">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-323">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2a4fe-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-325">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-325">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-326">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-328">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. DMTF \| matrice di memoria fisica \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-329">Se **true**, l'errore più recente è correggibile.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-329">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="2a4fe-330">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-330">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-331">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-331">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-335">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-336">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2a4fe-337">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2a4fe-338">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-339">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-342">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-343">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-343">Textual description of the object.</span></span>

<span data-ttu-id="2a4fe-344">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-348">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-349">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-349">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2a4fe-350">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-351">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-351">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-352">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-354">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,4 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-355">Indirizzo finale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria, per l'oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-355">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="2a4fe-356">L'indirizzo finale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-356">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="2a4fe-357">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-357">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2a4fe-358">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-359">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-359">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-360">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-362">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,15 "," MIF. DMTF \| matrice di memoria fisica \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-363">Operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-363">Memory access operation that caused the last error.</span></span> <span data-ttu-id="2a4fe-364">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="2a4fe-364">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="2a4fe-365">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-365">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-366">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-366">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a4fe-367">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-367">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-368">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-368">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="2a4fe-369">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-369">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="2a4fe-370">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-370">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="2a4fe-371">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-371">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-372">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-372">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-373">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-373">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-375">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. DMTF \| matrice di memoria fisica \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-376">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-376">Address of the last memory error.</span></span> <span data-ttu-id="2a4fe-377">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="2a4fe-377">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="2a4fe-378">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-378">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-379">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-379">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2a4fe-380">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-381">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-381">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-382">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-384">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-384">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2a4fe-385">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-386">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-386">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-387">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-387">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-389">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. DMTF \| array di memoria fisica \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-389">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-390">Dati acquisiti durante l'ultimo accesso errato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-390">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="2a4fe-391">I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="2a4fe-391">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="2a4fe-392">Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-392">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-393">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-394">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-394">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-395">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-397">Ordinamento dei dati archiviati nella matrice **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="2a4fe-397">Ordering for data stored in the **ErrorData** array.</span></span> <span data-ttu-id="2a4fe-398">Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-398">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-399">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-401">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-401">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="2a4fe-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-403">Byte meno significativo per primo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-403">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="2a4fe-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-405">Primo byte significativo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-405">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-406">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-406">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-407">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-409">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-409">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2a4fe-410">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-411">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-411">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-412">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-414">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Matrice di memoria fisica DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-415">Tipo di errore che si è verificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-415">Type of error that occurred most recently.</span></span> <span data-ttu-id="2a4fe-416">I valori 12-14 non sono definiti nello schema CIM, perché la semantica del tipo di errore e se è stato correggibile o meno è mista in DMI.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-416">The values 12-14 are undefined in the CIM schema since the semantics of the type of error and whether or not it was correctable are mixed in DMI.</span></span> <span data-ttu-id="2a4fe-417">La proprietà **CorrectableError** indica se è correggibile.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-417">The **CorrectableError** property indicates whether it was correctable.</span></span>

<span data-ttu-id="2a4fe-418">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-418">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a4fe-419">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-419">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-420">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-420">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2a4fe-421">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-421">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="2a4fe-422">**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-422">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="2a4fe-423">**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-423">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="2a4fe-424">**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-424">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="2a4fe-425">**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-425">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="2a4fe-426">**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-426">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="2a4fe-427">**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-427">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="2a4fe-428">**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-428">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="2a4fe-429">**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-429">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="2a4fe-430">Non **definito** (12)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-430">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="2a4fe-431">Non **definito** (13)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-431">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="2a4fe-432">Non **definito** (14)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-432">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-433">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-433">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-436">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-436">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-437">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato dall'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-437">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="2a4fe-438">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-438">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-439">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-439">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-440">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-440">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-442">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,21 "," MIF. DMTF \| array di memoria fisica \| 001,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-443">Intervallo, in byte, in cui è possibile risolvere l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-443">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="2a4fe-444">Se, ad esempio, gli indirizzi di errore vengono risolti in bit 11, ovvero in base a una tipica pagina, gli errori possono essere risolti in limiti di 4 KB e questa proprietà è impostata su 4000.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-444">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="2a4fe-445">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-445">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-446">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-446">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2a4fe-447">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-448">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-448">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-449">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-449">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-451">Ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-451">Time that the last memory error occurred.</span></span> <span data-ttu-id="2a4fe-452">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="2a4fe-452">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="2a4fe-453">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-453">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-454">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-454">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-455">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-455">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-456">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-456">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-458">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,16 "," MIF. DMTF \| array di memoria fisica \| 001,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-459">Dimensioni del trasferimento dei dati in bit che hanno causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-459">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="2a4fe-460">0 indica che non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-460">0 indicates no error.</span></span> <span data-ttu-id="2a4fe-461">Se la proprietà **errorInfo** è uguale a 3, "OK", questa proprietà deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-461">If the **ErrorInfo** property is equal to 3, "OK", then this property should be set to 0.</span></span>

<span data-ttu-id="2a4fe-462">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-462">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-463">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-463">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-464">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-466">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-467">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-467">Date and time the object was installed.</span></span> <span data-ttu-id="2a4fe-468">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-468">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2a4fe-469">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-469">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-471">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-473">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2a4fe-474">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-475">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-476">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-478">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-479">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-479">Label by which the object is known.</span></span> <span data-ttu-id="2a4fe-480">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2a4fe-481">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-483">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-484">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-485">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-486">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-486">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="2a4fe-487">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="2a4fe-488">Se il valore di **blockSize** è 1 (uno), questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-488">If the value of **BlockSize** is 1 (one), then this property is the total size of the storage extent.</span></span>

<span data-ttu-id="2a4fe-489">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="2a4fe-490">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-492">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-493">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-494">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-495">Stringa in formato libero che fornisce informazioni aggiuntive se la proprietà **ErrorType** è impostata su 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="2a4fe-495">Free-form string that provides additional information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="2a4fe-496">Se un valore diverso da 1 (uno), questa stringa non ha significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-496">If a value other than 1 (one), this string has no meaning.</span></span>

<span data-ttu-id="2a4fe-497">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-499">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-500">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-501">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-502">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="2a4fe-503">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2a4fe-504">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2a4fe-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-506">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-508">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2a4fe-509">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2a4fe-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2a4fe-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2a4fe-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-514">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2a4fe-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-516">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2a4fe-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-518">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2a4fe-519">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2a4fe-520">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2a4fe-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-522">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2a4fe-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2a4fe-524">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-526">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-527">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-528">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2a4fe-529">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2a4fe-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2a4fe-530">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2a4fe-531">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2a4fe-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="2a4fe-532">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-533">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-534">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-535">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-536">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="2a4fe-537">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-538">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-539">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-540">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-541">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,3 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-542">Indirizzo iniziale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria, per l'oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-542">Beginning address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="2a4fe-543">L'indirizzo iniziale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="2a4fe-544">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2a4fe-545">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-546">**Status**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-547">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-548">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-549">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-550">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-550">Current status of the object.</span></span> <span data-ttu-id="2a4fe-551">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2a4fe-552">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a4fe-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2a4fe-553">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2a4fe-554">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2a4fe-555">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="2a4fe-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-556">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2a4fe-557">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2a4fe-558">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2a4fe-559">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2a4fe-560">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2a4fe-561">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2a4fe-562">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2a4fe-563">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2a4fe-564">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-566">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-567">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-568">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2a4fe-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-569">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-569">State of the logical device.</span></span> <span data-ttu-id="2a4fe-570">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2a4fe-571">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a4fe-572">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a4fe-573">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2a4fe-574">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2a4fe-575">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2a4fe-576">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4fe-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-578">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-579">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-580">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-581">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="2a4fe-582">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-584">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-585">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-586">Se **true**, le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema; Se **false**, si tratta di un indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address; if **FALSE**, it is a physical address.</span></span> <span data-ttu-id="2a4fe-587">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-587">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="2a4fe-588">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-588">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a4fe-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4fe-590">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-591">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a4fe-591">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4fe-592">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a4fe-592">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a4fe-593">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-593">Scoping system's name.</span></span>

<span data-ttu-id="2a4fe-594">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a4fe-595">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a4fe-595">Remarks</span></span>

<span data-ttu-id="2a4fe-596">La classe **CIM \_ VolatileStorage** è derivata dalla [**\_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="2a4fe-596">The **CIM\_VolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="2a4fe-597">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-597">WMI does not implement this class.</span></span>

<span data-ttu-id="2a4fe-598">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-598">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2a4fe-599">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2a4fe-599">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a4fe-600">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a4fe-600">Requirements</span></span>



| <span data-ttu-id="2a4fe-601">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a4fe-601">Requirement</span></span> | <span data-ttu-id="2a4fe-602">Valore</span><span class="sxs-lookup"><span data-stu-id="2a4fe-602">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4fe-603">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a4fe-603">Minimum supported client</span></span><br/> | <span data-ttu-id="2a4fe-604">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a4fe-604">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a4fe-605">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a4fe-605">Minimum supported server</span></span><br/> | <span data-ttu-id="2a4fe-606">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a4fe-606">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a4fe-607">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a4fe-607">Namespace</span></span><br/>                | <span data-ttu-id="2a4fe-608">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2a4fe-608">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2a4fe-609">MOF</span><span class="sxs-lookup"><span data-stu-id="2a4fe-609">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a4fe-610"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a4fe-610"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a4fe-611">DLL</span><span class="sxs-lookup"><span data-stu-id="2a4fe-611">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a4fe-612"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a4fe-612"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a4fe-613">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a4fe-613">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a4fe-614">**\_Memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="2a4fe-614">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

