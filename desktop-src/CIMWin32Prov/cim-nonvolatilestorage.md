---
description: La \_ classe CIM NonVolatileStorage rappresenta le funzionalità e la gestione di risorse di archiviazione non volatili. La memoria non volatile include in modo nativo archiviazione flash e ROM.
ms.assetid: 39158b31-31f7-460c-aef1-1ca423badad6
ms.tgt_platform: multiple
title: Classe CIM_NonVolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage
- CIM_NonVolatileStorage.Access
- CIM_NonVolatileStorage.AdditionalErrorData
- CIM_NonVolatileStorage.Availability
- CIM_NonVolatileStorage.BlockSize
- CIM_NonVolatileStorage.Caption
- CIM_NonVolatileStorage.ConfigManagerErrorCode
- CIM_NonVolatileStorage.ConfigManagerUserConfig
- CIM_NonVolatileStorage.CorrectableError
- CIM_NonVolatileStorage.CreationClassName
- CIM_NonVolatileStorage.Description
- CIM_NonVolatileStorage.DeviceID
- CIM_NonVolatileStorage.EndingAddress
- CIM_NonVolatileStorage.ErrorAccess
- CIM_NonVolatileStorage.ErrorAddress
- CIM_NonVolatileStorage.ErrorCleared
- CIM_NonVolatileStorage.ErrorData
- CIM_NonVolatileStorage.ErrorDataOrder
- CIM_NonVolatileStorage.ErrorDescription
- CIM_NonVolatileStorage.ErrorInfo
- CIM_NonVolatileStorage.ErrorMethodology
- CIM_NonVolatileStorage.ErrorResolution
- CIM_NonVolatileStorage.ErrorTime
- CIM_NonVolatileStorage.ErrorTransferSize
- CIM_NonVolatileStorage.InstallDate
- CIM_NonVolatileStorage.IsWriteable
- CIM_NonVolatileStorage.LastErrorCode
- CIM_NonVolatileStorage.Name
- CIM_NonVolatileStorage.NumberOfBlocks
- CIM_NonVolatileStorage.OtherErrorDescription
- CIM_NonVolatileStorage.PNPDeviceID
- CIM_NonVolatileStorage.PowerManagementCapabilities
- CIM_NonVolatileStorage.PowerManagementSupported
- CIM_NonVolatileStorage.Purpose
- CIM_NonVolatileStorage.StartingAddress
- CIM_NonVolatileStorage.Status
- CIM_NonVolatileStorage.StatusInfo
- CIM_NonVolatileStorage.SystemCreationClassName
- CIM_NonVolatileStorage.SystemLevelAddress
- CIM_NonVolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fca29f0b279994dc0b844127fd1925850094da8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877401"
---
# <a name="cim_nonvolatilestorage-class"></a><span data-ttu-id="b4cbb-104">CIM \_ NonVolatileStorage (classe)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-104">CIM\_NonVolatileStorage class</span></span>

<span data-ttu-id="b4cbb-105">La classe **CIM \_ NonVolatileStorage** rappresenta le funzionalità e la gestione di risorse di archiviazione non volatili.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-105">The **CIM\_NonVolatileStorage** class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="b4cbb-106">La memoria non volatile include in modo nativo archiviazione flash e ROM.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-106">Nonvolatile memory natively includes flash and ROM storage.</span></span> <span data-ttu-id="b4cbb-107">Inoltre, la memoria non volatile può essere basata sull'archiviazione volatile, se la memoria volatile è supportata da una batteria.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-107">In addition, nonvolatile memory can be based on volatile storage, if the volatile memory is backed by a battery.</span></span> <span data-ttu-id="b4cbb-108">Questo scenario, ad esempio, viene descritto da un'istanza della relazione [**CIM \_ AssociatedBattery**](cim-associatedbattery.md) che fa riferimento all'archiviazione non volatile come **dipendente** e la batteria come attività **precedente** e un'istanza della relazione [**CIM \_ BasedOn**](cim-basedon.md) che fa riferimento all'archiviazione non volatile come **dipendente** e l'archiviazione volatile come attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-108">For example, this scenario would be described by an instance of the [**CIM\_AssociatedBattery**](cim-associatedbattery.md) relationship that references the nonvolatile storage as the **Dependent** and the battery as the **Antecedent**; and an instance of the [**CIM\_BasedOn**](cim-basedon.md) relationship that references the non-volatile storage as the **Dependent** and the volatile storage as the **Antecedent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4cbb-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b4cbb-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b4cbb-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b4cbb-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4cbb-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4cbb-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{18074AFA-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_NonVolatileStorage : CIM_Memory
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
  boolean  IsWriteable;
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

## <a name="members"></a><span data-ttu-id="b4cbb-114">Members</span><span class="sxs-lookup"><span data-stu-id="b4cbb-114">Members</span></span>

<span data-ttu-id="b4cbb-115">La classe **CIM \_ NonVolatileStorage** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b4cbb-115">The **CIM\_NonVolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="b4cbb-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="b4cbb-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="b4cbb-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4cbb-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b4cbb-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="b4cbb-118">Methods</span></span>

<span data-ttu-id="b4cbb-119">La classe **CIM \_ NonVolatileStorage** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-119">The **CIM\_NonVolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="b4cbb-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="b4cbb-120">Method</span></span>                                                                        | <span data-ttu-id="b4cbb-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4cbb-121">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4cbb-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-122">**Reset**</span></span>](reset-method-in-class-cim-nonvolatilestorage.md)                 | <span data-ttu-id="b4cbb-123">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="b4cbb-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b4cbb-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-nonvolatilestorage.md) | <span data-ttu-id="b4cbb-126">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b4cbb-127">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b4cbb-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4cbb-128">Properties</span></span>

<span data-ttu-id="b4cbb-129">La classe **CIM \_ NonVolatileStorage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-129">The **CIM\_NonVolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4cbb-130">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-133">Proprietà di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-133">Read/write properties of the media.</span></span>

<span data-ttu-id="b4cbb-134">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4cbb-135">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="b4cbb-136">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="b4cbb-137">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="b4cbb-138">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="b4cbb-139">**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-141">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-143">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,18 "," MIF. DMTF \| array di memoria fisica \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-144">Matrice di ottetti che contengono informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="b4cbb-145">Un esempio è la sindrome di controllo degli errori e correzione (ECC) oppure la restituzione dei bit di controllo se viene utilizzata una metodologia di errore basata su CRC.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="b4cbb-146">Nel secondo caso, se viene riconosciuto un errore a bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="b4cbb-147">In questo campo sono inclusi questo tipo di dati (la sindrome ECC, i dati di controllo o di bit di parità o altre informazioni fornite dal fornitore).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="b4cbb-148">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-149">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-150">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-153">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-154">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-154">Availability and status of the device.</span></span>

<span data-ttu-id="b4cbb-155">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-155">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4cbb-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4cbb-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b4cbb-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b4cbb-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b4cbb-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b4cbb-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b4cbb-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="b4cbb-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b4cbb-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="b4cbb-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b4cbb-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b4cbb-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b4cbb-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b4cbb-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b4cbb-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-169">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-169">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b4cbb-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-171">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-171">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b4cbb-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-173">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-173">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b4cbb-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b4cbb-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-176">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-176">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b4cbb-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-178">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-178">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b4cbb-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-180">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-180">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b4cbb-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-182">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-182">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b4cbb-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-184">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-184">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-185">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-185">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-186">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-188">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-189">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-189">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="b4cbb-190">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-190">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="b4cbb-191">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-191">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter 1 (one).</span></span>

<span data-ttu-id="b4cbb-192">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-192">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b4cbb-193">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-194">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-197">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-198">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-198">Short textual description of the object.</span></span>

<span data-ttu-id="b4cbb-199">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-200">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-200">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-201">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-203">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-203">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-204">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-204">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b4cbb-205">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-205">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b4cbb-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b4cbb-207"> (0)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-207">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-208">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-208">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b4cbb-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b4cbb-210">(1)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-210">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-211">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-211">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b4cbb-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b4cbb-213">(2)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-213">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b4cbb-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b4cbb-215">(3)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-215">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-216">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-216">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b4cbb-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b4cbb-218">(4)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-218">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-219">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-219">Device is not working properly.</span></span> <span data-ttu-id="b4cbb-220">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-220">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b4cbb-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b4cbb-222">(5)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-222">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-223">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-223">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b4cbb-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b4cbb-225"> (6)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-225">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-226">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-226">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b4cbb-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b4cbb-228">(7)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-228">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b4cbb-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b4cbb-230">(8)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-230">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-231">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-231">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b4cbb-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b4cbb-233">(9)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-233">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-234">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-234">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b4cbb-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b4cbb-236">(10)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-236">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-237">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-237">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b4cbb-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b4cbb-239">(11)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-239">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-240">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-240">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b4cbb-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b4cbb-242">12</span><span class="sxs-lookup"><span data-stu-id="b4cbb-242">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-243">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-243">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b4cbb-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b4cbb-245">(13)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-245">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-246">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-246">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b4cbb-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b4cbb-248">(14)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-248">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-249">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-249">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b4cbb-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b4cbb-251">(15)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-251">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-252">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-252">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b4cbb-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b4cbb-254">(16)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-254">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-255">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-255">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b4cbb-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b4cbb-257">(17)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-257">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-258">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-258">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b4cbb-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b4cbb-260">(18)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-260">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-261">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-261">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b4cbb-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b4cbb-263">(19)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b4cbb-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b4cbb-265">(20)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-265">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-266">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-266">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b4cbb-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b4cbb-268">(21)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-268">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-269">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-269">System failure.</span></span> <span data-ttu-id="b4cbb-270">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-270">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b4cbb-271">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-271">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b4cbb-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b4cbb-273">(22)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-273">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-274">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-274">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b4cbb-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b4cbb-276">(23)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-276">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-277">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-277">System failure.</span></span> <span data-ttu-id="b4cbb-278">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-278">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b4cbb-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b4cbb-280">(24)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-280">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-281">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-281">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b4cbb-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b4cbb-283">(25)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-283">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-284">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b4cbb-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b4cbb-286">(26)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-286">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-287">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-287">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b4cbb-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b4cbb-289">(27)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-289">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-290">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-290">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b4cbb-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b4cbb-292">(28)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-292">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-293">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-293">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b4cbb-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b4cbb-295">(29)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-295">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-296">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-296">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b4cbb-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b4cbb-298">(30)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-299">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b4cbb-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b4cbb-301">31</span><span class="sxs-lookup"><span data-stu-id="b4cbb-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-302">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-302">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-303">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-304">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-306">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-307">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b4cbb-308">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-309">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-309">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-310">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-312">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. DMTF \| matrice di memoria fisica \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-313">Se **true**, l'errore più recente è correggibile.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-313">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="b4cbb-314">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-314">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-315">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-315">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-319">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-319">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-320">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-320">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b4cbb-321">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-321">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b4cbb-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-323">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-326">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-327">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-327">Textual description of the object.</span></span>

<span data-ttu-id="b4cbb-328">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-329">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-329">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-332">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-333">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-333">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b4cbb-334">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-335">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-335">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-336">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-338">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,4 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-339">Indirizzo finale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria, per l'oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-339">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="b4cbb-340">L'indirizzo finale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-340">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="b4cbb-341">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="b4cbb-342">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-343">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-343">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-344">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-346">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,15 "," MIF. DMTF \| matrice di memoria fisica \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-347">Enumerazione che indica l'operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-347">Enumeration that indicates the memory access operation that caused the last error.</span></span> <span data-ttu-id="b4cbb-348">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="b4cbb-348">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="b4cbb-349">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-349">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-350">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-350">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4cbb-351">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-351">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4cbb-352">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-352">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="b4cbb-353">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-353">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="b4cbb-354">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-354">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="b4cbb-355">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-355">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-356">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-356">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-357">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-359">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. DMTF \| matrice di memoria fisica \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-360">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-360">Address of the last memory error.</span></span> <span data-ttu-id="b4cbb-361">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="b4cbb-361">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="b4cbb-362">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-362">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-363">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-363">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="b4cbb-364">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-366">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-368">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-368">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b4cbb-369">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-370">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-371">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-373">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. DMTF \| array di memoria fisica \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-374">Dati acquisiti durante l'ultimo accesso errato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-374">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="b4cbb-375">I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="b4cbb-375">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="b4cbb-376">Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-376">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-377">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-377">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-379">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-381">Ordinamento dei dati archiviati nella proprietà **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="b4cbb-381">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="b4cbb-382">Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-382">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-383">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-383">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4cbb-384">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-384">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="b4cbb-385">**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-385">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="b4cbb-386">**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-386">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-387">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-387">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-388">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-390">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-390">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b4cbb-391">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-392">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-392">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-393">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-395">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Matrice di memoria fisica DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-396">Tipo di errore che si è verificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-396">Type of error that occurred most recently.</span></span> <span data-ttu-id="b4cbb-397">I valori da 12 a 14 non sono definiti nello schema CIM perché DMI combina la semantica del tipo di errore e se è correggibile.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-397">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="b4cbb-398">Se un errore è correggibile è indicato nella proprietà **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="b4cbb-398">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span> <span data-ttu-id="b4cbb-399">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4cbb-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-401">Altro.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-401">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4cbb-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-403">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-403">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b4cbb-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-405">OK.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-405">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="b4cbb-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-407">Lettura non valida.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-407">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="b4cbb-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-409">Errore di parità.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-409">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="b4cbb-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-411">Errore a bit singolo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-411">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="b4cbb-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-413">Errore a doppio bit.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-413">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="b4cbb-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-415">Errore a più bit.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-415">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="b4cbb-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-417">Errore di bocconcino.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-417">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="b4cbb-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-419">Errore di checksum.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-419">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="b4cbb-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-421">Errore CRC.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-421">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="b4cbb-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (12)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-423">Non definito.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-423">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="b4cbb-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (13)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-425">Non definito.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-425">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="b4cbb-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (14)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-427">Non definito.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-427">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-428">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-428">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-429">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-431">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-431">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-432">Specifica se vengono utilizzati algoritmi di parità, algoritmi CRC, ECC o altri meccanismi.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-432">Specifies whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used.</span></span> <span data-ttu-id="b4cbb-433">È anche possibile specificare i dettagli sull'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-433">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="b4cbb-434">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-434">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-435">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-435">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-436">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-436">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-438">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,21 "," MIF. DMTF \| array di memoria fisica \| 001,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-439">Intervallo, in byte, in cui è possibile risolvere l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-439">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="b4cbb-440">Se, ad esempio, gli indirizzi di errore vengono risolti in bit 11, ovvero in base a una tipica pagina, gli errori possono essere risolti in limiti di 4 KB e questa proprietà è impostata su 4000.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-440">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="b4cbb-441">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-441">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-442">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="b4cbb-443">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-443">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-444">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-444">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-445">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-445">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-447">Ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-447">Time that the last memory error occurred.</span></span> <span data-ttu-id="b4cbb-448">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="b4cbb-448">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="b4cbb-449">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-449">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-450">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-450">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-451">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-451">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-452">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-454">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,16 "," MIF. DMTF \| array di memoria fisica \| 001,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-455">Dimensioni del trasferimento dei dati, in bit, che hanno causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-455">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="b4cbb-456">Il valore 0 (zero) indica che non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-456">A value of 0 (zero) indicates no error.</span></span> <span data-ttu-id="b4cbb-457">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-457">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="b4cbb-458">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-460">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-461">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-462">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-463">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-463">Date and time the object was installed.</span></span> <span data-ttu-id="b4cbb-464">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-464">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b4cbb-465">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-466">**IsWriteable**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-466">**IsWriteable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-467">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-469">Se **true**, l'archiviazione non volatile è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-469">If **TRUE**, non-volatile storage is writeable.</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-471">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-473">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b4cbb-474">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-475">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-476">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-478">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-479">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-479">Label by which the object is known.</span></span> <span data-ttu-id="b4cbb-480">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b4cbb-481">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-483">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-484">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-485">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-486">Numero totale di blocchi consecutivi. ogni blocco corrisponde alla dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-486">Total number of consecutive blocks, each block is the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="b4cbb-487">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="b4cbb-488">Se il valore di **blockSize** è 1 (uno), questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-488">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="b4cbb-489">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b4cbb-490">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-492">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-493">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-494">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-495">Stringa in formato libero che fornisce informazioni se la proprietà **ErrorType** è impostata su 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="b4cbb-495">Free-form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="b4cbb-496">Se non è impostato su 1, questa stringa non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-496">If not set to 1, this string has no meaning.</span></span>

<span data-ttu-id="b4cbb-497">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-499">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-500">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-501">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-502">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b4cbb-503">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b4cbb-504">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b4cbb-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-506">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-508">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b4cbb-509">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4cbb-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b4cbb-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b4cbb-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b4cbb-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-514">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b4cbb-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-516">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b4cbb-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-518">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b4cbb-519">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b4cbb-520">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b4cbb-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-522">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b4cbb-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b4cbb-524">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-526">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-527">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-528">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b4cbb-529">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b4cbb-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b4cbb-530">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b4cbb-531">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b4cbb-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b4cbb-532">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-533">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-534">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-535">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-536">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="b4cbb-537">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-538">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-539">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-540">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-541">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,3 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-542">Indirizzo iniziale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-542">Beginning address that is referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="b4cbb-543">L'indirizzo iniziale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="b4cbb-544">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="b4cbb-545">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-546">**Status**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-547">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-548">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-549">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-550">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-550">Current status of the object.</span></span>

<span data-ttu-id="b4cbb-551">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b4cbb-552">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4cbb-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b4cbb-553">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b4cbb-554">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b4cbb-555">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="b4cbb-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4cbb-556">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b4cbb-557">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b4cbb-558">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b4cbb-559">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b4cbb-560">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b4cbb-561">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b4cbb-562">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b4cbb-563">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b4cbb-564">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-566">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-567">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-568">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b4cbb-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-569">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-569">State of the logical device.</span></span> <span data-ttu-id="b4cbb-570">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b4cbb-571">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4cbb-572">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4cbb-573">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b4cbb-574">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b4cbb-575">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b4cbb-576">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4cbb-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-578">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-579">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-580">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-581">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="b4cbb-582">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-584">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-585">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-586">Se **true**, le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="b4cbb-587">Se **false**, si tratta di un indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-587">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="b4cbb-588">Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-588">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="b4cbb-589">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-589">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cbb-590">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-590">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cbb-591">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-592">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4cbb-592">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cbb-593">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b4cbb-593">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b4cbb-594">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-594">Scoping system's name.</span></span>

<span data-ttu-id="b4cbb-595">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-595">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4cbb-596">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4cbb-596">Remarks</span></span>

<span data-ttu-id="b4cbb-597">La classe **CIM \_ NonVolatileStorage** è derivata dalla [**\_ memoria CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-597">The **CIM\_NonVolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="b4cbb-598">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-598">WMI does not implement this class.</span></span>

<span data-ttu-id="b4cbb-599">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-599">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b4cbb-600">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-600">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4cbb-601">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4cbb-601">Requirements</span></span>



| <span data-ttu-id="b4cbb-602">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4cbb-602">Requirement</span></span> | <span data-ttu-id="b4cbb-603">Valore</span><span class="sxs-lookup"><span data-stu-id="b4cbb-603">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cbb-604">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4cbb-604">Minimum supported client</span></span><br/> | <span data-ttu-id="b4cbb-605">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4cbb-605">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4cbb-606">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4cbb-606">Minimum supported server</span></span><br/> | <span data-ttu-id="b4cbb-607">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4cbb-607">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4cbb-608">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4cbb-608">Namespace</span></span><br/>                | <span data-ttu-id="b4cbb-609">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b4cbb-609">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b4cbb-610">MOF</span><span class="sxs-lookup"><span data-stu-id="b4cbb-610">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4cbb-611"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4cbb-611"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4cbb-612">DLL</span><span class="sxs-lookup"><span data-stu-id="b4cbb-612">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4cbb-613"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4cbb-613"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4cbb-614">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4cbb-614">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4cbb-615">**\_Memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="b4cbb-615">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

